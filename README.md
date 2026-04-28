# React Build Day

A one-day beginner-friendly event where small teams design, build, and demo a simple interactive React app.

## What is this?

React Build Day is a structured hackathon for learners who are new to React. Teams of 2–4 people pick a project idea, build it together using core React fundamentals, and present a short demo at the end of the day.

The goal is not to build the most advanced app — it is to practice React by shipping something real.

## Guides

| Document | Audience | Description |
|---|---|---|
| [Learner Guide](react-build-day-learner-guide.md) | Participants | Project options, build process, GitHub workflow, and React reminders |
| [Judge Guide](react-build-day-ai-judge.md) | Judges / Instructors | Scoring rubric, evaluation criteria, award categories, and suggested questions |

## What teams will build

Each team chooses one of five starting ideas:

- **Shopping List** — add, mark, and delete items
- **Flashcard Quiz** — flip through questions and reveal answers
- **Mini E-Commerce Cart** — browse products and manage a cart
- **Mood Tracker** — log moods with notes and view history
- **Task Board** — move tasks through To Do, Doing, and Done

Teams are encouraged to customise the theme, design, and features.

## Minimum requirements

Every project must include:

- At least 3 components
- At least 1 `useState`
- At least 2 event handlers
- At least 1 list rendered with `.map()`
- At least 1 conditional render
- Basic styling

## How teams are judged

Projects are scored out of 100 points across six criteria: functionality, component structure, state and event handling, dynamic rendering, UI clarity, and demo explanation. See the [Judge Guide](react-build-day-ai-judge.md) for the full rubric and award categories.

## Getting started

Scaffold a new React app with Vite:

```bash
npm create vite@latest my-app -- --template react
cd my-app
npm install
npm run dev
```

Then read the [Learner Guide](react-build-day-learner-guide.md) for the recommended step-by-step build process and GitHub collaboration workflow.
