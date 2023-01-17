# COMP122 Overview
#### Version: Spring 2023

This repository provides you with material associated with COMP122.  During the semester, the professor will be adding additional information to this repository. As such, you will need to regularly perform a `git pull`operation to obtain the most up-to-date information.

In addition to this class-material repository, you will also need to clone a number of other repositories. This other repositories are primarily associated   All of this material are organized within a predefined file hierarchy for organizational purposes. 

This README.md file provides you with an overview of this structure, key information, and a set of tasks to perform to get ready for this semester.  

---
## Canonical Root: $HOME/classes/comp122
  * Important documents: reposited from various subdirector
    - introduction.md: Introductory Information for this class
    - assignments.md: Living document enumerating class assignments
    - syllabus.md: The course syllabus
    
  * General Subdirectories:
    - administrative: various files about the class

    - deliverables: directory for the placement of all deliverables)
      - 11-\<name\>-\<account\> (Section #1, Deliverable #1)
      - 24-\<name\>-\<account\> (Section #2, Deliverable #4)
      - ...
      - 40-\<name\>-\<account\> (Section #4, Deliverable #0)

    - bin: various programs associated with COMP122

    - reference: reference documents


  * Section Subdirectories
    - models-comp-comm/
      - lecture_ordering.md: inform regarding slide presentations
      - Lecture Notes (notes_mm_dd.md)
      - Addendum Notes per class <br>
        (addendum_mm_dd_XX.md where XX= MM, MA, TM, TA)
      - Copies of Slides within the "documents/" subdirectory

    - format-encodings/
      - with the same substructure as "models_comp_comm"

    - digital-logic/
      - with the same substructure as "models_comp_comm"

    - assembly-programming/
      - with the same substructure as "models_comp_comm"

---
## Key Information:
  * Software Requirements
    - Sublime Text (editor): https://www.sublimetext.com
    - One Markdown: from the AppStore or other Markdown Viewer
    - Slack (for class communication): https://slack.com 
    - Git: preinstall or https://gitforwindows.org
    - Java: preinstalled or https://www.java.com
  * Git Organization and Repositories
    - COMP122 Home: https://github.com/COMP122
    - COMP122 class material: https://github.com/COMP122/comp122-s23.git
  * Canonical Class Directory: $HOME/classes/comp122


---
## Tasks (to be complete ASAP)
  1. Establish Accounts:
     - https://slack.com: 
       - Your account should be associated with your @my.csun.edu address.
     - https://github.com: 
       - Your account name should be clearly identify yourself in a professional manner.
       - All deliverables are submitted via GitHub Classrooms.

  1. Install Software on your personal computer:
     - Sublime Text Editor: https://www.sublimetext.com
     - One Markdown: or other suitable Markdown Viewer
     - Slack: https://slack.com  <br />   
       * Consider installing the mobile application as well
     - Git for Windows: https://gitforwindows.org


  1. Join the Slack COMP122 work space:
     - Accept the  invitation <br/> via https://join.slack.com/t/comp122-csun/signup using your @my.csun.edu address.
     - Add the 'fitzgerald-s23' channel, this is where all class discussions are held.
     - Respond to the 'Hello Class!' via the 'reply to thread' option (do NOT "Also send to #fitzgerald-s23").
 

  1. Configure your github environment (https://githuyb.com)
     - Configure your account to authenticate using SSH. <br>
       refer to [Connect with SSH](https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh).
       - About SSH: READ
       - Check for existing SSH key:
       - Generate new SSH key: Create an empty passphrase
         * Adding your SSH key to the ssh-agent:  SKIP
       - Add a new SSH key
       - Test your SSH connection
     - I'll have more to say about SSH in future lectures.
 

  1. Setup your local comp122 environment: <br/>
     Launch a gitbash (Windows), or Launch a terminal (All other OSes)
      1. Create the canonical folder for the class: \~/classes/comp122 
         ```
         mkdir -p ~/classes/
         ```
     1. Clone a copy of this repository:
        ```
        cd ~/classes/
        git clone https://github.com/COMP122/comp122-s23.git comp122
        ```

     1. Update the appropriate shell startup file to source .profile.comp122.
        ```
        echo "source $HOME/classes/comp122/.profile.comp122"  >> .profile
        ```

     1. Ensure the 'MARS IDE' is appropriate registered with your computer
        - Open up Exporer (Windows) or Finder (Mac)
        - Naviage to the COMP122 bin directory:  ~/classes/comp122/bin/
        - Control-click the Mars4_5.jar icon, then choose Open from the shortcut menu.
        - Click Open.

  1. Test your local environment.  First open a new terminal and execute the following commands:
     ```
     cd $COMP122_HOME
     cd mips
     mars add4.s
     mips_subroutine add4 2 4 6 8
     ```
     
     Ensure your terminal has the following output
     ```
     dwarf:~ steve$ cd $COMP122_HOME
     dwarf:comp122 steve$ cd mips
     dwarf:mips steve$ mars add4.s
     MARS 4.5  Copyright 2003-2014 Pete Sanderson and Kenneth Vollmar
     
     10
     dwarf:mips steve$ mips_subroutine add4 2 4 6 8
             20; 0x00 00 00 14; 0b0000 0000 0000 0000 0000 0000 0001 0100;
     
     dwarf:mips steve$ 
     ```
     Note that the substring `dwarf: steve$ ` is my prompt. Your prompt will differ.

