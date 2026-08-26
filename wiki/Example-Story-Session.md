# Example: TeachMe for Story Improvement

This page shows a complete example of how TeachMe uses the Rung Teaching System in an ordinary conversation.

The purpose is not to prescribe one fixed writing lesson. It demonstrates the **interaction pattern**:

```text
learner names a broad goal
→ supplies the work
→ teacher reads it
→ optional Interview Mode narrows the target
→ one question leads to the next
→ a concrete skill emerges
→ learner attempts
→ teacher diagnoses
→ minimum help
→ learner retries
→ transfer test
```

---

# 1. Start with a normal request

The learner does not need to know Rung terminology.

```text
/teachme improve my story
[story attached]
```

The teacher should read the supplied story before diagnosing the learning target.

“Improve my story” is too broad to define one obvious skill. It could mean structure, pacing, prose, characterization, tension, scene construction, dialogue, or something else.

TeachMe can either choose the strongest learning target it can diagnose from the work or use **Interview Mode**.

A reasonable response is:

> I’ve read the story. “Improve my story” could lead in several useful directions. I can either choose the strongest learning target I see and start there, or interview you one question at a time so the target is based on what you want the story to accomplish. Which do you want?

Learner:

> Interview me first.

---

# 2. Interview Mode

Interview Mode is deliberately conversational.

It should **not** ask ten setup questions at once.

Each question uses the learner's previous answer to decide what matters next.

TeachMe:

> At the end of this scene, what do you most want the reader to understand or feel about Mara?

Learner:

> I want them to feel that she desperately wants to leave, but she is afraid that leaving means abandoning her brother.

TeachMe:

> Where in the current scene do you think the reader can most clearly see both halves of that conflict?

Learner:

> Probably when she picks up the car keys and then puts them back.

TeachMe:

> What in that moment tells the reader that her hesitation is specifically about her brother rather than just general fear or indecision?

Learner:

> Actually, nothing. I know that is why she is doing it, but I don’t think the reader does.

The teacher now has enough information. The interview should stop.

Continuing to ask background questions would add friction without improving the teaching decision.

---

# 3. Convert the broad goal into a skill

TeachMe:

> That gives us the first skill to work on: **making a character’s internal conflict legible through concrete scene details instead of relying on information that exists only in the writer’s head.**
>
> I’m not going to rewrite the scene for you. Let’s use the keys moment as the first attempt.

This is an important Rung move.

The project is still “the story,” but the learning target is now a reusable writing judgment.

---

# 4. First diagnostic attempt

TeachMe:

> Without adding an explanatory paragraph, what could Mara notice, touch, avoid, or react to that would connect putting the keys down specifically to her brother?

Learner:

> Maybe his school bag is sitting next to the door, and when she reaches for the keys she sees it.

TeachMe:

> Why is the school bag stronger than simply having her think, “I can’t leave him”?

Learner:

> Because the bag makes the brother physically present in the scene without explaining what she feels.

The teacher is not just checking whether the learner found a usable detail. It is testing whether they understand **why** it works.

---

# 5. Learner performs the revision

TeachMe:

> Write only that beat—two to four sentences. Keep the same basic action: she reaches for the keys and decides not to take them.

Learner:

> Mara hooked one finger through the key ring. Her brother’s backpack leaned against the door beneath his raincoat, one strap still twisted from where he had dropped it. She held the keys for another second, then set them back in the bowl.

The learner has now acted on the principle.

---

# 6. Diagnose the revision

TeachMe should not immediately rewrite the paragraph into a “better” version.

Instead it can ask:

> Which detail in your revision is doing the actual emotional work, and which detail might only be decoration?

Suppose the learner answers:

> The backpack is doing the work. The raincoat might just be extra description.

TeachMe can then test the reasoning:

> What makes the backpack connected to her decision in a way the raincoat is not yet connected?

The next intervention depends on the answer.

If the learner understands the distinction, continue with lighter support.

If the learner lacks a concept such as **concrete detail**, **subtext**, or **motivated action**, TeachMe should move up the Assistance Ladder, explain the minimum missing concept, and return the work to the learner.

---

# 7. Reattempt

The learner revises again using what they have learned.

TeachMe verifies the specific criterion that previously failed rather than simply saying the new version “feels better.”

For example:

> The revision now gives the hesitation a visible connection to the brother. Before we move on, state the test you could use on another scene to catch this problem yourself.

Learner:

> If I know why a character is hesitating, I should check whether the reader can point to anything in the actual scene that reveals that reason.

That may become a candidate standing principle.

---

# 8. Transfer

The original story cannot be the final proof because the learner has been coached through it.

TeachMe changes the surface details while preserving the principle:

> New situation: a character wants to accept a job overseas but feels responsible for an aging parent. Without directly stating the conflict in internal narration, sketch one small action or environmental detail that could make both pressures visible.

Now the learner has to recognize the underlying problem without being told “use the backpack trick.”

If they can do that and explain why their choice works, there is stronger evidence of transfer.

---

# 9. Fade assistance

Across later examples, TeachMe should gradually move from:

```text
“What could she notice?”
```

through:

```text
“What is missing from the scene?”
```

toward:

```text
“Diagnose this beat.”
```

and eventually simply audit the learner's independent judgment.

The target progression is:

```text
teacher carries reasoning
→ shared reasoning
→ learner carries reasoning
→ teacher audits
→ learner works independently
```

---

# 10. What Interview Mode is for

Interview Mode is especially useful when the request is broad and subjective:

```text
Teach me how to improve my story.
Teach me how to become a better writer.
Teach me how to improve this design.
Teach me how to make this presentation better.
```

The interview identifies **what the learner is trying to accomplish** before choosing the skill to practice.

It follows:

```text
question
→ answer
→ next question selected from that answer
→ enough evidence to define the target
→ stop interviewing
```

It is not intended for a skill that is already specific enough to test directly.

For example:

```text
/teachme how to tell whether a character's choice is motivated.
```

should normally proceed directly to a small diagnostic attempt rather than asking the learner to choose an interaction style first.

---

# The full example in one diagram

```text
/teachme how to improve my story
                 ↓
          story is supplied
                 ↓
         TeachMe reads it
                 ↓
      goal is still too broad
                 ↓
          INTERVIEW MODE
                 ↓
        one question at a time
                 ↓
      intended effect becomes clear
                 ↓
       concrete weakness appears
                 ↓
       define reusable skill
                 ↓
          learner attempts
                 ↓
        diagnose reasoning
                 ↓
       minimum useful help
                 ↓
          learner revises
                 ↓
       learner explains why
                 ↓
          changed example
                 ↓
          assistance fades
                 ↓
           independence
```

That is what Rung is supposed to feel like in use: **a conversation in which each teacher move is chosen from evidence produced by the learner's previous move.**

---

## Related pages

- [[Set Up and Use]]
- [[Teaching Loop]]
- [[Assistance Ladder]]
- [[Diagnosing Mistakes]]
- [[Mastery and Transfer]]
- [[TeachMe Agent Skill|Agent-Skills]]
