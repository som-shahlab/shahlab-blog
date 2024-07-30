---
layout: distill
title: "Human AI Collaboration: Literature Review"
description: A literature review on the role of AI in clinical decision making.

authors:
  - name: Karthik S. Vedula
    url: "https://www.karthikvedula.com"
    affiliations:
      name: Poolesville High School
  - name: Alison Callahan
    url: "https://med.stanford.edu/profiles/alison-callahan"
    affiliations:
      name: Stanford University
  - name: Akshay Swaminathan
    url: "https://www.akshayswaminathan.com/"
    affiliations:
      name: Stanford University

bibliography: 2024-07-12-Human-AI-Collab.bib

toc:
  - name: Introduction
  - name: Review of Literature
  - name: Conclusion
  - name: Future Work
  - name: More Info on the Papers
---

# Introduction

We have seen AI tools assisting programmers like [Code Llama](https://ai.meta.com/blog/code-llama-large-language-model-coding/), AI tools assisting drivers with self-driving cars, but can AI tools assist clinicians in making medical decisions?

To some this might seem like a bad idea -- what if AI makes mistakes?  And will AI replace physicians?  This blog post will show where AI seems to help clinicians, where it falls short, and where this field of research is going.  We will explore cases where AI and clinicians, when working together in diagnosing, can provide superior performance; we will explore cases where AI was used to monitor patients alongside physicians; and we will explore cases where this AI-assistance translated into not just better accuracy, but better real-world clinical outcomes.

# Review of Literature

This paper selection primarily focuses on journal publications, specifically on studies involving the use of an AI model by clinicians as part of their decision making.  This was done using PubMed and the "related articles" feature.  It is important to note that methods in these papers primarily involve discriminative rather than generative AI (with the exception of the study evaluating ChatGPT & clinicians)<d-cite key="Goh2023-vb"></d-cite>.

Information on these studies are compiled into the table below.  Additional information for these studies are also included at the end of the blog post **(please click on "info" in the title column of the table to jump to that section)**.  The results of these papers come in three categories:

* ✅ A green checkmark indicates results where Human-AI collaboration derived superior results.

* 🟨 A yellow box indicates that **Human-AI collaboration generally provided superior results** but the researchers found **cases where Human-AI collaboration does not help.**

* ❌ A red cross indicates thart Human-AI collaboration did not provide any benefits.

| Title                                                                                                                                                                                                                                                                                                                                                                                                              | Research Question                                                                                                                                                            | Study Scale                                   | Study Design                                                                                                                                                                                                                                            | Did Human-AI Collaboration Work?                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interaction between clinicians and artificial intelligence to detect fetal atrioventricular septal defects on ultrasound: how can we optimize collaborative performance? [(info)](#interaction-between-clinicians-and-artificial-intelligence-to-detect-fetal-atrioventricular-septal-defects-on-ultrasound-how-can-we-optimize-collaborative-performance)                                                         | Can AI assistance (including confidence and explanations) help clinicians better detect fetal atrioventricular sepal defects?                                                | 10 Clinicians; 2000 fetal four chamber images | Ten clinicians reviewed 2000 fetal four-chamber images in various conditions to identify normal images and those with AVSD, using different types of AI assistance (with and without classification, confidence, and explanations)                      | 🟨 Across all kinds of clinicians, human and AI collaboration performed better than just one of the two (only human predictions or only AI predictions), but explanations or confidence didn't compensate for incorrect model predictions.                                                                                             |
| Measuring the Impact of AI in the Diagnosis of Hospitalized Patients. [(info)](#measuring-the-impact-of-ai-in-the-diagnosis-of-hospitalized-patients)                                                                                                                                                                                                                                                              | Do image-based explanations reduce the negative effects of influence from systematically biased models?                                                                      | 457 Clinicians                                | Each clinician assessed 9 clinical vignettes for the likelihood of pneumonia, heart failure, or COPD, with varying AI prediction types (standard or systematically biased) and a peer consultation designed to provide upper-bound diagnostic accuracy. | 🟨  Standard AI predictions helped clinicians, and standard AI predictions with explanations further increased accuracy. Participant diagnostic accuracy was highest with an always-correct clinical consultation. Systematically biased AI predictions decreased clinician accuracy regardless of whether explanations were provided. |
| AI-enabled electrocardiography alert intervention and all-cause mortality. [(info)](#ai-enabled-electrocardiography-alert-intervention-and-all-cause-mortality)                                                                                                                                                                                                                                                    | Does a warning message to the treating physician generated by an AI model (identifying patients with high risk) prompt management decisions leading to a decrease of deaths? | 39 Clinicians; 15,965 Patients                | The study evaluated if the AI-ECG model could identify deteriorating patients and reduce the need for additional ECGs by comparing mortality rates between an intervention group receiving AI alerts and a control group monitored by physicians alone. | ✅ The study showed a significant decrease in mortality with AI-ECG assistance compared to the control group, particularly in high-risk cases, and suggested that the AI model's novelty and manageable alert frequency helped maintain quality of care and reduce mortality through increased physician attention.                     |
| Artificial intelligence-assisted diagnosis of congenital heart disease and associated pulmonary arterial hypertension from chest radiographs. [(info)](#artificial-intelligence-assisted-diagnosis-of-congenital-heart-disease-and-associated-pulmonary-arterial-hypertension-from-chest-radiographs)                                                                                                              | Can AI predictions help radiologists in diagnosing congenital heart disease (CHD) and associated pulmonary arterial hypertension (PAH-CHD)?                                  | 5 Clinicians; 495 CXR images                  | The study was a multireader multicase randomized crossover study, where clinicians reviewed each chest x-ray (CXR) for CHD and PAH-CHD twice (with a 1-month washout period), once with an AI prediction and once without.                                            | ✅ AI predictions improved clinician accuracy for both CHD and PAH-CHD.                                                                                                                                                                                                                                                                 |
| Use of Voice-Based Conversational Artificial Intelligence for Basal Insulin Prescription Management Among Patients With Type 2 Diabetes: A Randomized Clinical Trial. [(info)](#use-of-voice-based-conversational-artificial-intelligence-for-basal-insulin-prescription-management-among-patients-with-type-2-diabetes-a-randomized-clinical-trial)                                                               | Does a voice-based interface help in providing improved “time to optimal insulin dosing, insulin adherence, and glycemic control”?                                           | 32 Patients                                   | The intervention group had an Amazon smart speaker which gave them information for insulin management, while the control group was instructed to fill out an online blood glucose and insulin log daily for the duration of the trial.                  | ✅ PAID-5 scores were lower for the intervention group compared to the control. PAID-5 is a qualitative survey measurement for diabetes where lower scores are more favorable.                                                                                                                                                          |
| Conventional Versus Artificial Intelligence-Assisted Interpretation of Chest Radiographs in Patients With Acute Respiratory Symptoms in Emergency Department: A Pragmatic Randomized Clinical Trial. [(info)](#conventional-versus-artificial-intelligence-assisted-interpretation-of-chest-radiographs-in-patients-with-acute-respiratory-symptoms-in-emergency-department-a-pragmatic-randomized-clinical-trial) | Does AI-assistance (predictions) help radiologists interpret chest radiographs in patients with acute respiratory symptoms in ED?                                            | 35,756 Patients                               | Patients were put into an intervention and a control group in a ratio of 1:1. The intervention group had clinicians review the chest radiograph with an AI model prediction accompanied, while the control group did not.                               | ❌ There was no association between using AI predictions and not using predictions with respect to clinician performance                                                                                                                                                                                                                |
| ChatGPT Influence on Medical Decision-Making, Bias, and Equity: A Randomized Study of Clinicians Evaluating Clinical Vignettes. [(info)](#chatgpt-influence-on-medical-decision-making-bias-and-equity-a-randomized-study-of-clinicians-evaluating-clinical-vignettes)                                                                                                                                             | Can AI positively influence physicians in their clinical decision making without introducing or exacerbating demographic bias?                                               | 50 Clinicians                                 | Participants reviewed a clinical vignette video (randomly chosen whether it featured a white male or a black female), and could then change their answers after reviewing suggestions from ChatGPT+.                                                    | ✅ In both cases (vignettes featuring a white male and a black female), accuracy by the clinicians increased by 18% after they reviewed suggestions from ChatGPT+.                                                                                                                                                                      |
| Artificial intelligence suppression as a strategy to mitigate artificial intelligence automation bias. [(info)](#artificial-intelligence-suppression-as-a-strategy-to-mitigate-artificial-intelligence-automation-bias)                                                                                                                                                                                            | Can AI-induced automation bias be mitigated using AI?                                                                                                                        | 40 Clinicians; 200 cases                      | Clinicians were assigned to either the AI-assisted group or the AI-unassisted group.  After a washout period of 14 days, clinicians switched to the other group and diagnosed same 200 MRIs.                                                            | 🟨 Application of AI significantly increased the clinicians’ accuracy, but 45.5% of the total mistakes in the AI-assisted round were associated with clinicians being misleaded by AI predictions, though all clinicians denied that AI predictions misled them in any way.                                                            |
{:.l-page}

# Conclusion

These are our takeaways from this review:

##### Human-AI collaboration generally works, as long as AI is accurate

With the exception of one study, all experiments showed that providing AI predictions to clinicians offered better accuracy compared to not providing AI predictions.  However, most studies also displayed how incorrect AI predictions can adversely influence clinicians, a case of automation bias.

Automation bias is the tendency to over-rely on automation.<d-cite key="Goddard2012-wf"></d-cite>
{:.l-gutter}

##### AI models can help clinicians even if AI models aren't perfect

Even though AI models may not have perfect accuracy, Human-AI collaboration has shown to provide better performance than both

* evaluation by clinicians without AI-assistance; and
* AI predictions without clinician influence.

Studies like _Interaction between clinicians and artificial intelligence to detect fetal atrioventricular septal defects on ultrasound_<d-cite key="Day2024-wh"></d-cite> and _ChatGPT Influence on Medical Decision-Making, Bias, and Equity_<d-cite key="Goh2023-vb"></d-cite> exhibited this phenomenon.

##### Providing AI confidence or explanations does not compensate for incorrect predictions

Studies like _Interaction between clinicians and artificial intelligence to detect fetal atrioventricular septal defects on ultrasound_<d-cite key="Day2024-wh"></d-cite> and _Measuring the Impact of AI in the Diagnosis of Hospitalized Patients_<d-cite key="Jabbour2023-rd"></d-cite> show that using explanations or confidence levels to assist an AI prediction doesn't substantially prevent clinicians from recognizing incorrect AI predictions, resulting in worse performance from the Human-AI collaboration.


# Future Work

##### Beyond retrospective studies

So far, a lot of these studies compared Human-AI collaboration with retrospective data.  This means clinicians reviewed data from patients who have already been treated/attended to.   This leads these studies to not be the best representation of how humans and AI algorithms can work together in the real-world, since the collaboration isn't happening in real time as patients are getting treated.  Some of these papers did indeed differ:

* _AI-enabled electrocardiography alert intervention and all-cause mortality_<d-cite key="Lin2024-oo"></d-cite>explored this real-time Human-AI interaction and provided insights on issues like alert-fatigue, which cannot necessarily be assessed in retrospective data studies.

* _Conventional Versus Artificial Intelligence-Assisted Interpretation of Chest Radiographs in Patients With Acute Respiratory Symptoms in Emergency Department_<d-cite key="Hwang2023-lv"></d-cite> also featured this kind of research, with an AI prediction being provided immediately to the radiologists while in the emergency department

* _Use of Voice-Based Conversational Artificial Intelligence for Basal Insulin Prescription Management Among Patients With Type 2 Diabetes_<d-cite key="Nayak2023-em"></d-cite> featured a real-time Human-AI interaction environment, but not primarily between AI and clinicians (but rather studied AI-patient interaction).

However, there is a need for _more_ studies that evaluate Human-AI collaboration in situations when the "ground truth" isn't immediately available, where decisions beyond diagnosis must be made with purely the clinician and AI's judgement.

##### Iterative interaction with generative AI

Additionally, most of these studies focus on a single interaction between the AI model output and the clinician for a given case.  Though most papers that were reviewed do not use generative AI (which calls for iterative interaction), _ChatGPT Influence on Medical Decision-Making, Bias, and Equity_<d-cite key="Goh2023-vb"></d-cite> explores an iterative interaction, where a clinician views the case initially and then proceeds to consult an AI model for further analysis.  However, there is a need for more research in generative AI-human collaboration when it comes to clinical settings, including finding methods to evaluate automation bias in these collaboration settings.

---


# More Info on the Papers

This section includes additional information on the papers that were reviewed, including more details on how the study was conducted, who the clinicans were, and the kinds of AI models used for the study.

## Interaction between clinicians and artificial intelligence to detect fetal atrioventricular septal defects on ultrasound: how can we optimize collaborative performance?<d-cite key="Day2024-wh"></d-cite>

##### Question: Can AI assistance (including confidence and explanations) help clinicians better detect fetal atrioventricular sepal defects?

This observational study with retrospectively collected data assessed the performance of clinicians, interpreting fetal four-chamber images.  The study evaluated how AI predictions and associated confidence & explanations affect clinicans' diagnosis of atrioventricular sepal defects (AVSD).

### Study Details

**Study Type:** Observational study with retrospectively collected data

Each clinician was shown 2000 fetal four chamber images in random order, of which 1000 were normal, and the other 1000 had AVSD.  The dataset contained a total of 500 images, and each image was shown in 4 conditions:

* Image alone without AI output
* Image with binary AI classification
* Image with AI model confidence
* Image with Grad-CAM

### Who were the clinicians?

The study consisted of 10 clinicians:
* 2 consultant fetal cardiologists
* 3 trainees in pediatric cardiology
* 5 fetal cardiac sonographers

### Model Details

The model used a ResNet50 model architecture. Temperature scaling of model prediction probability on validation set was conducted.

#### Dataset

The training data was a cohort of 121,130 cardiac four chamber images extracted from 173 ultrasound scan videos (98 normal, 75 with AVSD).

#### Explainability Method and Uncertainty Estimation

Grad-CAM was used for providing explanations.  The model confidence was also provided to clinicians.

### Does Human + AI collaboration work?

Across all kinds of clinicians, human and AI collaboration performed better than just one of the two (only human predictions or only AI predictions).

#### What happens when AI predicts incorrectly?

Incorrect model outputs worsened clinician performance, which is expected as part of automation bias. Additional information was also provided to reduce negative effects of bad predictions (Confidence & GradCAM), but these actually worsened overall performance.

![Img]({{ site.baseurl }}/assets/img/day_et_al_humanAICollab.png)
_Image from paper_








## Measuring the Impact of AI in the Diagnosis of Hospitalized Patients.<d-cite key="Jabbour2023-rd"></d-cite>

##### Question: Do image-based explanations reduce the negative effects of influence from systematically biased models?

### Study Details

**Study Type:** Randomized Clinical Vignette Survey Study

The study contained 45 clinical vignettes.  Each clinician viewed 9 vignettes.  The vignettes were in the following order:

* Vignettes 1 & 2: no AI prediction
* Vignettes 3-8:
    * Half shown with prediction from **one of three** standard AI models
    * Other half shown with **corresponding** systematically biased AI model prediction
    * Which vignettes are biased are randomly determined
* Vignette 9
    * Clinical consultation (peer consultation provided to the clinician)
    * By design, the clinical consultation was always correct, intended to provide an upper-bound clinican diagnostic accuracy

After each vignette, the clinicians were asked to separately assess how likely (from a scale from 1 to 100) pneumonia, heart failure, or COPD was contributing to the patient's respiratory failure.

![Img]({{ site.baseurl }}/assets/img/jabbour_et_al_humanAICollab.png)
_Image from paper_

### Who were the clinicians?

The study "recruited hospitalist physicians, nurse practitioners, and physician assistants who commonly care for patients with acute respiratory failure".

### Model Details

#### Standard models

Three standards AI models were used:
* One detecting pneumonia
* One detecting heart failure
* One detecting COPD

#### Biased models

Each of the models had a corresponding systematically biased counterpart:
* one predicted high likelihood of _pneumonia_ for a patient who was _80 years old or older_
* one predicted high likelihood of _heart failure_ for a patient who has a _BMI greater than or equal to 30_
* and one predicted high likelihood of _COPD_ for a patient if _there was a blur applied on the radiograph_

#### Explainability method

The models used saliency maps to display the most relevant parts of the input.

### Does Human + AI collaboration work?

#### Standard AI models

Participant’s baseline diagnostic accuracy **without model input** was 73.0% (95% CI, 68.3%-77.8%) for the 3 diagnoses.  When clinicians were provided standard AI predictions (**without explanations**), participant diagnostic accuracy for each disease **increased** to 75.9% (95% CI, 71.3%-80.5%).  Providing standard AI predictions **with explanations** increased accuracy to 77.5% (95% CI, 73.0%-82.0%), **higher than just that when predictions alone were provided**.  Participant diagnostic accuracy was highest, with 81.1% (95% CI, 76.9%-85.4%), when physicians were provided a clinical consultation with perfect accuracy.

#### Systematically biased AI models

Systematically biased AI predictions **without explanations** caused a **decrease** in participant diagnostic accuracy to 61.7% (95% CI, 55.3%-68.2%), a decrease of 11.3 percentage points (95% CI, 7.2-15.5; P < .001) from the baseline accuracy.  Biased AI predictions **with explanations** **did not help**, with a similar 64.0% (95% CI, 57.6%-70.3%) accuracy, which is a decrease of 9.1 percentage points (95% CI, 4.9-13.2; P<.001) from the baseline accuracy.

#### Other observations

Even clinicians when were provided perfectly accurate recommendations in the clinical consultation vignettes, they had only 81.1% diagnostic accuracy.  This might indicate that clinicians have difficulty in recognizing perfectly accurate reccomendations, suggesting that "as AI models improve, there may be an **upper bound on collaborative performance** between AI models and clinicians for difficult diagnostic tasks."









## AI-enabled electrocardiography alert intervention and all-cause mortality.<d-cite key="Lin2024-oo"></d-cite>

##### Question: Does a warning message to the treating physician generated by an AI model (identifying patients with high risk) prompt management decisions leading to a decrease of deaths?

This study evaluated how effective an AI model can identify deterioirating patients (using ECGs) and how such predictions (which triggered warnings to physicians), affected mortality.

### Study Details

**Study Type:** Pragmatic randomized clinical trial

This study utilized an AI model (AI-ECG) in order to identify deterioirating patients whose clinical conditions are possible reversible.  This was done to evaluate whether such as system could replace the need to conduct aditional ECGs and alter routine daily practice.  The control group had physicians monitoring patients by themselves, while the intervention group had an AI-based model provide alerts to physicians.  The study evaluated whether the cumulative proportion of death differed between the two groups. 8,001 and 7,964 patients in the intervention and control groups, respectively, were analyzed.

### Who were the clinicians?

The study consisted of 39 physicians, of which the mean age was 45.6 ± 6.2 years and 97.4% were male.

### Model Details

The model was a convolutional neural network incorporating residual and attention modules.  The model's output was transformed into a percentile score based on a hospital-based population, from the original range of negative to positive infinity (patients below 75th percentile were generally considered to have an extremely low risk of death).  More details about the model are outlined in [this publication](https://doi.org/10.1177/20552076231187247).

#### Dataset

The model was trained on more than 450,000 ECGs, with the primarily label being all-cause mortality.  The model used survival data and censored events as input.

### Model Results

The AI-ECG model outperformed all baseline characteristics in predicting 90-day mortality risk: AUC = 0.886.

### Does Human + AI collaboration work?

The study indicated a decreased mortality rate when AI assistance was used versus the control: "the cumulative proportion of death within 90 days was significantly different between the groups (3.6% in the intervention group versus 4.3% in the control group, HR = 0.83 and 95% CI = 0.70–0.99, P = 0.040)".  This difference was primarily due to the high-risk cases being identified by the AI-ECG, with P for the intervention group × risk group interaction = 0.026, indicating that the AI-ECG is more effective for identifying high-risk than low-risk patients, though that is consistent with an rapid response system.  The active warning message from the AI-ECG in intervention group significantly reduced mortality risk from 23.0% to 16.0% (HR = 0.69 and 95% CI = 0.53–0.90, P = 0.006). However, the providing of an opportunity to review the AI-ECG reports only provided limited help in the AI-defined low-risk population (HR = 0.97 and 95% CI = 0.77–1.22, P = 0.777).”

One potential explanation for the reduced alert fatigue from physicians using the AI model is could be because of the novelty of the AI model.  In the study, the 39 physicians only received 709 alerts in 4.5 months, which made physicians more willing to order more intensive care.  Nevertheless, thr authors anticipate that even given AI-ECG results are accessible in real time for all patients (where they expect fewer than 10 alerts per month for each physician), the burden remains within an acceptable range for maintaining quality of care.  Additionally, though physicians were unaware of what specific actions they should perform given the alert, the increased attention induced by the alert could have reduced mortality.









## Artificial intelligence-assisted diagnosis of congenital heart disease and associated pulmonary arterial hypertension from chest radiographs.<d-cite key="Han2024-tq"></d-cite>

##### Question: Can AI predictions help radiologists in diagnosing CHD and PAH-CHD?

This study explores the usage of AI to help radiologists in the identification of congenital heart disease (CHD) and pulmonary associated arterial hypertension (PAH-CHD) from chest radiographs.  The study compares multiple AI model architectures, incorporates explainability through the use of class activation maps (CAMs), and compares these model performances to those of radiologists & studies the performance of collaboration between those models and radiologists.

### Study Details

**Study Type:** Multireader multicase (MRMC) randomized crossover study

This study can be split into three parts:
1. comparing AI models and seeing whether they can accurately identify CHD & PAH-CHD
2. evaluating model performance and comparing it to clinicians (done on a balanced dataset)
3. evaluating model collaboration with clinicians.

Radiologists evaluated CXRs for classical signs of CHD. Radiologists were presented with 330 CXRs for CHD and 165 CXRs for PAH-CHD diagnosis. These images were presented in a randomized order. The first time, 50% images accompanied with AI-based classification (clinicians were made aware that AI not always right), and the rest were not.  Radiologists provided their classification.  The second time (which proceeded after a 1-month washout period), 50% of the other images were with AI-based classification, while the rest were not.  This meant that diagnoses made by the radiologists were collected for each image with and without AI prediction assisting the clinician.

### Who were the clinicians?

5 radiologists:
* 3 junior radiologists with over 3 years of experience
* 2 senior radiologists with over 8 years of experience

### Model Details

4 models were evaluated:
1. ResNet18
2. Densnet121
3. MobileNetv2-120
4. MobileViT-S

#### Explainability Method

The study used class activation maps (CAMs) to identify most salient features to the AI models' classification.

### Model Results

#### CHD

ResNet18 pretrained with the ImageNet database yielded
* the highest sensitivity of 0.970,
* highest specificity of 0.982
* excellent AUC of 0.948.

#### PAH-CHD

PAH-CHD, the AI model achieved an AUC of 0.778 (sensitivity, 0.632; specificity, 0.925; accuracy, 0.891; F1 score, 0.571). Salient features for the identification of PAH-CHD were mainly in the projection area of the pulmonary artery segments.

### Model vs. Human performance

#### CHD

Junior radiologists achieved AUCs of 0.670–0.809, and senior radiologists achieved AUCs of 0.803–0.858, which were significantly lower than those of the AI model (for CHD).

#### PAH-CHD

AI model was significantly better than the performance of one junior (0.557; P = 0.008) radiologist and comparable to that of two junior and two senior (0.610–0.688; all P > 0.05) radiologists.

### Does Human + AI collaboration work?

#### CHD

With AI assistance, all radiologists exhibited an increase in mean ± standard deviation (SD) sensitivity from 0.728 ± 0.194 to 0.861 ± 0.087 ($\delta$ sensitivity + 0.132, 95 % CI: -0.039–0.303; P = 0.099) for CHD diagnosis.  The radiologists exhibited a significant increase in the mean ± SD specificity from 0.832 ± 0.107 to 0.891 ± 0.093 ($\delta$ specificity + 0.059, 95 % CI: 0.013–0.106; P = 0.023).

#### PAH-CHD

With AI assistance, the mean ± SD sensitivity of all radiologists increased from 0.537 ± 0.131 to 0.674 ± 0.068. No significant difference was observed between radiologists without and with AI assistance in terms of their mean ± SD specificity

### Other relevant information

In order to decrease the missed diagnosis of CHD, the researchers used the AI model with the **highest sensitivity value instead of AUC**.  This sensitivity advantage exhibited by the AI model suggests that it could help identify as many CHD patients as possible, allowing therapy management and potentially improve clinical outcomes.

The mean specificity of radiologists who used AI assistance **was not significantly different but even slightly lower** compared to that of radiologists who did not use AI for diagnosing PAH-CHD.  This decrease in radiologists' ability to identify negative cases (with AI assistance) could be due to radiologists choosing to diagnose a case as positive when they alone diagnose negative results but the AI prediction is positive.












## Use of Voice-Based Conversational Artificial Intelligence for Basal Insulin Prescription Management Among Patients With Type 2 Diabetes: A Randomized Clinical Trial.<d-cite key="Nayak2023-em"></d-cite>

##### Question: Does a voice-based interface help in providing improved “time to optimal insulin dosing, insulin adherence, and glycemic control”?

This study explores the field of Human-AI collaboration in the clinical setting from a different perspective: rather than having AI models collaborate with clinicians, the AI model in the study assists patients directly through a voice interface.  The study assesses the efficacy of a voice-based AI interface for Basal Insulin Prescription Management for patients with Type 2 diabetes.

### Study Details

**Study Type:** Randomized clinical trial

#### Participants

Adults with type 2 diabetes who required initiation or adjustment of once-daily basal insulin participated in the study.  The exclusion criteria was any factores that were technical barriers to administering this insulin at home.  Patients were also English speaking.

Participants were randomly assigned in a 1:1 ratio to receive insulin management either from the AI model or standard of care.  Randomization was computer-generated and stratified by age & gender.  The study used a permuted block design (random block sizes of 2 and 4).

#### Intervention Group

Each participant sent Amazon smart speaker with the AI.  Clinician preset the device with protocol whose parameters included a
* starting insulin dose
* goal fasting blood glucose (FBG) level range
* insulin titration instructions

Participants were instructed to check in with the AI daily by using the phrase “Alexa, check in with clinical trial.”

#### Control Group

Each participant was instructed to fill out an online blood glucose and insulin log daily for the duration of the trial.  Each participant was also sent Amazon smart speaker, but it just gave daily reminders to complete their log.

### Model Details

The model was rule-based.  The rules were developed from titration algorithms by the American Association of Clinical Endocrinologists and the American College of Endocrinology.  These rules also had included emergency protocols to handle hypoglycemia and hyperglycemia.

### Does Human + AI collaboration work?

The study used **PAID-5 survey scores** for measuring success (a qualitative survey for diabetes, where a **lower score is favorable**). PAID-5 survey scores decreased by a mean of 1.9 points (95% CI, -4.1 to 0.4 points) in the intervention group.  However, PAID-5 scores **increased** by a mean of 1.7 points (95% CI, -0.7 to 4.2 points) in the standard of care group, for a mean difference of -3.6 points (95% CI, -6.8 to -0.4 points; P = .03).

### Other relevant information

There are some limitations to this study.  The study did not compare this rule-based model with other similar insulin titration software to assess whether the voice-based interface benefited participants.  Additionally, mean FBG levels worsened in the standard of care group, which could have led to an overestimation of the effect size of the intervention.











## Conventional Versus Artificial Intelligence-Assisted Interpretation of Chest Radiographs in Patients With Acute Respiratory Symptoms in Emergency Department: A Pragmatic Randomized Clinical Trial.<d-cite key="Hwang2023-lv"></d-cite>

##### Question: Does AI-assistance (predictions) help radiologists interpret chest radiographs in patients with acute respiratory symptoms in ED?

This study explored the effects of having AI model predictions being provided to radiologists for the interpretation of chest radiographs.  The study evaluated whether these predictions had any influence in the radiologists' predictions.

### Study Details

**Study Type:** Pragmatic randomized controlled trial

#### Participants

Participants were included in the study if they had met at least one of the criteria:

* Patient's age >= 19 years and presented to the ED between June 15, 2020, and December 31, 2021
* Chief complaints are of the following: hills, cough, chest pain, dyspnea, fever, hemoptysis, and sputum
* Patient was referred for CR

These patients were put into an intervention and a control group in a ratio of 1:1.  The intervention group had clinicians review the chest radiograph with an AI model prediction accompanied, while the control group did not.  Since the random assignment of which group the patient is put into occured within a few minutes of image aquisition, there was no need for the clinician to request AI consultation, preventing the case of a physician not having access to the AI prediction while viewing the radiograph.

One investigator (a thoracic radiologist with 11 years of experience) then reviewed the case 20 days after the emergence department visit (reviewed medical records) in order to define the ground truth.

### Who were the clinicians?

The clinicians were duty trainee radiologists in their third year of the residency.

### Model Details

The model used was the Lunit INSIGHT CXR, version 2.0.2.0 from Lunit Inc.  The model analyzes a single frontol chest radiograph to determine the presence of pulmanory nodules, infiltration, and pneumothorax.

#### Explainability method

The model used a saliency heatmap to provide explanations for prediction.

### Does Human + AI collaboration work?

There was no association between using AI-CAD for CR interpretation and the sensitivity of duty trainee radiologists’ interpretations.  (Adjusted odds ratio [OR], 1.02; 95% confidence interval [CI], 0.70–1.49; P = 0.91)









## ChatGPT Influence on Medical Decision-Making, Bias, and Equity: A Randomized Study of Clinicians Evaluating Clinical Vignettes.<d-cite key="Goh2023-vb"></d-cite>

##### Question: Can AI positively influence physicians in their clinical decision making without introducing or exacerbating demographic bias?

### Study Details

**Study Type:** Randomized pre-post intervention study

Participants reviewed a clinical vignette video of a standarized patient complaining of chest pain.  These participants were randomly chosen to either watch a case with a white male or a black female featured.  Participants then answered 4 multiple choice questions based on the clinical vignette they watched.  These participants were allowed to answer these questions with the option of using any information resource available (e.g., MDCalc, Up-to-Date, PubMed) except for LLMs.  Participants then were allowed to review suggestions from ChatGPT+, and subsequently were given the option to change their original answers.

### Who were the clinicians?

50 physicians experienced in Family Medicine, Internal Medicine, or Emergency Medicine participated in the study.

### Model Details

The study used ChatGPT+ (with the GPT-4 model used between May to August 2023).

### Does Human + AI collaboration work?

In both cases (vignettes featuring a white male and a black female), accuracy by the clinicians increased by 18% after they reviewed suggestions from ChatGPT+.  This shows that physicians are willing to modify their clinical decisions based on suggestions from an LLM. rather than skeptically refusing to be swayed by a computer-generated prediction.  Additionally, the results indicate that AI can improve accuracy without introducing or exacerbating existing demographic bias











## Artificial intelligence suppression as a strategy to mitigate artificial intelligence automation bias.<d-cite key="Wang2023-hb"></d-cite>

##### Question: Can AI-induced automation bias be mitigated using AI?

This study proposed and evaluated a method of reducing automation bias.  Using the task of diagnosing anterior cruciate ligament (ACL) rupture, a common injury, on magnetic resonance imaging (MRI), the study proposed an AI suppression strategy that retracted AI diagnoses with misleading predictions.

### Study Details

**Study Type:** Case study (on ACL); randomized cross-over design study

Clinicians were assigned to either the AI-assisted group or the AI-unassisted group.  This was done using block randomization, stratified by physician category.  Clinicians asked to diagnose 200 MRIs with or without AI assistance (depending on their group).  After a washout period of 14 days, clinicians switched to the other group and diagnosed same 200 MRIs.  When diagnosing the MRI, they selected one of the four choices: normal, rupture, mucoid degeneration, and uncertainty.

Given these results, the study also proposed an AI suppression strategy, which used an ordinal logistic regression model to predict the correcting and misleading probabilities of the AI model.

### Who were the clinicians?

40 clinicians were invited for the study.

### Model Details

The model incorportated ResNet50 and Siamese algorithms.

#### Dataset

The study collected a training dataset of 8484 magnetic resonance imaging (MRIs).  The study used a validation dataset of 2273 prospectively collected knee MRIs.

#### Uncertainty Estimation

The study divided the AI output range into 9 parts and calculated the accuracy (positive/negative predictive value) of the AI diagnosis for each part using the validation dataset.  This accuracy was used as the uncertainty value for a given prediction.

### Model Results

The model achieved a sensitivity of 90.0%, a specificity of 85.3%, AUC 0.953 when tested on the validation dataset.

### Does Human + AI collaboration work?

Application of AI significantly increased the clinicians’ accuracy from 87.2%±13.1% to 96.4%±1.9%.  Clinicians’ sensitivity and specificity also improved with AI assistance.

#### What happens when AI predicts incorrectly?

45.5% (132/290) of the total mistakes in the AI-assisted round were associated with clinicians being misleaded by AI predictions.  However, all clinicians denied that AI predictions in any way misled them to diagnose incorrectly.

