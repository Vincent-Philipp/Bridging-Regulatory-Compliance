# Bridging-Regulatory-Compliance
The adoption of the EU AI Act on May 21, 2024, marks a significant regulatory shift that places new demands on industries that rely on AI systems. These regulations create a need for industries to prepare their AI systems to meet stringent requirements that ensure safety, transparency, and accountability. The AI Act requires that AI applications be categorized into one of four risk classes. The focus is on high-risk AI systems, which are subject to strict regulations. The need for clear metrics and standards is great, as many of the necessary standards from organizations such as ISO and DIN are still being developed. In this paper, we present guidelines for the development of high-risk AI systems that address the requirements of the AI Act. In addition, we map existing standards and metrics to the requirements, supported by solution approaches and best practices, as well as methods and tools. To ensure practicality, we evaluated and refined our guidelines using two use cases provided by an industry partner.

This living document specifies the requirements that were proposed in the paper [EU AI Act: A Practical Report on Bridging Regulatory Compliance and Industrial AI Standards]().

# Guidelines for conformity assessments
Below the developed guidelines are specified. Each guideline consists out of 4 parts. First the name of the guideline, followed by the articles of the EU AI Act where they are applicable to. Afterwards a short specification derived from the EU AI Act is given. Last methods, norms and standards, usefull tools as and best practices knowm to the authors are linked.

## AI expertise
Art 4; Art. 53

Providers and operators of AI systems must ensure that company employees have appropriate AI skills for their tasks, evaluated according to those tasks. 	ISO/IEC AWI 42105 Human oversight of AI systems [under development]

ISO/IEC AWI TR 42109 Use cases of human-machine teaming [under development]

## Classification of the application into a risk class of the AI Act
Art. 5; Art. 6; Art. 51; Annex II; Annex III; Annex XIII	

Risk assessment according to the risk classes of the AI Act

ISO/IEC TR 5339 Guidance for AI applications <br >
ISO/IEC TR 5469 Functional safety and AI systems <br >
ISO/PAS 8800 Safety and AI in road vehicles <br >
ISO/IEC AWI TS 22440-x Series Functional safety and AI systems [under development] <br >
ISO/IEC 23894 AI risk management <br >  
ISO/IEC 22989 Artificial intelligence concepts and terminology <br >
ISO/IEC 42001 AI management systems <br >
ISO 9001 Quality management systems requirements <br >
ISO/IEC FDIS 42005 AI system impact assessment [under development]  

## Requirements for GPAI providers
Art. 53; Art. 56; Annex XI; Annex XII
Technical documentation in accordance with Annex XI and, if applicable, Annex XII

ISO/IEC TS 8200 Controllability of AI systems <br >
ISO/IEC DIS 12792 Transparency taxonomy of AI systems [under development] <br >
ISO/IEC AWI TS 22443 Addressing societal concerns and ethical considerations [under development] <br >
ISO/IEC 23894 AI risk management <br >
ISO/IEC 42001 AI management systems <br >
ISO 9001 Quality management systems requirements <br >
ISO/IEC FDIS 42005 AI system impact assessment [under development]

## Assess the risk of the application for life and health
Art. 5 §1 (a); Art. 9; Art. 53; Art. 56
Risk assessment includes:
a) Identifying and analyzing known and foreseeable risks to health, safety, or fundamental rights when the high-risk AI system is used as intended.
b) Estimating and evaluating risks that may arise from intended use and reasonably foreseeable misuse.
c) Evaluating additional risks based on data collected through post-market surveillance.	ISO/IEC TR 5469 Functional safety and AI systems

ISO/PAS 8800 Safety and AI in road vehicles <br >
ISO/IEC AWI TS 22440-x Series Functional safety and AI systems [under development] <br >
ISO/IEC 26262 / DIN EN 61508 Functional Safety <br >
ISO/IEC 23894 AI risk management <br >
ISO 31000 Risk management <br >
ISO 9001 Quality management systems requirements <br >

## Description of the technical methods used to ensure data completeness
Art. 10 §2 (h), §5	
Analysis of use cases and training data; evaluation of health hazards and identification of relevant labels that include demographic or sensitive attributes. Detection of biases in relevant training data sets.	

ISO/IEC 5259-x Series Data quality <br >
Data Version Control (DVC) <br >

## Identify and document sensitive attributes in data
Art. 10 §2 (b), (f)

Findings of a test for sensitive data.	

ISO/IEC 5259-x Series data quality <br >
ISO/IEC TR 24027 Bias in AI systems <br >
ISO/IEC TR 24368 Ethical and societal concerns <br >
ISO/IEC AWI TS 22443 Addressing societal concerns and ethical considerations [under development] <br >
ISO/IEC 5339 Guidance for AI applications <br >
Gender-based Illicit Proximity Estimate, <br > 
Equalized Odds, <br > 
Equality of opportunity, <br > 
Demographic parity, <br >
Predictive equality, <br >
Conditional statistical parity,  <br >
Conditional use accuracy <br >

## Documentation of how the data distribution represents real-world conditions
Art. 10 §2 (d), §3

Recording of environment-specific situations; verification of representative data volumes per situation.

DIN SPEC 92005:2024-03 Quantifizierung von Unsicherheiten <br >
ISO/IEC 5259-x Series data quality <br >
ISO/PAS 8800 Safety and AI in road vehicles <br > 
ISO/IEC TS 4213 Assessment of machine learning classification performance <br >
Data Sheets / Data Cards

## Documentation of limitations such as errors, noise or biases in the data
Art. 10 §2

Documentation of systematic errors, biases and inaccuracies in the data.	

DIN SPEC 92005:2024-03 Quantifizierung von Unsicherheiten <br >
ISO/IEC 5259-x Series data quality <br >
ISO/PAS 8800 Safety and AI in road vehicles <br >
ISO/IEC TR 24029-x Series Robustness of neural networks

## Creating representative data splits	
Art. 10 §2, §3	

Ensure data reflects realistic conditions and avoids biases. Use stratification or randomization for representative data splits, and document methods for reproducibility. Prevent data leakage to avoid distorting model performance.

ISO/IEC 5259-x Series data quality <br >
[Scikit-learn methods for data splitting](https://scikit-learn.org/stable/)  
[Cleanlab for bias management ](https://github.com/cleanlab/cleanlab)

## Documentation of characteristics of the training and test data
Art. 10 §2, §3

Record data sources in detail (typology, volume, relevance). Thoroughly analyze data distribution and potential biases. Identify and document sensitive and demographic attributes for fairness assessments. Provide a complete description of methods used to ensure data quality, including preprocessing steps and their impact on data integrity.

ISO/IEC 23053:2022 Framework for AI System Performance using ML <br >
Frameworks: Ydata Profiling, Pandas Profiling, Great Expectations <br >
statistical methods: Kolmogorov-Smirnov-Test, Chi²-Test, Shapiro-Wilk-Test
Datasheets for datasets

## Ensuring the accuracy of the model	
Art. 15 §1; Art. 72

Evaluate model accuracy using application-specific metrics like precision, recall, F1 score, or AUC-ROC. Verify accuracy by comparing with established benchmarks or test metrics. Fully document test methods, evaluation metrics, results, and potential limitations.

ISO/IEC 23053:2022 – Framework for artificial intelligence (AI) systems using machine learning (ML) <br >
ISO/IEC TR 4213 – Evaluation of machine learning classification performance <br >
ISO/IEC TS 8200 – Controllability of automated AI systems <br >
ISO/IEC AWI 24970 Logging of AI systems [under development] <br >
Metrics and evaluation frameworks: Precision, Recall, F1-Score, AUC-ROC, RMSE, MAE <br >
Benchmarking tools: [MLflow](https://www.tensorflow.org/tensorboard) , [TensorBoard](https://mlflow.org/) , Scikit-learn Evaluation modules <br >
Monitoring and validation systems: Monitoring dashboards <br >

## Ensuring the robustness of the system	
Art. 10 §4, Art. 15 §1	

Conduct systematic tests to assess system robustness, including simulating edge cases and adversarial inputs. Ensure resilience to disruptions like erroneous data or unusual user interactions. Document measures and results to validate robustness and identify potential vulnerabilities. The system must meet required accuracy and security standards under various conditions.	ISO/IEC TR 24029-x Series robustness of neural networks.

ISO/IEC AWI 24970 AI system logging [under development] <br >
ISO/IEC 42001:2023 Information technology – Artificial intelligence – Management system <br >
Adversarial Robustness Toolbox (ART): open-source framework for conducting adversarial testing (GitHub)

## Documentation of the required level of explainability and interpretability of the model	
Art. 13, Art. 15 §3	

Use transparent, well-documented AI models, including operation, intended purpose, and foreseeable defects (Art. 13, §3). Evaluate necessary model complexity and determine explainability levels based on the use case, target group, and risks. Transparently state the limits of explainability, especially for complex models like deep learning. Ensure the explanation strategy aligns with legal and ethical requirements and is documented.	ISO/IEC TR 24028 Trustworthiness in artificial intelligence.

ISO/IEC 42001 AI management system <br >
ISO/IEC TR 24028 Trustworthiness  <br >
ISO/IEC 22989 Terminology <br >
ISO/IEC TS 8200 Controllability of AI systems <br >
ISO/IEC DTS 6254 Explainability and interpretability [in development] <br >
ISO/IEC DIS 12792 Transparency taxonomy of AI systems [in development] <br >
Explainability tools: SHAP (documentation), LIME (GitHub), Saliency Maps <br >
Model alternatives: Decision trees, generalized additive models (GAMs), linear models <br >

## Documentation of benchmarks, model evaluation and model selection	
Art. 10 §1-2, Art. 15 §1, §3, Annex VIII, Annex IX

Conduct a comprehensive model evaluation using suitable application metrics. Document results, test methods, benchmarks, and relevant scenarios. Transparently present limitations, potential risks, and edge cases. Ensure the evaluation meets regulatory and ethical standards.

ISO/IEC TR 24029-x Series robustness of neural networks <br >
ISO/IEC AWI 24970 AI system logging [under development] <br >
ISO/IEC 42001 AI management systems <br >
ISO 9001 Quality management systems requirements <br >
Evaluation platforms: [Weights & Biases (website)](https://wandb.ai/site) , [MLflow](https://www.tensorflow.org/tensorboard) <br >
Metrics: Precision, Recall, F1-Score, ROC-AUC, Log-Loss

## Documentation of the selected metrics and justification of their use in the context of the use case and, if necessary, considerations of fairness	
Art. 13; Art.15 §1, §2	

Use well-documented AI models. Documentation should include metrics used and their performance, including those related to specific individuals or groups for relevant use cases (Art. 13, §3(b)(ii), (v)). Referencing the use case and selection decisions adds transparency when interpreting performance. However, as per Article 15(2), specific metrics or limits to adhere to have not yet been developed.	

ISO/IEC TS 4213 Assessment of machine learning classification performance <br >
ISO/IEC TR 24027 Bias in AI systems  <br >
ISO/IEC AWI TS 22443 Addressing societal concerns and ethical considerations [under development] <br >
ISO/IEC 23053 Framework for AI Systems

## Documentation of the test design (AI system level)	
Art. 9 §6, §7, §8; Art. 60; Annex IV §2 (g); Annex IX, Art. 53

Ideally, create and document the test design before training, defining relevant metrics. It should consider the AI system's intended purpose and include details on validation and test data and their key characteristics. Indicate parameters used to measure robustness and other relevant requirements (including for high-risk AI systems and discriminatory effects, if applicable). Tests must be conducted before the AI system is marketed or deployed.	ISO/IEC TS 4213 Assessment of machine learning classification performance.

ISO/IEC TS 8200 Controllability of AI systems <br >
ISO/PAS 8800 Safety and AI in road vehicles <br >
ISO/IEC AWI 24970 AI system logging [under development] <br >
ISO/IEC AWI TS 42119-2 Overview of testing AI systems [under development] <br >
ISO/IEC CD TS 42119-3 Verification and validation analysis of AI systems [under development] <br >
Model Cards for Model reporting: 
model-card-toolkit

## Description of potential risks, edge cases and worst-case scenarios and simulation of these in test scenarios, if possible	
Art. 13 §3 (b)	

Systematically list all potential technical and operational risks and edge cases affecting the AI system's operation. Include clear definitions and examples of edge cases and worst-case scenarios. If possible, simulate these scenarios in realistic tests to evaluate the model's response.	SDV (Syntehtic Data Vault) offers various methods for generating synthetic data
Prototype Generation

## Description of the test results (AI system level)	
Art. 53 §1 (a), Annex IV §2 (g)

Provide comprehensive, transparent documentation of test results, including detailed performance metrics. Interpret results in relation to AI system objectives, highlighting potential weaknesses or risks. Use the test design to simulate potential risks, edge cases, and worst-case scenarios in test scenarios when possible.	

ISO/IEC TS 8200 Controllability of AI systems <br >
ISO/IEC AWI 24970 AI system logging [under development] <br >
ISO/IEC AWI TS 42119-2 Overview of testing AI systems [under development] <br >
ISO/IEC CD TS 42119-3 Verification and validation analysis of AI systems [under development] <br >
TensorBoard and Mlflow <br >
Version control tools, e.g. GitHub or Weights & Biases <br >
Model card toolkit

## Documentation of the model's limitations	
Art. 13 §3(b); Art.14 §4 (a); Annex IV §3; Art. 53

Describe all known model limitations comprehensively and understandably, considering both technical and contextual aspects. Indicate conditions where the model may not perform as expected and factors influencing its accuracy and reliability. Provide a clear presentation of possible failure scenarios and their effects.	

ISO/IEC DIS 12792 Transparency taxonomy of AI systems [under development] <br >
ISO/PAS 8800 Safety and AI in road vehicles  

## Documentation and explanation of measures derived from the test results
Not directly demanded by the EU AI Act / best practices

Clearly and systematically document all measures derived from test results, explaining the rationale behind each and referencing specific test results. Consider potential impacts of these measures on the AI system and its environment. Transparent presentation of decision-making processes is crucial to foster acceptance of proposed changes.	ISO/IEC TS 8200 Controllability of AI systems.

ISO/PAS 8800 Safety and AI in road vehicles <br >
ISO/IEC 23894: AI Risk Management <br >
ISO/IEC AWI TS 42119-2 Overview of testing AI systems [under development] <br >
ISO/IEC CD TS 42119-3 Verification and validation analysis of AI systems [under development]

## Post-market surveillance system	
Art 72; Annex VII	

Establish a PMMS to continuously monitor AI system usage data, performance, and malfunctions (Art. 72 §1). Regularly submit reports to designated authorities. Identify new risks from real-time data and assess their impact on safety and reliability (Annex VII §3). Develop and implement corrective actions to address deficiencies or comply with new regulations.	

ISO/IEC 42001 Information technology - Artificial intelligence - Management system <br >
ISO 9001 Quality management systems requirements <br >
ISO/IEC TS 8200 Controllability of AI systems <br >
ISO/IEC 5259-x Series Data quality

