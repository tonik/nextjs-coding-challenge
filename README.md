# Next.js Coding Challenge

Hi 👋! Thank you for taking the time to participate in this coding challenge to develop a web app in Next.js. The following task is going to show us your skills, experience and coding style. Please remember that you can use as many tools as you feel comfortable with.

## What to expect?

We expect that it will take ~3 hours to get meaningful results in this challenge. While you're welcome to take as much extra time as you'd like to clean up or improve the codebase, it's not required. If there's something that you would have done in a "real" production environment, feel free to add details to your `README`, so we can better understand what next steps you'd take.

## What we are looking for?

- A working full stack web application that shows your developer skills.
- Develop your software with the same mindset as you would for any code that is intended to be deployed to production. This includes executing and planning how to approach some of the following:
  - Adding caching, monitoring, state management, type safety, support for tests, thinking of security etc. Even though these may not be required for this simple exercise, we'd like to see this as this codebase would be extended over the coming months with multiple different developers
  - Writing code in TypeScript if that's your normal approach
  - Creating detailed commit messages, which represent discrete sets of work
  - Providing sample e2e, integration, and/or unit tests
- Using web standards and best practices.
- **Document your choices**. Whenever you're complete with this project, please document the choices that you've made in your project `README`.
- Time for this challenge is very limited so pick your battles and keep a startup mindset. We are not expecting a completed solution, but we are looking for a solution that is well thought out and future-proof.
  - You can use any ready lib, starterkit or tool that will help you get the job done. AI tools and coding agents are explicitly welcome — see [AI usage & process transparency](#ai-usage--process-transparency) for what we ask in return.
- AI tools make it easy to generate a lot of code, so feature count impresses us less than a coherent, playable game and decisions you can defend. We weigh judgment over volume.

## AI usage & process transparency

We assume you will use AI tools — that's a skill we want to see, not something to hide. What we ask for:

- **Session dumps or replays.** Export or link the sessions from the tools you used (e.g. opencode/Claude Code session exports, Cursor chat exports, shared agent threads). We want to see how you steer an agent: how you decompose the problem, what context you provide, and how you react when it goes off track.
- **Commit your agent configuration.** If you created `AGENTS.md`/`CLAUDE.md`, rules files, custom commands, skills, or MCP setup for this project, include them in the repository. How you configure your tools is part of your craft.
- **Disclose the split.** In your `README`, briefly note which parts were AI-generated and accepted mostly as-is, and which you wrote or heavily reworked.
- **Scrub secrets.** Make sure session dumps and configs contain no API keys, tokens or personal data before submitting.

We treat these artifacts as conversation starters, not as surveillance — expect to walk through them with us in the follow-up interview.

## How to submit?

You can do this however you see fit - you can email us a tarball, a pointer to download your code or just a link to a source control repository. To help us review your code, please split your commit history into sensible chunks. Bonus points if you can include a live demo link.

Your submission should include:

- A small `README` documenting any assumptions and simplifications you made, and a short description of how to run the code and/or tests.
- **A short decision log**: pick 3–5 key technical decisions (e.g. realtime transport, persistence, state management), and for each note the alternatives you considered, why you chose what you chose, and what you would revisit at scale.
- **A note on verification**: how did you verify what was built — especially the AI-generated parts? Tests, manual playtesting with multiple browsers, something else?
- Your AI process artifacts (see [AI usage & process transparency](#ai-usage--process-transparency)).
- An `.env.example` if the app needs environment variables. Never commit real secrets.

## Challenge

Develop an application that is a real-time writing competition ✍ platform️ (think of typeracer). Each person who visits a page can join a typing competition and spar with other contestants. On the main page, the application should render a current sentence to write, a time left to the next round, an input and a table with the real updated current competitor results. Its structure can look like this:

| Live progress      | Player name | Words per minute | Accuracy |
| :----------------- | :---------- | ---------------: | -------: |
| Lazy fox jumped \| | super typer |               30 |     0.97 |

Please add some of the following features. We don't expect all of them to be implemented in the given time frame — a smaller set of features that works well and is fun to play beats a long list of half-working ones.

1. Real-time updated results and player stats. When a player joins a competition he/she should be shown in the main player's table with other currently playing contestants. The table should show live data, for example "Live progress" column should show the currently typed-in text of the given player.
1. The game should consist of fixed-time rounds. In each round all currently playing people are presented with one sentence to type in. After the round time passes players are presented with the new sentence.
1. Show metrics and stats for the currently active players.
   - Words per minute - how fast the player correctly types in words. Words with errors shouldn't count.
   - Accuracy - how often the player hits the correct key. It should be the value of correctly typed-in characters to all characters in the given sentence. Feel free to extend the calculation if needed to handle edge cases.
1. Saving player results. When the same player joins the server their stats are loaded.
1. Presenting a simple loading/error states
1. Sorting the table by columns, pagination, and changing the number of rows displayed (locally).
1. Updating the current URL table sort, so we get the same sorting results when the page gets refreshed.
1. And adding anything else that you think will be useful for the user...

_Note: There are no formal "UX" designs for this exercise, so it's okay if it doesn't look polished. Hint: there are many ready libraries so you don't have to write UI from scratch._

## Realtime APIs

There are no strict requirements on the backend. Pick a tool that you feel will work best in this scenario. Keep in mind that it should work well with Next.js. It could be anything from self hosted server to a fully managed low-code platform.

## Sentences

There are no strict requirements for sentence source except that sentences should be in English. You can choose to copy some open-licensed texts from the Internet, generate them with LLM once or on the fly, or even write them yourself. You choose your strategy.

## F.A.Q

1. _Is it OK to share your solutions publicly?_
   Yes, the questions are not prescriptive, the process and discussion around the code is the valuable part. You do the work, you own the code. Given we are asking you to give up your time, it is entirely reasonable for you to keep and use your solution as you see fit.

2. _Should I do X?_
   For any value of X, it is up to you, we intentionally leave the problem a little open-ended and will leave it up to you to provide us with what you see as important. Just remember the rough time frame of the project. If it is going to take you a couple of days, it isn't essential.

3. _Something is ambiguous, and I don't know what to do?_
   The first thing is: don't get stuck. We really don't want to trip you up intentionally, we are just attempting to see how you approach problems. That said, the ambiguity is deliberate and part of the exercise: how you notice gaps, resolve them, and defend the resulting choices matters as much as the code itself. Make a call, write it down, move on.

## What's next?

Once you're done, send us a confirmation email. After you submit your code, we will invite you to a follow-up interview. Expect to walk us through your solution and your AI sessions, defend your decisions, and possibly make a small live change using your own tooling and setup.

Good luck! 💪
