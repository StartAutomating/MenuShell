

[Official Website](http://MenuShell.Start-Automating.com)


    
    
### MenuShell is a sweet and simple PowerShell module to help you make console menus.


Because everyone wants them, and no one wants to make them by hand.


To use MenuShell, just use the command Start-MenuShell.   To exit menu shell, type exit or quit.


Here's a simple demo MenuShell to explore your system:


    Start-MenuShell -Menu @{
            "Processes" = @{
                "Get" = { Get-Process } 
                Run = { Start-Process }  
            }
            "Services" = @{
        
            }
            "Performance" = @{
                "CPU" = { Get-Counter '\Processor(*)\% Processor Time'  } 
                'Disks' = { Get-Counter '\PhysicalDisk(*)\% Disk Read Time', '\PhysicalDisk(*)\% Disk Write Time', '\PhysicalDisk(*)\% Idle Time', '\PhysicalDisk(*)\% Disk Time' } 
        
            }
            "Disks" = @{
                "%Free" = { Get-Counter '\LogicalDisk(*)\% Free Space' } 
            }
        } 



MenuShell is built with one simple command (Start-MenuShell) and one formatter.  It was written with the help of [EZOut](http://ezout.start-automating.com).

