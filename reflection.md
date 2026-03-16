# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?
- List at least two concrete bugs you noticed at the start  
  (for example: "the secret number kept changing" or "the hints were backwards").

- #1 “Press Enter to Apply” did absolutely nothing, you had to press on the submit guess to actually get the app to do anything 
- #2 If the hint is the same, nothing changes when entering a new number, so its hard to know if it actually did anything 
- #3 Pressing new game doesn't do anything (only number of retries resets)
- #4 Also amount of retries it said I had did not match the amount I was actually given 

---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?
- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).
- Give one example of an AI suggestion that was incorrect or misleading (including what the AI suggested and how you verified the result).

- Used Claude as the AI tool for this project 
- Focused on the issue where pressing the enter key doesn't actually submit the number, you have to manually press the submit button for it do anything 
- The first thing I did was input the issue and ask the reasoning behind it, but it returned a long and confusing output, making it difficult to pinpoint the issue, so I created a more concise question, asking what line in the code deals with the enter key, and what line could be causing the error behind there being no submission of the number
- 
---

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?
- Describe at least one test you ran (manual or using pytest)  
  and what it showed you about your code.
- Did AI help you design or understand any tests? How?

- Firstly, by reviewing the changes suggested by the AI, particularly making sure the logic flowed correctly and followed similar pattern to other logic in the code. 
- Then running multiple tests created by the AI making sure all are passing as expecting and running the app again testing multiple inputs
- One test for the enter button error checks if nothing was inputted, this makes sure the app is working as expected, where nothing should occur if nothing is inputted 
- Yes, after finding and correcting the error the AI was able to design comprehensive tests tomake sure errors were fixed correctly 
---

## 4. What did you learn about Streamlit and state?

- In your own words, explain why the secret number kept changing in the original app.
- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?
- What change did you make that finally gave the game a stable secret number?

- The number kept changing in the original app because the number is being compared as an integer in some cases and as a string other times, making the correct guess be rejected every other turn
- Anytime you interact with a streamlit app the streamlit reruns the entire python script, not like a normal app where only one funciton is called, the whole file reexecutes 
- The change is that the secret is now always passed as an integer to check_guess 
---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
  - This could be a testing habit, a prompting strategy, or a way you used Git.
- What is one thing you would do differently next time you work with AI on a coding task?
- In one or two sentences, describe how this project changed the way you think about AI generated code.

- A habit I want to reuse is creating concise and direct questions for the AI that will produce the most useful outcome
- Something I would do differently is not starting out questions with vague inputs, but rather starting with these detailed questions to avoid wasting time or confusing myself with its outputs
- It changed how I think because it showed that AI is not always helpful, and can cause more confusing answers if prompts are not clear 
