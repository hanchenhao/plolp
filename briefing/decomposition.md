### Decomposition
*Break tasks into smaller, non-overlapping subtasks.*

**Motivation:** A complex request presented as one large task can overwhelm the LLM and lead to a disorganized or incomplete answer. The model might overlook some parts of the task or mix different issues together if everything is lumped in one prompt. Additionally, without separating concerns, the LLM may have difficulty addressing all aspects thoroughly, causing the final output to miss details or clarity.

**Solution:** Split the problem into clear, manageable subtasks, and handle them one by one. Ensure that each subtask is distinct (no overlap) and that together they cover all aspects of the original challenge (nothing important is left out). You can then guide the LLM through each smaller task in sequence or ask it to enumerate and solve them stepwise. This approach (following the "mutually exclusive, collectively exhaustive" principle) helps the model focus and produces more structured, complete answers, since the LLM can dedicate attention to each component of the problem in turn.

**Explanations:** 

I (the author) highly recommend the book "The McKinsey Way" to all my readers - it offers excellent framework to train and sharpen one's thinking process.

This chapter should focus more on **thinking** of human beings who uses LLM, not **action** of concretely how they use LLM. It is okay to have less example. Talk more about thinking methods.

Some thinking techniques to decompose a complex issue:

* Pipeline - split a complex task into subtasks according to stages, use output of early stage as input of later stage. For example, in order to compose a report, you can have first task to go online and search for all relevant news and articles, generate a full list of all raw materials, then the second task use those materials to analyze and write the report.
* Silo - split a complex task into subtasks according to vertical domains, so each vertical "silo" (with its own prompt file) can be specialized to its own domain. For example, in order to genearte a weekly newsletter, you might have one prompt to collect news in "geopolitics", another to collect news in "culture", so you can optimize the two prompts separatedly. (Of course, many parts in those two prompts might be reusable as attachments - see **Attachment Pattern**)
* Zoom In - split a complex task into subtasks according to the level of perfection (or detail). For example, in order to write a chapter of a book (like the author is doing with this book), you can first have a prompt to generate a briefing (structure and main points) of the chapter, then have another prompt to write with a lot of references (as attachments) and online searches.
* Divide and Integrate - still use the example of writing a book, you can have one prompt (or two prompts, as shown in "Zoom In") to write chapters, then have another prompt to integrate all prompts and write the openning and ending chapters, as well as marketing messages.

