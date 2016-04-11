#CircuitJS1

##Introduction

CircuitJS1 is an electronic circuit simulator that runs in the browser. It was originally written by Paul Falstad as a Java Applet. It was adapted by Iain Sharp to run in the browser using GWT.

For a hosted version of the application see:

* Paul's Page: [http://www.falstad.com/circuit/](http://www.falstad.com/circuit/)
* Iain's Page: [http://lushprojects.com/circuitjs/](http://lushprojects.com/circuitjs/)

Thanks to Edward Calver for 15 new components and other improvements. Thanks to Rodrigo Hausen for file import/export and many other UI improvements. Thanks to J. Mike Rollins for the Zener diode code. Thanks to Julius Schmidt for the spark gap code and some examples. Thanks to Dustin Soodak for help with the user interface improvements. Thanks to Jacob Calvert for the T Flip Flop. 

##Building the application

The tools you will need to build the project are:

* Eclipse - I am using the Kepler version.
* Google plugin for Eclipse to provide GWT.

This archive is a project folder for your Eclipse project space. Once you have a local copy you can then build and run in development mode or build for deployment. Running in development mode is done using the normal Eclipse run button or "Run As..." and choosing "Web Application (Super Dev Mode)" and then picking "Circuitjs1.html" as the initial page. Building for deployment is done using the Google button on the Eclipse taskbar and choosing "GWT Compile Project...".

GWT will build it's output in to the "war" directory. In the "war" directory the file "iframe.html" is loaded as an iFrame in to the spare space at the bottom of the right hand pannel. It can be used for branding etc.

##Deployment

* "GWT Compile Project..." as explained above. This will put the outputs in to the "war" directory in the Eclipse project folder. You then need to copy everything in the "war" directory, except the "WEB-INF" directory, on to your web server.
* Customize the header of the file "circuitjs1.html" to include your tracking, favicon etc.
* Customize the "iframe.html" file to include any branding you want in the right hand panel of the application


The link for the full-page version of the application is now:
`http://<your host>/<your path>/circuitjs1.html`
(you can rename the "circuitjs1.html" file if you want too).

Just for reference the files should look like this

```
-+ Directory containing the front page (eg "circuitjs")
  +- circuitjs.html - full page version of application
  +- iframe.html - see notes above
  ++ circuitjs1 (directory)
   +- various files built by GWT
   +- circuits (directory, containing example circuits)
   +- setuplist.txt (index in to example circuit directory)
```
   
## Embedding

You can link to the full page version of the application using the link shown above.

If you want to embed the application in another page then use an iframe with the src being the full-page version.

You can add query parameters to link to the full page version to change it's startup behaviour. The following are supported:
```
.../circuitjs1.html?cct=<string> // Load the circuit from the URL (like the # in the Java version)
.../circuitjs1.html?startCircuit=<filename> // Loads the circuit named "filename" from the "Circuits" directory
.../circuitjs1.html?euroResistors=<true|false>
.../circuitjs1.html?whiteBackground=<true|false>
.../circuitjs1.html?conventionalCurrent=<true|false>
```

## License

This program is free software; you can redistribute it and/or
modify it under the terms of the GNU General Public License
as published by the Free Software Foundation; either version 2
of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program; if not, write to the Free Software
Foundation, Inc., 51 Franklin Street, Fifth Floor, Boston, MA  02110-1301, USA.