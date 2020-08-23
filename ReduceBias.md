# Notes on reducing bias in data collection and data applications

## [Notes From Article 1](https://techcrunch.com/2018/11/06/3-ways-to-avoid-bias-in-machine-learning/)

### What effects will it have on us
1. Automation: Sometimes AI models are plugged into a programmatic function, which could lead to the automation of bias.
2. Influence: Since many a times people tend to trust the output of the AI systems, bias in people can get stregnten due to bias in AI.

**Reverse Psychological fact: AI can also help us fight bias in the datasets. By researching the outputs of the AI system we can see the bias in the datasets collected by humans**

***Even unsupervised learning is semi-supervised, as it requires data scientists to choose the training data that goes into the models. If a human is the chooser, bias can be present.***

### Three Keys to manage bias in AI
1. Choose the right learning model for the problem:
    - Each problem requires different solution and provides varied data resources. There's no single model to avoid bias, but there are parameters that can inform us about this.
    --
    - For example, supervised and unsupervised learning models have their respective pros and cons. Unsupervised models that cluster or do dimensional reduction can learn bias from their data set. If belonging to group A highly correlates to behavior B, the model can mix up the two. And while supervised models allow for more control over bias in data selection, that control can introduce human bias into the process.
    --
    - Excluding sensitive information from the model — may seem like a workable solution, but it still has vulnerabilities. In college admissions, sorting applicants by ACT scores is standard, but taking their ZIP code into account might seem discriminatory. But because test scores might be affected by the preparatory resources in a given area, including the ZIP code in the model could actually decrease bias.
--
2. Choose a representative data set:

    - Making sure the training data is diverse and includes different groups is essential, but segmentation in the model can be problematic unless the real data is similarly segmented.
    --
    - It is inadvisable to have different models for different groups both computationally and in terms of public relations. When there is insufficient data for one group, you could possibly use weighting to increase its importance in training, but this should be done with extreme caution. It can lead to unexpected new biases.
    --
    - For example, if you have only 40 people from Cincinnati in a data set and you try to force the model to consider their trends, you might need to use a large weight multiplier. Your model would then have a higher risk of picking up on random noise as trends — you could end up with results like “people named Brian have criminal histories.” This is why you need to be careful with weights, especially large ones.
--
3. Monitor performance using real data:
    - **It is important to simulate real world applications as much as possible when building models because sometimes things are not in control in real world.**
    --
    - When you’re examining data, you could be looking for two types of equality: equality of outcome and equality of opportunity. If you’re working on AI for approving loans, result equality would mean that people from all cities get loans at the same rates; opportunity equality would mean that people who would have returned the loan if given the chance are given the same rates regardless of city. Without the latter, the former could still hide if one city has a culture that makes defaulting on loans common.
    --
    - **Result equality is easier to prove, but it also means you’ll knowingly accept potentially skewed data. While it’s harder to prove opportunity equality, it is at least valid morally. It’s often practically impossible to ensure both types of equality, but oversight and real-world testing of your models should give you the best shot.**