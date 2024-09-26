<img src="./vso_processed.png" alt="VSODEV Tech Logo" style="max-width: 250px;">

# WELCOME

Welcome to **Vsodev Tech**! We are a dynamic startup specializing in Software Development and IT Consultancy, proudly based in the Philippines. Our team is composed of passionate software engineers dedicated to transforming the world through innovative technology solutions. We aim to provide exceptional services tailored to meet the diverse needs of businesses, from small startups to large enterprises.

### Mission
To empower businesses by delivering cutting-edge software solutions and expert consultancy services that drive growth, efficiency, and innovation.

### Vision
To be a leading technology partner recognized for our commitment to excellence, creativity, and the positive impact we create in the communities we serve.

Together, let’s build a better future through technology!

---
---
---

# ONBOARDING & DEVELOPMENT GUIDE

Welcome to the **Vsodev Tech** Onboarding & Development Guide! This document covers the tools, setup instructions, code structure, development protocols, and everything you need to know to get started.

---

## Table of Contents 📖

- [Tools You Will Need](#tools-you-will-need-🪛)
- [Code Structure](#code-structure-👷)
- [Development Protocols](#development-protocols-📓)
- [Coding Guide](#coding-guide-💡)
- [Branching & Version Control](#branching-amp-version-control-🌲)
- [Testing & Debugging](#testing-and-debugging-using-jest-🧪)
- [Communication Guidelines](#communication-guidelines-💬)
- [Best Practices](#best-practices-ℹ%ef%b8%8f)

---

## Tools You Will Need 🪛


Before you start working on our project, ensure that you have the following tools installed:

1. **[Node.js](https://nodejs.org/)**: The runtime environment for JavaScript. We recommend using the latest LTS version.
    - We recommend you using the **[Node Version Manager](https://github.com/nvm-sh/nvm)**, so you can switch version for different environment
2. **[Yarn](https://yarnpkg.com/)** or **npm**: Package managers to handle dependencies. We prefer Yarn for consistency.
3. **[Git](https://git-scm.com/)**: Version control system for managing project code on your machine.
4. **[Visual Studio Code](https://code.visualstudio.com/)**: Recommended code editor.
    - Extensions: 
      - ESLint
      - Prettier
      - GitLens
5. **[Postman](https://www.postman.com/)**: For testing APIs.
6. **[Docker](https://www.docker.com/)**: (We're not using it yet) Used for containerizing the project in some setups.
7. **[Figma](https://www.figma.com/)**: For accessing design files and collaborating on UI/UX discussions.
8. **[Discord](https://discord.com/)**: For team communication. Our project uses Discord for real-time chats and discussions. Make sure you join the team server.
9. **[Trello](https://trello.com/)**: For project and task management. We use Trello to organize tasks, track progress, and ensure everyone is on the same page.
10. **[Zoho](https://mail.zoho.com)**: For email communication. This will be your primary email for project-related accounts and communications.
11. **[GitHub](https://github.com/)**: For version control and collaboration. We use GitHub to host our repositories, manage code changes, and collaborate on project development.


---

# Code Structure 👷

Our codebase is organized to ensure scalability and maintainability. Below is an overview of the key directories and their purposes.

```bash
├── src
├── ├── assets          # Your libraries or utilities
├── │   ├── images
├── ├── ├── colors
├── ├── └── fonts
│   ├── libraries          # Your libraries or utilities
│   │   ├── redux          # Redux related logic
│   │   │   ├── actions    # Action creators
│   │   │   ├── reducers   # Reducers
│   │   │   ├── store.tsx   # Redux store configuration
│   │   │   └── types.tsx   # Type definitions for actions and state
│   │   ├── other-library   # Other libraries
│   │   ├── api            # API calls and services
│   │   └── utils          # Utility functions
│   ├── components         # React components
│   │   ├── common         # Common/shared components
│   │   └── specific       # Specific components
│   ├── contexts           # React Contexts
│   │   └── ReduxContext.tsx # Context for accessing Redux state
│   ├── screens            # Application screens
│   │   ├── Auth           # Authentication screens
│   │   ├── Dashboard      # Dashboard screens
│   │   └── Settings       # Settings screens
│   ├── styles             # Global styles or theme files
│   └── App.tsx             # Main application entry point
```
In context, the structure should be the same for all(Web Portal, APIs, and Apps)

---

# Development Protocols 📓

## 1. Project Setup
- Use TypeScript for all projects to ensure type safety and improved code quality.
- Structure projects following the organized file structure outlined above.
- Use a monorepo approach (if applicable) for managing multiple related projects with tools like Yarn Workspaces or Lerna.

## 2. Version Control
- Use Git for version control.
- Follow a branching strategy (e.g., Git Flow, GitHub Flow).
  - **Production Branch**: Production version of the codebase.
  - **Main Branch**: Stable version of the codebase.
  - **Development Branch**: Ongoing development work.
  - **Feature Branches**: For developing new features or bug fixes.
- Commit messages should follow the format: `type(scope): description` (e.g., `feat(auth): add login functionality`).
- Push code to a remote repository regularly to keep backups.

## 3. Code Quality ⚠️
Maintaining high code quality is **crucial** for ensuring the long-term success of the project. Follow these practices:

- **Use ESLint** for linting TypeScript code.
  - Configure ESLint with TypeScript support using `@typescript-eslint`.
- **Use Prettier** for code formatting.
  - Set up Prettier to work in tandem with ESLint.
- **Regularly run linters and formatters before committing code** to avoid introducing inconsistencies and bugs.

## 4. Testing
- Write unit tests using **Jest** for both Node.js and React projects.
- Use **React Testing Library** for testing React components.
- Maintain a code coverage threshold (e.g., 80% coverage).

## 5. Documentation (*Upcoming Implementation*)
- Use tools like **Docsify** or **Storybook** for documenting components and APIs.
- Maintain inline comments and documentation in code for complex logic.
- Write comprehensive README files for each project/module.

## 6. API Design
- Follow RESTful API principles for Node.js backends.
- Use **TypeScript interfaces** to define request and response structures.
- Implement error handling and logging for API requests.
- Use tools like **Postman** for API testing and documentation.

## 7. Component Design
- Use **React functional components** with hooks wherever possible.
- Ensure components are reusable and follow the single responsibility principle.
- Maintain a consistent styling approach (CSS Modules, Styled Components, etc.).

## 8. State Management
- Use **Redux** for state management in React applications.
- Use **React Context** for localized state management.
- Organize Redux logic (actions, reducers, store) following the folder structure outlined above.

## 9. Performance Optimization
- Use React’s built-in optimization techniques (e.g., `React.memo`, `useMemo`, `useCallback`).
- Monitor application performance using tools like Chrome DevTools.

---

# Code Guide 💡

Here’s an example of a simple functional component in TypeScript, demonstrating the use of interfaces and separate utility functions.

Files should always be separated for cleaner and well-documented codebase; you can always check the **[Code Structure](#code-structure)** for reference.

## Interface
Interfaces define the structure of objects in TypeScript. They are crucial for ensuring that objects adhere to a specific shape, improving type safety and code reliability. Grouping related interfaces in one file can enhance readability and provide clear context for their usage.

```typescript
export interface Counter {
  initialCount?: number;
}

```

## Types Declaration
Type declarations define the types that can be used in your application. This includes primitive types, union types, and object shapes. Keeping type declarations organized helps maintain clarity, especially when types evolve or expand.

```typescript
export type ButtonProps = {
  label: string;
  onClick: (e: event) => void;
}

```

## Functions
This structure provides a clear breakdown of each section's purpose while including a utility function example for clarity.

```typescript
export const calculateNewCount = (currentCount: number, delta: number): number => {
  return currentCount + delta;
};

```
## Custom Components
Custom components are reusable UI elements that can encapsulate specific functionality. They should be created for common patterns to promote code reuse and maintain consistency across your application. Separating these components helps in managing complexity and enhances maintainability.

```typescript
import React from 'react';
import { ButtonProps } from './types';

export const CustomButton: React.FC<ButtonProps> = ({ label, onClick }) => {
  return (
    <button onClick={onClick}>
      {label}
    </button>
  );
};
```

## Screen Components
Screen components are the primary building blocks of your application's UI. They should be designed to handle specific views and manage state and props effectively. Keeping them separate allows for better reusability and easier testing.
```typescript
import React, { useState } from 'react';
import { Counter } from './types'; // Importing the CounterProps interface
import { calculateNewCount } from './utils'; // Importing the utility function
import { CustomButton } from './custom-button';

const Counter: React.FC<Counter> = ({ initialCount = 0 }) => {
  const [count, setCount] = useState<number>(initialCount); // State to hold the count

  const increment = () => setCount((prevCount) => calculateNewCount(prevCount, 1)); 
  const decrement = () => setCount((prevCount) => calculateNewCount(prevCount, -1));

  return (
    <div>
      <h1>Count: {count}</h1>
      <CustomButton onClick={increment} label={'Increment'} />
      <CustomButton onClick={decrement} label={'Decrement'} />
    </div>
  );
};

export default Counter;

```

---

# Branching & Version Control 🌲

Effective branching and version control practices are essential for maintaining code quality and facilitating collaboration within teams. This guide outlines the best practices for using version control systems, such as Git.

## 1. Branching Strategy

- **Main Branch (`main` or `master`)**: The stable version of the project that should always be in a deployable state.
- **Development Branch (`develop`)**: The integration branch where features are merged and tested before being released.
- **Feature Branches**: Create a new branch for each feature or bug fix, typically named using the format `feature/<feature-name>` or `bugfix/<bug-name>`. This keeps the work organized and allows for parallel development.

### checkout
```bash
git checkout -b feature/new-login
```

## 2. Commit Practices
Descriptive Commit Messages: Write clear and concise commit messages that explain the purpose of the changes. Use the imperative mood (e.g., "Add new login feature").
Atomic Commits: Make commits that encapsulate a single logical change to the codebase. This makes it easier to understand the history and revert changes if necessary.
### commit
```bash
git commit -m "Add new login feature"
```
## 3. Merging Changes
Pull Requests (PR): Use PRs to review and discuss code changes before merging them into the main branch. This process facilitates collaboration and ensures code quality.
Rebase vs. Merge: Consider using rebase to maintain a cleaner commit history, but use merge when you need to preserve the history of how changes were integrated.
## 4. Tagging Releases
Semantic Versioning: Use tags to mark release versions following semantic versioning (e.g., v1.0.0). This practice makes it easier to track and manage releases.
### releases
```bash
git tag -a v1.0.0 -m "Release version 1.0.0"
```
## 5. Collaboration
Regular Syncing: Frequently pull changes from the main branch to keep your feature branches up-to-date and avoid merge conflicts.
Code Reviews: Encourage team members to review each other's code through pull requests to maintain code quality and share knowledge.
By adhering to these branching and version control practices, teams can enhance collaboration, maintain a clean codebase, and ensure the quality of their projects.

---

# Testing and Debugging Using Jest 🧪

Jest is a powerful testing framework for JavaScript and TypeScript applications, widely used for unit testing and integration testing. This guide outlines best practices for writing and organizing tests using Jest.

## 1. Writing Specs

### Spec Structure

Organize your specs alongside your components. Each spec file should follow the naming convention `<filename>.spec.ts`.

### Example Spec

Here's an example of a simple function and its corresponding Jest spec:

#### Function to Test

```typescript
// src/utils/calculate.ts
export const add = (a: number, b: number): number => a + b;

// src/utils/__tests__/calculate.spec.ts
import { add } from '../calculate';

describe('add', () => {
  it('returnw the sum of two numbers', () => {
    expect(add(1, 2)).toBe(3);
    expect(add(-1, -1)).toBe(-2);
    expect(add(0, 0)).toBe(0);
  });
});

```
2. Running Specs
You can run your specs using the following command:

```bash
npm test
````
You can also run specs in watch mode, which will automatically re-run specs when files are changed:

```bash
npm run watch
```
## 3. Debugging Specs
Jest provides built-in support for debugging. You can run specs in a debugging environment by using the --inspect flag:

```bash
Copy code
node --inspect-brk node_modules/.bin/jest --runInBand
```
This command allows you to connect your debugger and set breakpoints within your specs.

## 4. Best Practices
Keep Specs Isolated: Ensure that each spec is independent and does not rely on the state of other specs.
Use Descriptive Names: Name your spec cases and suites descriptively to indicate what is being tested.
Spec Edge Cases: Make sure to cover edge cases and unexpected inputs in your specs.
By following these guidelines and utilizing Jest effectively, you can ensure a robust testing strategy for your JavaScript and TypeScript applications.

# Communication Guidelines 💬

Effective communication is key to a successful workflow. We use the following tools to facilitate communication and collaboration:

## 1. Tools for Communication

### Make sure to have:

- **[Trello](https://trello.com/)**: We use Trello for task management and tracking project progress. Boards are created for different projects, and cards are used to manage tasks. Ensure to update the status of tasks regularly

- **[Zoho Mail](https://mail.zoho.com/)**: We utilize Zoho Mail for official communication. Make sure to check your email frequently and respond to messages promptly.

- **[Discord](https://discord.com/)**: We use Discord for real-time communication. It’s useful for team discussions, quick updates, and casual conversations. Channels are created for different topics or projects to keep discussions organized.

## 2. Communication Etiquette

- **Be Respectful**: Always communicate with respect and professionalism.
- **Be Clear and Concise**: When sending messages or emails, be clear and to the point.
- **Use Proper Channels**: Use Trello for task updates, Zoho for formal communication, and Discord for quick chats.
- **Provide Updates**: Regularly update your team on your progress and any challenges you face.

---

# Best Practices ℹ️

Following best practices in development ensures high-quality code and efficient workflows. Here are some recommended practices:

## 1. Code Quality

- **Use ESLint and Prettier**: Maintain code quality by using ESLint for linting and Prettier for formatting. Set them up to run automatically on your development environment.

## 2. Version Control

- **Use Git for Version Control**: Regularly commit your changes and push to the main branch. Follow the branching strategy defined in your team.

## 3. Documentation

- **Document Your Code**: Write clear comments and documentation for your code. Use markdown files to explain your code structure and functionality.

## 4. Testing

- **Write Tests**: Implement unit tests and integration tests to ensure your code works as intended. Use Jest for writing your test cases.

## 5. Regular Code Reviews

- **Conduct Code Reviews**: Regularly review each other's code to maintain quality and share knowledge among the team. Use pull requests for code submissions.

By adhering to these communication guidelines and best practices, we can ensure a productive and positive work environment.
