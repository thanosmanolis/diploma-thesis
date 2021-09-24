# riot_mde

A library for modelling devices (supported by [RIOT](https://github.com/RIOT-OS/RIOT)) and their connections, providing auto generated source code.

riot_mde provides a DSL (Domain Specific Language) for defining devices and connections between them. The DSL has been built using [textX](https://github.com/textX/textX) and through custom parsers the defined models are then used to generate code and diagrams.

Usage
-----
```
usage: riot_mde [-h] [--connections CONNECTIONS]

arguments:
  -h, --help            show this help message and exit
  --connections CONNECTIONS
                        Filename of a connection specification.
```

### Code generation

Currently only devices that exist in folder [supported_devices](riot_mde/supported_devices) are supported. 

After the definition of the devices and their connection has been done
the source code could be generated by
```
$ riot_mde --connections connection.con
```
The file connection.con should be located in folder [test_connections](test_connections). 

The result of this command is a C file with name of the connection file and a Makefile, both located to the folder [codegen](riot_mde/codegen).

Installation
--------------------

To install this repo:

    $ git clone https://github.com/robotics-4-all/2020_riot_mde_thanos_manolis
    $ python setup.py install
