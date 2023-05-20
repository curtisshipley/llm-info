#  Information about using LLMs

This is a small repo I put together to share various colabs, showing how to load and conduct inferences. Right now, there is only one colab, for MPT Instruct 7B.

## MPT 7B Instruct Colab

[MPT 7B Instruct Colab](Working_YT_MPT_Instruct_7B.ipynb)

This was taken from this [Source](https://colab.research.google.com/drive/1s2beg55SEV8ICHufhwcflYtUNskTX8kO?usp=sharing) This demonstrates how to load and perform inductions with the stock MPT 7B Instruct LLM. Node: The LLM takes about 6 minutes to load.

As of 5/20/2023 I had to add the following pip commands to get past this error:

```
ERROR: pip's dependency resolver does not currently take into account all the packages that are installed. This behaviour is the source of the following dependency conflicts.
torchaudio 2.0.2+cu118 requires torch==2.0.1, but you have torch 2.0.0 which is incompatible.
torchdata 0.6.1 requires torch==2.0.1, but you have torch 2.0.0 which is incompatible.
torchtext 0.15.2 requires torch==2.0.1, but you have torch 2.0.0 which is incompatible.
torchvision 0.15.2+cu118 requires torch==2.0.1, but you have torch 2.0.0 which is incompatible.
```
Added at top:
```
!pip install torch==2.0.0+cu118 torchvision==0.15.1+cu118 torchaudio==2.0.1+cu118 torchtext==0.15.1 torchdata==0.6.0 --extra-index-url https://download.pytorch.org/whl/cu118 -U
!pip install xformers==0.0.19 triton==2.0.0 -U
```
