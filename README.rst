
1. Welcome
==============

If you're reading this, you are probably thinking about contributing to the `DVC-Viking-Robotics <https://github.com/DVC-Viking-Robotics>`_ software part of the DVC Viking MASCCOT robot project. 
This is your starting point; think of this readme file as a the "GO" space on a Monopoly board game. You start here, land on a task, then come back around for another "GO" because all useful links will be contained here.


Our Progress
-------------
It's important that you know what we've done so far.

1. Fall 2018: `We built a small bluetooth-controlled rover <http://dvcrobotics.tech/timeline/>`_
2. Spring 2019: `We built the prototype for an autonomous DVC Viking tour-guide robot <http://dvcrobotics.tech/about-us/>`_
3. Fall 2019: `Right now! We are finishing our prototype to make the viking robot fully autonomous. It will drive from one side of the campus to the other without human assistance by the end of this semester <https://github.com/DVC-Viking-Robotics/about-us/blob/master/README.rst#our-progress>`_

2. What technologies are we using?
==================================
The mobile wifi controller that we created is hosted on a python webserver. In addition to that, we are using other programming technologies to optimize the controller and render it more efficient and user-friendly. 

If you aren't familiar with many of these terms, don't worry! Your first step should be to look up information on them so you are familiar with the terminology and utility. Here is a list:

Programming languages:
-----------------------
* Python (primary programming language)
* Flask (a python framework that facilitates the process of launching a standalone webserver)
* Javascript (used to dynamically update content on the webapp pages to display robot updates & transmit data)
* C++ (used on arduino's, that pipe sensor data to the server)

Protocols (Serial, Transfer, etc.):
-----------------------------------
* HTTP Requests
* Websocksets
* I2C 
* SPI
* Serial

Hardware & Sensors:
-------------------
- Ultrasonics
- Camera
- 9Dof sensor (Gyroscope, magnetometer, accelerometer)
- GPS (and RTK-GPS)
- Encoders (*not yet implemented*)
- LIDAR (*not yet implemented*)


3. What Do I Need to Know?
=============================

When contributing to a organization or community, they'll always recommend you review the "contributing guideline" document. No one ever really reads through the guidelines because they are usually long-winded and can get very complicated. The general rule for contributing is to keep things professional. Read our `contributing guidelines <https://github.com/DVC-Viking-Robotics/about-us/blob/new-guidelines/Contributing%20Guidelines.rst>`_.

The main programming language we use is Python. We also use C++ for software running on the Arduino. Other languages that are specific to web design include: HTML, CSS, and (if you dare) JavaScript.

4. What If I Am New/Rusty at Programming?
=================================================

That's good! Our primary goal as an organization is to learn, sharpen, and hone the skills you'll probably need in the world outside our small spectrum. Here are some links to great "learning-the-basics" resources to get you started:

* `Sololearn <https://www.sololearn.com/>`_ has some great walkthroughs on `Python <https://www.sololearn.com/Course/Python/>`_, `C++  (not arduino, but very similar) <https://www.sololearn.com/Course/CPlusPlus/>`_, `HTML <https://www.sololearn.com/Course/HTML/>`_, `CSS <https://www.sololearn.com/Course/CSS/>`_, `JavaScript <https://www.sololearn.com/Course/JavaScript/>`_, and many others. They also have an app on mobile platforms for `iOS <https://itunes.apple.com/us/app/id1210079064>`_ and `Android <https://play.google.com/store/apps/details?id=com.sololearn>`_; learn while you're on the toilet! Okay, its not Dr. Suess' "Green Eggs and Ham", but the walkthroughs are quick, easy, and painless.

* The best way to learn is to get your feet wet. That is to say: take a deep breathe and jump right in. This method may seem a little overwhelming, but we encourage asking your fellow team members for help and insights.

5. OK. OK. Where do I Jump In?
==================================

The following links will show tasks that need doing related to the software that runs on the robot. They are loosely ranked at:

1. `"Beginner" (for the Noobs) <https://github.com/DVC-Viking-Robotics/webapp/issues?q=is%3Aissue+is%3Aopen+label%3Abeginner>`_
2. `"Apprentice" (for those seeking a challenge) <https://github.com/DVC-Viking-Robotics/webapp/issues?q=is%3Aissue+is%3Aopen+label%3Aapprentice>`_
3. `"Master Wizard" (for those with experience that want to break through their knowledge's limits) <https://github.com/DVC-Viking-Robotics/webapp/issues?q=is%3Aissue+is%3Aopen+label%3A%22master+wizard%22>`_

If you're interested in web design, you need look no further. the repository that this README.rst lives in is our webpage's home. It sorely needs some tender love and care. We are open to different solutions in this regard

For instance this readme is written in a markup language reStructuredText ("rST" for short). rSt is being used to document our software (in the source code comment blocks) and host it on `ReadTheDocs.org <https://rtfd.io>`_. Our aim is to allow the software we write to be used by anyone trying to mimic ro improve upon it in their own context.
