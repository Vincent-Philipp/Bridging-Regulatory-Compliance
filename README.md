# Bridging-Regulatory-Compliance

# Guidelines for conformity assessments
Below the developed guidelines are specified. Each guideline consists out of 4 parts. First the name of the guideline, followed by the articles of the EU AI Act where they are applicable to. Afterwards a short specification derived from the EU AI Act is given. Last methods, norms and standards, usefull tools as and best practices knowm to the authors are linked.

## AI expertise
Art 4; Art. 53

Providers and operators of AI systems must ensure that company employees have appropriate AI skills for their tasks, evaluated according to those tasks. 	ISO/IEC AWI 42105 Human oversight of AI systems [under development]

ISO/IEC AWI TR 42109 Use cases of human-machine teaming [under development]

## Classification of the application into a risk class of the AI Act
Art. 5; Art. 6; Art. 51; Annex II; Annex III; Annex XIII	

Risk assessment according to the risk classes of the AI Act

ISO/IEC TR 5339 Guidance for AI applications
ISO/IEC TR 5469 Functional safety and AI systems
ISO/PAS 8800 Safety and AI in road vehicles  
ISO/IEC AWI TS 22440-x Series Functional safety and AI systems [under development]
ISO/IEC 23894 AI risk management
ISO/IEC 22989 Artificial intelligence concepts and terminology
ISO/IEC 42001 AI management systems
ISO 9001 Quality management systems requirements
ISO/IEC FDIS 42005 AI system impact assessment [under development]

## Requirements for GPAI providers
Art. 53; Art. 56; Annex XI; Annex XII
Technical documentation in accordance with Annex XI and, if applicable, Annex XII

ISO/IEC TS 8200 Controllability of AI systems
ISO/IEC DIS 12792 Transparency taxonomy of AI systems [under development]
ISO/IEC AWI TS 22443 Addressing societal concerns and ethical considerations [under development]
ISO/IEC 23894 AI risk management
ISO/IEC 42001 AI management systems
ISO 9001 Quality management systems requirements
ISO/IEC FDIS 42005 AI system impact assessment [under development]

## Assess the risk of the application for life and health
Art. 5 §1 (a); Art. 9; Art. 53; Art. 56
Risk assessment includes:
a) Identifying and analyzing known and foreseeable risks to health, safety, or fundamental rights when the high-risk AI system is used as intended.
b) Estimating and evaluating risks that may arise from intended use and reasonably foreseeable misuse.
c) Evaluating additional risks based on data collected through post-market surveillance.	ISO/IEC TR 5469 Functional safety and AI systems

ISO/PAS 8800 Safety and AI in road vehicles
ISO/IEC AWI TS 22440-x Series Functional safety and AI systems [under development]
ISO/IEC 26262 / DIN EN 61508 Functional Safety
ISO/IEC 23894 AI risk management
ISO 31000 Risk management
ISO 9001 Quality management systems requirements

## Description of the technical methods used to ensure data completeness
Art. 10 §2 (h), §5	
Analysis of use cases and training data; evaluation of health hazards and identification of relevant labels that include demographic or sensitive attributes. Detection of biases in relevant training data sets.	

ISO/IEC 5259-x Series Data quality
Data Version Control (DVC)

## Identify and document sensitive attributes in data
Art. 10 §2 (b), (f)

Findings of a test for sensitive data.	

ISO/IEC 5259-x Series data quality
ISO/IEC TR 24027 Bias in AI systems
ISO/IEC TR 24368 Ethical and societal concerns
ISO/IEC AWI TS 22443 Addressing societal concerns and ethical considerations [under development]
ISO/IEC 5339 Guidance for AI applications
Gender-based Illicit Proximity Estimate, 
Equalized Odds, 
Equality of opportunity, 
Demographic parity,
Predictive equality,
Conditional statistical parity, 
Conditional use accuracy

## Documentation of how the data distribution represents real-world conditions
Art. 10 §2 (d), §3
Recording of environment-specific situations; verification of representative data volumes per situation.

DIN SPEC 92005:2024-03 Quantifizierung von Unsicherheiten
ISO/IEC 5259-x Series data quality
ISO/PAS 8800 Safety and AI in road vehicles  
ISO/IEC TS 4213 Assessment of machine learning classification performance
Data Sheets / Data Cards

## Documentation of limitations such as errors, noise or biases in the data
Art. 10 §2	
Documentation of systematic errors, biases and inaccuracies in the data.	

DIN SPEC 92005:2024-03 Quantifizierung von Unsicherheiten
ISO/IEC 5259-x Series data quality
ISO/PAS 8800 Safety and AI in road vehicles  
ISO/IEC TR 24029-x Series Robustness of neural networks

## Creating representative data splits	
Art. 10 §2, §3	

Ensure data reflects realistic conditions and avoids biases. Use stratification or randomization for representative data splits, and document methods for reproducibility. Prevent data leakage to avoid distorting model performance.	ISO/IEC 5259-x Series data quality

Scikit-learn methods for data splitting 
Cleanlab for bias management 

## Documentation of characteristics of the training and test data
Art. 10 §2, §3

Record data sources in detail (typology, volume, relevance). Thoroughly analyze data distribution and potential biases. Identify and document sensitive and demographic attributes for fairness assessments. Provide a complete description of methods used to ensure data quality, including preprocessing steps and their impact on data integrity.

ISO/IEC 23053:2022 Framework for AI System Performance using ML
Frameworks: Ydata Profiling, Pandas Profiling, Great Expectations
statistical methods: Kolmogorov-Smirnov-Test, Chi²-Test, Shapiro-Wilk-Test
Datasheets for datasets

## Ensuring the accuracy of the model	
Art. 15 §1; Art. 72	
Evaluate model accuracy using application-specific metrics like precision, recall, F1 score, or AUC-ROC. Verify accuracy by comparing with established benchmarks or test metrics. Fully document test methods, evaluation metrics, results, and potential limitations.

ISO/IEC 23053:2022 – Framework for artificial intelligence (AI) systems using machine learning (ML)
ISO/IEC TR 4213 – Evaluation of machine learning classification performance
ISO/IEC TS 8200 – Controllability of automated AI systems
ISO/IEC AWI 24970 Logging of AI systems [under development]
Metrics and evaluation frameworks: Precision, Recall, F1-Score, AUC-ROC, RMSE, MAE
Benchmarking tools: MLflow , TensorBoard , Scikit-learn Evaluation modules
Monitoring and validation systems: Monitoring dashboards

## Ensuring the robustness of the system	
Art. 10 §4, Art. 15 §1	

Conduct systematic tests to assess system robustness, including simulating edge cases and adversarial inputs. Ensure resilience to disruptions like erroneous data or unusual user interactions. Document measures and results to validate robustness and identify potential vulnerabilities. The system must meet required accuracy and security standards under various conditions.	ISO/IEC TR 24029-x Series robustness of neural networks.

ISO/IEC AWI 24970 AI system logging [under development]
ISO/IEC 42001:2023 Information technology – Artificial intelligence – Management system
Adversarial Robustness Toolbox (ART): open-source framework for conducting adversarial testing (GitHub)

## Documentation of the required level of explainability and interpretability of the model	
Art. 13, Art. 15 §3	

Use transparent, well-documented AI models, including operation, intended purpose, and foreseeable defects (Art. 13, §3). Evaluate necessary model complexity and determine explainability levels based on the use case, target group, and risks. Transparently state the limits of explainability, especially for complex models like deep learning. Ensure the explanation strategy aligns with legal and ethical requirements and is documented.	ISO/IEC TR 24028 Trustworthiness in artificial intelligence.

ISO/IEC 42001 AI management system
ISO/IEC TR 24028 Trustworthiness 
ISO/IEC 22989 Terminology
ISO/IEC TS 8200 Controllability of AI systems
ISO/IEC DTS 6254 Explainability and interpretability [in development]
ISO/IEC DIS 12792 Transparency taxonomy of AI systems [in development]
Explainability tools: SHAP (documentation), LIME (GitHub), Saliency Maps
Model alternatives: Decision trees, generalized additive models (GAMs), linear models

## Documentation of benchmarks, model evaluation and model selection	
Art. 10 §1-2, Art. 15 §1, §3, Annex VIII, Annex IX	
Conduct a comprehensive model evaluation using suitable application metrics. Document results, test methods, benchmarks, and relevant scenarios. Transparently present limitations, potential risks, and edge cases. Ensure the evaluation meets regulatory and ethical standards.	ISO/IEC TR 24029-x Series robustness of neural networks.

ISO/IEC AWI 24970 AI system logging [under development]
ISO/IEC 42001 AI management systems
ISO 9001 Quality management systems requirements
Evaluation platforms: Weights & Biases (website) , Mlflow
Metrics: Precision, Recall, F1-Score, ROC-AUC, Log-Loss

## Documentation of the selected metrics and justification of their use in the context of the use case and, if necessary, considerations of fairness	
Art. 13; Art.15 §1, §2	

Use well-documented AI models. Documentation should include metrics used and their performance, including those related to specific individuals or groups for relevant use cases (Art. 13, §3(b)(ii), (v)). Referencing the use case and selection decisions adds transparency when interpreting performance. However, as per Article 15(2), specific metrics or limits to adhere to have not yet been developed.	

ISO/IEC TS 4213 Assessment of machine learning classification performance
ISO/IEC TR 24027 Bias in AI systems 
ISO/IEC AWI TS 22443 Addressing societal concerns and ethical considerations [under development]
ISO/IEC 23053 Framework for AI Systems

## Documentation of the test design (AI system level)	
Art. 9 §6, §7, §8; Art. 60; Annex IV §2 (g); Annex IX, Art. 53

Ideally, create and document the test design before training, defining relevant metrics. It should consider the AI system's intended purpose and include details on validation and test data and their key characteristics. Indicate parameters used to measure robustness and other relevant requirements (including for high-risk AI systems and discriminatory effects, if applicable). Tests must be conducted before the AI system is marketed or deployed.	ISO/IEC TS 4213 Assessment of machine learning classification performance.

ISO/IEC TS 8200 Controllability of AI systems
ISO/PAS 8800 Safety and AI in road vehicles  
ISO/IEC AWI 24970 AI system logging [under development]
ISO/IEC AWI TS 42119-2 Overview of testing AI systems [under development]
ISO/IEC CD TS 42119-3 Verification and validation analysis of AI systems [under development]
Model Cards for Model reporting: 
model-card-toolkit

## Description of potential risks, edge cases and worst-case scenarios and simulation of these in test scenarios, if possible	
Art. 13 §3 (b)	

Systematically list all potential technical and operational risks and edge cases affecting the AI system's operation. Include clear definitions and examples of edge cases and worst-case scenarios. If possible, simulate these scenarios in realistic tests to evaluate the model's response.	SDV (Syntehtic Data Vault) offers various methods for generating synthetic data
Prototype Generation

## Description of the test results (AI system level)	
Art. 53 §1 (a), Annex IV §2 (g)	
Provide comprehensive, transparent documentation of test results, including detailed performance metrics. Interpret results in relation to AI system objectives, highlighting potential weaknesses or risks. Use the test design to simulate potential risks, edge cases, and worst-case scenarios in test scenarios when possible.	

ISO/IEC TS 8200 Controllability of AI systems
ISO/IEC AWI 24970 AI system logging [under development]
ISO/IEC AWI TS 42119-2 Overview of testing AI systems [under development]
ISO/IEC CD TS 42119-3 Verification and validation analysis of AI systems [under development]
TensorBoard and Mlflow
Version control tools, e.g. GitHub or Weights & Biases
Model card toolkit

## Documentation of the model's limitations	
Art. 13 §3(b); Art.14 §4 (a); Annex IV §3; Art. 53

Describe all known model limitations comprehensively and understandably, considering both technical and contextual aspects. Indicate conditions where the model may not perform as expected and factors influencing its accuracy and reliability. Provide a clear presentation of possible failure scenarios and their effects.	

ISO/IEC DIS 12792 Transparency taxonomy of AI systems [under development]
ISO/PAS 8800 Safety and AI in road vehicles  

## Documentation and explanation of measures derived from the test results
Not directly demanded by the EU AI Act / best practices

Clearly and systematically document all measures derived from test results, explaining the rationale behind each and referencing specific test results. Consider potential impacts of these measures on the AI system and its environment. Transparent presentation of decision-making processes is crucial to foster acceptance of proposed changes.	ISO/IEC TS 8200 Controllability of AI systems.

ISO/PAS 8800 Safety and AI in road vehicles 
ISO/IEC 23894: AI Risk Management
ISO/IEC AWI TS 42119-2 Overview of testing AI systems [under development]
ISO/IEC CD TS 42119-3 Verification and validation analysis of AI systems [under development]

## Post-market surveillance system	
Art 72; Annex VII	

Establish a PMMS to continuously monitor AI system usage data, performance, and malfunctions (Art. 72 §1). Regularly submit reports to designated authorities. Identify new risks from real-time data and assess their impact on safety and reliability (Annex VII §3). Develop and implement corrective actions to address deficiencies or comply with new regulations.	

ISO/IEC 42001 Information technology - Artificial intelligence - Management system
ISO 9001 Quality management systems requirements
ISO/IEC TS 8200 Controllability of AI systems
ISO/IEC 5259-x Series Data quality

