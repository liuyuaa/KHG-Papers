# Paper List for Knowledge Hypergraph
> This is a collection of research papers on knowledge hypergraph, a.k.a., n-ary relational knowledge base (KB), higher-arity KB, multi-fold relational data, hyper-relational knowledge graph (KG).

## Overview
* [Fact Definition](https://github.com/liuyuaa/KHG-Papers#fact-definition)
* [Research Papers](https://github.com/liuyuaa/KHG-Papers#research-papers)
* [Public Dataset](https://github.com/liuyuaa/KHG-Papers#public-dataset)

## Fact Definition
- **tuple definition**
  - <a href="https://www.codecogs.com/eqnedit.php?latex=\inline&space;(r,e_1,e_2,\cdots,e_n)" target="_blank"><img src="https://latex.codecogs.com/png.latex?\inline&space;(r,e_1,e_2,\cdots,e_n)" title="(r,e_1,e_2,\cdots,e_n)" /></a>
- **role-entity definition**
  - <a href="https://www.codecogs.com/eqnedit.php?latex=\inline&space;\{rol_1:e_1,rol_2:e_2,\cdots,rol_n:e_n\}" target="_blank"><img src="https://latex.codecogs.com/png.latex?\inline&space;\{rol_1:e_1,rol_2:e_2,\cdots,rol_n:e_n\}" title="\{rol_1:e_1,rol_2:e_2,\cdots,rol_n:e_n\}" /></a>
- **triplet + attribute-value pairs definition**
  - <a href="https://www.codecogs.com/eqnedit.php?latex=\inline&space;(h,r,t)+\{a_1:v_1,a_2:v_2,\cdots,a_m:v_m\},\&space;(m\leq&space;n-2)" target="_blank"><img src="https://latex.codecogs.com/gif.latex?(h,r,t)&plus;\{a_1:v_1,a_2:v_2,\cdots,a_m:v_m\},\&space;(m=n-2)" title="(h,r,t)+\{a_1:v_1,a_2:v_2,\cdots,a_m:v_m\},\ (m=n-2)" /></a>

## Research Papers

* **m-TransH: On the Representation and Embedding of Knowledge Bases Beyond Binary Relations.**
  Jianfeng Wen, Jianxin Li, Yongyi Mao, Shini Chen, and Ruichong Zhang. IJCAI 2016. [paper](https://arxiv.org/pdf/1604.08642.pdf) [code](https://github.com/wenjf/multi-relational_learning)

  > m-TransH is directly extended from TransH in KG (tuple definition adopted).

* **RAE: Scalable Instance Reconstruction in Knowledge Bases via Relatedness Affiliated Embedding.**
  Ruichong Zhang, Junpeng Li, Jiajie Mei, and Yongyi Mao. WWW 2018. [paper](https://dl.acm.org/doi/pdf/10.1145/3178876.3186017) [code](https://github.com/lijp12/SIR) 

  > RAE further considers relatedness between entities using MLP, based on m-TransH (tuple definition adopted).

* **NaLP: Link Prediction on N-ary Relational Data.**
  Saiping Guan, Xiaolong Jin, Yuanzhuo Wang, and Xueqi Cheng. WWW 2019. [paper](https://www.researchgate.net/profile/Saiping_Guan/publication/333060086_Link_Prediction_on_N-ary_Relational_Data/links/5cdda342299bf14d959f3863/Link-Prediction-on-N-ary-Relational-Data.pdf) [code](https://github.com/gsp2014/NaLP)

  > NaLP concatenates role and  value embeddings, which are fed into convolution layer and fully connected layer to measure the score (role-value definition adopted). 

* **GETD: Generalizing Tensor Decomposition for N-ary Relational Knowledge Bases.**
Yu Liu, Quanming Yao, and Yong Li. WWW 2020. [paper](https://dl.acm.org/doi/pdf/10.1145/3366423.3380188) [code](https://github.com/liuyuaa/GETD)
	
	> GETD extends TuckER in KG with Tensor Ring decomposition utilized, which applies for n-ary relational KBs with single arity (tuple definition adopted).

* **HINGE: Beyond Triplets: Hyper-Relational Knowledge Graph Embedding for Link Prediction**.
Paolo Rosso, Dingqi Yang, and Philippe Cudré-Mauroux. WWW 2020. [paper](https://exascale.info/assets/pdf/rosso2020www.pdf) [code](https://github.com/eXascaleInfolab/HINGE_code)

	> HINGE learns from triplet and attribute-value pairs with convolutional layer, which are both fed into fully connected layer for final score (triplet + attribute-value definition adopted). 

* **NeuInfer: Knowledge Inference on N-ary Facts.**
Saiping Guan, Xiaolong Jin, Jiafeng Guo, Yuanzhuo Wang, and Xueqi Cheng. ACL 2020. [paper](https://www.aclweb.org/anthology/2020.acl-main.546.pdf) [code](https://github.com/gsp2014/NeuInfer)

	> NeuInfer learns from triplet and attribute-value pairs with fully connected layer, which are both fed into fully connected layer for final score (triplet + attribute-value definition adopted). 

* **HypE: Knowledge Hypergraphs: Prediction Beyond Binary Relations.**
Bahare Fatemi, Perouz Taslakian, David Vazquez, and David Poole. IJCAI 2020. [paper](https://arxiv.org/pdf/1906.00137.pdf) [code](https://github.com/ElementAI/HypE)

	> HypE  uses convolution filters to obtain entity embeddings, which are used to calculate score by multilinear product (tuple definition adopted).

* **StarE: Message Passing for Hyper-Relational Knowledge Graphs.**
Mikhail Galkin, Priyansh Trivedi, Gaurav Maheshwari, Ricardo Usbeck, and Jens Lehmann. EMNLP 2020. [paper](https://arxiv.org/pdf/2009.10847.pdf) [code](https://github.com/migalkin/StarE)

	> StarE utilizes CompGCN to update embeddings, which are further utilized for score by Transformer (triplet + attribute value definition adopted).

* **BoxE: A Box Embedding Model for Knowledge Base Completion.**
Ralph Abboud, ˙Ismail ˙Ilkan Ceylan, Thomas Lukasiewicz, and Tommaso Salvatori. NeurIPS 2020. [paper](https://arxiv.org/pdf/2007.06267.pdf)  [code](https://github.com/ralphabb/BoxE)

	> BoxE utilizes hyper-rectangles to obtain plausibility score for n-ary relational facts (tuple definition adopted).

* **G-MPNN: Neural Message Passing for Multi-Relational Ordered and Recursive Hypergraphs.**
Naganand Yadati. NeurIPS 2020. [paper](https://proceedings.neurips.cc/paper/2020/file/217eedd1ba8c592db97d0dbe54c7adfc-Paper.pdf)  [code](https://github.com/naganandy/G-MPNN-R)
  
	> G-MPNN unifies message passing for multi-relational ordered hypergraphs, which provides representation for link prediction in knowledge hypergraph (tuple definition adopted).

* **RAM: Role-Aware Modeling for N-ary Relational Knowledge Bases.**
Yu Liu, Quanming Yao, and Yong Li. WWW 2021. [paper](https://dl.acm.org/doi/pdf/10.1145/3442381.3449874)  [code](https://github.com/liuyuaa/RAM)
	
	> RAM introduces latent space and role-aware pattern matrix for multilinear scoring function (role-value definition adopted).

* **Searching to Sparsify Tensor Decomposition for N-ary Relational Data.**
Shiming Di, Quanming Yao, and Lei Chen. WWW 2021. [paper](xx)  [code](xx)

	> Leveraging AutoML for link prediction in n-ary relational KBs (tuple definition adopted).

* **ReAIE: Knowledge Hypergraph Embedding Meets Relational Algebra.**
Bahare Fatemi, Perouz Taslakian, David Vazquez, and David Poole. arxiv 2021. [paper](https://arxiv.org/pdf/2102.09557.pdf)  [code](https://github.com/baharefatemi/ReAlE)
	
	> ReAIE introduces the window concept to model the interaction of different elements of the embeddings, which are used to calculate dot scoring function (tuple definition adopted).

* **Link Prediction on N-ary Relational Data Based on Relatedness Evaluation.**
Saiping Guan, Xiaolong Jin, Jiafeng Guo, Yuanzhuo Wang, and Xueqi Cheng. TKDE 2021. [paper](https://ieeexplore.ieee.org/document/9405412)  [code](https://github.com/gsp2014/NaLP)
	
	> The journal extension of NaLP in WWW'19.
	> 
## Public Dataset:
* [JF17K](https://www.dropbox.com/sh/ryxohj363ujqhvq/AAAoGzAElmNnhXrWEj16UiUga?dl=0), firstly developed in **m-TransH**.
* [WikiPeople](https://github.com/gsp2014/WikiPeople) firstly developed in **NaLP**.
* [FB-AUTO](https://github.com/ElementAI/HypE/tree/master/data) and [M-FB15K](https://github.com/ElementAI/HypE/tree/master/data), firstly developed in **HypE**.
* [WD50K](https://github.com/migalkin/StarE/tree/master/data), firstly developed in **StarE**.


