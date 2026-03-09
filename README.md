1.Abstract-The project implemented a comparative analysis between two transformer-based models, BERT and RoBERTa. After finetuning them using scientific research text, we achieved good accuracy: BERT at 96% and RoBERTa at 93%. The data reveals that RoBERTa is excellent at identifying AI patterns, while BERT is more balanced in identifying scientific text based on sentence relationships.

2.Background: However, the development of models based on the transformer architecture has shifted NLP from context-free word representations to context-aware representations. This paper examines two of the most prominent models: BERT and RoBERTa, which is BERT's improved variant.

2.1 BERT Architecture

According to Devlin et al. (2018), "The core insight of BERT is to apply bidirectional training of Transformers for this task [language modeling]." Compared to previous models such as OpenAI GPT, which process texts left to right, BERT’s encoder processes the entire sequence of words simultaneously.
Masked Language Model (MLM): To train the model in a bidirectional fashion, BERT randomly masks 15% of the input text. The model will try to predict the original word from the context. This allows the BERT model to look at the context from the left as well as the right side, helping the model understand complex scientific vocabulary.
Next Sentence Prediction (NSP): For the pre-training of the BERT model, a task called Next Sentence Prediction is performed. This involves the prediction of whether the next sentence to a given sentence is the actual next sentence in the original text. This task is crucial, according to Devlin et al. as it helps the model understand the logical connection between scientific concepts and their conclusion.

2.2 RoBerta Architecture

Liu et al. (2019) replicate BERT and discover that the original model had not been trained well enough. They developed RoBERTa, which either matches or outperforms all models following BERT by altering several aspects of the training process:
Dynamic Masking: BERT follows a fixed masking pattern while pre-processing. RoBERTa follows a different mask for every input instance of the sequence in the model. This prevents memorization of some scientific terms in the model.
Deletion of NSP Task: The need for deleting the Next Sentence Prediction Task and training the models for long paragraphs of text (up to 512 tokens) is given in this argument. This is why RoBERTa is a strong pattern recognizer but slightly weak in inter-sentence logic when compared to BERT.
Training Data and Batch Size: RoBERTa was trained with ten times the amount of data as BERT (160 GB) and with larger mini-batches. The increased amount of training data allows RoBERTa to see many more examples of patterns in the data, making it possible for it to reach such a high Recall value (0.99) as reported in the results.
