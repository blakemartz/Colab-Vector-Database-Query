# Colab-Vector-Database-Query
Question Answering a directory of PDFs in Google Colab using LLaMa 2, FAISS, and LangChain

## Getting Started

You can use the open source Llama-2-7b-chat model in both Hugging Face transformers and LangChain. However, you have to first request access to Llama 2 models via Meta website and also accept to share your account details with Meta on Hugging Face website. It typically takes a few minutes or hours to get the access.

🚨 Note that your Hugging Face account email MUST match the email you provided on the Meta website, or your request will not be approved.


## Hugging Face token

You need to generate an access token to allow downloading the model from Hugging Face in your code. For that, go to your Hugging Face Profile > Settings > Access Token > New Token > Generate a Token. Just copy the token and add it in the below code

## Path to your directory of PDFs

Upload the PDFs you wish to query into a folder on your Google Drive. Update the PDF_directory variable below to the path of that folder.

###  codeblock
model_id = 'meta-llama/Llama-2-7b-chat-hf'

hf_auth = 'your_token_here'

pdf_directory = "/content/drive/MyDrive/your_directory_path"


## Run the notebook

In your Google Colab notebook, go to Runtime > Change runtime type > Hardware accelerator > GPU > GPU type > T4. You will need ~8GB of GPU RAM for inference and running on CPU is practically impossible.

Go to Runtime > Run all

It will take several minutes to download dependencies, process your files, and extract the embeddings to the vector database.

## Question Answer

Once all cells have completed, you can scroll to the bottom of the notebook and enter your question in the 'question' variable in the final cell. Run the cell to query the documents.


[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg\)](https://colab.research.google.com/github/blakemartz/Colab-Vector-Database-Query/blob/main/Colab_Vector_Database_Query.ipynb\)

