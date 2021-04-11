# Homological Perspective on Data

+ **[Organizational document.](https://karhunenloeve.github.io/STDA/tda_seminar.pdf)**
+ **[Slides of initial lecture.](https://karhunenloeve.github.io/STDA/FAU-Beamer.pdf)**
+ **[Introduction to persistent homology.](https://karhunenloeve.github.io/STDA/main-pershom.pdf)**
+ **[References for further reading.](https://gist.github.com/karhunenloeve/bd85b3527e339ab9d9b4e83aa5e189d5)**

Topological data analysis describes a field in computational topology that uses methods of algebraic topology to investigate sets of points using computer algebra. A particularly prominent tool is persistent homology.
Algebraic topology describes, characterises and distinguishes topological spaces. In this seminar we concentrate on tools for the calculation of homology groups on a filtration of the space. A filtration is a set of subsets up to a given space that induce an exact sequence of homomorphisms.

If we have a discrete set of points of a tame function f: U → ℝ, we want to specify the changes of their sublevel sets along this function. These sublevel sets have the form ℱ(f,c) = {x |  f(x) ⩽ c}. Starting with the smallest value, we want to show changes in the function. We know from calculus that the number of locally connected components changes only by extreme values. For a local minimum, a new connected component appears. For a local maximum, two connected components are merged. Thus we iterate through the values of the function {y₀, y₁, ... }, considering a finite set and defining a step size to obtain a discrete countable finite set, so that ||xₘ - xₗ|| = e for m > l. In each local maximum, we have two connected components that have the creation values c and c' for the time of their creation. We assume that c ⩽ c'. So the adjacent component with the value c is younger than the component with the value c', since the latter was created at a later function value. We merge the younger component with the older one and store this event as tuple (c,d) ∈ ℝ², where d is the local maximum of the function. If we run the whole function this way, we have a family of tuples describing all the changes of f. Since the very first connected component (the one created with the smallest function value) cannot be merged with another, this connected component is persistent throughout the run and will be persistent in all future. Therefore, d receives the value ∞. We now refer to the space of the tuples as extended Euclidean space ℝ² ∪ ∞. Since we consider the tuples as points in extended Euclidean space, we obtain a diagram, the so-called persistence diagram.

The seminar introduces which information can be read from a persistence diagram, how persistence diagrams are efficiently calculated and how this diagram is related to the so-called persistent homology. Furthermore, to generalize the example, it will be worked out how persistent homology can be calculated on multivariate data. You guess right, that persistence diagrams encode a ton of interesting features of data.

# Organizational details

+ *Participation:* If you want to participate in the seminar, please be present in all seminar units, especially in the first one, and actively participate in the discussions.
+ *Date and room:* So far our seminar room 08.130 of the Chair of Data Management (Computer Science 6, Friedrich-Alexander University Erlangen-Nuremberg) has been selected, but this could change. I will inform you by e-mail if there are any organizational changes.
+ *Preparation*: Every seminarist is obliged to make an appointment with me in the week before his or her presentation, in which we check possible difficulties and the quality and correctness of the notes and slides.
+ *Examination:* A seminar paper (8-10 pages) must be written on the presentations topic (60-80 minutes including questions during the presentation) and at the latest be submitted to me in electronic form the week after the lecture. The seminar papers are provided on the StudOn page of the seminar. The module grade is composed of: the evaluation of the presentation (50%) and the evaluation of the seminar paper (5\%).

# Lectures
+ Each presentation should last a maximum of 80 minutes and should include at least 60 minutes (10-15 minutes time for questions during the lecture). Projector, Powerpoint, overhead slides and blackboard writings are all permitted.
+ The most important aspects are that (1) you have understood exactly what you are talking about and (2) your presentation communicates the content to your fellow students in an understandable and educative way.
+ Try to design your presentation in such a way that you want to hear it yourself and that you have real added value over reading the underlying text in a textbook. Of course you can and should add or omit details or structure statements differently. This also includes explaining or pre-calculating geometric examples.
+ Many of the concepts discussed are not directly accessible. You will probably have to edit your texts several times to gain some understanding of the topic and to add many steps that are not described in detail in the literature. If you do not understand a particular concept, please make an appointment with me in time.
+ Begin preparing your presentation in time. Late preparation regularly turns out to be a problem in seminars. You probably need much more time for preparation than you think.
+ Plan your slides carefully. A disorganized presentation will reduce the quality of your talk. You should not only think about what you want to say, but also how and in what form you want to introduce and illustrate the concepts. Think about what is really essential and avoid too detailed text in your slides. 
+ Practice your presentation alone or with other students before you give it in the seminar. If you decide to use the blackboard, practice your presentation aloud with a fellow student or alone. Think about what exactly you want to show on the blackboard and write down your ideas beforehand.
+ Your seminar paper is a scientific paper. You must therefore list all sources used, both in the presentation and in the written version prepared. The citation standard is up to you, but must be consistent throughout.
+ All books can be borrowed from the university library. Please make your own efforts to obtain the copies. All articles can be downloaded free of charge from the university network. If there are any problems, please check first if the article is available for FAU. If not, please write to me in time and I will send you the corresponding copy.
