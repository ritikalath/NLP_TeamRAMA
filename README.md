# NLP_TeamRAMA
Asking Clarifying Question in an Open Domain Dialogue System


## Task Design

The ClariQ dataset contists of:


**User Request** : an initial user request in the conversational form
 e.g. What is Fickle Creek Farm, with a label reflects if clarification is needed ranged from 1 to 4.
 
 
**Clarification questions**: a set of possible clarifying questions.
e.g. do you want to know the location of fickle creek farm?


**User Answers**: each questions is supplied with a user answer.
e.g. no i want to find out where can i purchase fickle creek farm products.

We broadly divide our task into two parts:

To answer Q1: Given a user request, return a score from 1 to 4 indicating the necessity of asking clarifying questions
To answer Q2: Given a user request which needs clarification, return a ranked list of  clarifying question

## Files

Below we list the files in the repository:

./data/train.tsv and ./data/dev.tsv are TSV files consisting of topics (queries), facets, clarifying questions, user's answers, and labels for how much clarification is needed (clarification needs).
./data/test.tsv is a TSV file consisting of test topic ID's, as well as queries (text).
./data/test_with_labels.tsv is a TSV file consiting of test topic ID's with the labels. It can be used with the evaluation script.
./data/question_bank.tsv is a TSV file containing all the questions in the collection, as well as their ID's. Participants' models should select questions from this file.
./data/top10k_docs_dict.pkl.tar.gz is a dict containing the top 10,000 document ID's retrieved from ClueWeb09 and ClueWeb12 collections for each topic. This may be used by the participants who wish to leverage documents content in their models.
./data/single_turn_train_eval.pkl is a dict containing the performance of each topic after asking a question and getting the answer. The evaluation tool that we provide uses this file to evaluate the selected questions.
 



