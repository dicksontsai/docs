---
name: pop-quiz-generator
description: Generate pop quiz blog posts that test practical engineering knowledge with thoughtful questions and substantive answers for an advanced technical audience
---

# Pop Quiz Blog Post Generator

## Purpose

Generate interactive pop quiz blog posts that challenge readers' practical software engineering knowledge. These quizzes distill engineering experience into an informative and entertaining format that reveals knowledge gaps and reinforces critical concepts.

## When to Use

- Creating a new pop quiz blog post on any software engineering topic
- Testing reader understanding of advanced concepts beyond basic definitions
- Packaging practical engineering wisdom into an engaging format

## Core Principles

**Target Audience**: Slightly more advanced technical readers who already know the basics

**Quality Standards**:
- Avoid stating obvious facts or textbook definitions
- Focus on practical scenarios, edge cases, and nuanced understanding
- Test synthesis and application of knowledge, not just recall
- Questions should reveal gaps that even experienced engineers might have
- Answers should provide actionable insights and deeper understanding

## Format Structure

### 1. Introduction (2-3 paragraphs)
- Brief context explaining why this topic matters
- Hook that relates to the reader's experience (e.g., AI tools, common challenges)
- Clear statement that this is a pop quiz to discover knowledge gaps

**Tone**: Conversational but technical. Assume reader competence while acknowledging gaps exist.

### 2. Quiz Section (4-5 Questions)

Each question should:
- Test practical understanding, not memorization
- Include a helpful hint in parentheses that guides without revealing the answer
- Focus on WHY or HOW, not just WHAT
- Explore edge cases, trade-offs, or common pitfalls
- Be answerable but non-trivial

**Format**:
```
**Question N**: [Question text]? (Hint: [Guiding principle or context].)
```

**Examples of GOOD questions**:
- "Why do applications with global state present challenges for testing?" (tests understanding of consequences)
- "At what point do mocks become a liability rather than an asset?" (tests nuanced trade-offs)

**Examples of BAD questions** (too basic):
- "What is unit testing?" (definition-based, too obvious)
- "Should you write tests?" (yes/no, no depth)

### 3. Separator

```
---
```

### 4. Answers Section

For each answer:

1. **Concise Summary** (1 line) - Direct answer or key concept
2. **Detailed Explanation** - Why it matters, how it works, what goes wrong
3. **Examples or Specifics** - Concrete scenarios, code patterns, or common cases
4. **Depth Elements** - Edge cases, paradoxes, or counterintuitive insights
5. **Actionable Takeaway** (when relevant) - What to do with this knowledge

**Format**:
```
### Q1: [Question Topic]

[One-line summary/direct answer]

[Detailed explanation paragraph(s)]

[Lists, examples, or specific cases]

[Edge cases, warnings, or deeper insights]
```

**Quality Markers**:
- Answers should teach, not just validate
- Use lists to enumerate multiple causes, factors, or specific examples (e.g., "Common Causes: Race conditions, time dependencies, shared state...")
- Explain the "so what" - why this matters in practice
- Avoid fluff - the quiz is a standalone blog post and should be highest quality writing where every sentence adds value

## Content Guidelines

### What Makes Great Questions

1. **Practical Scenarios**: "Your test suite shows green but users encounter bugs. What are the blind spots?"
2. **Trade-off Analysis**: "When do mocks become a liability?"
3. **Paradoxes**: "AI generates 100% coverage. What failures might still lurk?"
4. **Root Causes**: "Why do [X] present challenges for [Y]?"
5. **Common Pitfalls**: "What factors cause [common problem]?"

### What Makes Great Answers

1. **Challenge Assumptions**: Coverage ≠ Correctness
2. **Provide Frameworks**: FIRST acronym for test design
3. **Call Out AI Limitations**: "AIs may optimize for passing, not correctness"
4. **Reveal Non-Obvious Truths**: Edge cases that catch people

## Integration with Blog

**File Location**: Create the MDX file at `blog/software-development/pop-quiz-{topic-slug}.mdx`
- Slug: Lowercase, hyphenated (e.g., `pop-quiz-software-testing`)

**Metadata**: Include frontmatter with title and description:
```yaml
---
title: 'Pop Quiz: {Topic Name}'
description: 'A pop quiz exploring {topic} concepts including {concept 1}, {concept 2}, {concept 3}, and {concept N}'
---
```

**Update Entries**: Follow the process in CLAUDE.md for adding Update entries to both topic and quarterly all-posts files

## Example Workflow

**User request**: "Create a pop quiz on software testing"

**Steps**:
1. Identify 4-5 key concepts worth testing (global state, flaky tests, coverage, etc.)
2. Craft questions that test understanding of WHY and HOW, not WHAT
3. Write introduction that connects to reader's context
4. Write substantive answers with examples and edge cases
5. Create MDX file: `blog/software-development/pop-quiz-software-testing.mdx`
6. Add Update entries to both all-posts files
7. Commit with descriptive message
