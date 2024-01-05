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
     <center><img src="https://github.com/SwamiKannan/Quick_and_Dirty-Supervised-Fine-Tuning/blob/main/images/access_hf1.png"></center><br>
     <li> In the Settings page, click on Access Tokens and then copy the link of the key in the access page</li>
    <center><img src="https://github.com/SwamiKannan/Quick_and_Dirty-Supervised-Fine-Tuning/blob/main/images/access_hf2.png"></center>
      Store this temporarily on a note page for step 5 below:
   </ol>
3. Run cell 1 to install the libraries
4. Run cell 2 to allow the notebook to access your Google Drive. This is **specifically** to allow the notebook to store all the generated products to your Google drive. Google colab deletes all the data it generates (models, logs, etc.) from its memory when the runtime is disconnected
5. Run cell 3 to authenticate your Huggingface account. This is **specifically** to allow the notebook to push your final finetuned model directly to your Huggingface account.
6. Fill in the details in the section <b>3. USER INPUTS"</b>. Mandatory details include:
   <ul>
      <li>Dataset name</li>
      <li>Split</li>
   </ul>
7. Update the code for the function update_dataset(). If no data processing is required, just point the appropriate column names to df['question'] and df['answer']. <br>
*Example: if the column "professor" in the dataframe has the input for the question, and the column "student" in the data frames has the input of the answer, update the function as follows:*
```
df['question] = df['professor']
df['answer']=df['student']
```
8. Run  the rest of the code cells one after the other
### Notes: 
<ul>
   <li>Make sure you do not store your Hugginface key where others can access it. Else, people can easily access any service (free or paid) if they have access to your key.</li>
   <li>Make sure the section <b>3. USER INPUTS</b> without any errors/ messages. Else, this will prevent the rest of the code from running acccurately.</li>
   <li>The default model used is <b>mistralai/Mistral-7B-v0.1</b> . Hence, if no model_name is given, this is the model that will be used.</li>
</ul>

#### Credits:
<sub> Speedometer image from <a href="https://www.pngegg.com/en/search?q=speedometer"> PNGEGG </a><br>
Tuning photo from <a href="https://bookdown.org/gmli64/do_a_data_science_project_in_10_days/fine-tune-models.html">Gangmin Li's Do A Data Science Project in 10 Days </a>
</sub>
