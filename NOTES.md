# Papers and their Summaries

## 1. Active Learning Principles for In-Context Learning with Large Language Models

[Semantic Scholar Link](https://www.semanticscholar.org/reader/91c37a88c2b320725057260677ae79f3cdaa492b) | [Arxiv Link](https://arxiv.org/abs/2305.14264)

### Main Idea

1. Selection of in-context learning examples using Active Learning approaches uncertainity, diversity, similarity and random sampling. (in a single iteration setting)
2. Experiments done on 15 models and 15 Classificationa and 9 mcq tasks
3. Uncertainity based sampling done using SPELL algorithm. Used perplexity, low perplexity set of in-context examples can yield better results.
4. Similarity : using KATE (KNN, augmented) with Sentence-Bert embeddings.
5. use K = 16 in prompting K-Shot.

### Datasets Used

### Anything I can add upon that

1. Using sophisticated algorithms like Q-learning, Self Adaptive, SG-ICL and MI in AL paradigm.
2. Rather using Active learning principles for prompting. We can use LLMs to identify what can be the best datapoints from the training data (with providing llm the labels) to train a classifier model.

---

## 2. Revisiting Relation Extraction in the era of Large Language Models

[Semantic Scholar Link](https://www.semanticscholar.org/reader/97782a67971c4ff1a74bf07e82fe20b2c4bf86c4) | [Arxiv Link](https://arxiv.org/abs/2305.05003)

### Main Idea

1. Nothing just Prompt tuning and Chain of Thought
2. Training Flan-T5 ; with generating label and also generating the explanation.
3. Evaluation done using Mechanical Turk
4. few-shot learning with GPT-3 yields near SOTA performance on standard RE datasets, outperforming fully supervised models
5. propose an approach to training Flan-T5 with Chain-of-Thought (CoT) style “explanations” (generated automatically by GPT-3) that support relation inferences; this achieves SOTA result

### Datasets Used

- ADE
- CoNLL
- NYT
- DocRED

### Anything I can add upon that

1. Nothing to be specific

-

## Self-Generated In-Context Learning: Leveraging Auto-regressive Language Models as a Demonstration Generator

[Semantic Scholar Link](https://www.semanticscholar.org/reader/dcbf62f17dad0f4554f91c822d141fb92f78429a) | [Arxiv Link](https://arxiv.org/abs/2206.08082)

### Main Idea

1. Use generated examples as In context learning to get the final answers
2. Compared the above with few shot and zero shot

### Datasets Used

- Classification datasets. like sst2, sst5

### Anything I can add upon that

1.

---

## A Survey of Active Learning for Natural Language Processing

[Semantic Scholar Link](https://www.semanticscholar.org/reader/3cd98a010b36832fc2bd8368cd4f34c72cd0ac6f) | [Arxiv Link]()

### Main Idea

1. Just goes over the standard practices in Active Learning
2. Query strategies :
   1. Informativeness : assign informative measures to each unlabelled instance individually
      1. Output Uncertanity: the most uncertain instances to be judged by the model outputs
      2. Disagreement : utilize multiple models and select the instances that are most disagreed among them
      3. Gradient Information : selecting instances that would most strongly impact the model. Since we donot know gold labels, the loss is calculated as the expectation over all labels.
      4. Performance Prediction : select instances that reduce future errors if labelled and added to the training set. Learning another model to select instances that lead to the fewest errors.
   2. Representativeness : measures how instances correlate with each other
      1. Density : instance's average similarity to all other instances
      2. Discriminative : select instances that are difference from already selected instances.
      3. Batch Diversity : select a batch on instances rather than just instance to make the process more effecient.
      4. Hybrid : at start use representativenesss strategy for sampling (as data is low) then shift to uncertainity when we have some training data.
3. Model Learning
   1. Model Mismatch : same best performing model is used throught the AL process , the query and the final model can mismatch. use a smaller distilled version of a pretrained model for querying, combined with psuedo labelling, sub sampling etc.
   2. Learning :
      1. Combine with Semi Supervised Learning
      2. Combine with Transfer LEarning
      3. Weak Supervision
      4. Data Augmentation

### Datasets Used

- No Datasets used

### Anything I can add upon that

1. We can brainstorm how can we either aid querying strategy or model learning. Something like a hybrid approach
2. We can label instances using LLMs on basis of informativeness and representativeness and then combine them together to make a better sampling strategy

## Active Learning for NLP with Large Language Models

[Semantic Scholar Link](https://www.semanticscholar.org/reader/3bc585cf8ae5953a5ea91a38a34981354f0a5a82) | [Arxiv Link]()

### Main Idea

1. Using GPT-3.5 and GPT-4 as annotators.
2. Evaluating whether a mixed GPT+human annotation can work better or equivalently in Active Learning Setting
   1. GPT annotates the data and identifies the instances where it is inconsistent
   2. Humans annotate the inconsistent instances only
   3. In AL use Random, Least confidence and breaking ties query strategies
3. AL on GPT+human annotated data performs similar or worse that just humans

### Datasets Used

- AGNews, TREC-6 and Rotten Tomatoes

### Anything I can add upon that

1. I am interested in something similar (reducing overall cost of AL)

## FreeAL: Towards Human-Free Active Learning in the Era of Large Language Models

[Semantic Scholar Link](https://www.semanticscholar.org/reader/386806bbd9d84e644ded24d4a9c7ea805c273891) | [Arxiv Link]()

### Main Idea

1. A collaborative method to combine LLMs and SLMs for active learning and removing human in the loop
2. LLMs are good source of coarse-grained information and SLMs are effective weak learners (and can distill valuable clean samples from noisy supervision). LLM operates as an active annotator infusinf its knowledge and SLM acts as a student to filter out the high quality input-label pairs to feed back the LLM for subsequent label refinery.
3. Method
   1. Active labelling by LLMs
      1. Initial annotation by Self Generated Demonstration
      2. Refined annotation in Subsequent Rounds
   2. Knowledge Distillation by SLMs
      1. Robust Self training
         1. Selection based technique + GMMs to find out clean samples, and consistency regularizations and back translation
      2. Demonstration Pool Filtering
         1. using a small loss criterion and k-mediods

### Datasets Used

-

### Anything I can add upon that

1.

##

[Semantic Scholar Link]() | [Arxiv Link]()

### Main Idea

1.

### Datasets Used

-

### Anything I can add upon that

1.
