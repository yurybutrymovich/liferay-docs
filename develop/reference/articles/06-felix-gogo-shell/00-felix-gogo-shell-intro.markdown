# Felix Gogo Shell [](id=using-the-felix-gogo-shell)

To interact with @product@'s module framework, you can use the Felix Gogo shell.
To access it, use a telnet client to connect to port `11311` of your Liferay
server's machine. Since the shell is accessible through telnet, it is only
available on the local network interface. Use the following command if you're
running Liferay locally:

    telnet localhost 11311

Once you connect, you should see a message that says *Welcome to Apache Felix
Gogo*. The prompt looks like this:

    g!

Here are some useful Gogo shell commands:

`help`: lists all the available Gogo shell commands. Notice that each command
has two parts to its name, separated by a colon. For example, the full name of
the `help` command is `felix:help`. The first part is the command scope while
the second part is the command function. The scope allows commands with the same
name to be disambiguated. E.g., scope allows the `felix:refresh` command to be
distinguished from the `equinox:refresh` command.

`help [command name]`: lists information about a specific command including a
description of the command, the scope of the command, and information about any
flags or parameters that can be supplied when invoking the command.

`lb`: lists all of the bundles installed in Liferay's module framework. Use
the `-s` flag to list the bundles using the bundles' symbolic names.

`b [bundle ID]`: lists information about a specific bundle including the
bundle's symbolic name, bundle ID, data root, registered (provided) and used
services, imported and exported packages, and more

`headers [bundle ID]`: lists metadata about the bundle from the bundle's
`MANIFEST.MF` file

`diag [bundle ID]`: lists information about why the specified bundle is not
working (e.g., unresolved dependencies, etc.)

`packages [package name]`: lists all of the named package's dependencies 

`scr:list`: lists all of the components registered in the module framework.
(*scr* stands for service component runtime.)

`services`: lists all of the services that have been registered in Liferay's
module framework.

`install [path to JAR file]`: installs the specified bundle into Liferay's
module framework

`start [bundle ID]`: starts the specified bundle

`stop [bundle ID]`: stops the specified bundle

`uninstall [bundle ID]`: uninstalls the specified bundle from Liferay's module
framework

For more information about the Gogo shell, please visit [http://felix.apache.org/documentation/subprojects/apache-felix-gogo.html](http://felix.apache.org/documentation/subprojects/apache-felix-gogo.html).

