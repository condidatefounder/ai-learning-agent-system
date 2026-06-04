# Zhixue Workshop

An open source prototype for personalized AI learning workflows. The project focuses on an Introduction to Artificial Intelligence course scenario and demonstrates a full learning loop: student profiling, local course-material RAG, multi-agent coordination, resource generation, study-path planning, tutoring answers, and learning evaluation.

![Desktop RAG workspace](screenshots/desktop-rag.png)

## Status

- Current version: `v0.2.0` open source maintenance foundation.
- Runtime: frontend-only prototype running in a local browser.
- Data boundary: uploaded course files are parsed locally in the browser and are not persisted after refresh.
- Use cases: course demos, AI education product prototyping, and multi-agent learning workflow research.

## Features

- Student profile generation from major, grade, goals, learning background, preferences, and quiz scores.
- Local RAG for `.txt`, `.md`, `.markdown`, `.json`, and `.csv` course materials.
- Seven learning agents: profile analysis, knowledge diagnosis, path planning, resource generation, quiz generation, tutoring, and content review.
- Personalized resources, including handouts, mind maps, exercises, code examples, and PPT/video scripts.
- Seven-day learning path focused on neural network fundamentals.
- Tutor answers grounded in retrieved course chunks and student weak spots.
- Learning evaluation with mastery score, skill radar, follow-up suggestions, and profile updates.

## Quick Start

Requirements:

- Node.js 18 or later.
- Python 3 for the static local server.

Run:

```bash
npm test
npm run serve
```

Open:

```text
http://localhost:5173
```

## Demo Flow

1. Select the neural network learning scenario.
2. Import sample course documents or upload text-based course material.
3. Ask a retrieval question, such as `Why does backpropagation need the chain rule?`.
4. Run retrieval and inspect Top-K chunks, source files, and relevance scores.
5. Run the multi-agent workflow.
6. Review the generated profile, resources, study path, tutoring answer, and evaluation.

More details are available in [docs/DEMO.md](docs/DEMO.md).

## Testing

```bash
npm test
```

The test suite covers:

- Student profiling and the multi-agent workflow.
- RAG document parsing, chunking, indexing, retrieval, and cited answers.
- UI contract checks for the workspace, upload controls, RAG area, and responsive styles.

## Roadmap

See [ROADMAP.md](ROADMAP.md). Near-term work includes:

- Integrating real model APIs.
- Adding server-side PDF/PPT/Word parsing.
- Adding persistent vector indexes.
- Adding teacher-side resource review.
- Exporting PPTX, PDF, and video scripts.

## Contributing

Contributions are welcome. Please read [CONTRIBUTING.md](CONTRIBUTING.md) before opening an issue or pull request.

Good first contribution areas:

- Add course sample materials.
- Improve RAG chunking and retrieval.
- Add accessibility tests.
- Add export workflows.
- Improve English documentation.

## Maintainer

- GitHub: [condidatefounder](https://github.com/condidatefounder)
- Email: condidatefound@gmail.com

## License

[MIT](LICENSE)
