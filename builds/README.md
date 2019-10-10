# temporalx license hack test

run through the registration process and "break" it.

What defines broken?

* You can use the same "UUID" (referred to as Temporal UUID) to register more than one machine
* You can use the same license on more than one machine
* You can use more than one license on one machine
* You can bypass the registration and license validation process entirely
* You can generate the same license across multiple machines
* You should not be able to display the application help without registering the machine you are running it on

With respect to the last point, you should not be able to display
```
NAME:
   tex-cli - TemporalX command-line management tool

USAGE:
   tex-cli-client-hack-amd64-linux [global options] command [command options] [arguments...]

VERSION:
   v1.0.0-rc1-3-g3f26dc5

AUTHORS:
   Alex Trottier <postables@rtradetechnologies.com>
   George Xie <georgex@rtradetechnologies.com>

COMMANDS:
   client   gRPC client subcommands
   config   configuration management tools
   admin    admin commands
   help, h  Shows a list of commands or help for one command

GLOBAL OPTIONS:
   --bootstrap, --bp          bootstrap against public ipfs
   --config PATH, --cfg PATH  load the configuration file at PATH (default: "./config.yml")
   --help, -h                 show help
   --version, -v              print the version
```

# registration process

You will have 5 UUID's to play with that may be used once per UUID, so you can generate up to 5 licenses for use on 5 different machines (these could be virtual machines, physical devices, etc...)

To register a machine you'll want to set one of the UUIDs you are given as an environment variable named `TEMPORAL_UUID`. Once you do that simply run the executable. On 64bit linux platforms you would simply run `$ ./tex-cli-client-hack-amd64-linux`
