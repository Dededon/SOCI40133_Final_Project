# SOCI40133_Final_Project
### Author: Ryan Leung (Liang)    
### Email: hleung@uchicago.edu

# Project Background
My final project is about the content analysis for all of the administrative lawsuits against police departments in U.S. Federal Courts. I have used a combined approach of keyword search and legislation code search to scrape in total 19K cases from the opinion database of Court Listener. The 19K cases are in HTML / XML format, and in this assignment, I have used 14K roughly cleaned cases from the database to perform the pre-analysis. Particularly, I'm interested in the timeframe after the 1960s, where notable civil rights cases, like Monroe v. Pape, have changed the landscape of administrative lawsuits in the U.S. legal field. I still have to perform data cleaning on the database, to identify the related metadata, case background and history, and decisions. 

# Importance in Substantive Topic
My research question is whether we could capture pattern of legal changes through variations of linguistic behaviours. Speaking in another way, my point of interest is what makes our the current status of administrative law in controlling police misconduct nowadays. First, I wonder what are the contexts of the administrative lawsuits within the database. Next, I am curious about what legal resources, and what contexts of legal resources, are referenced in the making of judicial decisions. 

# Research Question
What topics of law is invoked in the legal discussion? How can we extract patterns of legal change?

# Method Deisgn
1. First, I used unsupervised topic modelings methods to capture the topic of the law of matter, to observe what are the topics of legal principles are being cited and "circulated" throughout the judicial discourses.
2. Next, I use keyword search to extract the paragraphs of motions made in the cases. As motion is a procedural device in lawsuits, I expect languages to be more formalized in these paragraphs.
3. I trained Skip-gram and C-BOW models on the paragraphs of motions. I use K-SVD decomposition to extract the discourse atoms. After that, I visualize the distribution for the discourse atoms in the paragraphs of motion-making for interpreting the temporal change in topics of motion.
4. Last, I train a Word2Vec model on the full corpus, to see the semantic change of "motion" and "claim", by visualizing how their co-occurences with legal terminologies in the context change along the time.

# File Description
**Topic_Modeling.ipynb**: Codes to do topic modeling with the cited legal documents.
**Topic_Distribution.ipynb**: Codes to do normalize the yearly distribution of the topics.
**paragraph_embedding.ipynb**: Codes to generate a paragraph embedding with Sentence Transformers. As the results are not satisfying, it is not presented in the final paper.
**discourse_atom.ipynb**: Codes to generate the discourse atom.
**dynamic_word2vec.ipynb**: Codes to train and generate the visualization for the Dynamic Word2Vec.

# Keywords
Semantic Space, Topic Modeling, Latent Dirichlet Allocation, Dynamic Word2Vec, Discourse Atom
