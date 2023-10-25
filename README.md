# LINACS Window’s User Installation Guide

This is a guide for the installation and execution of the LINACS code in a Windows environment.    


# 1.)	Programs

1.1)	Required:
 
•	LINACS codes
Contains all the subroutines for the design and multiparticle tracking.
There are several folders: 
o	LINACSsrfSIM contains all the subroutines.
o	LINACsrfSIMrun has all the scripts to run the program and analyze the outputs.
o	References contain detailed information about the input scripts and related publications.
o	Hlists has files to generate the Hofmann chart.

•	Absoft Tools program
It is a set of Fortran compilers for Microsoft Windows. It compiles the subroutines on LINACS to create the executable for running the program.
A license was required, but Absoft has now gone out of business. An alternative free-source compiler option may become available.
•	Python
LINACS GUI and Graphics tools run in a Python environment.
•	Kivy
An open-source software library for the rapid development of applications equipped with novel user interfaces, such as multi-touch apps

1.2)	Recommended:

•	PyCharm
An integrated development environment used for programming in Python in Windows.


# 2.)	Installation

The user is assumed to have downloaded and installed the auxiliary programs (Absoft Tools, Python, PyCharm, and Kivy).

For the installation of Python in Windows, please check this website (https://www.python.org/downloads/windows/).

For the installation of PyCharm, please check this website (https://www.jetbrains.com/help/pycharm/installation-guide.html).

For the installation of Kivy, please check this website (https://kivy.org/).


1)	Copy the two directories (LINACSsrfSIM and LINACsrfSIMrun) in the desired place of your computer.
2)	Open Absoft Tools and create a new project. Under this new project set the path of folder LINACSsrfSIM. We recommend using the preferences that appear in Fig.1.

   ![Fig1](https://github.com/Byeerendon/LINACS-Window-s-User-Installation-Guide/assets/65529667/ea387f27-e84b-444a-8bf6-aff0f54a2218)
      
                                        Figure 1. Absoft Tools preference settings.             
3)	Go to the LINACsrfSIMrun folder, open linacgui.py, and update the path according to the location of your folders (LINACSsrfSIM and LINACsrfSIMrun), as shown in Fig. 2.

  ![Fig2](https://github.com/Byeerendon/LINACS-Window-s-User-Installation-Guide/assets/65529667/c9703cb7-1f33-4afa-8d35-27230f034793)

                                           Figure 2. linacguis.py script.

4)	In the LINACsrfSIMrun folder, open linacgui.kv and update the path according to your files.
5)	In LINACsrfSIMrun folder, open LINACSGUIsupport.bat. This is an executable used for the compilation of the subroutines. Here you must update the path according to the location of your folders, kivy, and Absoft Tools program, see Fig.3.

![Fig3](https://github.com/Byeerendon/LINACS-Window-s-User-Installation-Guide/assets/65529667/82f896d8-1690-4f8f-b97f-8d8d1625411f)
 
                                        Figure 3. LINACSGUIsupport.bat script.

6)	In the LINACsrfSIMrun folder, open LINACSsimGraphics and update the paths according to your files.

 

# 3.)	Run

1)	In the LINACsrfSIMrun folder, open the tapeinput.txt file.  This file provides all the inputs necessary to run the program. 
2)	A detailed explanation of the inputs is given in LINACSrfqSim_Card_instructions.txt and an example is provided in the book Elements of Ion Linear Accelerators + Calm in the Resonances and Other Tales, R.A. Jameson, and The LINACS Codes Release, both on ResearchGate. 
3)	Modify and save the input parameters according to your design.
4)	Open Pycharm and run linacgui.py (Fig. 4).

 ![Fig4](https://github.com/Byeerendon/LINACS-Window-s-User-Installation-Guide/assets/65529667/b2c5fc51-db6f-4294-86e0-1d30184444b4)

                                    Figure 4. Execute the linacgui script in Pycharm.

5)	A GUI command will appear, select RFQ, and modify the inputs according to your design, as shown in Fig. 5. Detailed information can be found in The LINACS Codes Release.

 ![Fig5](https://github.com/Byeerendon/LINACS-Window-s-User-Installation-Guide/assets/65529667/c6d66724-f837-4b3c-ab95-ef8f7a7245f2)

                                     Figure 5. GUI control of LINACS

6)	Click run RFQ Vane Design, to generate the RFQ design. See Fig. 6. 

 ![Fig6](https://github.com/Byeerendon/LINACS-Window-s-User-Installation-Guide/assets/65529667/3e99ff6f-ebc1-489c-ad20-9a3ce2e35fb5)

                                     Figure 6. Output run of the RFQ Vane design.

7)	To run multiparticle tracking, click the buttons of simul and graphic on the right upper part of the GUI. The input beam parameters and the number of macroparticles are defined in the tapeinput.txt. Information on the particles transmitted (NGOOD) and particles inside the bucket (NALYZ) is provided cell by cell. In addition, extra information is printed on a certain given number of cells, see Fig. 7.
   
 ![Fig7](https://github.com/Byeerendon/LINACS-Window-s-User-Installation-Guide/assets/65529667/3129d8cc-0390-4829-a91c-5d709c2c7bb0)

                                      Figure 7. Information about the run

8)	The output files are saved in the LINACsrfSIMrun folder. Please see LINACSrfSIM Runs,Files.docx for more information. 
9)	At the end of the simulation, a summary of the design and a plot of the most relevant figures are produced. See Fig.8.
    
![Fig8](https://github.com/Byeerendon/LINACS-Window-s-User-Installation-Guide/assets/65529667/b8cbdba6-64ff-4708-8f47-8cf69bb16b8e)
 
                                  Figure 8. Summary graphics and the result of LINACS simulation.

# 4.)	Contact

Please do not hesitate to contact us if you require further assistance or encounter any bugs. 

Bruce Yee-Rendon (email: byee@post.j-parc.jp)

# 5.)	References

•	R. A. Jameson et al “The LINACS Codes Release”, online download  
https://ln5.sync.com/dl/01ce57220/v23cfj82-gsx74hws-runykxcf-btqmfe2a

•	R.A. Jameson, RFQ designs and beam-loss distribution for IFMIF, Report No. ORNL.TM-2007/001, ORNL (2007).  (ResearchGate)

•	Y. Kondo, T. Morishita and R.A. Jameson, Development of a radio frequency quadrupole linac implemented with the equipartitioning beam dynamics scheme, Phys. Rev. Accel. Beams 22 (2019)120101.

•	R. A. Jameson, and B. Yee-Rendon, Improved bunching and longitudinal emittance control in an RFQ, JINST 17, P12011 (2022).

•	B. Yee-Rendon, Y. Kondo, J. Tamura, K. Nakano, F. Maekawa, S. Meigo, and R. A. Jameson., Design and Beam Dynamics Studies of an ADS RFQ Based on an Equipartitioned Beam Scheme, in Proceedings of 19th Annual Meeting of the Particle Accelerator Society of Japan, online, Japan, October 18 - 21, 2022, pp. 499–502.
