# Source tree #

----------
## contrib ##
Code contributed by the community.
This code is usually not maintained
by the developers but by the respective
community contributors.


## direct ##
Mid-level tools/subsystems which supports show development,
and scene-composition.  It contains pretty much *all* of Panda's Python code with some C++.  
Includes code which sets up and initializes PANDA (using Python
wrapper functions which call low-level C++ counterparts).  
Includes python modules for mid-level show coding systems: 
actors, directdevices (high-level wrappers around low-level 
input devices such as joysticks, magnetic trackers, etc.), 
finite state machines, 2D gui elements,
intervals, tasks, and the DIRECT tk widget classes and panels.


## dmodels ##
Similar to /models but processed by makepanda, models that still need to be converted to .egg at build time

Their origin is probably Disney

## dtool ##
This tree contains base classes and core functionality that the
other Panda libraries rely on, such as basic threading constructs, 
file reading/writing constructs and the configuration system. 
It also contains interrogate, which is used to generate Python bindings for Panda3D.

## makepanda ##
Panda3D building system.


## models ##
Contains some free models for use in samples.
They origin is probably CMU


## panda ##
Low-level 3D graphics engine code.  Primarily C++.
 
Includes code for graphics/scene graph setup/manipulation/rendering,
graphic state guardians (interfaces to OpenGL, Direct X, tinypanda(based on TinyGL)), 
and source code for many PANDA systems:
animation, audio, gui, input devices, particles, physics, shaders, etc.

### android ###
-update me-

### androiddisplay ###
-update me-

### audio ###
-update me-

### audiotraits ###
-update me-

### awesomium ###
-update me-

### bullet ###
Panda has classes that represent underlying bullet objects, that basically wrap around it and integrate it with Panda classes and structures.

For instance, there's BulletRigidBodyNode, which is a class that extends a PandaNode and as such can be placed inside the panda scene graph. 
However, it stores a btRigidBody object from bullet, and exposes methods that are wrappers around that underlying Bullet object.

### cftalk ###
connected frame protocol

### chan ###
Animation channels.  This defines the various kinds of
AnimChannels that may be defined, as well as the MovingPart class
which binds to the channels and plays the animation.  This is a
support library for char, as well as any other libraries that want
to define objects whose values change over time.

### char ###
-update me-

### cocoadisplay ###
-update me-

### collada ###
-update me-

### collide ###
This package contains the classes that control and detect collisions

### configfiles ###
This package contains the housekeeping and configuration files needed by things like attach, and emacs.

### cull ###
This package contains the Cull Traverser.  The cull traversal collects all
state changes specified, and removes unneccesary state change requests.  
It also
does all the depth sorting for proper alphaing.


### device ###
Device drivers, such as mouse and keyboard, trackers, etc...  
The base class for using various device APIs is here.


### dgraph ###
Defines and manages the data graph, which is the hierarchy of devices, tforms, and any other things which might have an input or an output and need to execute every frame.

### display ###
Abstract display classes, including pipes, windows, channels, and display regions.

### distort ###
-update me-

### doc ###
Documentation Panda3D developers considered that doesn't fit in any of the packages.
For contents please see the part 2 ("other") of this manual.


### downloader ###
Tool to allow automatic download of files in the background.

### downloadertools ###
-update me-

### dxgsg9 ###
Handles all communication with the DirectX backend, and manages state to minimize redundant state changes.

### dxml ###
-update me-

### egg ###
A.k.a. the "egg library", this reads, writes, and manipulates egg files.  It knows nothing about the scene graph structure in the rest of the player; it lives in its own little egg world.

### egg2pg ###
A.k.a. the "egg loader", this converts the egg structure read from the egg library, above, to a scene graph structure, suitable for rendering.

egg2pg reads egg file and converts it to a Panda scene graph. 
ie. in-memory structure of PandaNode etc. 

I'm assuming "pg" stands for "panda graph".

Also, technically, the "egg" tree reads the .egg file into in-memory
 EggData structures, and egg2pg converts those to scene graph structures.
When egg2pg converts that into  scene graph structures egg files
from memory get deleted. If you want to keep them around, you can use
 the lower-level interfaces yourself.

### egldisplay ###
-update me-

### event ###
Tools for throwing, handling and receiving events.

### express ###
-update me-

### ffmpeg ###
-update me-

### framework ###
A simple, stupid framework around which to write a simple, stupid demo program.  Handy for quickly writing programs that can open a window and display the OmniTriangle.

### gles2gsg ###
-update me-

### glesgsg ###
-update me-

### glgsg ###
 Handles all communication with the GL backend, and manages state to minimize redundant state changes.

### glstuff ###
-update me-

### glxdisplay ###
X windows display classes that replace Glut functionality.

### gobj ###
Graphical non-scene-graph objects, such as textures and geometry primitives.

### grutil ###
-update me-

### gsgbase ###
Base GSG class defined to avoid cyclical dependency build.

### iphone ###
-update me-

### iphonedisplay ###
-update me-

### linmath ###
Linear algebra library.

### mathutil ###
Math utility functions, such as frustum and plane

### movies ###
-update me-

### nativenet ###
-update me-

### net ###
Net connection classes

### ode ###
-update me-

### osxdisplay ###
-update me-

### pandabase ###
-update me-

### parametrics ###
-update me-

### particlesystem ###
Tool for doing particle systems.  Contains various kinds of particles, emiters, factories and renderers.

### pgraph ###
-update me-

### pgraphnodes ###
-update me-

### pgui ###
-update me-

### physics ###
Base classes for physical objects and forces.  Also contains the physics manager class.

### physx ###
-update me-

### pipeline ###
-update me-

### pnmimage ###
Reads and writes image files in various formats, by using the pnm and tiff libraries. 
PNMImage class manages reading and writing image files from disk.

One of the properties of PNMImage is that all images are laid out (almost) the same way in memory, regardless of their properties. This makes it very easy to write a class like PNMPainter, which can paint equally well on grayscale, grayscale/alpha, 24-bit, 32-bit, or 64-bit images. 

### pnmimagetypes ###
-update me-

### pnmtext ###
-update me-

### pstatclient ###
-update me-

### putil ###
-update me-

### recorder ###
-update me-

### rocket ###
-update me-

### skel ###
-update me-

### speedtree ###
-update me-

### testbed ###
C test programs, that primarily link with framework.

### text ###
Package for generating renderable text using textured polygons.

### tform ###
Data transforming objects that live in the data graph and convert raw data (as read from an input device, for instance) to something more useful.

### tinydisplay ###
-update me-

### vision ###
-update me-

### vrpn ###
Defines the specific client code for interfacing to the VRPN API.

### wgldisplay ###
Windows OpenGL specific display classes.

### windisplay ###
-update me-

### x11display ###
-update me-


## pandatool ##
This tree contains various utility tools that are used to manipulate model
files and convert models from other formats to Panda3D's .egg format (and vice versa).


## samples ##
Contains samples to demonstrate how Panda3D works.


