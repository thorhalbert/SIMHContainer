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
 Possibily handle overlay of a "green bar" background.
 
 - Printer terminal emulator and frame buffer - make PDF audit -- useful for console.  LA-36/120/180
 
 - Video terminal emulator and frame buffer.   Manage VTxxx terminals.
 
 - Paper tape controller.
 
 - Card punch controller.   
 
 - Plotter controller (though Simh doesn't have controllers for this -- I may add one).
 
