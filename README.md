# Read, Love, Pray  [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

This is a list of papers :bookmark_tabs: that I particularly enjoy and would love to share with you. If you have papers that you want to share, just put it down as an issue and I will update the list!

##### Table of Contents  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Machine Learning](#machine-learning)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Neuroscience](#neuroscience)
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Distributed System](#distributed-system) 

======

<a name="machine-learning"/>
### Machine Learning

* #### [A Few Useful Things to Know about Machine Learning](https://github.com/WesleyyC/Read-Love-Pray/blob/master/a-few-useful-things-to-know-about-machine-learning.pdf)

  This article summarizes twelve key lessons that machine learning researchers and practitioners have learned. While these lessons are simple to understand, I learn something new everytime I read it.


* #### [Deep learning](https://github.com/WesleyyC/Read-Love-Pray/blob/master/deep-learning.pdf)

  This is a review paper by Yan LeCun et al. and it gives a good general picture about deep learning. In my opinion, what a wikipedia page should look like after the summary section.
  
* #### [Dropout](https://github.com/WesleyyC/Read-Love-Pray/blob/master/dropout.pdf)

  Regularization is a very important component in machine learning. This paper in particular, talks about the regularization challenge in deep learning. While deep learning in some way mimic human's brain strucutre with layers of process, it does not provide the flexibility in structure as human brain do. This paper describes a simple way to create a robust deep learning model that allow some of the "neurons" turn down during the reading. What is particularly beautiful about this paper is that it starts with a biology motivation and end with a great mathmatical solution for machine learning.
  
* #### [Go Game and Deep Learning](https://github.com/WesleyyC/Read-Love-Pray/blob/master/mastering-the-game-of-Go-with-deep-neural-networks-and-tree-search.pdf)

  This is a very high profile paper. While the concepts in the paper are not new, the way Deepmind teams put them together is an engineering gem. Plus, it is a interesting challenge as Go is not an easy game...
  
======  

<a name="neuroscience"/>
### Neuroscience

* #### [A Quantitativer Description of Membrane Current](https://github.com/WesleyyC/Read-Love-Pray/blob/master/A%20Quantitativer%20Description%20of%20Membrane%20Current%20and%20its%20Application%20to%20Conduction%20and%20Excitation%20in%20Nerve.pdf)

  This paper far before we knew anything about ion channel in neuro signaling, but via rigorous experiment setup and amazing imagination, Hodgkin and Huxley formula the ion channel behavior which still makes sense today. (It does take a while to get used to their notation since they used different sign for polarization and hyperpolarization...)
  
* #### [Transient Dynamics versus Fixed Points in Odor Representations by Locust Antennal Lobe Projection Neurons](https://github.com/WesleyyC/Read-Love-Pray/blob/master/Transient%20Dynamics%20versus%20Fixed%20Points%20in%20Odor%20Representations%20by%20Locust%20Antennal%20Lobe%20Projection%20Neurons.pdf)

  How PCA, a classic feature reduction techniques in ML, could help us visualize neuro coding and reveal the "state" coding regime?
  
* #### [Cortical Neural Ensemble Responses Emerges Suddenly](https://github.com/WesleyyC/Read-Love-Pray/blob/master/Cortical%20Neural%20Ensemble%20Responses%20Emerges%20Suddenly.pdf)

  By the same token as the above paper, how hidden markov model could be used to explain neuro coding, specifically temporal coding.

======  

<a name="distributed-system"/>
### Distributed System

* #### [Paxos made simple](https://github.com/WesleyyC/Read-Love-Pray/blob/master/paxos.pdf)

  This is not a paper but a very simple and clear explanation for Paxos, which is considered to be difficult to understand. I think Paxos is a super neat idea to replicate nodes and imagine a bunch machine vote about what they want to do together is hilarious. While not very efficient communication wise, forcing partition overlap using majority is so simple in math and so powerful in system.
  
* #### [Dynamo](https://github.com/WesleyyC/Read-Love-Pray/blob/master/dynamo.pdf)

  Dynamo is an interesting paper for me because it shows what engineering really is. Amazon has a unique need to make sure all the put operation to went through with a 99.9% SLA and they specifically design a system for it. This is also a very well written paper with good description of related work and their motivation, which shows a great deal of engineering mind set. The ring hash + vitrual node idea is also very cute and actually inspire some [other interesting distributes system @ Uber for realtime dispatching](https://eng.uber.com/intro-to-ringpop/), which again, is an unique problem with a specifically engineered solution.
  
* #### [ZooKeeper](https://github.com/WesleyyC/Read-Love-Pray/blob/master/zookeeper.pdf)

  Love open source work and good modulization! While there are other synchronized core out there, I find reading this paper entertaining because it shows how we can use a simple primitive to implement other complex system.
  
* #### [ZooNet/Composition of Synchronized Core](https://github.com/WesleyyC/Read-Love-Pray/blob/master/modular-composition-of-coordination-services.pdf)

  This is a relatively new paper continue the topic of ZooKeeper. While synchornized core is simple to use, it is hard to put them together and have multiple applications with their own ZooKeeper instance synchornizing with each other. However, this paper used a incredibly simple client-layer code to fix the problem (150 lines of code) and that really captures the beauty of solving system problem. Moreover, they find a "bug" in the ZooKeeper after 3.x version iteration and improve the performance, again, with some very simple code/idea.
  
* #### [MapReduce](https://github.com/WesleyyC/Read-Love-Pray/blob/master/mapreduce.pdf)

  I am a big fan of functional programing so reading this paper is like an orgasm with the "map" and "reduce" function. It is neat that Jeff Dean and his wingman, Sanjay Ghemawat, decided to think of distributed computing problem as map and reduce and endup modulized the idea with cute engineering refinement/discussion.

* #### [Spanner](https://github.com/WesleyyC/Read-Love-Pray/blob/master/spanner.pdf)

  Another paper from Google Research! This is a super complicated system including Paxos, time clock etc. However, it really push the boundary about what's the best we can do with the most advanced technology and knowledge in system's world. Its a good engineering lesson to see how all the piecies are putting together and make sense.
  
* #### [Farm](https://github.com/WesleyyC/Read-Love-Pray/blob/master/farm.pdf)

  Well, yet another paper yells "We want it all!". This paper is super cool with its "one-sided" disk read (i.e. control other computers' disk read/write to memory without interupting their cpu) and memory cahce database (which is possible with a special battery that can move memory into disk during sudden power failure). We want it all!

  
