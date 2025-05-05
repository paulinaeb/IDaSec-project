# Spam detection model using LSTM

**Description**: in this branch, you can find how to develop an LSTM model in order to detect spams in two main scenarios:
- Normal spam emails/messages (e.g. 'click the link for free money')
- Evasion spam emails/messages (e.g. 'cl   ick the link for fr33 monEy')

## Structure  
- before_evasion notebook
  in this notebook, you can find the whole pipeline of developing the LSTM model and saving it's weights
  you can find it here
  [View the model_development](https://github.com/paulinaeb/IDaSec-project/blob/exp3/my_exp3/before_evasion.ipynb)

- after_evasion notebook
  in this notebook, you can find the use of the pretrained model in order to test it on evasion methods
  you can find it here
  [View the evasion_analysis](https://github.com/paulinaeb/IDaSec-project/blob/exp3/my_exp3/after_evasion.ipynb)

## References

medium

[https://yashpaneliya.medium.com/decoding-lstm-using-pytorch-eda47d7d1766]

kaggle for datasets

[https://www.kaggle.com/datasets/wcukierski/enron-email-dataset]

Analytics vidhya

[https://www.analyticsvidhya.com/blog/2021/05/sms-spam-detection-using-lstm-a-hands-on-guide/]
