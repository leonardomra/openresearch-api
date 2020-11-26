# OpenResearch API

The OpenResearch API is an highly expandable, modular and scalable cloud service that provides the means to train, fine-tune and deploy language models. This project aims at establishing a ground infrastructure (RESTful API) on top of which machine learning services based on language models can be refined and have their results coupled with third-party systems. Such use cases include the enhancement of aggregators, chatbots, dashboards, etc.  

In this regard, the API supports at the moment Topic Modeling with Latent Dirichlet Allocation (LDA), Named Entity Recognition with BioBert (NER + BioBert), and Question & Answering with BioBert (Q&A + BioBert). Once these models are published online, the API enables seamless integrating with third-party services, so that the following use cases are possible:

* Classification of thousands of documents into automatically identified categories;
* Semantic information retrieval using natural language;
* Extraction of keywords (e.g. gene/protein; disease; drug/chemical; species; mutation). 

## Build 

Build all services of the API locally with Docker Compose:

`docker-compose -p "OpenResearch" -f docker-compose-openresearch.yaml up --build`