
# Expected Productivity Gains From Virtual Reality Software Engineering Environments
// # What if we could use VR to create software?

I believe that software engineers could be more productive if they were able to work in a virtual reality (VR) environment.  VR enables software engineers to be completely surrounded in a truly three dimensional work environment, rather than being limited to a few 2D monitors in front of them.  VR also facilitates interaction—such as head rotation—that is both more familiar to users and more powerful than a traditional mouse and keyboard.

//VR devices render a slightly different image for each eye (stereoscopic rendering) which allows humans to sense depth in the images just like in the physical world. 

## True 3D
Previously, virtual 3D objects have been displayed on a 2D screen.  Rotation and movement are often allowed via mouse or keyboard controls but it is easy to forget the current orientation in relation to the big picture.  This is an issue fundamental to the problem of losing an entire dimension when displayed on a monitor.  VR overcomes this by literally allowing a user's view to complete an entire 360 degrees around them, just like in the physical world.  Having this immersive environment retains the third dimension and greatly helps users navigate the space and in essence, helps them get stuff done.

## Improved Interaction
Head mounted displays like the Oculus Rift are able to sense more of the human body.  The Rift can detect head rotation and head position relative to the camera in 3 dimensional space and rotates the virtual display in accordance to the user's muscle movement.  A novice user may have trouble remembering keyboard controls for 3D rotation, but they won't forget that simply turning their physical head controls the rotation.  Along with head movement, familiar hand gestures can also be used for more natural interaction and omni-directional treadmills would allow users to walk around their code by physically walking on the treadmill.

// ---------------

## Introduction

Programming environments from the previous decades still do not address programmer issues despite advances in psychology, neuroscience, and social aspects of software development.
As a result, problems still persist.  Developers still experience disorientation when navigating code~\cite{Henley:2014}.
Developers still experience problems comprehending code~\cite{Maalej:TOSEM:2014}.  These basic issues also impede other important software engineering activities. For example,
in code review, due to insufficient ability to navigate and understand the code under review, developers mostly report issues, such as convention violations, instead of discussing design flaws or defects
~\cite{bacchelli:ModernCodeReviewChallenges}.  

Researchers have explored the cognitive issues underlying several problems developers experience~\cite{Parnin:2012}.
For example, \emph{spatial memory}, a memory system in the parahippocampus that supports the ability to retain spatial awareness, is supported by place cells that fire as a person navigates through a physical space and other contextual cues in the environment.  Even after a single exposure, these memories can persist as long as a year.  The disorientation developers experience in programming environments often result from failures to engage a human's innate processing of spatial memory. Ko et al.~\cite{Ko:2006} observed that developers lost track of relevant code because they had to temporarily navigate to another location and forgot how to find the original location. This loss ocurred when the cues they relied on, such as position of scroll bars and document tabs, were disrupted as a result of their navigation.  Kuhn~\cite{Kuhn:2010} describes how developers maintain an internal spatial representation of code, and refer to code as being ``above or below'' other code.

\emph{Affordances} are devices that leverage innate cognitive mechanisms.
Researchers have attempted to improve interfaces that incorporate the human capacity for attention, cognition, and memory.
For example, in one study, participants organized their web bookmarks by positioning screenshots of the pages on various piles in a 3-dimensional space~\cite{Robertson:1998}. 

Similarly, researchers have incorporated affordances for spatial memory in programming environments.  Code Canvas~\cite{DeLine:CodeCanvas} positions code files on a large scrollable, zoomable plane which preserves stable spatial positions of code.  Code Bubbles~\cite{Bragdon:CodeBubbles} allows a developer to quickly position related fragments of code on an infinitely scrollable screen, which improves navigation and comprehension of fragments.  Patchworks~\cite{Henley:2014}, removes management of fragments and introduces a more stable layout, to improve disorientation that was still present with users of Code Bubbles.


Spatial memory is just one such affordance that can be leveraged to improve programming environments and there are many others that could be better used. 
This paper describes how head-mounted virtual reality (VR) displays coupled with gesture input provide several affordances not yet fully utilized in programming environments. 
We then describe several VR systems we have prototyped and how VR can be applied to software engineering.  Finally, we provide a brief discussion of future work, open research questions, and challenges of using VR in software engineering with existing technologies.



## Affordances in Virtual Reality
We describe a set of affordances that VR provides and describe the potential benefits of integrating them into programming environments.

### Spatial Cognition
Existing 3D visualizations attempt to take advantage of spatial cognition but lose much of their impact when displayed on a 2D screen~\cite{Teyseyre:Overview3DSoftwareVisualization}.
In contrast, head-mounted virtual reality displays allow the user to update their view by moving their body or rotating their neck, even a full 360 degrees.
Additionally, these displays render a slightly different image for each eye (stereoscopic rendering) which enables the human eye to more easily sense depth of images on the display.

Virtual reality can directly mimic the affordances offered by physical navigation. Based on electrocorticography (eCoG) recordings on the surface of the brain, place cells could be observed firing in the same sequence as a person navigated a virtual town and again when they later recalled the paths through the town~\cite{Ekstrom:2003}.


### Manipulation and Motion
The affordances provided by manipulation of a physical object can result in improved perception and retention. 
For example, the affordances offered by turning pages of a book result in increased comprehension and recall as when compared to reading the same text on computer displays~\cite{Noyes:2008}.
Additionally, the ability to serendipitously browse and relocate material is improved.
// http://embodiedknowledge.blogspot.com/2011/12/classic-experiment-by-held-and-hein.html
Motion in a physical space, through exertions such as walking, have important cognitive consequences~\cite{Oppezzo:2014}.
//Simply going for a walk increases creativity, even prior to starting the creative task~\cite{Oppezzo:2014}.
Other affordances can be aided by motion. For example, perception of depth is enhanced by self-actuated movement in a space~\cite{Held:1963}.

Researchers have explored integrating natural interactions with existing programming environments~\cite{Delimarschi:2014}.
Through input devices such as the Leap Motion, it is possible to physically interact with virtual objects.
Physical movement is also possible in virtual spaces.  Body harnesses\footnote{\url{http://cyberith.com/product/}} allow free movement in a virtual space such as walking, running, jumping and crouching.

### Liveness
Liveness is a powerful affordance that can be defined by the speed and level of responsiveness to actions offered by an environment~\cite{Tanimoto:Liveness}.
The potency of giving programmers a direct and immediate connection to their creations has been well illustrated in Bret Victor's seminal lecture, ``Inventing on Principle''~\cite{Victor:InventingOnPrincipleVideo}.//\cite{Victor:InventingOnPrincipleTranscript}.

When liveness is violated, the results can be nauseating.
Simulator sickness is distinct from motion sickness, in that it arises due to a mismatch between a person's interaction and the expected response of the environment.
For example, a person in virtual reality can become nauseous when they attempt to interact with the system but the system does not respond quickly enough.

## Applications
We have built VR prototypes for live coding and code review which concretely demonstrate the benefits of using the affordances of VR.
We argue that the benefits described in this section can also be extended to other software engineering activities.

Both of these systems use a head-mounted display (Oculus Rift - Development Kit 2) and a Leap Motion Controller for gesture recognition.

### Live Coding
\textsc{RiftSketch}\footnote{\url{http://www.youtube.com/watch?v=SKPYx4CEIlM}} is a live coding environment built for VR which allows users to describe a 3D scene using the Three.js library\footnote{\url{http://threejs.org/}}.
//It allows a user to describe a 3D scene using geometries, materials, textures, lights, meshes and other primitives provided by the Three.js library, which is a convenient wrapper for the WebGL APIs available in modern browsers. 
// TODO: add pic of RiftSketch

\textsc{RiftSketch} presents a user with a simple text editor, floating in front of them in an otherwise empty VR world. 
As the user types code into the editor, the world around them updates instantly to display the 3D scene dictated by their code. 
\textsc{RiftSketch} also allows the user to animate their scene via a callback function which is executed on every frame. 
The user can manipulate the state of the 3D scene in this looped block of code in order to add behaviour to the objects in their scene.
This animation makes the user truly feel \emph{inside} the scene in a way not captured by a 2D screenshot.

To assist in interaction with the keyboard, we allow reality to shine through by using a web camera mounted on the Rift and project that image in the system.
// TODO: add equipment pic and RiftSketch with webcam pic


### Liveness
\textsc{RiftSketch} demonstrates liveness by providing a tight feedback loop between code written and its effect in a virtual environment, and to quickly experiment with various solutions, algorithms and calculations. 
\textsc{RiftSketch} is also very promising as a learning tool since users can see their mistakes immediately and correct themselves without an intermediate compile step that might otherwise act as a hindrance.  
These benefits are especially evident in \textsc{RiftSketch} when the code describes a VR scene. 
As the authors have previously experienced, watching the entire virtual world change around you as you type can be an extremely powerful and engaging experience.

#### Hand Manipulation of Code
Furthermore, \textsc{RiftSketch} provides the user with shortcuts and input methods to quickly edit numbers in the code that they write. 
Keyboard shortcuts allow the user to increment or decrement numbers in the code by factors of 0.1, 10 or 100. 
Integration with the Leap Motion Controller provides users with the ability to manipulate numbers using an up and down hand motion.
This allows users to continuously modify a number using their hand and instantly see how this affects the scene, enabling faster feedback than manually typing one number at a time.
Numbers in the code could represent anything, from the X, Y or Z components of a position or rotation vector, the red, green or blue components of an object's material or a component in the calculation of an object's animated speed.

#### Usage Example
Consider the following scenario: A space mission has just landed a probe on the surface of a comet.
After 10 years in flight, the probe lands against all odds but in a position that is unable to receive sunlight.
Automated telemetry programs cannot find a feasible flight path.
As a programmer, you are tasked with updating the lander's software to reposition itself safely on solid ground and you have 24 hours before its batteries die and the probe deflects off the comet surface. 
Thankfully the companion orbiter has gathered detailed information about the surface around the landing site and telemetry data shows exactly where and how the lander is positioned.

You update your simulation with the data and step into \textsc{RiftSketch} to survey the situation. 
After assessing the lander's options, you iterate on possible solutions, first by using hand gestures to manipulate a possible path and scale thrust settings, 
and then the keyboard to refine the code. 
With each solution, you observe the lander's behavior inside \textsc{RiftSketch}.
You walk around the lander to inspect its position after each maneuver, leaning in to ensure that its feet are planted firmly in the regolith, and zooming out to an orbital view to verify that its new position maintains a line-of-sight to the orbiter on this lob-sided comet. 

Finally, after having run the simulation dozens of times in \textsc{RiftSketch}, you pass the software on to review.


### Code Review
\textsc{Immersion} represents methods as code fragments similarly to Code Bubbles~\cite{Bragdon:CodeBubbles} and displays groups of fragments as piles on the floor like BumpTop~\cite{Agarawala:BumpTop}.
Piles can be expanded into a more detailed ring for an overview and detail visualization~\cite{Shneiderman:InfoVisTaxonomy}.

// TODO: add pic of Immersion

#### Spatial Reasoning
The reviewer initially sees the active fragment in the center of the screen (see Figure~\ref{fig:Immersion}) with other relevant fragments distributed around the floor in piles. 
Reviewers use spatial cognition to judge the relevance of piles by how far away the pile is as well as the size of the pile.
The reviewer is able to scan the labels of the piles and number of fragments in each pile to quickly verify if each pile is indeed relevant.

\textsc{Immersion} divides the floor into sections based on packages of the system and color codes the sections to indicate how much that package has been modified by the code under review.
By walking between packages, we expect reviewers to have better mental models due to the increased usage of spatial reasoning.
Similarly, we expect that reviewers would be able to more easily recall review details after the review since the spatial elements of their brains were more engaged.

//\textsc{Immersion} uses semantic zoom to make method names readable even when at the back of the ring and the fragments retain a scaled height enabling the reviewer to approximate its length. 

### Gesture Interaction
Reviewers can make a grabbing motion to select a pile and then can pull their hand up to transform the pile into a ring of fragments for more detailed inspection.
The reviewer is now able to read the foremost fragment in the circle and can make horizontal finger swipes to rotate the circle and read other fragments. 
The reviewer can pinch the foremost ring fragment on the top and bottom and move it to the middle of the screen to become the active fragment.
If the reviewer wants to return to the previous method, they can move their hand as if clearing off a desk.

We have initially focused on supporting exploration--comments can be added via keyboard input, but we are investigating alternative ways to mark and flag code.


#### Usage Example
Consider the previous comet scenario where a programmer has implemented a repositioning flight path for the lander.

A reviewer puts on a Rift and enters \textsc{Immersion} to ensure this solution will actually work.
She notes an edge case which might cause a collision and suggests gently crashing the companion orbiter into the probe to avoid a larger collision.
The original programmer implements the suggestion in \textsc{RiftSketch}, ensures the simulation works and celebrates before submitting the correction to the reviewer.
However, the reviewer sees a section of code light up in \textsc{Immersion}.
As she walks over to the section she sees that it is the collision detection section warning that the system will not allow this code to execute outside of the simulator.
She realizes she can allow the execution by shutting off the engine just before impact to override the system.
They upload the code and the lander repositions itself as expected.


## Discussion
// TODO: improve heading

### Simulation
Interacting with a simulation might require positioning a virtual cursor which can be challenging when you only have a 2D view of the scene. 

VR, on the other hand, allows users to view, explore and manipulate simulated worlds directly. One can imagine a user physically turning their head to look around a simulated car plant or using their hands, via a Leap Motion controller, to interact with a simulated robot. 
These direct interactions provide a subtle but important advantage over 2D-projected simulations. 
This sense of immersion gives the users unimpeded access to the simulation which allows for quicker turn-around when testing or debugging the simulated software, especially if combined with an in-situ live coding solution like \textsc{RiftSketch}.

In practical applications, one could extend the concept of live coding and tight feedback loops in order to create customized programming environments. VR programming environments could allow the user to take advantage of the malleability and expanse of virtual worlds. For example, a user could live code a widget that indicates some statistic of the code they are currently editing, such as the cyclomatic complexity, test coverage or test result. The widget would update itself as the user typed, not unlike existing code feedback tools such as NCrunch \footnote{NCrunch automated concurrent testing tool: http://www.ncrunch.net/}, and they could position the widget in their virtual periphery.

// TODO - relate to comet


### Remote Collaboration
Both \textsc{RiftSketch} and \textsc{Immersion} could help facilitate remote collaboration.
Multiple programmers located around the world could join each other in a VR live coding space to figure out how to land the comet from the motivating example.
They would be able to provide extra insight and could arrive at the solution faster.

A different set of programmers could then join each other in a VR code review environment to review the proposed solution.
They are able to see what each person is thinking based on their annotations of the piles of information in their section of the system.

Co-located development teams are able to communicate in person. Distributed teams can try, but the technology is too slow and it doesn't feel right. High Fidelity \footnote{https://highfidelity.io/} is implementing infrastructure for virtual worlds that is fast enough for developers to be able to sense body language and hear audio in real time. Distributed development teams will have the foundational issues of remote communication solved which enables a shared VR environment to become truly powerful.

A benefit of co-location is pair programming, where two developers program at the same computer and can catch each others errors. VR and body sensing with a device like PrioVR would enable remote developers to be at a shared virtual desk right next to each other. They would be able to see the same files, talk in real time, and even point to which line of the code they are talking about. 

#### Pair Design
Co-located teams can design together around a whiteboard in a conference room as they talk through the problems of the system. A shared VR environment could have a similar room with sketching space that everyone can see. Developers could drag-and-drop files or code snippets to display on the walls around them. They could then discuss and annotate the code. Additionally, visualizations such as structure diagrams or architecture of related systems could be overlaid on a wall for reference.

#### Data Visualization
Remote workers could experience immersive visualizations together. A control flow graph could be represented by a maze of rooms through which the team could walk. The team members could trace different paths and yet still be shown an overlay of where each of the other members are and how these positions relate to each other. Currently remote workers can each trace separate paths of the code but have a hard time communicating what those paths are and how they relate to each other.

Remote workers often miss out on many benefits that in-person communication can bring. Shared VR spaces tailored to developers' activities can fill some of the gaps caused by distance and help the team to function better together. 


### Open Questions
\textbf{Degrees of Immersion.} 
Augmented reality devices such as Google Glass, aim to help the user complete tasks in the physical world by adding information overlays. Augmented reality seeks to help the user in the physical world while virtual reality seeks to completely replace physical reality. \emph{Is it more useful to immerse the user in a completely virtual environment, or to enhance their physical world?}


\textbf{Input Forms.}
Gaming console controllers work well for navigation and limited action support but are surpassed by keyboards at text entry. However, such devices require users to interact with both the physical and virtual worlds at the same time. Gesture recognition removes interaction with the physical world but can cause physical strain. Voice recognition could reduce strain but may feel awkward in a shared work space. \emph{What is the best way for the user to provide input to a VR system?}


### Challenges

#### Separation from the Physical
Putting on a VR headset means blocking out the rest of the physical world, including coworkers. Peers may lack the opportunity to ask questions and physical communication is stifled. Additionally, the VR headset wearer may have trouble interacting with the physical world while in VR. A webcam mounted to the headset enables some interaction with the physical world, as seen in Figure~\ref{fig:rift}, but has a limited field of view.

#### 3D Mapping
Some problems don't have an inherent 3D representation which makes display in VR a challenge. As seen in \textsc{Immersion}, 2D code can be displayed in VR but the code itself does not have a third dimension and thus loses the expressiveness of 3D. This could be an area well suited to 3D metaphorical programming as suggested by Ko et al.~\cite{Ko:LearningBarriers}.

#### Technology Limitations
The 1080p resolution of the Oculus Rift Development Kit 2 allows for passable text reading, but needs improvement for multi-hour sessions. The Rift also requires users to measure the distance between their pupils for more accurate stereoscopic rendering, but current utilities are either time consuming or hard to use properly. Eyeglass wearers must go through extra trial and error to see if the headset is best used with glasses on and a reduced field of view or replace their glasses with stronger lenses in the Rift and have increased blurriness.



## Conclusions
Two-dimensional development environments have not been able to take full advantage of affordances such as spatial cognition, manipulation, and liveness.
This paper describes a vision of how software engineering can use virtual reality for new kinds of tools that can take advantage of these affordances.
We described how both live coding and code review could benefit from VR tools but we envision many other software engineering activities can benefit from virtual reality as well.





//////////////////////////////////////////
//////// NOTES
//////////////////////////////////////////

//We describe our vision of what software engineering would look like with VR by illustrating various principles across four different immersive VR environments.
//First, we show how an immersive code review environment could enable software engineers to more easily analyze and navigate information which leads to increased understanding of the software. Secondly, we show how an immersive live coding environment could enable much faster development times when creating 3D scenes.
//Next we show how a social immersive environment could improve communication among remote development teams.
//Finally, we show how an immersive environment could be used to experience physical analogs of abstract software.
//We provide a brief discussion of some open research questions and discuss some of the challenges of using VR in software engineering with existing technologies.
//[Discussion]

//(stable locations), code bubbles (quick associations), patchworks (reduce view management issues in code bubbles).

//Andrew Bragdon has implemented a system called Code Bubbles that enables the user to pull out methods from a file. 
//The user is then able to move and group the methods as desired.  
//Code Bubbles also can display the call graph for the selected method and allows the user to open called methods.

//Code Canvas added semantic zoom to the Code Bubbles tool, allowing the user to gain a better understanding of how the current section of the system fits into the system as a whole~\cite{DeLine:CodeCanvas}.
// lacked a set of rich and stable environmental cues.

//Place cells, navigation, Kuhn (natural). Disorientation here.  Research has gradually introduced solutions that incrementally introduce elements that improve spatial memory support in programming environments (Desert, code canvas, code bubbles, patchworks, etc).  But where is the design ultimately heading?

//Understanding, navigating, and changing software systems is daily challenge for software developers.

//a main window for viewing content with a set of navigational links (tabs, tree views, and search results) to allow transitions between content.  
//Research advances: More advanced forms allow multiple fragments or windows software to be displayed at once.

//but limited design choices and increasing 
//scale of development efforts grate against these capacities.  
//Spatial memory.  Kuhn.

// http://www.scientificamerican.com/article/reading-paper-screens/
// http://healthland.time.com/2012/03/14/do-e-books-impair-memory/

//The choices developers have available so far is to choose between better links to software while coding in a main document (e.g. recommendation systems)
//or showing all the software (never escaping some form of view management due to the limited space to display content).


//The motivation for these approaches (spatial memory).

//Developers spend a large amount of time navigating source code.
//In a laboratory study of 10 experienced Java developers, Ko. Developers spent, on average, 35 percent of their time performing the mechanics of navigation within and between source files. Previously, I studied data~\cite{Parnin:2006b} from twelve programmers collected over several months of development activity in the professional workplace and found that developers work with 57--83 methods in a day (25\// and 75\// percentile respectively) and frequently switched between those methods as they worked. 60\// of transitions were to different classes.

//Observations of developers suggest they frequently rely on associations with \emph{environmental cues}\textemdash interface elements of the programming environment\textemdash 
//for navigating and understanding new code.  For example, Ko et al.~\cite{KoMaintenance06} observed that programmers use cues, such as open-document tabs and scrollbars, 
//for maintaining context during their programming tasks.  However, these cues are often insufficient: The act of navigation often disturbs the state of environmental cues, 
//and the paucity of interface elements, such as tabbed panes, which often only contain a file name, starves associability.
//In studies of developer navigation histories, a common finding is that developers frequently spend time flipping through open tabs because they fail to associate the tabs with desired code locations~\cite{Singer05}.

//Interactive displays of various sizes and form can greatly expand the mental workspace of developers.  
//Pulling aside a particular item of interest can be far easier and less costly than managing everything as a fragment or hoping for an 
//intelligent heuristic to provide access to the correct artifacts.

//[Applications of VR in software engineering]
// This section could be said in better words or bullet points, or VR, or *something*

