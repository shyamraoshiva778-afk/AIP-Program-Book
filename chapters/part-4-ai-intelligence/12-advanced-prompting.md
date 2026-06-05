# Day 12: Advanced Prompting — Becoming a Prompt Pro

> **"The quality of your prompts determines the quality of your AI's responses."**
> — AIP Principle

---

## 🧠 Learning Objectives

By the end of this chapter, you will be able to:

- [ ] Use chain-of-thought prompting for complex problems
- [ ] Create multi-step prompts for complex academic tasks
- [ ] Control AI output format precisely
- [ ] Use iterative prompting to refine answers
- [ ] Design your own advanced prompt templates
- [ ] Combine multiple techniques for powerful results

---

## 📖 Chapter Content

### 12.1 What is Advanced Prompting?

On Day 3, you learned the basics: Role + Context + Task.

**Advanced prompting** is about:
- Handling COMPLEX tasks (not just simple Q&A)
- Getting EXACTLY the output you want
- Making AI reason step by step
- Combining multiple requests in one prompt
- Refining results through conversation

Think of it like this:

```
Beginner: "Explain photosynthesis."
                          ↓
Intermediate: "Act as a biology teacher. Explain photosynthesis to class 9."
                          ↓
Advanced: "Act as a biology teacher. Explain photosynthesis step by step.
           Include the equation, where it happens, and why it matters.
           Then give me 5 practice questions. Format as a study guide."
                          ↓
Expert: [Creates their own custom prompt system for any topic]
```

Today, you become the Expert.

### 12.2 Technique 1: Chain of Thought (CoT)

**Chain of Thought** means asking AI to "think step by step." This produces much better results for complex tasks.

#### Without Chain of Thought:
```
You: What is 15% of 80?
AI: 12.
(You don't know HOW AI got that answer)
```

#### With Chain of Thought:

📱 **COPY THIS INTO YOUR AI CHAT:**
```
You: What is 15% of 80? Let's think step by step.
AI: 
Step 1: 10% of 80 = 8
Step 2: 5% of 80 = 4 (half of 10%)
Step 3: 15% = 10% + 5% = 8 + 4 = 12
Answer: 12
(You can see the reasoning AND learn the method!)
```

#### CoT Prompt Template:

```
Solve this problem step by step:

[Your problem]

For each step, explain:
1. What you are doing
2. Why you are doing it
3. The result of this step

Then give the final answer.
```

#### When to Use CoT:
- Math problems
- Complex reasoning questions
- Essay planning
- Analysis tasks
- Any multi-step problem

### 12.3 Technique 2: Multi-Step Prompts

A multi-step prompt combines several requests in ONE message.

#### Before (Multiple Messages):
```
You: Give me a summary of the water cycle.
AI: [Summary]
You: Now give me 10 questions on it.
AI: [Questions]
You: Now create flashcards.
AI: [Flashcards]
```

#### After (ONE Powerful Prompt):
```
You: I am studying the water cycle. Please do ALL of the following:

Step 1: Give me a one-paragraph summary of the water cycle
Step 2: List the 5 most important terms with definitions
Step 3: Create 10 practice questions (5 easy, 3 medium, 2 hard)
Step 4: Create 10 flashcards in Q&A format
Step 5: Suggest 3 common exam mistakes on this topic

Format each step clearly with headings.
```

**Result:** You get a COMPLETE study package in one response!

#### Multi-Step Template:

```
📱 TYPE THIS INTO YOUR AI CHAT:
─────────────────────────────────
I am studying [Topic]. Complete ALL these steps:

Step 1: [First task]
Step 2: [Second task]
Step 3: [Third task]
Step 4: [Fourth task]

Format rules:
- Label each step clearly
- Use bullet points for lists
- Keep each section concise
─────────────────────────────────
```

### 12.4 Technique 3: Format Control

You can tell AI EXACTLY how to format the output.

#### Table Format:
```
Create a comparison table with this exact format:

| Feature | [Topic A] | [Topic B] |
|---------|-----------|-----------|
| Definition | | |
| Key Points | | |
| Examples | | |
| Advantages | | |
| Disadvantages | | |

Use markdown table format.
```

#### JSON Format (for copying to apps):
```
List the key concepts of [Topic] in JSON format:

{
  "topic": "[Topic]",
  "concepts": [
    {
      "name": "Concept 1",
      "definition": "...",
      "importance": "high/medium/low"
    },
    ...
  ]
}
```

#### Bullet Point Format:
```
Summarize [Topic] using only bullet points.
Rules:
- Maximum 7 bullets
- Each bullet = maximum 15 words
- First word of each bullet = action verb
- No full sentences, use fragments
```

#### Flashcard Format:
```
Create 10 flashcards in this exact format:

---
Question: [Question 1]
Answer: [Answer 1]
---

---
Question: [Question 2]
Answer: [Answer 2]
---
```

### 12.5 Technique 4: The "Persona System"

Instead of ONE role, create a SYSTEM of roles that work together:

```
I want you to play THREE roles in this conversation:

Role 1: TEACHER — Explain concepts simply and clearly
Role 2: EXAMINER — Test my understanding with questions
Role 3: COACH — Give me feedback and encouragement

For this topic [Topic], cycle through these roles:

Phase 1 (Teacher): Explain the topic in 5 minutes
Phase 2 (Examiner): Ask me 3 questions
Phase 3 (Coach): Give me feedback on my answers

Switch roles when I say "Next role."
```

### 12.6 Technique 5: Constraint Prompting

Add constraints to get more focused answers:

```
Explain [Topic] with these constraints:

✅ DO:
- Use simple language (Class 8 level)
- Give 2 real-life examples
- Keep it under 300 words
- End with a one-sentence summary

❌ DO NOT:
- Use technical jargon without explanation
- Include unnecessary details
- Assume prior knowledge
- Use complex sentences

Format as: Explanation → Examples → Summary
```

### 12.7 Technique 6: The "Teach Me" Progression

This technique takes you from beginner to expert in one conversation:

```
I am a complete beginner on [Topic]. Take me through
a 4-stage learning progression:

Stage 1: "The Basics" (What EVERYONE should know)
Stage 2: "Core Understanding" (What good students know)
Stage 3: "Deep Dive" (What excellent students know)
Stage 4: "Expert Level" (What enthusiasts/researchers know)

For each stage:
1. Give me the key information
2. Ask if I have questions
3. Give me 2-3 practice problems
4. Move to next stage only when I say "Ready"

Start with Stage 1.
```

### 12.8 Technique 7: Prompt Chaining

Prompt chaining means using the OUTPUT of one prompt as the INPUT for the next.

**Example: Essay Writing Chain**

```
LINK 1: Generate Ideas
"I need to write an essay on [Topic]. Give me 5 possible thesis statements."

LINK 2: Choose & Develop
"I choose thesis #3. Help me create an outline with:
- Introduction points
- 3 body paragraph topics
- Conclusion points"

LINK 3: Write Section
"Using the outline, write the introduction paragraph for my essay."

LINK 4: Expand
"Now write body paragraph 1 based on the outline."

LINK 5: Review & Refine
"Here is my completed essay draft. Review it and suggest 3 improvements."
```

### 12.9 Technique 8: Negative Prompting (What NOT to Do)

Tell AI what to AVOID:

```
Analyze this topic [Topic]. 

POSITIVE instructions (what to include):
- Key facts and figures
- Important dates/people
- Real-world applications

NEGATIVE instructions (what to exclude):
- Do NOT include opinions
- Do NOT speculate
- Do NOT oversimplify complex ideas
- Do NOT use vague language like "it is believed"
```

### 12.10 Creating Your Prompt Template Library

Advanced users create TEMPLATES they reuse:

#### Template 1: Complete Chapter Study Kit
```
Create a complete study kit for [Chapter] from [Subject]:

1. One-page summary
2. 20 flashcards
3. 15 practice questions (5 easy, 5 medium, 5 hard)
4. 3 memory tricks/mnemonics
5. Common mistakes section
6. Quick revision checklist

Format everything in clear sections with emoji headers.
```

#### Template 2: Exam Preparation System
```
I have [X] days until my [Subject] exam.
Chapters to cover: [List]

Create a preparation system:

1. PRIORITY LIST: Rank chapters by exam importance (use marks weightage)
2. DAY-BY-DAY SCHEDULE: What to study each day
3. REVISION PLAN: When to revise each chapter
4. PRACTICE TESTS: When to take mock tests
5. WEAK SPOT FIX: How to identify and fix weak areas
```

#### Template 3: Research Deep Dive
```
I want to deeply research [Topic]. Guide me through:

Day 1: Overview & key concepts
Day 2: History & development
Day 3: Current state & applications
Day 4: Debates & controversies
Day 5: Future possibilities

For each day, give me:
- What to learn (3-5 key points)
- Questions to think about (2-3)
- Something surprising or counterintuitive (1)
```

### 12.11 The Master Prompt Builder

Here is a system to build YOUR OWN advanced prompts:

```
STEP 1: GOAL
├── What do I want? (Summarize? Analyze? Create? Practice?)
└── Example: "I need to create revision notes for a chapter"

STEP 2: ROLE
├── Who should AI be?
└── Example: "Act as my revision guide creator"

STEP 3: CONTEXT
├── What does AI need to know about me?
└── Example: "I am in class 9, this is Science chapter 5"

STEP 4: TASKS
├── What exactly should AI do? (List all steps)
└── Example: "1. Summarize, 2. Create flashcards, 3. Make questions"

STEP 5: FORMAT
├── How should the output look?
└── Example: "Use headings, bullet points, and tables"

STEP 6: CONSTRAINTS
├── Any rules or limits?
└── Example: "Maximum 500 words, class 8 level language"

STEP 7: VERIFICATION
├── How should AI check its work?
└── Example: "After answering, list any assumptions you made"
```

---

## ✋ Practical Activity

### Activity 1: Compare Beginner vs Advanced Prompts

Take ONE topic. Try each prompt type and compare:

| Prompt Type | Your Prompt | AI's Response Quality |
|-------------|-------------|----------------------|
| Basic (no RCT) | "Tell me about [topic]" | |
| Intermediate (RCT) | Role + Context + Task | |
| Advanced (Multi-step + Format) | Multi-step with format control | |
| Expert (Chain + Constraints) | Full system prompt | |

**Which level gave the best result? What was the difference?**

### Activity 2: Build Your Prompt Library

Create 3 prompt templates you will use regularly:

1. **For understanding concepts** (Day 12.10 Template 1 modified)
2. **For exam preparation** (Day 12.10 Template 2 modified)
3. **For your own custom need** (Think of a specific task you do often)

Save these templates — you will use them forever!

---

## 📝 For Your Category

### 🟢 For Pass & Improve Students
> **Task:** Use the "Teach Me" Progression (Technique 6) for a topic you find difficult. Start at Stage 1 and go as far as you can. Even Stage 1 will help you understand better!

### 🔵 For High Scorers
> **Task:** Use the "Complete Chapter Study Kit" template (Template 1) for your next exam chapter. Use everything it generates — summary, flashcards, questions, mnemonics. Track if your performance improves.

### 🟣 For Deep Learners
> **Task:** Use the "Research Deep Dive" template (Template 3) for a topic that fascinates you. Complete all 5 days. Write a one-page "research paper" at the end summarizing what you discovered.

---

## ⚡ Chapter Summary

- **Chain of Thought (CoT):** Ask AI to "think step by step" for better reasoning
- **Multi-Step Prompts:** Combine multiple requests in ONE prompt
- **Format Control:** Tell AI EXACTLY how to format output (tables, JSON, bullets)
- **Persona System:** Use multiple AI roles in one conversation
- **Constraint Prompting:** Set rules for what AI should and should not do
- **Teach Me Progression:** Go from beginner to expert level
- **Prompt Chaining:** Use output of one prompt as input for next
- **Negative Prompting:** Tell AI what to avoid
- **Build a Prompt Template Library** for different tasks
- Use the **Master Prompt Builder** to design your own prompts

---

## 🎯 Key Takeaways

```text
✅ Chain of Thought = Better reasoning from AI
✅ Multi-step prompts = Complete study packages in one go
✅ Format control = Get exactly what you want
✅ Constraints = Focused, high-quality answers
✅ Build templates = Save time, get consistent results
✅ You are now a Prompt Pro!
```

---

## 🎒 Homework / Practice Task

1. **Rewrite your 3 most common prompts** using advanced techniques
2. **Create a "Prompt Library" document** with your best templates
3. **Test the "Teach Me" progression** on a friend — teach them using AI-generated stages
4. **Share one advanced prompt template** with a classmate

---

## 💡 Daily Reflection Prompt

> **"What is ONE task you do repeatedly with AI? How can you create a template to do it better and faster?"**

---

## 📌 Instructor Notes

- This chapter is the culmination of all prompting skills learned so far
- Advanced prompting is what separates "AI users" from "AI power users"
- Emphasize the efficiency gain — one multi-step prompt saves 10 messages
- Have students share their best templates with the class
- The "Prompt Library" concept is valuable — encourage students to build theirs

---

*© 2026 Kabali Gamer. All rights reserved. Made for students, by Kabali Gamer.*

**Congratulations! You have completed Day 12.**
**Tomorrow: AI Ethics & Safety!** 🚀
