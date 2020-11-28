# SIMHContainer

Containerize SIMH and add an API to it.

Docker build for latest SIMH.

Python tools:

- Connect to Remote Console, and provide an gRPC control plane.
  - Base configuration.
  - Dynamically modify configuration.
  - Disk/tape mounts, paper tape mounts, card reader.

- Line printer controller.   Connect a FIFO to printers, watch printer spoolers,
 create PDF files automatically.   Handle overprint/underline/bold automatically.
 I'd love old fashioned printer art to work.   Handle mounting different form sizes.
 Possibly handle overlay of a "green bar" background.
- Printer terminal emulator and frame buffer - make PDF audit -- useful for console.  LA-36/120/180
- Video terminal emulator and frame buffer.   Manage VTxxx terminals.
- Paper tape controller.
- Card punch controller.
- Plotter controller (though Simh doesn't have controllers for this -- I may add one).
- Blinkenlight interface -- this will likely be in C since the rpc interface is mostly in C.  
I'm thinking ultimately that this would be a streaming interface via gRPC or Kafka.

I am mostly interested in the DEC emulators, and the Altairs.  But I will try to make many of these generic.
There maybe a generic configuration (a json packet), and eventually there may be mongo backing database, or
a gRPC interface into a configuration system.

This package is intended to be the handler for a VR emulator system, a graphical simulation, which I intend to be fully functional.

Dockerhub:   https://hub.docker.com/repository/docker/thorhalbert/simhbase
