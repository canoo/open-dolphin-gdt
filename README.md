
#GDT Templates for Open-Dolphin

## Installation
* if not done already install gdt: see see [gdt](https://github.com/svene/directory_template)
* invoke: gdt.sh install -github canoo open-dolphin-gdt

## Update
If you already have installed open-dolphin-gdt but want to use a newer version of a template update open-dolphin-gdt as follows:

* gdt.sh update open-dolphin-gdt

## Open Dolphin template

Directory Template to start a new [Open Dolphin](http://open-dolphin.org/) project.

* create an empty directory and cd into it
* invoke: gdt.sh opendolphin

You can run the application in two modes, the develop/test/debug mode and the remote mode.

To run it in develop mode invoke:

* gradle :combined:run

which should show a small window with a button on it. If you click it you should see some messages
on the terminal illustrating the commands which are sent from client to server and vice versa.


To run int in groovy and development mode invoke:

* gradle runWithGroovy

To run it in remote mode invoke:

* gradle jettyRun

and in a second terminal

* gradle :client:run

Note that the client and the server communication messages now appear in the client respectively server terminal.

To continue have a look at the Open Dolphin tutorial of [DolphinJumpStart](https://github.com/canoo/DolphinJumpStart)

