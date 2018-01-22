To run this project and evaluate it you will need to host the files on a local server and then on the web with ngrok.
If you are new to this and need help just follow the directions below. Assumption is you are using Linux.

PREP
1. Load files on to your desktop main screen.

2. Open file path FEND7/src and install ngrok at the top level of the project.

3. Open terminal

4. cd to the files. example script: $> cd desktop/FEND7/src

5. Find out what version of python you have running by running $> python -V



HOST YOUR PROJECT
6a. If python 2 run $> python -m SimpleHTTPServer 8080
6b. If python 3 run $> python -m http.server 8080

7. Open up browser and type in url  localhost:8080

8. Open a new tab in your terminal.

9. cd to the files. example script: $> cd desktop/FEND7/src

10. Run $> ./ngrok http 8080 to host your locally hosted webpage on the web so you have a webpage that can be analyzed by Google Page Insights Tool

11. Copy url that appears in your terminal window and paste it your browser url field.

12. Open Google Page Insights and copy paste the same url to be analyzed.




