
# Using Virtual Reality to Create Software: A Likely Future

I believe that software engineers could be more productive if they were able to work in a virtual reality (VR) environment.  Why? Firstly, VR enables software engineers to be completely surrounded in a truly three dimensional work environment, rather than being limited to a few 2D monitors in front of them.  Secondly, VR facilitates interaction that is both more familiar to users and more powerful than a traditional mouse and keyboard such as head rotation.

## What is Virtual Reality?
For those who aren't familiar with [virtual reality](http://en.wikipedia.org/wiki/Virtual_reality), it is a big step towards allowing humans to interact with digital equipment in ways that are more like the physical world. These  interactions take more advantage of the capabilities of the human body potentially resulting in higher productivity, more creative opportunities, lower learning curves, and increased user satisfaction.

### Current VR Devices
This is currently accomplished mainly by devices like head-mounted displays such as the [Oculus Rift](https://www.oculus.com/). 

### Depth
The Rift renders a slightly different image for each eye (this is called *stereoscopic rendering*) which allows humans to sense depth in the images just like in the physical world. 

// TODO: how can this help?

### Body Movement
The dream of VR is, while seated at your computer, being able to think about walking down the street and this actually causes your virtual persona to walk down the street. (link to Brain computer interface with VR paper) Although this sounds crazy, a proof of concept experiment has already been run. This is nowhere near consumer availablilty though, but there are a plethora of devices already available that enable the computer to sense our physical body movement.  The Leap Motion Controller is a thumb sized device that can sense hand and finger bones quite precisely when placed near your keyboard. The Kinect camera can sense arm, leg, and torso movements accurately. An omnidirectional treadmill like Virtuix Omni allows physical walking to translate to avatar movement. Body harnesses like the Cyberinth further allow crouching and jumping.

// TODO: add links to devices

But wait, you may be asking the question: "Physical movement is cool, but what value does it add to VR?" We use our physical bodies everyday to accomplish all kinds of tasks. Most computers (desktops and laptops) are controlled via keyboard and mouse. Mobile computers (phones, phablets, and tablets) remove the mouse since we can use our fingers for control. This *direct manipulation* requires little explanation to new users

The end goal is *direct manipulation* where (http://www-ihm.lri.fr/~mbl/ENS/FONDIHM/2013/papers/Hutchins-HCI-85.pdf)

// TODO: how can this help?

#### Head Rotation and Movement
Rift wearers can even move their physical head to update their view of the virtual world. Rotating their physical head to the left actually causes the virtual world to rotate too!

#### Hand Gestures
Leap Motion, Data Glove, other new devices, company just bought by Oculus.

#### Lower-body Movement
Omnidirectional treadmills. 

#### Full body suits
PrioVR.

VR allows people to see in true 3D and allows for easier and more natural interaction. These advantages have started to revolutionize both [gaming](http://www.techradar.com/us/news/gaming/beyond-oculus-the-future-of-virtual-reality-gaming-1255974) and [film making](http://www.jauntvr.com/) and could revolutionize software engineering as well.

## True 3D
Previously, virtual 3D objects have been displayed on a 2D screen.  Rotation and movement are often allowed via mouse or keyboard controls but it is easy to forget the current orientation in relation to the big picture.  This is an issue fundamental to the problem of losing an entire dimension when displayed on a monitor.  VR overcomes this by literally allowing a user's view to complete an entire 360 degrees around them, just like in the physical world.  Having this immersive environment retains the third dimension and greatly helps users navigate the space and in essence, helps them get stuff done.

// taken from paper:
Existing 3D visualizations attempt to take advantage of spatial cognition but lose much of their impact when displayed on a 2D screen~\cite{Teyseyre:Overview3DSoftwareVisualization}.
In contrast, head-mounted virtual reality displays allow the user to update their view by moving their body or rotating their neck, even a full 360 degrees.
Additionally, these displays render a slightly different image for each eye (stereoscopic rendering) which enables the human eye to more easily sense depth of images on the display.

// Why will VR take off when 3D TV sucked?

## Improved Interaction
Head mounted displays like the Oculus Rift are able to sense more of the human body.  The Rift can detect head rotation and head position relative to the camera in 3 dimensional space and rotates the virtual display in accordance to the user's muscle movement.  A novice user may have trouble remembering keyboard controls for 3D rotation, but they won't forget that simply turning their physical head controls the rotation.  Along with head movement, familiar hand gestures can also be used for more natural interaction and omni-directional treadmills would allow users to walk around their code by physically walking on the treadmill.

// TODO: integrate the below paragraph.
For example, perception of depth is enhanced by self-actuated movement in a space~\cite{Held:1963}.

Researchers have explored integrating natural interactions with existing programming environments~\cite{Delimarschi:2014}.
Through input devices such as the Leap Motion, it is possible to physically interact with virtual objects.
Physical movement is also possible in virtual spaces.  Body harnesses\footnote{\url{http://cyberith.com/product/}} allow free movement in a virtual space such as walking, running, jumping and crouching.

// TODO
// Who will benefit the most from VR software engineering tools? 3D developers (for now)
// Will normal developers still benefit?

### Liveness
// TODO: Read Tanimoto's paper about Liveness levels and then show how/if VR fits in.
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
RiftSketch\footnote{\url{http://www.youtube.com/watch?v=SKPYx4CEIlM}} is a live coding environment built for VR which allows users to describe a 3D scene using the Three.js library\footnote{\url{http://threejs.org/}}.
//It allows a user to describe a 3D scene using geometries, materials, textures, lights, meshes and other primitives provided by the Three.js library, which is a convenient wrapper for the WebGL APIs available in modern browsers. 
// TODO: add pic of RiftSketch

RiftSketch presents a user with a simple text editor, floating in front of them in an otherwise empty VR world. 
As the user types code into the editor, the world around them updates instantly to display the 3D scene dictated by their code. 
RiftSketch also allows the user to animate their scene via a callback function which is executed on every frame. 
The user can manipulate the state of the 3D scene in this looped block of code in order to add behaviour to the objects in their scene.
This animation makes the user truly feel \emph{inside} the scene in a way not captured by a 2D screenshot.

To assist in interaction with the keyboard, we allow reality to shine through by using a web camera mounted on the Rift and project that image in the system.
// TODO: add equipment pic and RiftSketch with webcam pic


### Liveness
RiftSketch demonstrates liveness by providing a tight feedback loop between code written and its effect in a virtual environment, and to quickly experiment with various solutions, algorithms and calculations. 
RiftSketch is also very promising as a learning tool since users can see their mistakes immediately and correct themselves without an intermediate compile step that might otherwise act as a hindrance.  
These benefits are especially evident in RiftSketch when the code describes a VR scene. 
As the authors have previously experienced, watching the entire virtual world change around you as you type can be an extremely powerful and engaging experience.

#### Hand Manipulation of Code
Furthermore, RiftSketch provides the user with shortcuts and input methods to quickly edit numbers in the code that they write. 
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

You update your simulation with the data and step into RiftSketch to survey the situation. 
After assessing the lander's options, you iterate on possible solutions, first by using hand gestures to manipulate a possible path and scale thrust settings, 
and then the keyboard to refine the code. 
With each solution, you observe the lander's behavior inside RiftSketch.
You walk around the lander to inspect its position after each maneuver, leaning in to ensure that its feet are planted firmly in the regolith, and zooming out to an orbital view to verify that its new position maintains a line-of-sight to the orbiter on this lob-sided comet. 

Finally, after having run the simulation dozens of times in RiftSketch, you pass the software on to review.


### Code Review
Immersion represents methods as code fragments similarly to Code Bubbles~\cite{Bragdon:CodeBubbles} and displays groups of fragments as piles on the floor like BumpTop~\cite{Agarawala:BumpTop}.
Piles can be expanded into a more detailed ring for an overview and detail visualization~\cite{Shneiderman:InfoVisTaxonomy}.

// TODO: add pic of Immersion

#### Spatial Reasoning
The reviewer initially sees the active fragment in the center of the screen with other relevant fragments distributed around the floor in piles. 
Reviewers use spatial cognition to judge the relevance of piles by how far away the pile is as well as the size of the pile.
The reviewer is able to scan the labels of the piles and number of fragments in each pile to quickly verify if each pile is indeed relevant.

Immersion divides the floor into sections based on packages of the system and color codes the sections to indicate how much that package has been modified by the code under review.
By walking between packages, we expect reviewers to have better mental models due to the increased usage of spatial reasoning.
Similarly, we expect that reviewers would be able to more easily recall review details after the review since the spatial elements of their brains were more engaged.

//Immersion uses semantic zoom to make method names readable even when at the back of the ring and the fragments retain a scaled height enabling the reviewer to approximate its length. 

### Gesture Interaction
Reviewers can make a grabbing motion to select a pile and then can pull their hand up to transform the pile into a ring of fragments for more detailed inspection.
The reviewer is now able to read the foremost fragment in the circle and can make horizontal finger swipes to rotate the circle and read other fragments. 
The reviewer can pinch the foremost ring fragment on the top and bottom and move it to the middle of the screen to become the active fragment.
If the reviewer wants to return to the previous method, they can move their hand as if clearing off a desk.

We have initially focused on supporting exploration--comments can be added via keyboard input, but we are investigating alternative ways to mark and flag code.


#### Usage Example
Consider the previous comet scenario where a programmer has implemented a repositioning flight path for the lander.

A reviewer puts on a Rift and enters Immersion to ensure this solution will actually work.
She notes an edge case which might cause a collision and suggests gently crashing the companion orbiter into the probe to avoid a larger collision.
The original programmer implements the suggestion in RiftSketch, ensures the simulation works and celebrates before submitting the correction to the reviewer.
However, the reviewer sees a section of code light up in Immersion.
As she walks over to the section she sees that it is the collision detection section warning that the system will not allow this code to execute outside of the simulator.
She realizes she can allow the execution by shutting off the engine just before impact to override the system.
They upload the code and the lander repositions itself as expected.


## Discussion
// TODO: improve heading

### Simulation
Interacting with a simulation might require positioning a virtual cursor which can be challenging when you only have a 2D view of the scene. 

VR, on the other hand, allows users to view, explore and manipulate simulated worlds directly. One can imagine a user physically turning their head to look around a simulated car plant or using their hands, via a Leap Motion controller, to interact with a simulated robot. 
These direct interactions provide a subtle but important advantage over 2D-projected simulations. 
This sense of immersion gives the users unimpeded access to the simulation which allows for quicker turn-around when testing or debugging the simulated software, especially if combined with an in-situ live coding solution like RiftSketch.

In practical applications, one could extend the concept of live coding and tight feedback loops in order to create customized programming environments. VR programming environments could allow the user to take advantage of the malleability and expanse of virtual worlds. For example, a user could live code a widget that indicates some statistic of the code they are currently editing, such as the cyclomatic complexity, test coverage or test result. The widget would update itself as the user typed, not unlike existing code feedback tools such as NCrunch \footnote{NCrunch automated concurrent testing tool: http://www.ncrunch.net/}, and they could position the widget in their virtual periphery.

// TODO - relate to comet


### Remote Collaboration
Both RiftSketch and Immersion could help facilitate remote collaboration.
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
Some problems don't have an inherent 3D representation which makes display in VR a challenge. As seen in Immersion, 2D code can be displayed in VR but the code itself does not have a third dimension and thus loses the expressiveness of 3D. This could be an area well suited to 3D metaphorical programming as suggested by Ko et al.~\cite{Ko:LearningBarriers}.

#### Technology Limitations
The 1080p resolution of the Oculus Rift Development Kit 2 allows for passable text reading, but needs improvement for multi-hour sessions. The Rift also requires users to measure the distance between their pupils for more accurate stereoscopic rendering, but current utilities are either time consuming or hard to use properly. Eyeglass wearers must go through extra trial and error to see if the headset is best used with glasses on and a reduced field of view or replace their glasses with stronger lenses in the Rift and have increased blurriness.



## Conclusions
Two-dimensional development environments have not been able to take full advantage of affordances such as spatial cognition, manipulation, and liveness.
This paper describes a vision of how software engineering can use virtual reality for new kinds of tools that can take advantage of these affordances.
We described how both live coding and code review could benefit from VR tools but we envision many other software engineering activities can benefit from virtual reality as well.
