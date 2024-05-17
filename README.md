# 1st Place HooHacks 2024 (Art & Gaming) KeyGlow 🎹✨

## [UVA Engineering Article](https://engineering.virginia.edu/news-events/news/who-won-hoohacks-2024-these-2-uva-teams-are-still-glowing)

Here you'll find the code for KeyGlow, the piano instructor that lights up your keyboard with a projector to help you learn how to play the piano! This project won 1st place in the Art & Gaming category at HooHacks 2024.

## Inspiration 📜
As three people who love making music, we wanted a way to learn and improve at piano faster and more intuitively. Our key insight is that the best way to learn (especially for beginners) is to have the feedback projected directly on the physical keyboard in front of you. There are currently no tools on the market that do anything like this.

## What it does ❓
Our tool places a projector above the MIDI piano/keyboard where you are playing and displays green on each note when it is pressed (or should be pressed during a demo!). In a Simon Says manner, you progressively play more and more of your chosen song until our extremely detailed analyzer algorithm believes you have properly mastered the section according to your proficiency level.

## How we built it 🏗
There are a few parts to our project. The core code is written in Python, including a keypress visualizer built in PyGame and a custom play analysis algorithm capabale of detecting the time, severity, and nature of any mistake. We leverage GPT-3.5 to help the system give helpful and personalized feedback based on this analysis. Beyond this, we have a frontend Next.js web app which runs locally on your computer to give you a nice interface for choosing a song and interacting with the program. The main Python process and Next.js app talk to each other through a Flask web server to keep the data in-sync.

## Challenges we ran into 🚩
The hardest part of the process by far was working with MIDI data that is created by playing keys on a MIDI keyboard. We found this format to be extremely convoluted and not ideal for the kind of work we were doing. Even basic tasks like splitting the original MIDI track into multiple even-length segments took us a very long time to figure out. Beyond this, there were naturally challenges analyzing the difference between the track you played and the reference - this is a notoriously difficult task when it comes to timing, etc.

## Accomplishments that we're proud of 🌟
The visualization looks much better than we possibly could have imagined. We are genuinely very excited at just how great it looks when you press a key and it lights up in real time. The alignment is very, very strong, and overall the process flows smoothly. We are also very proud of our analyzer algorithm that compares your playing to the reference file - as we said before, this is an extremely difficult task that requires a deep understanding of both music in general and how the MIDI data format works.

## What we learned 📚
We are now, for all intents and purposes, fluent in the MIDI format after spending so many hours working with it. Beyond this, we all improved significantly at PyGame, and we learned more about communicating properly between processes. On the non-technical side, we learned that it is important to get a base product working before we add too many features (especially under a 24 hour time constraint) as well.

## KeyGlow 👀
We hope that beginners and professionals alike take interest in such a tool to help them learn their pieces faster than reading from sheet music. We can confidently say that there is nothing else out there quite like it. Our first goal at improvement would be to make it smaller and cheaper so it could be sold like a standard attachment on top of a MIDI controller - we believe this to be 100% doable. We would also like to continue further with one of our stretch goals which was to have an LLM take in the feedback output from the analyzer and talk to you in natural language about what you can improve on.
