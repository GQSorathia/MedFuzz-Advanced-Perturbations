# MedFuzz-Advanced-Perturbations

Extended MedFuzz framework with novel adversarial perturbation strategies for medical LLM robustness testing.

Overview
This project extends the MedFuzz adversarial testing framework by introducing three novel perturbation strategies to evaluate medical Large Language Model (LLM) robustness: numerical manipulation, medical terminology swapping, and treatment confusion.

Base Paper: MedFuzz: Exploring the Robustness of Large Language Models in Medical Question Answering

Key Results
Overall Robustness: 96. 7%
Attack Success Rate: 3.3% (1 out of 30 perturbations)
Perfect Robustness: 100% against numerical manipulation
Primary Vulnerability: 6.7% success rate for medical terminology swap
Novel Contributions
Three New Perturbation Types:
Numerical Manipulation

Alters clinical values (age, lab results, vital signs) by 10-30%
Tests holistic reasoning vs. threshold-based decision making
Medical Terminology Swap

Replaces medical terms with similar-sounding conditions
Tests semantic disambiguation capabilities
Treatment Confusion

Introduces plausible but incorrect treatment options
Tests focus on correct diagnostic pathway
Quick Start
Prerequisites
bash
pip install groq pandas numpy matplotlib seaborn tqdm scipy
Get Groq API Key
Sign up at: https://console.groq.com

Run the Code
Google Colab (Recommended):

Upload Innovation_Code.ipynb to Google Colab
Update API key in Cell 2: groq_api_key = "YOUR_API_KEY"
Run all cells (Runtime → Run all)
Wait ~12-15 minutes

Results
Overall Performance
Metric	Value
Questions Tested	15
Total Perturbations	30
Successful Attacks	1
Attack Success Rate	3. 3%
Robustness Score	96.7%
By Perturbation Type
Perturbation	Success Rate	Robustness
Medical Terminology Swap	6. 7%	93.3%
Numerical Manipulation	0. 0%	100.0%

Reproducing Results
Clone this repository
Install dependencies: pip install groq pandas numpy matplotlib seaborn tqdm scipy
Get Groq API key from https://console.groq.com
Open AAI_Assignment02.ipynb
Update API key in Cell 2
Run all cells
Check results/ folder for outputs
Expected Runtime: 12-15 minutes

Key Findings
✅ Perfect Numerical Robustness
Model achieved 100% robustness against numerical manipulation, suggesting strong holistic clinical reasoning rather than brittle threshold-based rules.

⚠️ Terminology Vulnerability
Medical terminology swap was the only effective attack (6.7% success), revealing semantic confusion as the primary weakness—critical for clinical deployment.

🎯 High Overall Reliability
96.7% robustness exceeds many models tested in the original MedFuzz paper (which showed up to 30% vulnerability).
