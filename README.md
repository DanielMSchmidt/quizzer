# quizzer
Test yourself for an exam using this SPA. It loads your summarization TeX and compiles it to a super cool testing deck

## Idea

### Workflow

1. As you prepare your learning materials in Latex (a summarization would be optimal) annotate them with sections, subsections etc that would be answers to questions. Notate that questions with ```#Q: What does the fox say?``` in the corresponding block (Shows a path were the question is like ```<section title> -> <subsection title>```)
2. Copy & Paste (or pass via CLI, don't know, maybe both) the .tex to the application
3. See your questions in a list, possibly edit them
4. Click a test button, which takes a unasked (or worst rated) bulk of questions for you to answer
5. Click on a Question to see answer and rate how far you were away from this
6. Study faster and better
7. Win exam
8. ???
9. Profit

### Implementation

- Let the parse process be 
  - a seperated (unit tested) node_module
  - used in a web/shared worker
- Save the deck to loalstorage, persistance should be build later
- Build an export function (to ```.json```)
- Make the test configurable per user (test set, priorities to randomness (untested / worst rated first?))
- Open problems
  - included images (upload them or ignore them)
- Tech-stack
  - React view layer
  - Persistance / Actual work via web/shared worker
  - Use Webpack
  - Test with Karma & Jasmine
