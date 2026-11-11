# Source-Based Study

English | [Português](README.pt-BR.md)

A claude.ai project instruction that makes Claude ask you questions about a source, one concept at a time, instead of explaining it to you.

Send a link, pasted text, a file, or an idea. Claude lists the concepts in the source and tests you on each one with eight learning techniques.

## Why use it instead of "teach me X"

When you ask Claude to teach a topic, Claude writes an explanation and you read it. Reading feels like learning, but you do not test your memory.

This instruction changes the order:

- You answer a question before you read the explanation.
- Claude explains only what your answer showed that you do not know.
- Claude gives the correct answer and names your specific error after every answer.
- Claude does not praise your answers and does not lecture.

The trade-off: a session is slower than reading a summary. If you need a fast overview, ask for a summary instead.

## Example

This example is illustrative. Claude replies in the voice format: short messages, one question each.

> **Claude:** I read the source. It has 3 concepts: 1. Principal and rate. 2. Compounding. 3. The rule of 72. Before I explain concept 1, what do you think "principal" means in a loan?
>
> **You:** The interest?
>
> **Claude:** Not exactly. Outside the source, the principal is the original amount of money, before any interest. Interest is the cost that Claude adds on top. In your own words, how does the interest rate relate to the principal?

## Use it

1. Open claude.ai and create a new project.
2. Copy the content of `instructions.md` (on macOS, run the command below).
3. Paste it into the project instructions.
4. Open a new chat in the project and send your source.
5. Answer the first question.

```bash
pbcopy < instructions.md
```

> **Tip:** use voice mode when you can. You answer by speaking, which uses the production effect. A review found that producing items by saying, writing, or typing them can improve some forms of long-term memory compared with silent reading ([MacLeod and Bodner, 2017](https://uwaterloo.ca/memory-attention-cognition-lab/sites/default/files/uploads/files/macleodbodner_cdps17_0.pdf)).

Accepted sources: a public link, pasted text, a PDF or other file, or an idea without a source. For an idea, Claude finds a source on the web and shows you the link first.

## How a session works

Claude repeats these steps for each concept. Claude gives the correct answer and your specific error after every answer (step 6).

| Step | What you do | Technique |
|---|---|---|
| 1 | Answer 1 or 2 questions before any explanation. | [Pretest](https://pubmed.ncbi.nlm.nih.gov/37640836/) |
| 2 | Read a complete solution, step by step. Claude shows this only for calculations and procedures without code. | [Worked example](https://link.springer.com/article/10.1007/s10648-023-09745-1) |
| 3 | Explain in your own words how the concept works. | [Self-explanation](https://link.springer.com/article/10.1007/s10648-018-9434-x) |
| 4 | Explain why the concept is true. | [Elaborative interrogation](https://www.uwlax.edu/catl/guides/teaching-improvement-guide/how-can-i-improve/elaborative-interrogation/) |
| 5 | Answer 2 or 3 new questions without the source. | [Retrieval practice](https://eric.ed.gov/?id=EJ1141817) |
| 6 | Get the correct answer and the specific error after each answer. | [Feedback](https://www.frontiersin.org/articles/10.3389/fpsyg.2019.03087/full) |
| 7 | Explain the full concept to a beginner. | [Learning by teaching](https://onlinelibrary.wiley.com/doi/10.1111/jpr.12221) |
| 8 | At the end, answer mixed questions from all concepts. | [Interleaved practice](https://www.psychologie.uni-wuerzburg.de/fileadmin/06020400/2019/Brunmair_Richter_in_press__2019_META-ANALYSIS_OF_INTERLEAVED_LEARNING.pdf) |

After the last concept, Claude asks at least one open question per concept in mixed order (steps 5 and 8), then says that the session is complete. If you leave and return, Claude continues with the next concept that is not complete.

## Limits

- Claude cannot read private links or pages that need a login. Paste the text in these cases.
- The instruction does not schedule reviews. It does not suggest spaced review. Track your reviews outside the project.
- Claude uses only facts from the source or from the web. When Claude has no source for a fact, it says so.
- No evaluation compares sessions with this instruction to other ways of studying. The research above covers each technique, not this combination.

## Change the instruction

1. Edit `instructions.md`.
2. Test it with a short source.
3. Check that each message in the practice phase ends with exactly one question and has no more than 4 sentences before it.
