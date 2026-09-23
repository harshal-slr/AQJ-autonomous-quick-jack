===============================================================
 AUTONOMOUS QUICK JACK (AQJ)
 Digital Modeling of Interactive Systems and Interfaces (DMISI)
 Universita degli Studi di Napoli Federico II (UniNa)
===============================================================

OVERVIEW
--------
The Autonomous Quick Jack (AQJ) is an automated vehicle-lifting device
that positions itself under a selected wheel and raises the vehicle with
minimal human intervention, aimed at faster and safer tire changes and
undercarriage inspections than a traditional jack stand.

This repository contains the project files: the SolidWorks CAD model,
a MATLAB / Simscape Multibody physics simulation, structural load-case
studies, and supporting documentation.

NOTE: All files are uploaded individually (flat), not in folders. Before
using the CAD or MATLAB model, download the files and place the related
ones together in a single folder on your computer so their internal
references resolve correctly (see HOW TO USE below).


REQUIREMENTS
------------
- SolidWorks (to open .SLDPRT parts, .SLDASM assemblies, .SLDDRW drawings)
  * SolidWorks Simulation add-in to open the .CWR study result files
- MATLAB / Simulink with Simscape and Simscape Multibody
  (developed with the Simscape Multibody Contact Forces Library v24.2.x,
   i.e. MATLAB R2024b or newer)
- A viewer for .STEP / .STL if you only need the neutral CAD geometry


FILES IN THIS REPOSITORY
------------------------
SolidWorks CAD (keep these together in one folder after download):
  - Autonomous Quick Jack.SLDASM   MAIN top-level assembly (open this first)
  - Body Assembly.SLDASM           body/frame sub-assembly
  - LM- Assembly_Final.SLDASM      linear-motion / lifting mechanism assembly
  - LM- Assembly_Final-CASE 1..4.CWR   SolidWorks Simulation load cases
  - Individual parts: Base Plate, Car_Base, body panels, AQJ_Wheel,
    Gearmotor, NEMA 17 motor, shafts, spacers, brackets, fasteners (.SLDPRT)
  - Gearmotor.STEP / nema 17.stp   neutral CAD geometry for other tools

MATLAB / Simscape Multibody simulation:
  - Contact_Forces_Library.prj     MATLAB project file (open this first)
  - aqj_one.slx                    main Simscape Multibody model
  - scenario_one.mat               simulation scenario / parameters
  - aqj_matlab_model.png           model screenshot
  - Simscape Multibody Contact Forces Library (v24.2.5.2)  required dependency

Documentation and results:
  - Autonomous Quick Jack.pdf / .SLDDRW   engineering drawing
  - LM- Assembly_Final-CASE *.docx / .LOG  simulation reports and logs
  - Autonomous Quick Jack.docx     project proposal
  - PW8_Autonomous Quick Jack.pptx  presentation
  - Project image renders (.png / .jpg)


HOW TO USE
----------
0. DOWNLOAD FIRST
   - GitHub's web preview cannot open SolidWorks or MATLAB files.
   - Download the files you need and group the related ones into a single
     folder locally so cross-references (assemblies, model paths) resolve.

1. VIEW THE CAD MODEL
   - Put all .SLDPRT, .SLDASM and .SLDDRW files in the same folder.
   - Open  Autonomous Quick Jack.SLDASM  in SolidWorks.
   - If any part is reported missing, point SolidWorks to the folder that
     contains the downloaded parts.
   - No SolidWorks? Use the .STEP / .STL files for geometry only.

2. REVIEW THE STRUCTURAL ANALYSIS
   - With the SolidWorks Simulation add-in enabled, open
     LM- Assembly_Final.SLDASM and load the CASE 1..4 (.CWR) studies.
   - Matching reports/logs are the LM- Assembly_Final-CASE *.docx follow the steps to perform load cases.

3. RUN THE PHYSICS SIMULATION
   - Keep the MATLAB files and the Contact Forces Library together in one folder.
   - Open MATLAB (R2024b or newer) with Simscape Multibody installed.
   - Open  Contact_Forces_Library.prj  (loads paths and dependencies),
     then open and run  aqj_one.slx.
   - scenario_one.mat holds the scenario parameters loaded by the model.

4. READ THE DOCUMENTATION
   - Start with the drawing PDF and the project image renders, then the
     proposal .docx and the presentation .pptx.


NOTES
-----
- SolidWorks assemblies only open correctly when every referenced part is
  in the same local folder.
- The MATLAB model depends on the Contact Forces Library; keep it in the
  same folder as the project file after download.


AUTHORS
-------
Harshal Rajesh Kokitkar
Shwetali Vitthal Bhuingade
Master's in Autonomous Vehicle Engineering, UniNa
