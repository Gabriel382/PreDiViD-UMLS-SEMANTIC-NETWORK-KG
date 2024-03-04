# PreDiViD-UMLS-SEMANTIC-NETWORK-KG
Code for manipulating UMLS's metathesaurus and semantic network to create a Knowledge Graph that can be further explored for medical applications.

## What is UMLS? And why a graph?

The Unified Medical Language System (UMLS) is a set of ontologies and associated resource files, lexicons, etc. that together provide a comprehensive set of structured concepts, codes, and text descriptors for the biomedical domain. UMLS is widely used in biomedical informatics research and in a variety of clinical software products, but the raw UMLS files are a bit unwieldy. If you want to do more than simply load UMLS into a database and search for a given concept, code, etc. its structure can be difficult to understand and manipulate.

My own work has focused on natural language processing (NLP) and I've often encountered situations where I want to find all of the synonyms for a given clinical concept, or I want to know hierarchical relationships for a given term (Ex. "Atherosclerosis is a type of cardiovascular disease."). In many of these cases, UMLS can help, but it often doesn't seem worth the effort to parse all of the raw UMLS files.

Even though it wasn't designed to be used this way, I've found that it often helps to think of UMLS as a graph. Different ontologies can be combined in a flexible way to produce graph structures that represent different subsets of UMLS, and the nodes of the graph (concept unique identifiers, or CUIs) can be decorated with synonyms, billing codes, or whatever you want. So I've written some basic code that converts the raw UMLS files into a graph structure, the details of which can be manipulated using a single configuration file.

The cose is based on this github project https://github.com/Nguyendat-bit/UMLS-KG

Here, both UMLS's CUI and AUI from the metahesaurus, and the STY from the Semantic Network are represented as nodes in the knowledge graph.

## Tutorial

Follow the referenced github (https://github.com/Nguyendat-bit/UMLS-KG) instructions for setup. Then, run "meta-semantic.ipynb" to generate 
extra csv tables for the semantic network and its relations.

## Some Final Notes

This is just some utility code that I've found useful - it is not production-grade and there are bound to be errors. Please let me know if you find any. My plan is to refine it in the coming months. If you're part of the biomedical research community and have any advice or want to contribute, I'd love to hear from you. I can be reached at bethany.percha@mssm.edu.

Please note that this code is released under the [GPL](https://www.gnu.org/licenses/gpl-3.0.en.html). 

