### HOTPOT QA

In the current Question Answering applications, the answers generally can be able to found in a specific part of the context without reasoning. In these applications, there is no need to make inference and look at different parts of the text to reach an answer. It is clear that this is not the case in many of the questions wee see in our daily lives. When we try to find an answer to a question, the answers may not always be found in the context directly and we may need to look at different parts of the text and make some kind of inference. This is where traditional Question Answering systems are stuck. 

In this project, the main goal is to develop a model that can be able to make inference and reasoning when required to be able to find an answer to the different types of questions. Because there are some ready-to-use datasets that can be used for this goal, data preparation step is skipped. The dataset that is used in this project is HotpotQA because of the the reasons below: 

1) It was prepared to test the systems' ability to make reasoning and inference in a large context. 
2) It is quite diverse and relatively large dataset. There are different types of questions in different structures and in different topics. For example, there are comparison questions (e.g. Who was born in the capital of the England, Charlie Chaplin or Grant Kirkhope ?), yes/no questions as well as regular questions that we typically see in our daily lives. (e.g. The John Wall Dance is a dance performed by flexing the arms and twisting the wrist, John Wall, an American professional basketball player for the Washington Wizards, of the National Basketball Association (NBA), first performed the eponymous dance during his introduction at Big Blue Madness in October 2009, at which location?). 
3) It includes the supporting facts, in other words, sub-texts that lead to the answers. The supporting facts help the model to make inference and reasoning.  

Up until now, the best performing model was achieved by filtering out the documents that are not related to the answers by using a document classifier that was trained with a pairwise learning-to-rank loss. After filtering out these documents, the rest of the documents that are related to the answers are then put into the model to predict the answer and supporting facts jointly. The model that is trained with these filtered documents is optimized based on both token-level (for answers) and sentence-level prediction (for supporting facts) with the use of attention-based interaction between these two tasks. 









