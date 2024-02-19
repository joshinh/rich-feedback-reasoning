# rich-feedback-reasoning
This repository contains the data for the AAAI workshop paper titled 'Improving Multi-Hop Reasoning in LLMs by Learning from Rich Human Feedback'

We collect rich human feedback for two datasets: strategyQA (located in `data/strategyqa`) and sports understanding from BigBench (location in `data/sports_understanding`).

### Dataset Details

The `train.json` file for strategyQA and sports understanding contains 1565 examples and 796 examples respectively which were used for finetuning. Additionally, for strategyQA `eval.json` contains 173 additional examples which were used to evaluate if models can judge the correctness of their generations.

### Dataset Attributes

1. **Original** - contains the original datapoint from the respective dataset with all the attributes (e.g. input, ground truth answer etx.)

2. **Generation** - model generated answer and chain-of-thought with few shot prompting. The model used was GPT-J for strategyQA and Flan-T5 for sports understanding.

3. **Correction** - corrected answer and chain-of-thought collected from annotators.

4. **Subquestions** - decomposition of the original question into subquestions which need to be answered to answer the original question.

5. **ErrorType** - list of different types of errors present in the model generation (**Generation**). The types of errors and their shorthands are: FE - factual error, MF - missing fact, IR - irrelevant fact, LI - logical inconsistency, None - no error.

6. **\{ErrorType\}_reason** - where ErrorType is either FE, MF, IR, LI. This contains the reason, in natural language, why that particular error type is present in the model generation.




