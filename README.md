# AI Product Operating System (AI-POS)

> "Turn AI into your product team."

## 🚀 What is AI-POS?

AI-POS is a context-driven framework for product development. It decouples **Product Strategy**, **Management**, and **Engineering** from specific product details, allowing you to use a single suite of AI workflows (slash commands) for any product.

By defining your project context once, you enable AI agents to act as expert Product Managers, Architects, and Engineers who already "know" your product's goals, constraints, and users.

---

## 🔄 How it Works

AI-POS follows a rigorous product lifecycle:
**Idea** → **Explore** → **Define** → **Plan** → **Build** → **Review** → **Ship**

1. **Context**: You fill out a `project-context.md`.
2. **Roles**: AI-POS loads a behavioral persona (e.g., Product Strategist).
3. **Workflows**: AI-POS executes a structured process (e.g., `/create-prd`).
4. **Output**: You get high-quality, strategic artifacts (PRDs, System Designs, etc.).

---

## 🏁 Quick Start

1. **Clone the Repo**:
   ```bash
   git clone https://github.com/wanibisen3/ai-product-os.git
   ```
2. **Set Your Context**:
   Copy `context/project-context-template.md` to `context/project-context.md` and fill it out.
3. **Run a Workflow**:
   Use any AI tool to execute the workflows in `workflows/`.

---

## 🛠️ Using with AI Tools

### Using with Antigravity
The system works natively with Antigravity’s slash command system.
- **Setup**: Copy the contents of the `roles/`, `scripts/`, `context/`, and `workflows/` directories into your project's `.agents/` folder.
  - Workflows must go into `.agents/workflows/` to be recognized as slash commands.
  - Roles, scripts, and context files should remain in the root of `.agents/` or as referenced in the workflow files.
- **Usage**: Type `/` in the Antigravity chat to see and run any AI-POS workflow (e.g., `/create-prd`).
- **Flow**: Antigravity automatically loads the **Role** and **Context** from the specified paths.

### Using with Cursor
To use AI-POS as slash commands in Cursor:
- **Setup**: Reference the `roles/`, `workflows/`, and `context/` directories in your project.
- **Rules**: Add the contents of your preferred roles to your `.cursorrules` file to define persistent behavioral instructions.
- **Usage**: Use `@` to reference a workflow file in the chat: `@create-prd "Implement the login feature"`.
- **Optimization**: You can also define global "Rules for AI" in Cursor's settings to make these workflows always available.

### Using with Claude Code
- **Repo Setup**: Open your terminal in the `ai-product-os` directory.
- **Invoking**: Run `claude` and point it to the workflows.
- **Example**: "Claude, read `context/project-context.md` and `workflows/system-design.md`. Now design the architecture for a new notification service."

---

## ⭐ AI-POS FOR NON-CODERS (SLASH COMMANDS)

You don't need any coding knowledge or terminal skills to manage a product with AI-POS. By using an AI-powered editor like **Antigravity**, **Cursor**, or **Claude Code**, you can trigger complex workflows using simple **slash commands**.

### 1. Set Your Context
Fill out `context/project-context.md` once. This tells the AI everything about your product.

### 2. Use Slash Commands
Instead of writing complex prompts, just type `/` followed by a workflow name. The AI will automatically load the right **Role** and **Context**.

### 3. Manage Everything with Prompts
You can even handle technical tasks like Git using natural language:
- **/git-ops**: "I'm done with the landing page, please save my changes and upload them to GitHub."
- **/execute-issue**: "Implement the new login button as described in issue #12."
- **/deploy**: "Everything looks good, let's deploy this to staging."

### Why this works
AI-POS turns code-level files (`workflows/*.md`) into executable instructions for the AI. You focus on the **strategic intent**, and the AI handles the **technical execution**.

---

## 📊 Example Workflow

1. **Input**: "I want to add a referral system."
2. **Step 1**: Run `/validate-idea`. **Output**: Strategic rating and risks.
3. **Step 2**: Run `/create-prd`. **Output**: Full requirement doc with user stories.
4. **Step 3**: Run `/system-design`. **Output**: Technical blueprint and data schema.
5. **Step 4**: Run `/implementation-plan`. **Output**: Step-by-step milestones.

---

## 📈 Recommended Starting Path

1. **Explore the Problem**: Start with `workflows/explore-problem.md` to validate the "Why."
2. **Define the ICP**: Use `workflows/define-icp.md` to nail your target user.
3. **Validate the Idea**: Run `workflows/validate-idea.md` to check strategic fit.
4. **Specify**: Run `workflows/create-prd.md`.

---

## 💡 Why AI-POS is Different

- **Context First**: Most AI prompts are generic. AI-POS forces the AI to respect your specific product constraints and goals.
- **Role-Based**: It doesn't just "write code"; it thinks like a Strategist, then a Designer, then an Engineer.
- **Tool Agnostic**: Works in any IDE, any terminal, or any chat window.

---

## 🧩 Extensibility

Need a custom process?
1. Create a new `.md` file in `workflows/`.
2. Link it to an existing role in `roles/`.
3. Add it to your project.

---

## 📄 License
MIT

---

## 🤝 Contributing
See `CONTRIBUTING.md` for details on how to add new roles or workflows.
