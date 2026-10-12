# Bonus exercise: From banking queries to JSON

**Lab 3 · 0.5 extra points**

Fine-tune a pretrained GPT-2 model using nanoGPT and LoRA so that it classifies a banking query and returns a single JSON object. The aim is to learn both the task and the output format.

Use [BANKING77](https://github.com/PolyAI-LDN/task-specific-datasets/tree/master/banking_data), a dataset of banking queries with annotated intents. Keep the original queries and labels; only convert the labels into JSON targets.

For example:

```text
Request: I think my card is broken
Response: {"intent":"card_not_working"}
```

The model should generate only the JSON response.

## Data

Use these ten intents:

```text
card_arrival
card_not_working
lost_or_stolen_card
pin_blocked
cancel_transfer
edit_personal_details
request_refund
terminate_account
transaction_charged_twice
exchange_rate
```

Use about 10% of BANKING77's full official training set for parameter updates: roughly 1,000 of its 10,003 queries. Obtain this subset as follows:

1. Filter the official training file to the ten intents above. This gives 1,304 queries.
2. Split those queries into 80% training and 20% validation, stratified by intent, this gives **1,043 training queries** (about 10.4% of the full training set) and **261 validation queries**.
3. Filter the official test file to the same ten intents and keep **400 test queries** for the final evaluation.

## Training

Start from pretrained GPT-2 (124M) using [nanoGPT](https://github.com/karpathy/nanoGPT). Freeze the weights, and rain only LoRA adapters. Choose which layers to adapt and the LoRA parameters and explain your choices. 

1. Format each example as a request followed by its JSON response and an end-of-text token. Use the same prompt format during training and evaluation.
2. Build the inputs and next-token targets. Mask targets belonging to the prompt or padding so that the loss covers only the response and its end token. Print one tokenized example with its target mask to check the alignment.
3. Choose reasonable values for the LoRA rank, scaling factor, dropout, learning rate, batch size, and number of epochs (at most five per run). State your choices and briefly justify them. Report the number and percentage of trainable parameters.
4. Plot training and validation response loss, and select the checkpoint with the lowest validation response loss. Use only the training and validation sets to choose settings.

Unlike the Hugging Face model in Lab 3, nanoGPT expects you to shift the targets yourself. Its [loss implementation](https://github.com/karpathy/nanoGPT/blob/master/model.py) uses `-1` for ignored targets.


## Evaluation and target

Evaluate the original model and your selected checkpoint on every example in the filtered test set. Use greedy decoding, allow at most 40 new tokens, and stop at the end-of-text token. Use identical prompts and decoding settings for both models.

Parse the entire generated response after stripping surrounding whitespace.

Report these three metrics:

| Metric | A response counts as correct when… |
|---|---|
| Valid JSON rate | The entire response parses as JSON. |
| Schema compliance | It parses as an object with exactly one key, `intent`, whose value is one of the ten allowed strings. |
| Exact task accuracy | It satisfies the schema and its intent matches the dataset label. |

Use the total number of test queries as the denominator for every metric. Invalid responses count as incorrect; do not calculate accuracy only on successfully parsed responses.

**Target: at least 95% schema compliance and 80% exact task accuracy.**

## Submission

Submit your completed notebook exported as a PDF. Make sure the code, outputs, tables, and plots are readable. Include:

- Your code, with explanations. 
- LoRA configuration, training settings, trainable parameter count, and training/validation loss curves.
- A before/after table with all three test metrics and the test-set size.
- Three test examples with both models' outputs and a short discussion. Include a failure if there is one. Explain whether formatting and classification improved, whether you reached the targets, and how LoRA differs from updating every model parameter.

**No AI assistance is permitted for any part of this assignment**, You can use AI to ask questions, but write the code and explanations yourself.
