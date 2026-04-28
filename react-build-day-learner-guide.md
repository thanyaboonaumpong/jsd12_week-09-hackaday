# React Build Day — Learner Introduction & Event Guide

Welcome to **React Build Day**.

Today is a one-day beginner-friendly event where you will work in a small team to build a simple interactive React app.

This is not about building the most advanced app.

This is about practicing React, solving problems together, and proving to yourself that you can turn an idea into a working frontend project.

---

# Your Mission

Your team’s mission is to build a small React app that helps someone:

- Track something
- Organize something
- Decide something
- Learn something
- Buy or choose something
- Complete a simple task

By the end of the day, your team should have a working app that you can demo to others.

---

# Main Learning Goal

By the end of today, you should be able to say:

> “I can build a small React app using components, props, state, events, conditional rendering, lists, forms, and basic styling.”

---

# React Concepts You Should Practice

Your project should include as many of these React concepts as possible:

| Concept | Meaning |
|---|---|
| Components | Breaking the UI into smaller reusable parts |
| Props | Passing data from one component to another |
| `useState` | Remembering and updating information in the app |
| Event handlers | Running code when users click, type, or submit |
| Conditional rendering | Showing different UI depending on the situation |
| Lists and `.map()` | Displaying multiple items from an array |
| Forms | Getting user input |
| Basic styling | Making the app clear and usable |

---

# Minimum Project Requirements

Your app should include:

- At least 3 components
- At least 1 use of `useState`
- At least 2 event handlers
- At least 1 list rendered with `.map()`
- At least 1 conditional rendering example
- Basic styling
- A short team demo

---

# Recommended Project Options

Choose one project idea as your starting point.

You can customize the theme, design, and extra features.

---

## Option 1: Shopping List App

Build an app that helps users manage a shopping list.

### Core Features

- Add an item
- Display all items
- Mark an item as bought
- Delete an item
- Show total number of items

### Stretch Features

- Filter by all / bought / not bought
- Clear completed items
- Save items to `localStorage`

---

## Option 2: Flashcard Quiz App

Build an app that helps users study using flashcards.

### Core Features

- Show one question at a time
- Reveal the answer
- Move to the next question
- Show current question number

### Stretch Features

- Track score
- Restart quiz
- Add categories

---

## Option 3: Mini E-Commerce Cart

Build a simple shopping cart app.

### Core Features

- Show product cards
- Add product to cart
- Show cart items
- Show total price

### Stretch Features

- Increase or decrease quantity
- Remove item from cart
- Filter products by category

---

## Option 4: Mood Tracker App

Build an app that helps users track their mood.

### Core Features

- Select a mood
- Add a short note
- Display mood entries
- Delete an entry

### Stretch Features

- Count moods
- Filter by mood
- Add date or time

---

## Option 5: Task Board App

Build a simple task board.

### Core Features

- Add a task
- Show tasks in columns
- Move task from To Do to Doing to Done

### Stretch Features

- Delete task
- Add priority
- Search or filter tasks

---

# Suggested Team Roles

You do not have to follow these exactly, but they can help your team organize.

| Role | Responsibility |
|---|---|
| Component Lead | Helps decide how to split the UI into components |
| State Lead | Helps manage `useState` and app data |
| UI Lead | Helps with layout, styling, and user experience |
| Demo Lead | Helps prepare the final presentation |

Everyone should still understand the whole project.

Do not let only one person code everything.

---

# GitHub Collaboration Guide

Your team should use GitHub to collaborate.

## Recommended Workflow

1. One team member creates the primary project repository.
2. The remaining team members fork the primary repository.
3. Each team member clones their own working repo.
4. Each team member creates a feature branch.
5. Each team member commits their work.
6. Each team member opens a Pull Request.
7. The team reviews and merges Pull Requests into `main`.

## Important Rule

Nobody should push directly to `main`, including the person who owns the primary repo.

The `main` branch should represent the working version of the project.

---

# Repo Owner Workflow

The person who creates the primary repo does not need to fork their own repo.

They can work directly from the primary repo, but they should still create a branch and open a Pull Request.

Example:

```bash
git clone <primary-repo-url>
cd project-name
git checkout -b feature/header-component
```

After making changes:

```bash
git add .
git commit -m "Add header component"
git push origin feature/header-component
```

Then open a Pull Request from:

```txt
feature/header-component → main
```

---

# Other Team Members Workflow

Other team members should fork the primary repo first.

Then clone their own fork:

```bash
git clone <your-fork-url>
cd project-name
git checkout -b feature/cart-component
```

After making changes:

```bash
git add .
git commit -m "Add cart component"
git push origin feature/cart-component
```

Then open a Pull Request from:

```txt
your-fork:feature-cart-component → primary-repo:main
```

---

# What Is a Pull Request?

A Pull Request is a GitHub feature.

Git helps us track and share code changes.

GitHub adds teamwork features on top of Git.

A Pull Request is GitHub’s way of asking:

> “Can we review and merge my branch into the main project?”

A Pull Request lets your team:

- Review code
- Leave comments
- Discuss changes
- Check what files changed
- Merge safely into `main`

---

# Recommended Build Process

Follow these steps.

---

## Step 1: Understand the User

Before coding, answer:

- Who is this app for?
- What problem does it solve?
- What is the simplest version that would still be useful?

Example:

> This app is for students who want to revise vocabulary using flashcards.

---

## Step 2: Sketch the UI

Draw a quick wireframe on paper, whiteboard, or a digital tool.

Ask:

- What should the user see first?
- What buttons are needed?
- What information should be displayed?
- What changes when the user interacts with the app?

---

## Step 3: Break the UI into Components

Think in React components.

Example for a Shopping List App:

```txt
App
├── Header
├── AddItemForm
├── ShoppingList
│   └── ShoppingItem
└── Summary
```

Example for a Mini E-Commerce Cart:

```txt
App
├── Header
├── ProductList
│   └── ProductCard
├── Cart
│   └── CartItem
└── TotalPrice
```

---

## Step 4: Build the Static Version First

Before adding state or interactivity, build the app with hard-coded sample data.

This helps you focus on structure before logic.

Example:

```jsx
const products = [
  { id: 1, name: "Coffee", price: 80 },
  { id: 2, name: "Tea", price: 60 },
  { id: 3, name: "Cake", price: 120 },
];
```

---

## Step 5: Add State

Use `useState` when the app needs to remember something that can change.

Examples:

```jsx
const [items, setItems] = useState([]);
```

```jsx
const [cart, setCart] = useState([]);
```

```jsx
const [selectedMood, setSelectedMood] = useState("");
```

Ask:

- What data changes when the user interacts?
- Where should this state live?
- Which component needs access to this state?

---

## Step 6: Add Events

Use event handlers when users interact with the app.

Examples:

```jsx
<button onClick={handleAddItem}>Add Item</button>
```

```jsx
<form onSubmit={handleSubmit}>
```

```jsx
<input onChange={handleChange} />
```

Common user actions:

- Click a button
- Type into an input
- Submit a form
- Select an option
- Delete an item
- Filter a list

---

## Step 7: Render Lists with `.map()`

Use `.map()` to display items from an array.

Example:

```jsx
{items.map((item) => (
  <ShoppingItem key={item.id} item={item} />
))}
```

Remember:

Every item rendered from a list needs a unique `key`.

---

## Step 8: Add Conditional Rendering

Use conditional rendering to show different UI depending on state.

Examples:

```jsx
{items.length === 0 ? (
  <p>No items yet.</p>
) : (
  <ShoppingList items={items} />
)}
```

```jsx
{isAnswerVisible && <p>{currentCard.answer}</p>}
```

Good apps tell users what is happening.

Examples:

- No items yet
- Cart is empty
- Please enter a name
- Quiz completed
- No results found

---

## Step 9: Style the App

Focus on clarity first.

Your app does not need to look perfect.

Aim for:

- Clear spacing
- Readable text
- Buttons that are easy to find
- Simple layout
- Consistent styling

If using Tailwind, useful classes include:

```txt
p-4
m-4
flex
grid
gap-4
rounded
shadow
border
text-xl
font-bold
bg-gray-100
```

---

## Step 10: Prepare Your Demo

Your final demo should be short and clear.

Each team will have around 3 minutes.

Use this structure:

1. What did you build?
2. Who is the app for?
3. What are the main features?
4. What React concepts did you use?
5. What was the hardest problem or bug?
6. What would you improve next?

Example:

> We built a Flashcard Quiz App for beginners learning JavaScript.  
> Users can view a question, reveal the answer, and move to the next card.  
> We used components, props, `useState`, event handlers, and conditional rendering.  
> The hardest part was updating the current question without going past the final card.  
> Next, we would add score tracking and categories.

---

# Recommended Folder Structure

```txt
src/
  App.jsx
  main.jsx
  data/
    sampleData.js
  components/
    Header.jsx
    Button.jsx
    Card.jsx
```

You can add more files as needed.

---

# Helpful Questions When You Get Stuck

## If your UI is confusing

Ask:

- Can we simplify the layout?
- What should the user do first?
- Is every button clearly named?

## If your code is confusing

Ask:

- Can this be a separate component?
- Is this variable name clear?
- Are we storing too much in state?
- Can we explain this code to another beginner?

## If your state is not updating

Ask:

- Did we call the setter function?
- Are we mutating the array directly?
- Are we using the latest state correctly?
- Is the event handler actually connected?

## If your team is stuck

Try this:

1. Stop coding for 3 minutes.
2. Explain the problem out loud.
3. Write the expected behavior.
4. Check the current state.
5. Use `console.log()`.
6. Ask an instructor.

---

# Important React Reminders

## Components are functions that return UI

```jsx
function Header() {
  return <h1>My App</h1>;
}
```

---

## Props pass data into components

```jsx
function ProductCard({ product }) {
  return <h2>{product.name}</h2>;
}
```

---

## State stores data that changes

```jsx
const [count, setCount] = useState(0);
```

---

## Events make the app interactive

```jsx
<button onClick={() => setCount(count + 1)}>
  Add
</button>
```

---

## `.map()` renders lists

```jsx
{names.map((name) => (
  <p key={name}>{name}</p>
))}
```

---

# What Judges Will Look For

Judges are not expecting a perfect app.

They are looking for evidence that your team practiced React fundamentals.

You will be judged on:

- Does the app work?
- Did you use components?
- Did you use state and events?
- Did you render data dynamically?
- Is the UI understandable?
- Can your team explain what you built?

---

# What Makes a Strong Beginner Project?

A strong beginner project is:

- Simple but working
- Easy to understand
- Built with clear components
- Interactive
- Explained well by the team

A small working app is better than a big broken app.

---

# Teamwork Expectations

During the event:

- Share the keyboard
- Talk through decisions
- Help each other understand
- Ask questions early
- Commit your code regularly if using Git
- Make sure everyone can explain at least one part of the app

The goal is not only to finish.

The goal is to learn together.

---

# Final Reminder

Today is about practice.

You may get stuck. That is normal.

You may see errors. That is normal.

You may need to rewrite something. That is normal.

React starts to make sense when you build, break, debug, and rebuild.

By the end of today, your team should be able to say:

> “We built something real with React, and we understand how it works.”
