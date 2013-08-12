
# GDT Templates for Open-Dolphin

Directory Template to start a new [Open Dolphin](http://open-dolphin.org/) project.

### Recent changes
* 12.8.2013: it is not necessary anymore to install the *dt_java* templates.

### Prerequisites
* You need to have Java 1.7 or at least 1.6. Note that GDT does not work with Java 1.8 yet since groovy's @Grab annotations currently have
a problem with Java 1.8

* You need a groovy installation. I recommend [gvm](http://gvmtool.net/) to easily install and manage your groovy
installation.

## Installation
If not done already install gdt:

	groovy https://raw.github.com/svene/gdt_bin/master/gdt_setup.groovy

(for details see [gdt](https://github.com/svene/directory_template) )


Install the open-dolphin template:

	gdt.sh install -github canoo open-dolphin-gdt

### Update
If you already have installed *open-dolphin-gdt* but want to use a newer version of a template update open-dolphin-gdt as follows:

	gdt.sh update open-dolphin-gdt

### Troubleshooting
if you still have an old version of *dt_java* it might still contain the old *opendolphin* template which will
cause a conflict with the one from 'open-dolphin-gdt'. So if there still is a folder *~/.gdt/dt_java/templates/opendolphin*.
do a *gdt.sh update dt_java*. In case it is still existing remove the folder *.gdt/dt_java* and do a fresh install of *dt_java*:

	gdt.sh install -github svene dt_java

## Using the Open Dolphin Template

	mkdir mydolphin
	cd mydolphin
	gdt.sh opendolphin
	chmod +x gradlew

You can run the application in two modes, the *develop/test/debug* mode and the *remote* mode.

To run it in develop mode invoke:

	./gradlew :combined:run

which should show a small window with a button on it. If you click it you should see some messages
on the terminal illustrating the commands which are sent from client to server and vice versa.


To run int in groovy and development mode invoke:

	./gradlew runWithGroovy

To run it in remote mode invoke:

	./gradlew jettyRun

and in a second terminal

	./gradlew :client:run

Note that the client and the server communication messages now appear in the client respectively server terminal.

To continue have a look at the Open Dolphin tutorial of [DolphinJumpStart](https://github.com/canoo/DolphinJumpStart)

