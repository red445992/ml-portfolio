## Data Quality Issues
    Machine learning models learn patterns from the data they are trained on, which means their outputs are heavily influenced by the quality, diversity, and fairness of that data. If the training data contains bias, the model is likely to reproduce or even amplify that bias in its predictions.

    A notable example is Amazon’s recruitment tool used between 2014 and 2017. The system was designed to screen resumes and rank candidates from 1 to 5. However, the model was trained on data from the company’s previous 10 years of hiring practices—data that reflected a male-dominated tech industry. As a result, the model learned to favor male applicants and systematically penalized resumes that included the word "women" or referenced women’s organizations. This led to an unfair and biased hiring process, ultimately reinforcing existing gender imbalances.

    GARBAGE IN -> GARBAGE OUT
    This example highlights the importance of incorporating fairness, accountability, and transparency when building machine learning systems.

## Ethical Consideration
    In 2016 microsoft releases TAY chatbot in twitter which learned from public interaction in Twitter. However, in few hours, users start feeding it in appropriate contents and text leading TAY to act in the same way and start posting offensive contents, text and images in the twitter. It start giving harmful responses leading to shutdown with in 24 hrs of deployment.

    This shows a key ehtical consideration of AI: Bias from unfiltered user input, importance of responsible AI deployment.