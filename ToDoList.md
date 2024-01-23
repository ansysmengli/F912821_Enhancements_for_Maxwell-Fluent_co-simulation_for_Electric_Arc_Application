# F912821_Enhancements_for_Maxwell-Fluent_co-simulation_for_Electric_Arc_Application
This feature is the enhancement for electrical arc modeling simulation. The co-simulation happens among AEDT, Fluent, Twin Builder, and Motion using System Coupling. 

# SYC time sequences
[SC Sequence diagram.pdf](https://github.com/ansysmengli/F912821_Enhancements_for_Maxwell-Fluent_co-simulation_for_Electric_Arc_Application/files/14027905/SC.Sequence.diagram.pdf)



# Task status table
| Task   |   UI Code Changes status |  UI test status |  Solver test status |  QA test status |    
|----------------|---------|---------|---------|---------|
| Core Dialog | :heavy_check_mark:  | :heavy_check_mark: | N/A | ❌
| SCP file (new qunatities and restart)  | :heavy_check_mark:  | :heavy_check_mark: | N/A | ❌
| Workflow (with Motion)  | 🕛  | 🕛 | N/A | ❌
| Validation (dialog user input)  | :heavy_check_mark:  | :heavy_check_mark: | N/A | ❌
| Property windows | N/A  | N/A | N/A | N/A
| Solution management | N/A  | N/A  | N/A | N/A
| Postprocessing | N/A   | N/A  | N/A | N/A
| I/O | N/A  | N/A | N/A | N/A
| undo/redo | N/A  | N/A | N/A | N/A
| scripting | N/A  | N/A | N/A | N/A
| Solution invalidation | N/A  |  N/A  | N/A | N/A
| Optimetrics (parametric sweep)  | N/A  | N/A | N/A | N/A
| 3D component | N/A  | N/A | N/A | N/A
| Feature flag protection (add for motion and completed for surface loss)  | ❌  | ❌ | N/A | ❌

:heavy_check_mark:: completed

❌: not completed

🕛: in progress


# To Do List and issues for futher
## Mesh related
- If we do not have geometry change, then we do not need to have re-mesh in Maxwell
- For initial steps if we can get initial mesh with default conductivity then we do not need to simulate and make adaptive simulation with default conductivity, this may save also some time.
- After the mapping from Fluent then we need to make adaptive simulation, we can map the Fluent results to each adaptive mesh of Maxwell
## Linux releated
- For parallel computing, Maxwell can not be connected in Linux using batch script
## Surface Loss UI
- Simulate the loss with the following formular:
Cathode: Q̇ c=Ji(Vc+Vi−Φc)= Ki* Resistive Sheet/Thin Layer bc loss (nonlinear) + ki*J*(15.58V-4.65), Anode: Q̇ a=Je(Va+Φa)=ke* Resistive Sheet/Thin Layer bc loss (nonlinear)  + ke*J*4.65
![image](https://github.com/ansysmengli/F912821_Enhancements_for_Maxwell-Fluent_co-simulation_for_Electric_Arc_Application/assets/110839247/eb653e63-a24d-4f19-afb8-0fac1bf8b8ce)




