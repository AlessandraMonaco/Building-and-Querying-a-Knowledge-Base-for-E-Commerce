# BUILDING AND QUERYING A KNOWLEDGE BASE FOR E-COMMERCE : a Protègè project

## The Domain and the Knowledge Base
This repository implements a simple Knowledge Base for E-commerce domain in Protègè 5.5.0.
We considered a fictionary e-commerce website, selling technological products, having two subdomains:
- A **Product domain** storing all the information related to products (categories, subcategories, properties and details);
- A **Customer domain** storing information related to customer accounts on the website and their activities (purchases, product visualizations, reviews,...).

The KB is stored in the file e-commerce.owl, and has the following size:

Axiom	1315	

Logical axiom count	818	

Declaration axioms count	217	

Class count	44	

Object property count	9	

Data property count	28	

Individual count	129	

Annotation Property count	11

## Motivations and goals
In the E-commerce domain, semantics can really help to derive significant insights from data, in order to
- improve *customer experience* with better product retrieval and recommendation (similar products, related products, products bought together, products bought by similar users,..);
- support *customer analysis and segmentation*, diving customers basing on patterns or definitions related to their actions on the website, allowing to segment by country (looking at delivery locations), by categories or macro-categories of products they are interested in (ex: AppleFan, GamerCustomer), or *gold customers* (spending a lot of money on the website), and to analyze single user histories but also customer preferences over products (best seller product, most clicked product, most reviewed,...).

Moreover, the use of an ontology instead of a standard database allows to have a flexible representation of the domain, making possible to instanciate different properties for different category of products, without respecting a predefined schema with predefined property names.

## Querying and reasoning
Thanks to Protègè flexibility (many plugins, reasoners, views, query languages) and usability (good graphic interface), we were able to easily reason and query extracting interesting insights from our toy dataset.
Reasoning and inference has been done using *Pellet* reasoner.

We performed the following **Reasoning tasks** using OntoDebug plugin:
- Knowledge Base **consistency** and **coherency** checking;
- **Atoms entailment** (entailed and non-entailed test cases are stored as annotations in the KB);
- **Solving inconsistencies** using the Debugger;

We also queried the KB using the supported query languages:
- **DL queries** (description logics, Open World Assumption);
- **SPARQL queries** (triple based, Closed World Assumption);
- **SQWRL queries** (rule-based, Owl-RL profile, Open World Assumption with the possibility to simulate Closed World with set operators).


## How to use this repository
1. Download *Protègè 5.5.0* (or the latest version that you find) and Pellet, SPARQL, SQWRLTab, DLquery tabs
2. Import e-commerce.owl in Protègè 
3. Start Pellet resoner to debug and to inferences
4. Copy queries contained in folders SPARQL-queries, DL-queries, SQWRL-queries of this repo and paste them in the correspondent tab of Protègè

If you are interested in more details you can check presention.pdf file.
