# React Build Day — AI Judge Guide, Scoring Rubric & Awards

## Purpose

This document is for the AI judge, instructors, mentors, or human judges evaluating beginner React projects during a one-day React Build Day / Hackaday event.

The purpose of judging is not to reward only the most advanced or visually polished app. The goal is to recognize evidence of learning, teamwork, practical React fundamentals, debugging, and the ability to explain what was built.

This event is designed for beginner software developer learners practicing React.

---

# Judging Philosophy

Judge beginner projects by asking:

> Did this team understand and practice the core React concepts they were expected to use?

Reward teams that show:

- A working simple app
- Clear component structure
- Correct use of `useState`
- Meaningful event handling
- Dynamic rendering with arrays
- Clear explanation of their code
- Good teamwork and problem-solving

Do not over-reward:

- Beautiful UI with weak React logic
- Complex features that the team cannot explain
- AI-generated code that the team does not understand
- One strong learner doing all the work
- Unnecessary technical complexity

The best beginner project is not always the most complex project.

---

# Core Scoring Rubric

Total score: **100 points**

| Criteria | Points | What Judges Should Look For |
|---|---:|---|
| App works without major errors | 20 | The app runs successfully, key features work, and there are no major crashes during the demo. |
| Clear use of React components | 20 | The UI is broken into meaningful components instead of everything being placed in one large file. |
| Correct use of state and events | 20 | The app uses `useState` and event handlers to make the UI interactive. |
| Dynamic rendering of data | 15 | The app uses data, arrays, `.map()`, `.filter()`, or similar logic to render content dynamically. |
| UI clarity and usability | 15 | The app is understandable, easy to use, and visually organized, even if the design is simple. |
| Demo explanation | 10 | The team clearly explains what they built, how it works, and which React concepts they used. |

**Total: 100 points**

---

# Detailed Evaluation Guide

## 1. App Works Without Major Errors — 20 points

| Score Range | Description |
|---|---|
| 16–20 | App runs smoothly. Main features work correctly. Minor bugs only. |
| 11–15 | App mostly works, but some features are incomplete or inconsistent. |
| 6–10 | App runs, but several important features are broken. |
| 0–5 | App does not run or cannot be meaningfully demonstrated. |

Look for:

- App can be opened locally or deployed
- Main user flow works
- No major runtime errors in the browser
- Demo does not collapse because of broken core functionality

---

## 2. Clear Use of React Components — 20 points

| Score Range | Description |
|---|---|
| 16–20 | App is clearly divided into reusable and meaningful components. |
| 11–15 | Some components are used, but the structure could be clearer. |
| 6–10 | Components exist but are not used effectively. |
| 0–5 | Most of the app is written in one large component with little structure. |

Examples of good component structure:

```txt
src/
  App.jsx
  components/
    Header.jsx
    ProductCard.jsx
    ProductList.jsx
    Cart.jsx
    CartItem.jsx
```

Judge whether components have clear responsibilities.

Good signs:

- Components are named clearly
- Components are not too large
- Props are used to pass data
- Similar UI pieces are reused

---

## 3. Correct Use of State and Events — 20 points

| Score Range | Description |
|---|---|
| 16–20 | `useState` and event handlers are used correctly and confidently. |
| 11–15 | State and events mostly work, but there are some logic issues. |
| 6–10 | State is attempted but not clearly understood. |
| 0–5 | Little or no meaningful state or event handling is used. |

Look for examples such as:

```jsx
const [items, setItems] = useState([]);
```

```jsx
<button onClick={handleAddItem}>Add Item</button>
```

Good signs:

- User actions update the UI
- State is updated through setter functions
- Arrays are not mutated directly
- Event handlers are connected correctly
- The team can explain what state they used and why

---

## 4. Dynamic Rendering of Data — 15 points

| Score Range | Description |
|---|---|
| 12–15 | Data is rendered dynamically using `.map()`, `.filter()`, or similar logic. |
| 8–11 | Dynamic rendering is present but limited. |
| 4–7 | Data rendering is attempted but has bugs or unclear logic. |
| 0–3 | Most content is hard-coded. |

Look for examples such as:

```jsx
{products.map((product) => (
  <ProductCard key={product.id} product={product} />
))}
```

```jsx
const filteredItems = items.filter((item) => item.completed === false);
```

Good signs:

- Arrays are used to store data
- `.map()` is used to render lists
- Each list item has a `key`
- `.filter()` or similar logic is used if the project needs filtering
- The app avoids unnecessary repeated hard-coded JSX

---

## 5. UI Clarity and Usability — 15 points

| Score Range | Description |
|---|---|
| 12–15 | App is easy to understand, clear, and pleasant to use. |
| 8–11 | App is usable but could be better organized visually. |
| 4–7 | App works but is confusing or difficult to navigate. |
| 0–3 | UI is incomplete or very hard to understand. |

Focus on clarity, not perfection.

Look for:

- Clear layout
- Readable text
- Buttons that make sense
- Useful empty states
- Good spacing
- Simple visual hierarchy
- Basic responsive layout if attempted

---

## 6. Demo Explanation — 10 points

| Score Range | Description |
|---|---|
| 8–10 | Team clearly explains the app, features, React concepts, and challenges. |
| 5–7 | Team explains the app but misses some technical or reflective details. |
| 2–4 | Demo is unclear or very limited. |
| 0–1 | Team cannot explain the app meaningfully. |

Recommended demo structure:

1. What did you build?
2. Who is it for?
3. What features work?
4. What React concepts did you use?
5. What was the hardest bug or challenge?
6. What would you improve next?

---

# Optional Bonus Recognition

Bonus points do not need to affect the final score unless judges want them to.

Optional bonus: **up to 10 extra points**

| Bonus Area | Points | Description |
|---|---:|---|
| Stretch feature completed | +3 | Team added a useful extra feature beyond the core requirements. |
| Strong teamwork | +3 | Team collaborated well and shared responsibilities. |
| Clean code or naming | +2 | Code is readable, well-named, and easy to follow. |
| Creative idea or theme | +2 | The app has a memorable concept, user story, or design idea. |

---

# Judging Awards

These awards are designed to recognize different strengths. Not every award has to go to the highest-scoring team.

## Main Awards

### Best Overall React App

Awarded to the team with the strongest balance of functionality, React usage, usability, and demo explanation.

Judges should look for:

- App works well
- React concepts are used clearly
- UI is understandable
- Team explains their work confidently

---

### Best Use of React State

Awarded to the team that shows the clearest and most meaningful use of `useState`.

Judges should look for:

- State changes update the UI correctly
- User interactions are handled well
- State is not unnecessarily duplicated
- The team can explain what state they used and why

---

### Cleanest Component Structure

Awarded to the team that organizes their app into clear, reusable components.

Judges should look for:

- Components have clear responsibilities
- Props are passed meaningfully
- Files are organized logically
- Code is easier to understand because of the structure

---

### Most Useful App

Awarded to the team that builds the app with the clearest real-world use case.

Judges should look for:

- Clear target user
- Practical problem being solved
- Features that support the user’s goal
- App feels usable beyond the event

---

### Best Beginner-Friendly Code

Awarded to the team whose code is easiest for another beginner to understand.

Judges should look for:

- Clear variable names
- Simple logic
- Minimal unnecessary complexity
- Code that another learner could learn from

---

## Creative and Encouragement Awards

### Most Creative Concept

Awarded to the team with the most original or memorable idea.

Judges should look for:

- Interesting theme
- Fun user experience
- Creative adaptation of a simple project brief
- Personality in the app

---

### Best UI Improvement

Awarded to the team that makes the app visually clear and pleasant to use.

Judges should look for:

- Good layout
- Clear spacing
- Consistent styling
- Thoughtful use of color, typography, or Tailwind classes

---

### Best Debugging Comeback

Awarded to the team that overcame a meaningful technical challenge.

Judges should look for:

- Team faced a real bug or blocker
- Team explained how they solved or worked around it
- Team showed persistence
- Learning was clearly visible

---

### Best Team Collaboration

Awarded to the team that worked together especially well.

Judges should look for:

- Shared participation
- Good communication
- Everyone understands the project
- Demo is not dominated by only one person

---

### Best Demo Explanation

Awarded to the team that explains their project most clearly.

Judges should look for:

- Clear explanation of the app
- Clear explanation of React concepts
- Honest reflection on challenges
- Confident but humble presentation

---

# GitHub Collaboration Expectations

The expected beginner-friendly GitHub workflow is:

1. One team member creates the primary GitHub repository.
2. Other team members fork the primary repository.
3. Each learner works on a feature branch.
4. Each learner opens a Pull Request before merging code.
5. Nobody should push directly to `main`, including the repository owner.

Important clarification:

- Pull Request is a GitHub feature, not a core Git feature.
- Git records commits and merges.
- GitHub records Pull Requests, comments, approvals, and review discussions.
- After a Pull Request is merged, Git history may show a merge commit, but the full Pull Request record stays on GitHub.

Repo owner workflow:

```bash
git clone <primary-repo-url>
cd project-name
git checkout -b feature/header-component
```

Then:

```bash
git add .
git commit -m "Add header component"
git push origin feature/header-component
```

The repo owner then opens a Pull Request from:

```txt
feature/header-component → main
```

Other members usually open a Pull Request from:

```txt
their-fork:feature-name → primary-repo:main
```

Judges may optionally recognize teams that use GitHub collaboration well, but do not over-penalize beginners for imperfect Git history if they clearly practiced collaboration.

---

# Suggested Final Judging Process

1. Each team demos for 3 minutes.
2. Judges ask 1–2 short questions.
3. Judges score using the 100-point rubric.
4. Judges select main winners by score.
5. Judges select special awards based on observed strengths.

---

# Suggested Questions for Teams

Use these questions to evaluate understanding:

1. Which components did your team create, and why?
2. What data did you store in state?
3. Which user actions trigger state changes?
4. Where did you use `.map()` or `.filter()`?
5. What was your hardest bug?
6. Which part of the app are you most proud of?
7. What would you improve if you had one more day?

---

# Final Note for Judges

Please remember that this is a beginner React event.

Reward learning, not perfection.

The best project is the one where the team can say:

> “We understand what we built, how it works, and what we learned.”
