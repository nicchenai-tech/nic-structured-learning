# Nic Structured Learning

**Structure before detail. Connection before memorisation. Application before exams.**

Nic Structured Learning is a personal AI-assisted teaching skill for learning mathematics, Python, computer architecture, machine learning, and AI. It is designed for learners moving into technical disciplines who need concepts organised before details are introduced.

The project combines instructional design with reusable AI instructions. It guides an AI tutor to build knowledge maps, connect prerequisites, teach through worked reasoning, and test mastery through independent transfer rather than passive recognition.

## Core mechanisms

### Teaching pipeline

```text
Why -> Problem -> Concept -> Mechanism -> Result -> Application
```

The tutor begins with the problem a concept solves, places it in a larger structure, explains how it works, and then applies it.

### Mastery loop

```text
Closed-notes attempt
-> Diagnose the exact stuck step
-> Repair the missing knowledge
-> Retest with a changed problem
```

Mastery is evaluated at three levels:

1. **Recognition** — the learner understands a shown solution.
2. **Reproduction** — the learner solves the same type without notes.
3. **Transfer** — the learner solves a changed version independently.

Recognition alone is not treated as mastery. Reproduction is the minimum evidence of learning; transfer is the target for assessment readiness.

## What the skill does

- Creates a compact knowledge map before teaching substantial new material.
- Connects each concept to its prerequisites and later applications.
- Explains technical terminology in accessible language.
- Uses supplied course materials as the primary source for course-specific claims.
- Separates source-supported content, general background, and inference.
- Adjusts teaching for new topics, individual concepts, practice, revision, and assessment preparation.
- Provides guided attempts and progressively removes support.
- Gives feedback on the precise reasoning step, not only the final answer.

## What this project is

This repository is an **AI learning skill / instructional system**. It defines teaching decisions and feedback behaviour for a compatible AI environment.

It is not, by itself, an autonomous AI agent. An AI host may add agentic capabilities such as reading course files or using tools, but those capabilities are not implemented by this repository.

## Repository structure

```text
nic-structured-learning/
|-- SKILL.md
|-- agents/
|   `-- openai.yaml
|-- docs/
|   `-- methodology.md
|-- examples/
|   `-- mathematics-session.md
|-- LICENSE
`-- README.md
```

## Installation

### Codex

Copy this repository into your Codex skills directory:

```text
$CODEX_HOME/skills/nic-structured-learning
```

Then invoke it in a task:

```text
Use $nic-structured-learning to teach me this topic from the big picture to independent practice.
```

### Other AI environments

`SKILL.md` can be adapted as a system instruction or reusable prompt in another environment. Tool use, file access, persistence, and skill discovery depend on the host product.

## Example use cases

```text
Use $nic-structured-learning to help me understand vectors before matrices.
```

```text
Use $nic-structured-learning to organise these lecture notes and prepare me for the quiz one problem at a time.
```

```text
Use $nic-structured-learning to diagnose why I cannot solve partial-derivative questions independently.
```

See [the mathematics session](examples/mathematics-session.md) for a compact worked example.

## Design documentation

The rationale behind the teaching pipeline, adaptive support, evidence handling, and mastery model is documented in [docs/methodology.md](docs/methodology.md).

## Academic integrity

This skill is intended for learning, revision, and permitted assessment support. Learners remain responsible for following their institution's assessment rules. It should not be used during a closed-book assessment or any assessment that prohibits AI or external assistance.

Do not commit private course files, personal student data, credentials, or restricted assessment materials to a public repository.

## Roadmap

- Add lightweight learning-state records across sessions.
- Develop subject-specific examples without hard-coding one curriculum.
- Create evaluation cases for recognition, reproduction, and transfer.
- Test how consistently different AI models follow the teaching workflow.

## License

Released under the MIT License.

