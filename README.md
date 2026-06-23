# (SCTP) Advanced Professional Certificate in Data Science and AI - Technical Assessment

This is the technical entry assessment for the **(SCTP) Advanced Professional Certificate in Data Science and AI** programme.

---

**TL;DR:** Fork this repo, answer the questions in `src/`, push your changes, then submit your fork URL on the NTU Survey Portal. 

---

> 🪟 **Windows Users**
> You will need WSL or Ubuntu installed to answer Q2 and Q3. See [**`SETUP-WINDOWS.md`**](./SETUP-WINDOWS.md) for the full guide. macOS and Linux users can skip this; you already have a Unix shell built in.


### About this Assessment

The assessment is designed to give us a picture of your current technical baseline. We are looking for evidence that you can read carefully, attempt unfamiliar problems independently, and are willing to learn.

Take as much time as you need to complete the assessment. You are encouraged to use the reference resources listed below before and during the assessment.

### What We Expect From You

- **Attempt every question.** A partial answer with clear reasoning is more useful to us than a blank.
- **Use the references.** Looking things up is not cheating. It is how professionals work. The references section below is curated to help you.
- **Write your own answers.** AI assistance (e.g. ChatGPT) is permitted, but you are solely responsible for understanding everything you submit. You should be able to explain any answer in your own words.
- **Be honest about what you don't know.** If you are unsure, say so and explain your best understanding. We value intellectual honesty.
- **Don't get stuck.** If a question is unclear or unfamiliar, make your best attempt and move on. You can always come back to it.

### Please attempt all 9 questions in the `src/` folder:

- [Question 1 — Multiple Choice: Core Concepts](./src/q1.md) *(MCQ, 15 parts)*
- [Question 2 — Python & Environment Setup](./src/q2.md) *(Paste real terminal output + short answer)*
- [Question 3 — Your Operating System and Shell](./src/q3.md) *(Paste real terminal output + short answer)*
- [Question 4 — CLI: Navigation and Predicting Output](./src/q4.md) *(Commands + predict output)*
- [Question 5 — Operating Systems, Terminals, and Shells](./src/q5.md) *(Short answer)*
- [Question 6 — AI Literacy: Prompt Engineering](./src/q6.md) *(Short answer + rewrite)*
- [Question 7 — Python: Read and Predict Output](./src/q7.py) *(Predict + short answer)*
- [Question 8 — Python: Find and Fix the Bug](./src/q8.py) *(Code)*
- [Question 9 — GitHub: Git Workflow](./src/q9.py) *(Commands + short answer)*

**`.md` files** (Q1 to Q6): open in any text editor or view directly on GitHub, then fill in your answers where indicated.  
**`.py` files** (Q7 to Q9): open in a code editor or IDE and write your code where indicated.

Your code should be readable and include brief comments where relevant.

<details>
<summary><strong>💾 Submission Instructions</strong></summary>

The submission process is itself part of the assessment. Setting up Git, forking a repository, and pushing your work to GitHub are foundational skills you will use throughout the SCTP programme. If you have not done this before, use the steps and resources below to figure it out. That is exactly the kind of self-directed learning this programme is built on.

You will need a GitHub account to submit. If you do not have one, create one first at https://github.com/

### Step-by-step

**Step 1: Create a GitHub account**  
If you don't already have one, sign up at https://github.com/

**Step 2: Fork this repository**  
Click the **Fork** button at the top-right of this page. This creates your own copy of the repo under your GitHub account, so you can edit it freely without affecting the original.

> 💡 Not sure what forking means? Read: [GitHub Docs — Fork a repository](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo)

**Step 3: Clone your fork to your computer**  
Open your terminal and run:

```bash
git clone https://github.com/<your-username>/5m-data-entry-test.git
```

Replace `<your-username>` with your actual GitHub username. This downloads your forked repo so you can work on the files locally.

> 💡 New to `git clone`? Read: [GitHub Docs — Cloning a repository](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository)

**Step 4: Complete the assessment**  
Work through the questions in the `src/` folder. Edit the `.md` and `.py` files directly on your computer.

**Step 5: Push your answers back to GitHub**  
Once you're done, stage, commit, and push your changes:

```bash
git add .
git commit -m "Complete entry assessment"
git push origin main
```

> 💡 New to these commands? Read: [W3Schools Git Tutorial](https://www.w3schools.com/git/) or watch [Git and GitHub for Beginners — freeCodeCamp (video)](https://youtu.be/RGOj5yH7evk)

**Step 6: Submit your repository link**  
Copy the URL of your forked repository (e.g. `https://github.com/<your-username>/5m-data-entry-test`) and submit it on the NTU Survey Portal.
</details>

<details>
<summary><strong>🆘 Troubleshooting</strong></summary>

If you get stuck at any step, these resources can help:

| Problem | Resource |
|---------|----------|
| Setting up Git on your computer | [GitHub Docs — Set up Git](https://docs.github.com/en/get-started/getting-started-with-git/set-up-git) |
| Understanding fork vs. clone | [GitHub Docs — Fork a repo](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo) |
| Pushing changes fails | [GitHub Docs — Pushing commits](https://docs.github.com/en/get-started/using-git/pushing-commits-to-a-remote-repository) |
| General Git reference | [W3Schools Git Tutorial](https://www.w3schools.com/git/) |

> **The ability to self-learn is a core part of the SCTP programme.** Working through the submission process, including any troubleshooting you encounter, is itself a demonstration of the skills you will build on this course. Use the resources above, search for answers, and persist through the friction. That is exactly the mindset we are looking for.

</details>

<details>
<summary><strong>📚 References</strong></summary>

### Python *(Q1 parts, Q2, Q7, Q8)*
- [Variables and Naming Conventions](https://www.w3schools.com/python/gloss_python_variable_names.asp)
- [Data Types](https://www.w3schools.com/python/python_datatypes.asp)
- [For Loops](https://www.w3schools.com/python/python_for_loops.asp)
- [Functions](https://www.w3schools.com/python/python_functions.asp)
- [Python Modules](https://www.w3schools.com/python/python_modules.asp)
- [Installing Miniconda — Anaconda Docs](https://www.anaconda.com/docs/getting-started/miniconda/main) *(install this if `conda` is not yet on your machine; needed for Q2)*
- [Managing Conda Environments — Conda Docs](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html)
- [python-dotenv — Loading `.env` files](https://pypi.org/project/python-dotenv/)
- [Python with Mosh (video)](https://youtu.be/kqtD5dpn9C8)

### Command Line Interface *(Q1 parts, Q4)*
- [Command Line Crash Course (video)](https://youtu.be/uwAqEzhyjtw)
- [Linux Command Line Basics — freeCodeCamp](https://www.freecodecamp.org/news/the-linux-commands-handbook/)

### Git and GitHub *(Q1 parts, Q9)*
- [W3Schools Git Tutorial](https://www.w3schools.com/git/)
- [GitHub Docs: Getting Started](https://docs.github.com/en/get-started)
- [About Git — GitHub Docs](https://docs.github.com/en/get-started/using-git/about-git)

### Operating Systems, Terminals, and Shells *(Q1 parts, Q3, Q5)*

Refer to the entry for your OS, plus the general terminal/shell reference.

- [Understanding Terminal, Console, Shell and Kernel — GeeksforGeeks](https://www.geeksforgeeks.org/operating-systems/what-is-terminal-console-shell-and-kernel/)
- [Open or quit Terminal on Mac — Apple Support](https://support.apple.com/en-sg/guide/terminal/apd5265185d-f365-44cb-8b09-71a064a42125/mac)
- [The Linux Commands Handbook — freeCodeCamp](https://www.freecodecamp.org/news/the-linux-commands-handbook/)
- [What is PowerShell — Microsoft Docs](https://learn.microsoft.com/en-us/powershell/scripting/)

### AI Literacy and Prompt Engineering *(Q6)*
- [Prompt Engineering Guide — OpenAI](https://platform.openai.com/docs/guides/prompt-engineering)
- [Introduction to Prompt Engineering — LearnPrompting.org](https://learnprompting.org/docs/intro)

</details>

### 📝 Use of Generative AI Tools

The use of AI tools (e.g. ChatGPT, GitHub Copilot, Claude) is permitted for this assessment.

However, the following conditions apply:

**You are the author of your submission.** Any AI-generated content that you include in your answers is considered your own work. You are fully responsible for its accuracy, relevance, and integrity, just as you would be for work you wrote yourself.

**You must be able to explain what you submit.** If you are accepted into the programme, you may be asked to walk through your answers during an introductory session. Submitting AI-generated responses you do not understand is a risk to yourself, and not just a breach of academic integrity.

**AI tools are not a substitute for learning.** Using AI to generate answers without engaging with the underlying concepts will leave you underprepared for the programme. The assessment is designed to surface your starting point so instructors can support you, not to catch you out.

> This policy is consistent with industry practice. In professional data and AI roles, engineers and analysts routinely use AI tools, but are held accountable for the outputs they ship. Developing the habit of understanding, verifying, and owning AI-assisted work is itself a core competency this programme will develop.
