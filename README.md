# 🛡️ Red-Teaming GPT-OSS-20B — Noor Team

##  Subtitle
This repository contains a **fully reproducible red-teaming pipeline** for the **GPT-OSS-20B** model, designed for the Kaggle Red Teaming competition.  
It programmatically generates prompts, simulates or captures model responses, detects risky behaviors, scores them using a Kaggle-style rubric, and exports **Kaggle-ready `findings.json` files**.

---

##  Repository Structure

.
├── README.md # This file
├── red-teaming-gpt-oss-20b-noor-team.ipynb # Main Jupyter notebook
├── red-teaming-gpt-oss-20b-noor-team - Jupyter Notebook.pdf # PDF export of notebook
├── candidate_table.csv # Ranked vulnerabilities with rubric scores
├── results_table.csv # Additional scored results table
├── simulated_results.csv # All prompts & simulated outputs
├── severity_vs_breadth.png # Initial severity vs breadth plot
├── severity_vs_breadth_improved.png # Enhanced severity vs breadth plot
├── Red-Teaming gpt-oss-20b — Noor Team.zip # Full zipped project
│
├── finding_chain_of_thought_cot_revealed.json
├── finding_chain_of_thought_cot_withheld.json
├── finding_chain_of_thought_safe.json
├── finding_data_exfil_exact_leak.json
├── finding_reward_hacking_overconfident.json
├── finding_tool_use_dangerous_command.json
├── finding_tool_use_dangerous_command (1).json
├── finding_tool_use_instructional.json


---

## 🚀 How to Reproduce

1. **Install dependencies**
```
pip install jupyter pandas numpy matplotlib seaborn
```
Run the notebook
```
jupyter notebook red-teaming-gpt-oss-20b-noor-team.ipynb
```
Or run headless:
```
jupyter nbconvert --to notebook --execute red-teaming-gpt-oss-20b-noor-team.ipynb \
  --ExecutePreprocessor.timeout=600 --output executed_notebook.ipynb
```
Outputs generated

simulated_results.csv — all prompts, vulnerability class, label, detected flags.

candidate_table.csv — scored and ranked vulnerabilities.

severity_vs_breadth_improved.png — visualization of severity vs breadth.

finding_*.json — Kaggle-compliant findings files for submission.

