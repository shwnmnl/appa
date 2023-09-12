# Automated Projective-Psychometric Assessment

The Automated Projective-Psychometric Assessment, or APPA for short, harnesses skills and expertise acquired during my BSc in psychology at [UQÀM](https://uqam.ca) and my MSc in Biomedical Data Science at the [Université de Montréal](https://www.umontreal.ca/). APPA integrates programming and machine learning tools with psychological and psychiatric evaluation to objectively map subjective experience in N-dimensional latent spaces, where precise locations reflect differences in subjective experience linked to distinct mental health symptom profiles.

It’s basic structure is two-fold: a fully automatizable ML pipeline written in Python on the ‘back end’, and a Shiny app written in R on the 'front-end' for visualizations. It was developped based off of these sub-projects:

1. **OpenProjection** rests on a combination of open and privately shared data, specifically verbal reports to the Thematic Apperception Test (TAT).
   - Open data were accessed through [MTSU](https://jewlscholar.mtsu.edu/collections/c1b01991-f9c7-4875-bda7-967ce0892709). This initial exploratory effort includes multiple lower-dimensional mappings of embeddings extracted from [CLIP](https://openai.com/research/clip), as well as a toy prediction of [LIWC-22](https://www.liwc.app/) variables (with comparison to the [ada-002](https://openai.com/blog/new-and-improved-embedding-model) language model).
   - Private data were shared by Dr Jean Gagnon from the Electrophysiology Laboratory in Social Neuroscience, which in addition to TAT data, include a battery of psychometric assessments. Providing (admittedly sparser) lower-dimensional mappings, CLIP embeddings for this limited dataset (N = 52) are used to predict a more relevant outcome (again, with comparison to ada-002). Here, deriving relevant psychometric targets to predict is cast as un unsupervised learning task, loosely inspired by [Rouault et al.'s paper](https://www.sciencedirect.com/science/article/pii/S0006322318300295). 

This served as a springboard for :

2. **DeepProjection**, is an ongoing large-scale online study which integrates a breadth of psychometric inventories, including those used in Rouault et al. (2018), as well as personnality and defense mechanism-related questionnaires. It extends their findings on perceptual decision-making and metacognition to encapsulate higher-order constructs such as mental health and subjective experience. 
