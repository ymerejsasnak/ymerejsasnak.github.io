# Welcome to my Portfolio
*...a perpetual work in progress...*

-----

## Introduction

Hello. My name is Jeremy. I tend to prefer JK. [contact me](mailto:Jeremy.JK.Kansas@gmail.com)

This portfolio started life as part of the capstone class for my CS degree, but I never really felt comfortable with the end result; the writing felt fluffy and bloated (as bad college writing too often does), and I spent far more time fulfilling the specific requirements of the assignment(s) and less time presenting my self and my work in a way that I felt best. As of this writing I have no professional work experience in programming or software development, though I have had some freelancing successes over the past couple months. Instead of droning on about myself, let's get into the projects.

-----

## Voltage Modular Modules

The following items are components to be used as part of Cherry Audio's Voltage Modular Eurorack-inspired software modular synthesis system. I designed and developed each of the modules below. As of this writing, I'm approaching about 200 sales over about three months, which while modest at best, I'm still happy with for such a niche product, and it shows that I can complete a fully working product people are willing to buy. 

In each instance, I worked to maintain a separation of concerns, using OOP principals to separate things out into sensible classes and associated methods.

, and thus created a class to handle individual audio samples, a class to manage the loading and playback of all loaded samples, and a class to calculate the random values to be used based on user-set parameters. I worked hard to make sure everything was well-formatted to remain readable and understandable, with clear variable/class/method names, attention to spacing, comments to indicate organization or explain less obvious pieces of code, etc. Still, it is not a polished masterpiece of development. While I have a great appreciation for elegant, beautifully architected code, I understand that the only real value that code has (aside from a learning experience) is in its life as a published product.

Working up to the release of this module presented a number of hurdles to overcome, including figuring out how to work within the system and API provided while achieving my design goals. Part of the API includes prebuilt generators and effects, but instead of using the built-in sample player, I found it better and more flexible to build my own for this and subsequent modules - thus making it important to make the code generic and uncoupled to thus be reusable. To save preset data, I needed to output a bytestream to the system, something I had not yet had opportunity to explore, but again I knew to turn to Java's documentation and was able to quickly learn the basics and apply that knowledge to the task at hand.

There were a few hard lessons to learn along the way. The first involved how sample data was saved: I had designed the module to only retain the pathname of the file and reload it each time a preset was reloaded, based on my own preference for keeping audio on disk rather than saving it within a project. And this was my error: designing based on my own personal use case, rather than considering different options for different workflows. I've since remedied this in subsequent updates. Sadly, the first of those updates provided another debacle, otherwise known as a "learning experience" - I changed the state saving code to account for various new options, including path vs file data, while completely ignoring any checks for old versions, thus rendering those bytestreams unusable. 

Version control (atomic commits with accurate messages)
class structures w/ oop principles striving for readability and reusability (get finished) self-doc
post-launch maintenance (feature reqs bugs)
various algorithms and techniques - interpolation (linear and cubic), byte streams, threads, etc
documentation, changelogs
debugging
email team, customer, forums, etc

iterative development (like agile??)

research into antialiasing and oversampling

optimization/graphics

*I have not made the code for these publicly available, though I can share it upon request.*

### Random Sampler

<img src="https://ymerejsasnak.github.io/rsamp.png" height="300">



[Random Sampler on the Cherry Audio store](https://store.cherryaudio.com/modules/jks-random-sampler)

### Sample Scrubber

<img src="https://ymerejsasnak.github.io/scrubber.png" height="300">

[Sample Scrubber on the Cherry Audio store](https://store.cherryaudio.com/modules/jks-sample-scrubber)

### CV Canvas

<img src="https://ymerejsasnak.github.io/cv2.png" height="300">

[CV Canvas on the Cherry Audio store](https://store.cherryaudio.com/modules/jks-cv-canvas)

### Sample Swarm

<img src="https://ymerejsasnak.github.io/swarm1.png" height="300">

[Sample Swarm on the Cherry Audio store](https://store.cherryaudio.com/modules/jks-sample-swarm)




-----






### Selected School Projects (?)

I'd rather get into the projects right away, but I guess for those interested, I'll give a little introduction to myself. Skipping this is fine. Anyway, I am a passionate (perhaps obsessive?) problem solver and an intensely critical thinker. I love to exercise both my powers of creativity and logical thinking - and nowhere is this better on display that in my explorations into where music and programming meet. I have an insatiable thirst for knowledge, an interest not just in computer science topics such as interests range from artificial intelligence, to games and graphics programming, to creativity and education software, to an emerging interest in legacy systems and embedded systems, to mathematics – but I also have a long-standing and deep-seated love and respect for topics in art, history, literature, music, psychology, and so much more.


While common wisdom often tells us to specialize, to focus on an area of expertise, I can’t help but be more of a generalist. Twist my arm a bit and I'll say my focus lies in back-end Java. OK?Still, I think my inherently interdisciplinary nature has its own value, which is too often overlooked. Not just in computer science – where my  Coupled with all of this is my strong ability to direct my own learning process, something I’ve been doing naturally for much of my life, now exercised and honed through years of online coursework. Even now, I am furthering my knowledge and understanding of digital signal processing (at least, specifically as it applies to sampled audio), something I was not able to “officially” study before.


But any intellectual challenge can be great Whether it be reconstructing C code from a disassembled binary, or manipulating vectors in order to build shaders for OpenGL graphics, or coding a successful merge sort, I still find that if I am presented with the logical building blocks, so to speak, I love nothing more than to find a way to fit them together to solve the problem at hand. At the same time, I’ve developed my ability to relate the piece of whatever puzzle I am currently dealing with to the bigger picture, the end goal.

I emjoy solitary work, but I understand the value of communication and collaboration to create any significantly complex projects.
collab. Most significant systems or components are too complex for a single person to realistically create and support alone, thus collaboration is key. The only way for people to collaborate successfully on a project is to help each other out, to properly outline requirements and carefully implement designs, to use coding best practices such as good naming conventions and formatting and commenting, to test code before submitting it for review, to graciously accept constructive criticism, to accurately log security issues, to provide audience appropriate documentation – in a single word, at every step in the process, it’s all about communication.


With all of that said, we can now move on to a few specific artifacts that showcase some of my knowledge and abilities. I feel it’s quite difficult to illustrate the full range of my potential with a limited number of examples – take them, then, for what they are: working software artifacts that I’ve created, that show some specific problems solved using some specific techniques or tools. From these, I hope one can mentally extrapolate to the potential projects these actual projects may hint at. Less abstractly, these artifacts are also a record of much of what I mentioned above: self-directed learning, creativity and problem solving, a wide range of interests. Finally, these artifacts, all of them, are flawed. It’s important to note that I am well aware of these flaws – the areas where security is weak or features are incomplete or code is a horrid mess – and I am able to communicate this understanding to others, and I am able to, given time, address these flaws. Still, software, as a product of the human mind – a beautiful and powerful and incredibly flawed thing in itself – this is almost inevitable. As we wrestle against the intricate requirements of complex systems, nothing is ever finished, everything is a work in progress, but so is life.

Finally, a quick rundown of what you'll find here, with links: the first section is Vm, then school, then other interesting(old) github things

Note for portfolio:

“no illusions that this is “production ready” code in any sense, but it does show that I have the skills and knowledge to meaningfully contribute to an existing codebase”

demonstrated teamwork, initiative, and the ability to finish a project and get it to market
Customer communication, ca communication etc
50%-good solution that people actually have solves more problems and survives longer than a 99% solution that nobody has because it’s in your lab where you’re endlessly polishing the damn thin

“””

-----

### Other Older Projects (?) 

-----


### Software Engineering and Design

Next, let me direct you to the first of those artifacts, a simple REST API for performing CRUD operations on a MongoDB database:

[Client/Server code](https://github.com/ymerejsasnak/clientserver)

And also, a narrative on why I chose this item, what enhancements I made, and what I learned:

To fulfill the category of software engineering and design, I have chosen to revisit my final project from CS 340 (Client/Server Development). In this project, I created a basic Python program to perform database operations on a MongoDB database using the Pymongo library. I implemented create, read, update, and delete operations, as well as a few more specialized operations specific to the provided database. In addition, I integrated a simple microserver on top of that using Bottle.py and created a RESTful API to allow a client entity to access to the underlying CRUD functionality, and ultimately the Mongo database itself, via HTTP requests.

This particular artifact, even in its original state, was one of my favorite projects to come out of my education. I enjoyed the taste of the “full stack” experience with all of the separately interacting layers – the database, the APIs, the HTTP requests. I feel that this project showcases knowledge of a lot of different skills and tools, including using NoSQL databases, working with the JSON format, developing Python code, learning and incorporating unfamiliar libraries (Pymongo, Bottle), implementing REST APIs, and understanding HTTP protocols. However, despite all this, the original project falls far short of software design ideals. It was then my desire to improve the program by restructuring according to object oriented principles, thus making the code more modular and reusable, better prepared for potential collaboration, extension, and maintenance. In addition, making the code more robust and secure with the inclusion of unit tests, more checks for errors, and overall attention to security, showcases the ability to identify weaknesses and be mindful of quality control. Finally, ensuring everything is readable, especially in thoroughly updating each method’s doc string, helps in future enhancements and collaboration by making the code more comprehensible. Looking at it in a positive light, it could be said that I laid the groundwork for the further enhancement of the artifact by myself or others, though the code as yet falls far short of what I hoped for.

With the enhancements I have made, despite my lukewarm feelings about them, I have still touched on four of the five course outcomes. In making the code more readable and maintainable, I am preparing it for others who may have to work with it, thus paving the way for more painless collaboration. Both in writing about the artifact here, and in more thoroughly documenting the code, I have further exercised my ability to communicate about software and code in writing. As noted above with regard to each different element that was a part of this, I have demonstrated my ability to use techniques and tools, and to scour documentation and learn new tools as necessary to reach development goals and implement required functionality. Finally, while not reaching the ironclad fortress I had initially hoped for, inclusion of more checks for flaws and errors at least put the code on the right path to safety, though far more work in that regard would be needed.

While the entire enhancement process has given me more experience with all of the tools involved, and further developed my ability to analyze how understandable my code is in preparation for others to view or interact with it, a different lesson stands out to me. This particular enhancement has taught me that I still need to plan a project in far more detail before being able to accurately gauge the difficulty and effort/time requirements. I originally felt that such a simple project (essentially four core operations spread across two interacting classes) could easily be brought up to a near-professional level in about a week. While I still believe, given far more time to research each library more thoroughly, improve my Python ability, and devise more thorough tests, I could come close to attaining this ideal, I simply had unrealistic expectations given my level of knowledge and experience. Upon diving in deeper into the Python code and the libraries used, I found my understanding of them to be far less than I had first assumed; this should have been no surprise, for in any sub-area of development knowledge, what I know will likely always be outweighed by what I don’t know. I think remembering that and remaining humble and realistic in the face of it is a very important lesson – but also, with a computer science background, it is easier to know how to learn what is needed for the project at hand, and how to use relevant documentation, and how to implement new ideas and employ new technologies. In addition, given that I was one person working over a very constrained time frame, could I truly expect the polished piece of professional software that existed in my mind? Still, as mentioned above, I have managed to mold the project into a new shape, so to speak, and have added a basic framework of unit tests, and have updated the readability of everything by improving naming and writing extensive doc strings. All of this makes the project more conducive to further such enhancements, at least nudging it a bit closer to that ideal I had hoped for. 

---

### Data Structures and Algorithms

Next we have the second artifact, a script for pulling data from a RaspberryPi with attached GrovePi, and a hash table for storing the data for quick lookup:

[WetSpec and Hash Table](https://github.com/ymerejsasnak/wetspec-script)

And again, a narrative describing the piece and the process:

To fulfill the second category of the ePortfolio, which is centered on data structures and algorithms, I have chosen to add a hash table to my Emerging Systems final project. The original artifact is a script for gathering weather data using a Raspberry Pi and Grove Pi attachment with sensors. The project is simple in that its main function is to periodically record values for temperature and humidity from the attached sensors. These values are then stored in a list and written to a JSON file. I had always felt that the data storage aspect could be improved upon and so decided to implement a simple hash table in which to store the values instead (which again could easily be formated in JSON if necessary).

For this category, I initially had trouble coming up with an idea that didn’t feel contrived or redundant. In the end, I settled on the hash table idea because I felt it would be an interesting challenge, an opportunity to build a useful data structure from scratch, and to weigh all the various algorithmic and storage considerations that come along with that. Of course, in a real world scenario, it would be a lot easier to just use a built-in structure – such as Python’s dictionary, or if more complex data storage is desired, a full-fledged database – but only through creating my own hash table and thinking through the different considerations and trade-offs did I actually feel I was exercising my knowledge and abilities. With my hash table, the data can now be looked up by a specific date and time with much better performance than simply linearly searching through a list of all items. Compared to the built-in Python dictionary, however, my hash table is almost 10 times slower. Still, given that mine was created in a short period of time while the Python data structure is something that’s been improved and fine-tuned over many versions, I consider that a success.

This enhancement met the course objectives I expected it to. Its primary purpose, as far as objectives were concerned, was to showcase my problem solving ability, my ability to think algorithmically and apply computer science practices, and also my ability to evaluate the various trade-offs, such as efficiency or memory usage, one must consider in any solution. But this enhancement, as any, also allows for further demonstration of coding best practices – whether for readability and collaboration or for security. Also, it provides yet another opportunity for showing my ability to communicate in writing, in both a descriptive and analytical fashion.

In the end, this piece of the project taught me a lot, but in ways that initially surprised me. The actual implementation of the core structure of the hash table class and its methods was much easier than I had anticipated, but fine-tuning its operation proved to be very challenging. The date/times used as keys were difficult to hash effectively because they were generally regularly spaced values (each was ‘rounded,’ so to speak, to the nearest half hour mark). I tried various tricks to make the values hash more randomly, but nothing worked to my liking, so I returned to my original plan, which was just performing a modulus operation of a numerical representation of the key by the size of the table. Because of this simplicity of the hash function, the table size became more important and really needed to be a prime-valued size to help spread out the entries. I toyed with non-prime tables since they would be easier to resize, but ultimately found them to have far too many collisions. Next, my initial plan had been to resize the table when it reached about 75% capacity, but this proved to be too high given that my collision resolution strategy was straightforward linear probing (inserting the data into the first non-colliding index) so I settled for about 50% capacity. From this we come to the most glaring example of a difficult trade-off: I can perform over 10,000 random look-ups on my hash table in a fraction of a second (based on my simple performance tests) but at the cost of memory – at any time there are empty spaces equaling anywhere from about 1 to 3 times the number of actual data points.

![Performance Screenshot](https://ymerejsasnak.github.io/perfpic.png)

---

### Databases

To fulfill the databases category, I again went back to my [Python and MongoDB Client/Server](https://github.com/ymerejsasnak/clientserver) project. Whereas in the first category, I made a number of general improvements to the original program, this time I focused on adding another level to the software stack, allowing access to the database via HTML and asynchronous Javascript calls.

This item offered a lot of opportunity to explore and showcase different skills as it had many different moving parts interacting in various ways. Of course, the fact that it is centered around CRUD operations on a database makes it a perfect choice for the database category, and the enhancement provided many opportunities to reflect on various aspects of accessing databases from different layers of the software stack. I think this is best highlighted by the care and awareness that must be maintained as messages are transmitted through each layer of the stack. We have string input converted to JSON in an HTTP request, following Python method calls down to Mongo commands, before finally returning a result and propagating it up through the stack to be displayed in the message window of the form. Also, in a lot of systems, the database is essentially invisible to many average users, so this enhancement is also important in that it touches on how everything connects – from end user actions with an app or web page, down to the storage of the data itself – and addresses real-world database function.

This artifact and the implemented enhancements further support course outcomes. Awareness of collaboration and a team environment means I always strive to keep code readable and free of other issues so that others may view it or work with it without confusion. Again, as with the other two enhancements, this one provided an opportunity to exercise code review skills and verbal communication skills during the planning stages, then to exercise written communication skills and analytical skills during the composition of the narrative. As I’ve already written, and will elaborate on further below, this enhancement shows a variety of skills and tools. I was unable to directly address security in my enhancement, due to some challenges and time constraints outlined below, but this artifact does present a great opportunity to at least be aware of necessary further enhancements to address security issues.

This enhancement came with many different challenges, some expected and some not. For one, I knew when initially choosing this enhancement that I might be taking on a bit of risk in that I hadn’t actually written any HTML or Javascript in five or more years. There were, in fact, some moments early on where I wasn’t sure how to proceed. However, as in earlier enhancements, I found that my education and previous experience allowed me to find resources and apply new syntax and commands on top of already familiar concepts of software construction and algorithmic thinking, making it fairly easy to adapt to these unfamiliar languages and paradigms. I was able to progress, in a matter of days, from not even remembering how to structure an HTML document to having a functioning (if minimal and maybe a bit ugly) web interface for a database. As I’ve written elsewhere, this ability to quickly learn and adapt to different technologies, libraries, tools, etc. should be invaluable in a field often driven by innovation.

Not all went smoothly, however. I had many issues initially with trying to get the index.html page to actually communicate with the Bottle.py server I had running locally. I was getting error messages related to Cross Origin Resource Sharing, which I was vaguely familiar with from prior web experience, but I didn’t understand how it applied to my situation. Then I realized, on my machine, I was running the server on “localhost” but loading the HTML file directly from my C drive, which the browser interpreted as different origins. From here, I just had to figure out how to statically serve files directly from Bottle, so that the index.html would also come from the same host, and this issue would be resolved. Through this, I was able to exercise problem solving and research skills to resolve my issue, and get a deeper understanding of web programming in the process.

This enhancement also really drove home the value of collaboration and separation of duties. As usual, while first setting out to perform this enhancement, I had a smoothly-functioning, nice-looking, error-free web page in mind – and I could get there, given much more time. But for such a software stack to be fully functional, user friendly, and perhaps most of all secure, a team would be better able to achieve this as each could focus on different aspects: back end, front end, UI/UX, visual design, testing, security, etc. As a solo developer within very limited time constraints, I could really only hope to lay the groundwork for the ideal concept I had, enacting core functionality – but through well-formatted and commented code, as well as helpful git commit messages with small and frequent commits, I would hope to pave the way for others to more easily find their way when contributing to my base code.


