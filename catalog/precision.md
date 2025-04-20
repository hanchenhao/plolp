# Precision

*Always use precise language. Give clear instructions. Refer to entities without ambiguity.*

## Motivation

Imprecise prompts can easily cause an LLM to misunderstand what you really want. If your wording is vague or if you refer to the same thing by different names, the model can get confused. Any ambiguity or lack of clarity often results in answers that are off-target or contain mistakes, because the AI ends up guessing your intent or filling in missing details. The outcome is usually frustrating for you as the user – you receive an output that isn’t what you needed, all because the prompt left too much room for interpretation.

## Solution

The solution is to craft your prompt with clarity, specificity, and consistency. In practice, this means following a few key guidelines:

- **Use specific wording:** Say exactly what you mean. Avoid vague terms or broad requests that could be interpreted in multiple ways.
- **Give clear, structured instructions:** If you have several tasks or questions, list them explicitly (for example, as a numbered list) rather than hiding them in one long paragraph. This way, the AI won’t overlook anything.
- **Maintain consistent references:** Stick to the same names or terms for key concepts throughout your prompt. If you mention “the project” at first, don’t call it “this initiative” later on without clarification. Define any important term or abbreviation (you can even include a brief glossary) so the AI knows exactly what you’re referring to.
- **Eliminate ambiguity:** Anticipate anything that might be unclear and clarify it upfront. It’s better to explain a bit more in your prompt than to leave the model guessing what you meant.

## Challenge

Have you ever gotten a response from an AI that made you think, *“Huh? That’s not what I meant at all!”* If so, you’re not alone. Often the culprit is an imprecise prompt. When we, as humans, talk to each other, we can rely on context, ask clarifying questions, or read tone and body language. An AI like a Large Language Model doesn’t have those luxuries – it only knows what you type. So if your prompt isn’t crystal clear, the AI will **still** do its best to answer, but its “best guess” might miss the mark completely.

Let’s look at some common problems caused by imprecise prompts:

### Vague or Ambiguous Language

One big issue is using language that’s too vague. For example, imagine you tell the AI: *“Summarize this report and make it good.”* What does “good” mean in this context? Should the summary be brief? Highly detailed? Written in an engaging style? Since *“make it good”* is fuzzy, the AI has to guess your intent. You might get a summary, but it could be **good** in ways you didn’t care about and **bad** in the ways you do (perhaps it’s verbose when you wanted concise, or it focuses on the wrong sections).

Similarly, phrases like *“a bit,” “some,” “several,”* or *“in a nice way”* introduce ambiguity. Telling the model *“Explain the policy a bit more”* leaves it unclear how much detail or what kind of explanation you actually want. Does *“a bit more”* mean one extra sentence or a full page of clarification? The AI might err on the side of caution and give only a trivial addition, leaving you underwhelmed.

Another form of ambiguous wording is using terms with multiple meanings without clarification. If you say, *“List the key drivers of the program,”* do you mean driving factors (as in reasons), or people who drive vehicles for the program (literal drivers)? In everyday conversation, we resolve such ambiguities with context or follow-up questions. But an AI might pick the less relevant interpretation and go off on a tangent simply because the prompt wasn’t specific. For instance, it might literally list the people responsible for driving something if it misinterprets *“drivers”*. A human colleague would likely ask, “Wait, what do you mean by drivers?” but the AI just forges ahead with one interpretation.

The lesson here is that words like *“good,” “better,” “effective,”* or domain-specific jargon can be interpreted many ways. If your prompt contains them without further qualification, you’re rolling the dice on what the AI thinks you mean. The result is often a response that technically uses your words but doesn’t fulfill your actual need.

### Inconsistent or Unclear References

Another common pitfall is inconsistency in how you refer to things. Humans are pretty good at understanding that *“the project”* and *“the initiative”* might mean the same thing in a conversation. An AI, however, doesn’t have real-world intuition — it relies on pattern matching and context in text. If you call something *“Project Alpha”* in one sentence and later just say *“the pilot program,”* the model might wonder: *Are these the same thing, or is this another project?* 

For example, consider a prompt: *“Draft an announcement about the New Education Initiative for 2025. Explain what the initiative is and its benefits. The program should also mention how it builds on the current system.”* Here the initiative is also called *“the program”* in the next line. A person might figure out you’re still talking about the New Education Initiative, but an AI could momentarily be unsure if “the program” refers to something else (perhaps a specific software program?). Even if the AI does infer they’re the same, that extra mental leap on the model’s part increases the chance of a mix-up or a less coherent answer.

Inconsistent naming can lead to answers that mix terms or create confusion in the output. The AI might hedge and define terms incorrectly, or repeat information because it isn’t sure if you introduced a new concept. I often see users inadvertently cause this. In one case, a user asked the AI to analyze *“the 2024 Hiring Policy”* and later in the same prompt referred to it as *“the new recruitment plan.”* The AI ended up treating them as separate items, giving a disjointed answer that talked about two policies when there was really only one. The prompt’s shift in wording introduced an ambiguity that a human editor could catch, but the AI could not.

The fix here is straightforward: pick a name or description and stick to it. If it’s a long name, you can introduce a clear abbreviation (e.g., “New Education Initiative (NEI)”) and use that consistently. Also, be careful with pronouns like *“it,” “they,” “this”* if there are multiple subjects in play. *“The committee discussed the school’s results with the teachers, and they decided to implement changes.”* Who does *“they”* refer to — the committee or the teachers? A reader might guess from context; an AI might not guess correctly. In a prompt, a misinterpreted pronoun can send the answer off course. So it pays to take an extra second to explicitly name the subject: e.g., *“...and the **committee members** decided to implement changes.”*

### Multiple Requests Jammed Together

When you ask an AI a compound question or give a long, multi-part instruction in one go, you run the risk of it addressing only part of your prompt. The model might latch onto what it perceives as the main task and neglect the rest, especially if the tasks are not clearly separated.

For example, you might prompt: *“Review the attached survey results and create a brief report. Include the key findings, identify any problems, and suggest possible improvements.”* That’s a perfectly reasonable request from a human perspective — we understand it has several components. However, if this entire instruction is given as one continuous block of text, the AI might miss one of the pieces. Perhaps the output summarizes the key findings but omits suggestions for improvements, because that last clause got a bit lost in the complexity of the sentence.

I’ve seen this happen. A colleague once asked an AI: *“Summarize the policy document, highlight three main challenges, and draft two recommendations for each challenge.”* The result? The summary came back fine and it listed three challenges, but it provided only one recommendation for each – the AI overlooked the word *“two”* because the instruction was buried in a long sentence. The user ended up with only half of what they wanted.

The problem is not that the model refuses to do all parts; it’s that our prompt didn’t emphasize each part clearly enough. To the AI, it was all one big blended task. Without clear delineation, it might do the first couple of things it noticed and inadvertently skip the rest.

The solution is to break out each request explicitly. In the prompt above, if we instead number the tasks (e.g., 1. Summarize the document, 2. Highlight three challenges, 3. Provide two recommendations per challenge), it’s almost guaranteed the AI will address each one methodically. By partitioning the prompt, you remove any ambiguity about there being multiple distinct tasks. When instructions are clear and separated, the AI can follow them like a checklist. If they’re mashed together in a paragraph, you’re relying on the model to parse the sentence and internally create that checklist – something it might not always do correctly.

### Unstated Context and Assumptions

Sometimes the lack of precision isn’t in the words you *do* write, but in what you *don’t* write. If your prompt assumes the AI knows certain background information or understands your intentions that you haven’t explicitly spelled out, you may get a surprise. The model has vast knowledge of public information, but it doesn’t know *your* specific situation unless you tell it.

Consider this prompt: *“Draft the annual report in our standard format and tone.”* You might have a very clear idea of what *“our standard format and tone”* means – perhaps your organization’s reports always start with an executive summary, then sections A, B, C, and use a formal tone with limited jargon. The AI, on the other hand, has no idea what your standard format is. Without additional details, it will produce a report in some generic format it assumes is okay. The result could be missing sections or stylistically off, not matching what you envisioned as “standard.” The user in this case might be disappointed: *“This isn’t in the format we always use.”* But the AI isn’t a mind reader; the prompt was imprecise by relying on an implied convention that the model couldn’t possibly know.

Another example: *“Summarize the recent policy change and its impact.”* If you don’t specify what the policy change is, the AI will try to infer it. Maybe it will think of a well-known recent policy change in your domain, or it will stay generic: “There has been a recent change in policy which has various impacts...” – which ends up being so general it’s useless. The prompt assumed context that wasn’t actually given to the model. This is a subtle form of imprecision: everything you wrote might be clear, but a key detail was left out, making the request itself ambiguous. Are you talking about a policy change in a specific document you have (which the AI hasn’t seen unless you provided it), or a government policy change in the news? The AI might guess wrong.

The takeaway here is to double-check if you’re expecting the AI to “already know” something. If so, it’s safer to include that context explicitly or adjust the prompt to clarify. For instance: *“Draft the annual report. Use the format from last year’s report (introduction, accomplishments, challenges, next steps) and adopt the same formal tone.”* Now the model has concrete guidance on format and tone, instead of a vague reference to “our standard.” In short, make no assumptions — if it’s important to the task, state it plainly.

**In summary,** imprecision in a prompt can take many forms, but they all boil down to the AI being forced to fill in blanks or make assumptions. When the AI has to guess, you relinquish control over the output. Sometimes you get lucky and it guesses right; many times you won’t. The cost is a response that misses the mark and requires you to spend more time fixing it or prompting again. This challenge is exactly what the Precision pattern aims to overcome: by using precise language, you eliminate those guesswork gaps and ensure the AI clearly understands exactly what you’re asking for.

## Example

Let’s walk through a practical example of how **Precision** can dramatically improve the quality of a prompt. Imagine you are a civil servant preparing to introduce a new training program for teachers. You want the AI to draft a briefing note about this program that you can share with school principals and staff.

Suppose you start with an initial prompt like this:

**Original Prompt (imprecise):**

> Please write a briefing note about the new training program we will launch next year in schools. It should cover the main goals of the program and how it will be rolled out, as well as any improvements over current training methods. Make sure it's in our standard format and that the tone is professional but engaging.

At first glance, this prompt might seem okay. But several imprecisions lurk within it:  
- **Unclear references:** What is “the new training program”? It isn’t named or described, so the poor AI only knows that such a program exists, not what it entails. Also, what are the “current training methods” that the program improves upon? The prompt assumes the model is aware of the existing methods, which it isn’t.  
- **Multiple tasks in one sentence:** The request bundles together the program’s goals, rollout plan, and improvements, all in one paragraph. There’s a risk the AI might focus on one or two of those and neglect the others.  
- **Ambiguous instructions:** “Our standard format” is meaningless to the AI since it doesn’t know your organization’s standard. The model might just guess a format. Likewise, “professional but engaging” gives a general sense of tone but no specifics on what “engaging” means (should it include a story, or just avoid dry language?).

Given this prompt, an AI will do its best, but the output may not satisfy you. It might produce a generic briefing note that talks about a training program in broad terms (because it doesn’t know the details), and it could easily miss some of the points (maybe it covers goals and rollout but says little about improvements). It certainly won’t magically follow your organization’s secret format.

Now, let’s apply the **Precision** pattern to improve this prompt. We’ll make the language exact, provide needed details, and structure the instructions clearly:

**Revised Prompt (precise):**

> **Task:** Draft a briefing note for school principals about the upcoming **New Teacher Training Initiative (NTTI)**, launching in 2025. This program will modernize teacher development by replacing the current **In-Service Workshop** model of training. (NTTI introduces hands-on mentorship and online modules, which should increase teacher engagement and skill uptake compared to the old approach.)  
>  
> **Please cover the following points in the briefing note:**  
> 1. **Overview of NTTI:** Explain what the New Teacher Training Initiative is and outline how it will be rolled out over the next year in schools.  
> 2. **Objectives:** List the main goals of NTTI (what it aims to accomplish for teacher development).  
> 3. **Improvements over Current Method:** Describe how NTTI differs from the current in-service training method and what benefits or improvements it brings.  
>  
> **Format and Tone:** Begin with a short introduction that introduces NTTI and end with a brief conclusion. Use a formal, professional tone, but make sure the language is clear and accessible to a general audience (engaging but not overly casual).

Let’s unpack what changed and why it makes a difference:

- **We provided context and defined terms upfront.** The revised prompt immediately names the program (NTTI) and even gives a bit of background on it (what it is and what it replaces). We also identified the old method as the “In-Service Workshop” model and hinted at how NTTI is better (mentorship and online modules for more engagement). Now the AI doesn’t have to guess what the program or the current methods are – we’ve told it. The output can include concrete details (like mentioning those mentorship and online components) instead of staying generic.

- **We broke the request into clear, numbered items.** Instead of one long sentence with multiple clauses, we have a structured list of three specific points to cover. The AI can clearly see it needs to produce an Overview, discuss Objectives, and then describe Improvements. This structured approach ensures the model won’t skip any part: it will address each numbered point in order. We’ve essentially given the AI a mini-outline to follow.

- **We clarified the format and tone.** The vague “standard format” instruction is replaced with concrete guidance: we specify having an introduction and conclusion (which implies a structured note) and we emphasize the tone should be professional yet accessible. “Professional but engaging” is now translated into “formal tone, clear and accessible to a general audience” – which is easier for the AI to interpret correctly. The model now knows exactly how to organize the note and what style to use.

With this refined prompt, the AI’s output will be much more on target. You can expect a briefing note that starts by introducing NTTI and its purpose, then has separate sections or paragraphs for the overview, objectives, and improvements, and ends with a concluding statement. It will use the term NTTI throughout (since we established that acronym) and will explicitly compare NTTI to the old workshop model as instructed. The tone should come across as professional yet reader-friendly, as we directed.

To illustrate the difference, here’s a simplified peek at what the AI might produce before and after applying the Precision pattern:

- **Possible output from the original prompt (fragment):** *“A new training program will be launched next year to help teachers. It has several goals to improve teaching practices and will be rolled out across schools. This initiative is expected to make current training better.”* … (Notice how generic and unclear this is – the model hasn’t mentioned any specifics, because none were provided in the prompt.)

- **Possible output from the revised prompt (fragment):** *“**Introduction:** The **New Teacher Training Initiative (NTTI)**, launching in 2025, is a comprehensive program to modernize teacher training by replacing the current in-service workshops.  
**Overview:** NTTI will roll out next year across all district schools in phases, starting with an orientation session for principals in January…  
**Objectives:** The main goals of NTTI are 1) to equip teachers with modern instructional techniques, 2) to provide ongoing mentorship, and 3) to incorporate online learning modules for continuous development.  
**Improvements:** Unlike the old workshop-based training, NTTI offers hands-on mentorship and flexible online modules. This approach is expected to engage teachers more effectively and improve skill uptake…  
**Conclusion:** In summary, NTTI represents a significant improvement in how we prepare our educators, and by the end of 2025 we anticipate…*” (This version is well-structured, uses the correct names, and includes the concrete details we provided in the prompt.)

As you can see, the revised prompt leads to a far more detailed and organized output. By applying Precision, we’ve made it practically impossible for the AI to misinterpret our request. The briefing note we get back is likely to need only minor tweaks (if any) before it’s ready to use, rather than a major rewrite. This example shows how using unambiguous, specific language in your prompt can save you time and ensure you get exactly the kind of response you’re looking for. In short, the more precise your prompt, the better the AI’s answer – what you ask for is what you get.
