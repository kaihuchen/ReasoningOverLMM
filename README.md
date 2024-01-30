# Diagnostic Reasoning with Medical Images

This post is a preliminary study on issues related to the use of a multimodal LLM (Large Language Model), such as OpenAI's GPT-4V, for making medical diagnosis based on a medical image (such as X-ray, CT scan, MRI scan, ultrasound scan, etc.). Doing so would involve the following topics:

- **Which LLM** is suitable for such a purpose. For now we will focus only on OpenAI's GPT-4V model, since in another study we have seen [good result when applying it to autonomous driving](https://github.com/kaihuchen/AutonomousBackseatDriver/blob/main/README.md).
- **Sufficient knowledge in the LLM**, i.e., whether the LLM in question has been trained to contain sufficient knowledge for the task. For this we will choose to defer for now.
- **Diagnostic Reasoning**: making correct diagnosis is often not an one-shot activity, but rather may need to ask the right questions and take many steps. In other words, it is really a process of performing diagnostic reasoning. The main goal of this study is to find whether GPT-4V has sufficient capacity to perform diagnostic reasoning. 

# Basic test setup:
- Our test is performed using Custom GPT created in OpenAI's GPTs Store
- GPT-4 (which implicitly includes GPT-4V) is selected as its working model. 
- The following X-ray image is used for testing, which 
![](images/X-Ray%20Squarepants%20toy%20in%20chest.jpg)
- The main thing that we experiment with is the prompt in the **Insructions** of the the Custom GPT's configuration.

# Test #1: simple prompting
The following simple prompt is used for this test

> Give detailed description of this image for areas of concern only, analyze it like a medical radiologist. Keep answers as concise as possible without warning messages.
  
Response from GPT-4V:

> This is a cervical spine X-ray image showing an anterior cervical discectomy and fusion (ACDF) with a plate and screw construct. The cervical vertebral bodies appear to be in good alignment, and there is no evidence of hardware failure or malposition on this single view. The tracheal air shadow is midline, and there is no soft tissue swelling anterior to the spine. The lung apices are clear without evidence of pneumothorax or pleural effusion.
> 
> However, this is only a single view, and evaluation of spinal fusion and hardware integrity is typically done with multiple views to assess for alignment, hardware positioning, and potential complications such as adjacent segment disease or hardware failure.
> 
> Degree of Urgency: Based on this image alone, without any clinical context, it would be a 3. However, if the patient has new or worsening symptoms, this could indicate a more urgent situation.

Assessment:

- GPT-4V zoom in on an incorrect, and failed to explore other possibilities
- GPT-4V classifies the problem as non-urgent diagnosis which is adequate




