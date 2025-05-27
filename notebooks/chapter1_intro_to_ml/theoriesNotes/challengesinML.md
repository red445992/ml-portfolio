## Data Quality Issues
    Machine learning models learn patterns from the data they are trained on, which means their outputs are heavily influenced by the quality, diversity, and fairness of that data. If the training data contains bias, the model is likely to reproduce or even amplify that bias in its predictions.

    A notable example is Amazon’s recruitment tool used between 2014 and 2017. The system was designed to screen resumes and rank candidates from 1 to 5. However, the model was trained on data from the company’s previous 10 years of hiring practices—data that reflected a male-dominated tech industry. As a result, the model learned to favor male applicants and systematically penalized resumes that included the word "women" or referenced women’s organizations. This led to an unfair and biased hiring process, ultimately reinforcing existing gender imbalances.

    GARBAGE IN -> GARBAGE OUT
    This example highlights the importance of incorporating fairness, accountability, and transparency when building machine learning systems.

## Ethical Consideration
    In 2016 microsoft releases TAY chatbot in twitter which learned from public interaction in Twitter. However, in few hours, users start feeding it in appropriate contents and text leading TAY to act in the same way and start posting offensive contents, text and images in the twitter. It start giving harmful responses leading to shutdown with in 24 hrs of deployment.

    This shows a key ehtical consideration of AI: Bias from unfiltered user input, importance of responsible AI deployment.

## Data Privacy and Security
    ML model are trained on sensitive data(medical reports, Financial reprt) which risk in leaking the private information either through output or adversarial attack

    Eg: Membership Inference Attack: Hackers can determine if a sepcific person's data is used to train model or not
        Deepfake Misuse: Generative AI model can create realistic fake images/videos enabling misinformation or fraud.
## Model Interpretability ("Black Box" Problem)
    Many advanced Ml model (eg deep neural network) operates as "Black boxes" making it difficult to understand how they arrive at the predicition. This lack of transparency raises the question of ethical or practical concerns.
    Eg: Health Care: A model diagnosing diseases might achieve 95% accuracy in detecting brain tumor but fails to explain which features drove this decision. Doctors cannot trust or correct its reasoning without interpretability.