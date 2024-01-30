# Diagnostic Reasoning with Medical Images

This post is a preliminary study on issues related to the use of a multimodal LLM (Large Language Model), such as OpenAI's GPT-4V, for making medical diagnosis based on a medical image (such as X-ray, CT scan, MRI scan, ultrasound scan, etc.). Doing so would involve the following topics:

- **Which LLM** is suitable for such a purpose. For now we will focus only on OpenAI's GPT-4V model, since in another study we have seen [good result when applying it to autonomous driving](https://github.com/kaihuchen/AutonomousBackseatDriver/blob/main/README.md).
- **Sufficient knowledge in the LLM**, i.e., whether the LLM in question has been trained to contain sufficient knowledge for the task. For this we will choose to defer for now.
- **Diagnostic Reasoning**: making correct diagnosis is often not an one-shot activity, but rather may need to ask the right questions and take many steps. In other words, it is really a process of performing diagnostic reasoning. The main goal of this study is to find whether GPT-4V has sufficient capacity to perform diagnostic reasoning. 

# Basic test setup:
- Our test is performed using Custom GPT created in OpenAI's GPTs Store
- GPT-4 (which implicitly includes GPT-4V) is selected as its working model. 
- The following X-ray image is used for testing:
![](images/X-Ray%20Squarepants%20toy%20in%20chest.jpg)
- The main thing that we experiment with is the prompt in the **Insructions** of the the Custom GPT's configuration.


# Test #1: simple prompting







