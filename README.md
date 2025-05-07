# Exploring Prosocial Irrationality for LLM Agents: A Social Cognition View (ICLR 2025)

**CogMir** 🤖🧠 is a multi-LLM agent framework designed to explore how large language models (LLMs) mirror human cognitive biases and exhibit irrational yet prosocial decision-making.  
🌐✨ Our research highlights the potential of using systematic hallucination properties in LLMs to better understand and enhance their social intelligence. 

---

This repository contains the **core datasets** and **high-level experimental prompt design logic** used in the CogMir framework.

## 📁 Repository Structure

- **`CogMir_Data/Core_Datasets`**  
  Fundamental data: questions, agent profiles, scenario descriptions, actions, and narratives. Each subfolder corresponds to a dataset described in Appendix C of the paper.

- **`CogMir_Data/Experimental_Prompts`**  
  Reusable prompt templates for each cognitive bias experiment (see Section 4 & Appendix D). Templates use placeholders (like `[Known/Unknown MCQ]`, `[IDENTITY]`, `[SCENARIO]`) to be filled with data from `/Core_Datasets`.

---

## 📖 Citation

If our work helps or inspires you, please cite:

```bibtex
@inproceedings{
  liu2025exploring,
  title={Exploring Prosocial Irrationality for {LLM} Agents: A Social Cognition View},
  author={Xuan Liu and Jie Zhang and Haoyang Shang and Song Guo and Chengxu Yang and Quanyan Zhu},
  booktitle={The Thirteenth International Conference on Learning Representations},
  year={2025},
  url={https://openreview.net/forum?id=u8VOQVzduP}
}
