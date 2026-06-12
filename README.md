# ResearchClawArena

ResearchClawArena is a benchmark for evaluating the end-to-end research capability of AI Scientist agents.

It provides unified research tasks, standardized task inputs, agent-generated research artifacts, and process-level evaluation settings. The benchmark is designed to measure how different AI Scientist systems understand research goals, plan experiments, execute research workflows, generate intermediate artifacts, and produce final outputs.

## Links

Project Website: [ResearchClawArena](https://agentos-openlab.github.io/research-claw-arena/)  
Dataset: [ResearchClawEval on Hugging Face](https://huggingface.co/datasets/agentos-openlab/researchclaweval)

## Overview

ResearchClawArena evaluates AI Scientist agents under a shared benchmark protocol.

For each research topic, multiple agents are given the same core task objective. The task is adapted into the required input format of each agent while preserving the same research goal and evaluation target.

ResearchClawArena emphasizes process-level evaluation. It records and compares the research process of each agent, including task understanding, research planning, experiment design, code generation, execution logs, intermediate results, analysis, and final deliverables.

This enables direct comparison not only of what each agent produces, but also of how each agent conducts research.

## Evaluated Agents

ResearchClawArena includes outputs from the following AI Scientist agents:

- EvoScientist
- Auto Research Claw
- Deep Scientist
- AI Researcher
- ARIS
- The AI Scientist v2
- Dr. Claw

## Dataset Organization

The dataset is organized by research topic. Each topic contains the outputs produced by different agents under the same benchmark task.

```text
researchclaweval/
├── topic_1/
│   ├── evoscientist/
│   ├── auto_research_claw/
│   ├── deep_scientist/
│   ├── ai_researcher/
│   ├── aris/
│   ├── the_ai_scientist_v2/
│   └── dr_claw/
├── topic_2/
│   └── ...
└── ...
```

Each agent folder contains its generated research artifacts, such as research plans, code, experiment logs, intermediate outputs, analysis notes, reports, and final results.

## Evaluation Focus

ResearchClawArena focuses on practical research execution ability across the full research workflow.

The benchmark evaluates whether an AI Scientist agent can:

- Understand the research task
- Formulate a feasible research plan
- Design meaningful experiments
- Generate and revise code
- Track execution logs and intermediate results
- Analyze failures and adjust the workflow
- Produce final outputs aligned with the task objective
- Follow the benchmark protocol
- Support comparison with other agents

## Process-Level Evaluation

Final results alone are not enough to evaluate AI Scientist agents.

Two agents may achieve similar final scores while following very different research processes. One may produce a clear plan, run controlled experiments, debug failures, and provide interpretable analysis. Another may reach a result through accidental trial-and-error with poor traceability.

ResearchClawArena captures these differences by evaluating the full research trajectory. This makes the benchmark suitable for studying scientific reasoning, experiment design, tool use, debugging ability, and research workflow quality.

## Usage

Clone the dataset from Hugging Face:

```bash
git lfs install
git clone https://huggingface.co/datasets/agentos-openlab/researchclaweval
```

Then inspect the topic folders and compare the outputs from different AI Scientist agents.

## Citation

If you use ResearchClawArena or the ResearchClawEval dataset, please cite the project and dataset links:

```bibtex
@misc{researchclawarena,
  title = {ResearchClawArena: Benchmarking AI Scientist Agents with Process-Level Evaluation},
  author = {AgentOS OpenLab},
  year = {2026},
  howpublished = {\url{https://agentos-openlab.github.io/research-claw-arena/}}
}
```

## License

Please refer to the license information provided in the dataset repository.
