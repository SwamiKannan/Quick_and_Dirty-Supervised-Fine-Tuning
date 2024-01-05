# Quick and Dirty series: Fine tuning a Huggingface model with a Huggingface Dataset
<center><img src="https://github.com/SwamiKannan/Quick_and_Dirty-Supervised-Fine-Tuning/blob/main/images/cover3.png"></center>

This is basically a quick get to go fine-tuning exercise, inspired by the hundreds of notebooks that have been done for Diffusion models. 

# Requirements:
1. A Google account (with Drive and Colab available)
2. A [Huggingface account](https://huggingface.co/join)

## Usage:
1. Upload this notebook to Google Colab.
2. Copy your Huggingface key. A Huggingface key can be obtained as follows:
   <ol>
     <li> Login to Huggingface </li>
     <li> In the top right corner, click on the profile link and go to Settings</li>
     <center><img src="https://github.com/SwamiKannan/Quick_and_Dirty-Supervised-Fine-Tuning/blob/main/images/access_hf1.png"></center>
     <li> In the Settings page, click on Access Tokens and then copy the link of the key in the access page</li>
      <center><img src="https://github.com/SwamiKannan/Quick_and_Dirty-Supervised-Fine-Tuning/blob/main/images/access_hf2.png"></center>
      Store this temporarily on a note page for step 5 below:
3. Run cell 1 to install the libraries
4. Run cell 2 to allow the notebook to access your Google Drive. This is **specifically** to allow the notebook to store all the generated products to your Google drive. Google colab deletes all the data it generates (models, logs, etc.) from its memory when the runtime is disconnected
5. Run cell 3 to authenticate your Huggingface account. This is **specifically** to allow the notebook to push your final finetuned model directly to your Huggingface account.
6. Fill in the details 
   </ol>

#### Credits:
<sub> Speedometer image from <a href="https://www.pngegg.com/en/search?q=speedometer"> PNGEGG </a><br>
Tuning photo from <a href="https://bookdown.org/gmli64/do_a_data_science_project_in_10_days/fine-tune-models.html">Gangmin Li's Do A Data Science Project in 10 Days </a>
</sub>
