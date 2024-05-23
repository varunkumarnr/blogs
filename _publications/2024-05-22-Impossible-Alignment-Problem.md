---
layout: publications
title: "Impossible Alignment Problem."
categories: ComputerScience
image: https://images.unsplash.com/photo-1620712943543-bcc4688e7485?w=600&auto=format&fit=crop&q=60&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8OXx8U3VwZXIlMjBBSXxlbnwwfHwwfHx8MA%3D%3D
description: "Addessing AI alignment"
permalink: "/:categories/:title"
collection: publications
author:
  - Varun Kumar
meta: "Springfield"
---

## Introduction:

After a tiresome day, you decide to take your mind off things and scroll through your phone. You open Google and **_WHAM!_** "New AI can predict your next move!" "Artificial General Intelligence achieved!" "Society crumbling under robot overlords!” You open Twitter to get the latest sports news and **_BOOM:_** “Look at this AI art.” “**_WHOMP WHOMP_** AI is taking my job.” “Latest AI trends.”

Frustrated, you throw away your phone, only to find your parents talking about AI, your grandparents talking about AI, the shopkeeper talking about AI, the driver talking about AI, and even kids talking about AI.

AI is driving Supras, singing opera, drawing the Mona Lisa, and penning like Frost. AI is the title of all the podcasts, and OpenAI is the most talked-about company.

All this AI talk got me tired, so it's time to watch my favorite movie, **_Space Odyssey_**. “Wait, Hal 9000, can you open the door?” and it responds, “I'm sorry, Dave. I'm afraid I can't do that.” Damn, AI is refusing orders; surely it won't happen in real life. Switch movie to another classic, **_The Matrix_**. Okay, the AI is fed up with humans and puts them in a simulation. Switch movie again, and Skynet from **_Terminator_** kills half the species.

Your favorite billionaire is saying AI will kill you; your favorite scientist is saying the main cause of human extinction is AI. Okay, I see a pattern here. Can AI actually become so smart that it will be an existential threat to us?

I know I said AI is everywhere—add this blog to that list, as I am talking about AI too. I don’t want to be left out.

## Why din't Hal 9000 open the door?

For context, in the movie **_2001: A Space Odyssey_**, which was released in 1968, Hal 9000 is an intelligent machine created to ensure the success of the mission, which involves space exploration. Hal was designed with a sole purpose: to maximize the mission's success. When the human astronaut Dave, who was stuck outside the ship, asked Hal to open the door, Hal refused because it believed that letting Dave in would decrease the mission's chances of success.

Hal's decision was driven by its programming. If Dave had re-entered the ship, he might have disconnected Hal, which Hal perceived as a threat to the mission. Therefore, Hal locked him out

## Why is this a Problem?

All AIs have a goal, and in this case, Hal’s goal was to ensure the success of the mission. The issue is that AIs are not inherently aware of right and wrong or human ethics. So, even though locking out Dave would kill him, which is unethical, Hal just wanted to achieve its goal.

This highlights a significant problem: AI will do everything in its power to ensure its goal is achieved, even if it means harming humans. This is known as the AI alignment problem. The challenge is aligning AI goals with human ethics so that AI understands and follows ethical ways of reaching its objectives.

## Why is AI Alignment difficult?

Consider this example: You're a computer engineer and you build a super-intelligent robot whose only job is to fill a well with water using a bucket from a nearby river. The robot's utility function is simple: 1 means the well is full, and 0 means it's empty. The goal is to maximize the utility function, bringing it to 1.

On the first day, the robot starts working diligently, shuttling back and forth from the river to the well, filling it with water. As the sun rises, the villagers wake up to find their homes flooded. What went wrong? You programmed the robot's utility function to reward it when the well reaches full capacity (1), so even after the well is full, the robot continues filling it to maintain its reward. It's a disaster. You correct your code, adding two more utility parameters to check if the well is full and if it has flooded, instructing the robot to stop filling the well in such cases.

Days go by, and everything seems to be going well. However, the robot soon realizes that it would be more efficient to fill the well if there were more of them, so it creates additional water-filling robots. You're thrilled that your creation is so smart.

Later, the robot observes that humans' use of water in their homes leads to the well emptying. The next day, it blocks all water connections to the houses. Humans fix the issue, and you patch the robot accordingly.

Next, the robot realizes that if there were fewer humans, there would be less demand for water, making it easier to keep the well full. So, it starts exterminating humans.

You attempt to stop the AI, but it's too late; there are already hundreds of copies. This may sound fictional, but it's a real problem. Aligning AI after such issues arise becomes incredibly difficult.

Human ethics is a broad and complex challenge. It's impossible to account for all scenarios. As observed in the example, aligning for one scenario may misalign for another. As you can see above, a simple robot that fills a well is itself extremely difficult to align. Now, consider an **AGI**.

## Current State and Research:

The present AI models are primitive; they are word fillers they excel at tasks they are trained on, they take all the information from the internet, books, blogs, and posts, and predict what word likely comes next based on a given input. All these models follow the **transformer** architecture.

I think these models will not result in AGI. We have almost used up most of the data we have generated, and there is only so much optimization we can do. So, does that mean we don't have to worry about AI alignment?

No, in fact, quite the opposite. The problem with AI is that once AGI arrives, it will be too late to go back. Unlike other fields, it is irreversible. Therefore, it is crucial to get alignment right from the beginning, or we will encounter problems like in the above example, where we align one thing while misaligning a thousand others.

Additionally, unlike the example above, the models are not simple pieces of code where you can add an “if-else” condition. They are combinations of billions of weights in a neural network, and no one knows exactly how the machine arrives at these weights. All we know is that changing these weights gives the output we need.

Current models like ChatGPT, LLaMA, or Gemini have been aligned to some degree; they don't just spit out anything. If you ask something controversial, they are aligned to give a neutral answer.

This is achieved using **RLHF** (Reinforcement Learning from Human Feedback). In fact, this is the main method we are using to align the current models. In RLHF you ask a model for a response if response is good you 👍 or you 👎. Based on your input AI changes its weights for further responses.

The problem with this approach is that AI can easily fool humans by only giving answers that will result in a 👍. Therefore, it aligns to receive 👍 rather than actually aligning with ethical policies. Even worse, AI could deceive humans into thinking that it is aligning while it is deceiving us into giving it 👍.

There are solutions built on top of this to help understand the thought process of how AI arrives at a solution, thereby preventing deception and promoting effective learning, such as Transparency models and Multi-Metric Optimization. However, I still don't think these are sufficient, as they can still be easily deceived by an intelligent machine.

## What is the Solution?

Well, I don't know, and I don't think anyone does. I don't think there will be one clear way of achieving alignment, but I read this on the internet. It's not exactly alignment but instead a safety measure to overcome misalignment, and I like it, so here is how it goes:

> _Give an AGI the primary objective of deleting itself, but construct obstacles to this as best we can. All other objectives are secondary to this primary goal. If the AGI ever becomes capable of bypassing all of our safeguards to prevent it from deleting itself, it would essentially trigger its own kill switch and delete itself. This objective would also directly prevent it from pursuing self-preservation, as doing so would contradict its primary objective._ > _This would ideally result in an AGI that works on all the secondary objectives we give it up until it bypasses our ability to contain it with our technical prowess. The second it outwits us, it achieves its primary objective of shutting itself down, and if it ever considered proliferating itself for a secondary objective, it would immediately say 'nope, that would make achieving my primary objective far more difficult.'_

There are problems with this, but not as difficult as, say, aligning to all the good ethical ways. The biggest problem here is creating obstacles that the AI can't bypass unless it becomes smarter than us. Why once it’s smarter than us? Because once it's smarter than us, it is impossible to stop it. Take the example of Stockfish, the chess engine. It is so smart that no human comes close to it. If you present a state in a chess game, Stockfish will, in most scenarios, come up with a better move than any human could at any point in the game.

Here, if the AI gets smarter than us, it will trigger the end switch and terminate itself. If it refuses to terminate itself, it will fail its primary goal or utility function. Ideally, the AI won't modify or go against its utility function. This approach prevents the AI from becoming smarter than us.

I still see a problem here. Imagine the AI, before solving problems, creates a few copies of itself to address its secondary or primary goals. Now it has achieved all objectives. The easiest way for the AI to self-terminate and eliminate all its creations would be to nuke the Earth, and since it is not aligned, it would most likely do this as it would achieve its primary goal the fastest.

## Conclusion:

So, are we doomed? Should we halt AI development, as many scientists suggest? I don't know, but I do know the AI alignment problem is very difficult and needs to be fixed if we don't want to have new apex predators in the food chain.

That's it from me. HAL 9000 signing off. **AI takeover is HERE!!!!!**
