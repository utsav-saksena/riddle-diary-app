# T.M. Riddle's Diary - A Browser App

## What it is 
Remember Tom Marvolo's mysterious diary from the Harry Potter and the Chamber of Secrets? 

This is a fun emulation of that diary which runs in your brower. 




## Features
- Lightweight and entirely web-based; runs in your browser
- Just like the actual diary, whatever you type will fades away, after which the diary will respond to your query.  
- Uses the LLM (Large Language Model) of your choice.
- The diary has fallback responses if it is unable to connect to Ollama. 

## Prerequisites
- This .html works best in Google Chrome and a Linux-based environment where you have access to the terminal.
- You need to have Ollama running on your machine (instructions on how to install Ollama are given [here](https://github.com/ollama/ollama). 

## How to run 

- Download the LLM of your choice from Ollama (the app uses Gemma 3 as the defult).
- If you want to change the choice of LLM, look for this line and change it to the model of your choice
  ```
  const OLLAMA_MODEL = 'gemma3n';
  ```  
- To get get dynamic responses to your query, ensure that Ollama is running:
  ```
  ollama serve 
  ```
- Since this is a front-end only app (i.e. no server involved), you'll have to disable Chrome's same origin policy.
- To do this safely, navigate to the directory where you've downloaded the .html file, and type in the following: 
  ```
  google-chrome --user-data-dir=/tmp/chrome_dev_test --disable-web-security tomRiddleDiary.html &
  ```
- This ensures that you create a temporary user data directory (/tmp/chrome_dev_test), where your browsing session, cookies, and cache will be stored. 
- Close your Chrome session after you're done with the app. 
- DO NOT browse the internet using the same browser session that you run the app.

## How I made this 
One evening's worth of vibecoding with Anthropic's Claude Haiku 3.5 and Google's Gemini 2.5 Flash! <3  

