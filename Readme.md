#ISMT S-117 Text Analytics and Natural Language Processing (2020 Summer)
##Final Project
#Resume Screening System Using RoBERTa
###by Micheal Choi Kwong Chak

vec2rec package: All code is in the vec2rec python package. There are 6 python notebooks:
- [0.installation.ipynb](vec2rec/0.installation.ipynb) - Installation procedure for Colab. This is to allow the correct packages to be installed on Colab. Expected python package combination is also included.
- [1.explore_dataset.ipynb](vec2rec/1.explore_dataset.ipynb) - in addition to what is done above to explore the datasets, LDA and BERT embedding is used to discover data pattern and suitability of transformer usage.
- [2.create_labels.ipynb](vec2rec/2.create_labels.ipynb) - as mentioned above, we do not have a labelled dataset between job and resume work experience to train the model with. This notebook is to build the training set using the heuristic of RoBERTa sentence-pair similarity of the Job Title as the label, which is joined with Job Description from the Job Posting and Resume for subsequent training (Job Titles are not included in training).
- [3.use_cosine_similarity.ipynb](vec2rec/3.use_cosine_similarity.ipynb) - instead of using transformer model, this code uses the RoBERTa embedding to embed the job descriptions then see how well cosine similarity perform as a predictor
- [4.sentence_pair.ipynb](vec2rec/4.sentence_pair.ipynb) - Train RoBERTa model sentence pair with the labelled dataset we created in 2 and see how well the model performs as a predictor to the training and validation sets
- [5.model_trial.ipynb](vec2rec/5.model-trial.ipynb) - run the test dataset against the model and see how well it performs.

Other directories
1.	[data](data) – contains job and resume dataset
2.	[saved_models](saved_models) – contains STS-B saved model for label creation, and Good-SM saved_model as one of the better trained models in notebook 4. As the model pickle files are too large, they are zip and split – and needs to be recombined by tools like winzip before they can be used again.
3.	[docs](docs) – contains documentation
