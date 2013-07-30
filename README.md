
#GDT Templates for Open-Dolphin

## Installation
* if not done already install gdt: see see [gdt](https://github.com/svene/directory_template)

Install the standard templates:

* gdt.sh install dt_java

Install the open-dolphin template:
* gdt.sh install -github canoo open-dolphin-gdt

##Troubleshooting
if you still have an old version of 'dt_java' it might still contain the old 'opendolphin' template which will
cause a conflict with the one from 'open-dolphin-gdt'. So if there still is a folder '~/.gdt/dt_java/templates/opendolphin'.
do a 'gdt.sh update dt_java'. In case it is still existing remove the folder '.gdt/dt_java' and do a fresh install of 'dt_java':

* gdt.sh install -github svene dt_java

## Update
If you already have installed open-dolphin-gdt but want to use a newer version of a template update open-dolphin-gdt as follows:

* gdt.sh update open-dolphin-gdt

## Using the Open Dolphin template

Directory Template to start a new [Open Dolphin](http://open-dolphin.org/) project.

* create an empty directory and cd into it
* invoke: gdt.sh opendolphin

Install the gradle wrapper and make it executable:
* gdt.sh gradlewrapper
* chmod +x gradlew

You can run the application in two modes, the develop/test/debug mode and the remote mode.

To run it in develop mode invoke:

* ./gradlew :combined:run

which should show a small window with a button on it. If you click it you should see some messages
on the terminal illustrating the commands which are sent from client to server and vice versa.


To run int in groovy and development mode invoke:

* ./gradlew runWithGroovy

To run it in remote mode invoke:

* ./gradlew jettyRun

and in a second terminal

* ./gradlew :client:run

Note that the client and the server communication messages now appear in the client respectively server terminal.

To continue have a look at the Open Dolphin tutorial of [DolphinJumpStart](https://github.com/canoo/DolphinJumpStart)

