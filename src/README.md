**** READ ME ****

PROJECT
---
WEBSITE OPTIMIZATION - UDACITY FRONT END DEVELOPER NANODEGREE


DEVELOPER CONTACT
---
fictitious at gmail dot com


BUILD TOOLS
---
Sublime Text v3.0
ngrok
Python v3.6.0
Google Developer Tools 01/2018
Google Page Insights 01/2018
ImageMagick v7.0.5
Node.js v6.10.2
GRUNT

OPTIMIZATIONS
---
index.html -> needed updates to it's Critical Render Path
- render blocking css inlined
- img files resized to lowest possible dimensions in order to reduce file download size
- async .js files removed from Critical Render Path


views/js/main.js -> frames rate was not meeting standard 60fps
- resizePizzas() was rewritten as it was computationally costly with adding any value. Scope of original
function was recalling multiple computations and looking up numbers every time the loop ran causing Forced Synchrounous
Layout Changes that were causing massive jank, ipso facto effecting user experience. Simplified greatly. Used Classroom lesson to iron it out.


views/js/main.js -> computational inefficiencies for dynamic functionality
- updatePositions() reduced number of pizzas program was updating and declared consistent variables outside of scope of loops to reduce the number of instances a variable be created therefore reducing computational power being used.


GENERAL USAGE NOTES
---
If you would like to run this project and evaluate it you will need to host the files on a local server and then on the web with ngrok.
If you are new to this and need help just follow the directions below. Assumption is you are using Linux.


TO EVALUATE
---
1. Load files on to your desktop main screen.

2. Open file path FEND7/src and install ngrok at the top level of the project.

3. Open terminal

4. cd to the files. example script: $> cd desktop/FEND7/src

5. Find out what version of python you have running by running $> python -V

6a. If python 2 run $> python -m SimpleHTTPServer 8080
6b. If python 3 run $> python -m http.server 8080

7. Open up browser and type in url  localhost:8080

8. Open a new tab in your terminal.

9. cd to the files. example script: $> cd desktop/FEND7/src

10. Run $> ./ngrok http 8080 to host your locally hosted webpage on the web so you have a webpage that can be analyzed by Google Page Insights Tool

11. Copy url that appears in your terminal window and paste it your browser url field.

12. Open Google Page Insights and copy paste the same url to be analyzed.

13. Open Google Dev Tools and evaluate fps.




