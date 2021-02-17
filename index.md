# Welcome to my Portfolio
*...a perpetual work in progress...*

-----

## Introduction

Hello. My name is Jeremy. These days I tend to prefer JK, but it doesn't really matter. You can get in touch with me by email [here](mailto:Jeremy.JK.Kansas@gmail.com).

This portfolio started life as part of the capstone class for my CS degree, but I never really felt comfortable with the end result; the writing felt fluffy and bloated (as bad college writing too often does), and I spent more time fulfilling the specific requirements of the assignment(s) and less time presenting my self and my work in a way that I felt best. As of this writing I have no professional work experience in programming or software development, though I have had some freelancing successes over the past couple months. Instead of droning on about myself, let's get into the projects.

-----

## Voltage Modular Modules

The following items are components to be used as part of Cherry Audio's Voltage Modular Eurorack-inspired software modular synthesis system. I designed and developed each of the modules below. As of this writing, I have gotten 200+ sales over a time period of about three months. While these numbers are modest at best, I still count it as a success given its status as a niche product. More importantly, these modules show that I can design, implement, and release a fully working product people are willing to buy. 

In each instance, I did my best to follow best practices, including keeping code readable and reusable. Still, none of these are polished masterpieces of development, nor should they be. While I have a great appreciation for elegant, clear, beautifully architected code, I understand that the only real value that code such as this has (aside from a learning experience) is in its life as a published product.

Beyond that, the experience with these modules has given me further practice. I employed Git for version control, striving to keep my commits atomic with clear/accurate messages. I wrote exhaustive documentation to introduce the end users to each feature and the underlying function of the modules. I also have since been involved with post-launch maintenance and updates, including communication with customers and Cherry Audio employees and implementing bug fixes and feature requests. The various modules gave me an opportunity to work with a number of concepts and techniques, including concurrency, byte streams, digital signal processing (filtering, aliasing, interpolation, etc.), optimization, and even UI/UX considerations.

*Note: These repos are not public, but I do share some pieces of code in the linked detail sections.*

### Random Sampler

<img src="https://ymerejsasnak.github.io/rsamp.png" height="300">

This module allows the user to load up to 8 audio samples and then randomly trigger them, while also adding randomized variation to a number of parameters including volume, pitch, and start offset. More development details [here](sampler.md).

[Random Sampler on the Cherry Audio store](https://store.cherryaudio.com/modules/jks-random-sampler)

### Sample Scrubber

<img src="https://ymerejsasnak.github.io/scrubber.png" height="300">

This module allows the user to load up an audio sample and control playback position with a control voltage. More development details [here](about:blank).

[Sample Scrubber on the Cherry Audio store](https://store.cherryaudio.com/modules/jks-sample-scrubber)

### CV Canvas

<img src="https://ymerejsasnak.github.io/cv2.png" height="300">

This module allows the user to draw four different custom curves and read/output them in various ways to control any other parameters of other modules. A lot of options and random generation functions are included as well. More development details [here](about:blank).

[CV Canvas on the Cherry Audio store](https://store.cherryaudio.com/modules/jks-cv-canvas)

### Sample Swarm

<img src="https://ymerejsasnak.github.io/swarm1.png" height="300">

This module allows the user to load a sample and, based on a few settings, it overlays the sample on the output buffer the chosen number of times. More development details [here](about:blank).

[Sample Swarm on the Cherry Audio store](https://store.cherryaudio.com/modules/jks-sample-swarm)

-----

## Other Notable Projects

### Full Stack Project

This was a school project, and I don't have any illusions about this being wonderful, robust, polished code. It's a very basic full-stack CRUD project. It uses MongoDB with a provided stock database as its basis, interacts with the MongoDB with Python (Pymongo) code, builds a RESTful API on top of it with Python and Bottle, and then accesses it from a browser via asynchronous HTTP requests made from an HTML/Javascript form. 

[Client/Server code](https://github.com/ymerejsasnak/clientserver)

My idealized goals: 
- structure according to object oriented principles
- make the code more modular and reusable
- prepare code for potential collaboration, extension, and maintenance
- add units tests, error checks, and be more mindful of security and quality control
- ensure readability for myself and others (collaboration is KEY!)

The project as it stands falls far short of these ideals, at least in my eyes, but the beginnings of most of the above are there. At the very least, it does show some experience with a full stack and an understanding of how different technologies interact. 

Some notable nuggets of wisdom earned through this project:
- Time constraints can lead to security considerations suffering in the push to get things done on time.
- My education and experience makes adapting to unfamiliar or rusty languages/platforms/tools/etc (HTML and Javascript in this case) navigable and manageable.
- Nothing in development ever goes smoothly, and sometimes for silly oversights: I had many issues initially with trying to get the index.html page to actually communicate with the Bottle.py server I had running locally. I was getting error messages related to Cross Origin Resource Sharing, which I was vaguely familiar with from prior web experience, but I didn’t understand how it applied to my situation. Then I realized, on my machine, I was running the server on “localhost” but loading the HTML file directly from my C drive, which the browser interpreted as different origins (thus leading to a CORS error). From here, I just had to figure out how to statically serve files directly from Bottle, so that the index.html would also come from the same host, and this issue would be resolved. Through this, I was able to exercise problem solving and research skills to resolve my issue, and get a deeper understanding of web programming in the process.
- Collaboration makes complex software possible. Given a lot of time, I could eventually reach my ideal, or close enough, but for such a software stack to be fully functional, user friendly, and perhaps most of all secure, a team would be better able to achieve this as each could focus on different aspects: back end, front end, UI/UX, visual design, testing, security, etc. As a solo developer within very limited time constraints, I could really only hope to lay the groundwork for the ideal concept I had, enacting core functionality – but through well-formatted and commented code, as well as helpful git commit messages with small and frequent commits, I would hope to pave the way for others to more easily find their way when contributing to my base code.

-----

### Data Readings and Hash Table

[WetSpec and Hash Table](https://github.com/ymerejsasnak/wetspec-script)

Another school project. It started as a script for pulling weather data from a Raspberry Pi with attached Grove Pi. I later implemented a hash table to store the weather data and allow quick lookup based on the date/time of the reading. This was mainly a programming exercise - a professional script would of course use a pre-built data structure, or more likely use a full-fledged database for storage. After performing rough performance tests, I found my simple hash table to be much more efficient than a linear search, but still less efficient than Python's built-in dictionary type. Given that date/time readings would necessarily be made in order, testing against a binary search would have been informative as well.

The hashing function was simple: performing a modulus operation of a numerical representation of the key by the size of the table. Because of this simplicity of the hash function, the table size became more important and really needed to be a prime-valued size to help spread out the entries. I toyed with non-prime tables since they would be easier to resize, but ultimately found them to have far too many collisions. Next, my initial plan had been to resize the table when it reached about 75% capacity, but this proved to be too high given that my collision resolution strategy was straightforward linear probing (inserting the data into the first non-colliding index) so I settled for about 50% capacity. From this we come to the most glaring example of a difficult trade-off: I can perform over 10,000 random look-ups on my hash table in a fraction of a second (based on my simple performance tests) but at the cost of memory – at any time there are empty spaces equaling anywhere from about 1 to 3 times the number of actual data points.

Here is a screenshot showing a printout of some stats and results of running my tests twice:

![Performance Screenshot](https://ymerejsasnak.github.io/perfpic.png)

-----

### Android App

[Android ePortfolio](https://github.com/ymerejsasnak/ePortfolio)

Yet another school project. This is a functional, though ugly and SO FAR from perfect, Android ePortfolio app that allows users to add text, images, sounds, etc and store them in an SQLite database and then view and/or play them back. 

-----

## Miscellaneous Projects

C++ and GLSL code to render a pretty bad-looking wooden spoon:  [OpenGL Spoon](https://github.com/ymerejsasnak/OpenGLSpoon)  

Part of a reverse engineering project. Assembly to C translation provided here as a text file: [Assembly to C conversion](https://github.com/ymerejsasnak/ymerejsasnak.github.io/blob/master/assemblyToC.txt)

Unfinished implementation of an [LC-3](https://en.wikipedia.org/wiki/Little_Computer_3) virtual machine in C:  [LC-3 Virtual Machine](https://github.com/ymerejsasnak/lc3_vm)

Actually pretty cool maze game...though lacking lots of polish:  [Python Maze Game](https://github.com/ymerejsasnak/THE-MAZE)

First attempt at implmenting a simple genetic algorithm:  [Python Genetic Algorithm](https://github.com/ymerejsasnak/python-ga)

Old Javascript Browser Games:
- [Browser Terrarium Simulation](https://github.com/ymerejsasnak/terrarium)
- [Browser Memory Game](https://github.com/ymerejsasnak/memory-game)
- [Browser Snake-Like Game](https://github.com/ymerejsasnak/snake)
- [Browser Lights Out Game](https://github.com/ymerejsasnak/lights-out)

A couple interesting Ruby things:
- [Ruby CLI Web Server and Browser](https://github.com/ymerejsasnak/cli-web-server-and-browser)
- [Ruby Mergesort](https://github.com/ymerejsasnak/mergesort)

-----

[contact me](mailto:Jeremy.JK.Kansas@gmail.com)
