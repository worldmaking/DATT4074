
# DATT4074 | DIGM6074 Synthesis Workshop

## Course Information

Wednesdays, 9.30am-12.20pm, [Fine Arts building room ACW 103](https://find.yorku.dev)

This includes both 
- *DATT4074 Creative Audio Signal Processing II: **Synthesis Workshop*** and 
- *DIGM 6074 Generative Sound & **Synthesis Workshop***

**Instructor:** [Graham Wakefield](https://discover.academics.yorku.ca/Graham.Wakefield) g rrr w aaa a t yo rk u do t ca

> For those that don’t know me, I’m a researcher and Associate Professor in Digital Media, but I’m also deeply involved in the audio software/hardware industry as a developer for audio software [(Max/MSP's gen~)](https://cycling74.com), a developer of software for dedicated audio hardware platform ([Electrosmith Daisy](https://daisy.audio/)), and for professional audio hardware products (recently launched: [Fancyyyyy K-Accumulator](https://www.fancysynthesis.net/)), all experience I’ll be bringing to the course.  

Office hours: Thursdays, 9:30am-11:30am, in the Alice Lab - GCFA 309

**Course material** is available at or linked from [this website](https://alicelab.world/DATT4074) -- bookmark it! 

**Assignments** will be handled through **e-Class** 
- Undergraduate at [https://eclass.yorku.ca/course/view.php?id=157128]()
- Graduate at [https://eclass.yorku.ca/course/view.php?id=157121]() 

**Class recordings**: I often share screen and record classes via Zoom. This doesn't mean the class is hybrid (in-person attendence is required and will be accounted), but I have heard that it has been useful for many students to be able to review sessions after class hours, or to view a live class on their personal laptop screens. 
- [Zoom meeting (same link every week)](https://yorku.zoom.us/j/93856257447?pwd=38tAeaKReiULvX3vOMVORoW3bJQIOD.1)
- [Add it to your calendar (.ics file)](https://yorku.zoom.us/meeting/tJclcu-qqzwuHtNdaKtRMtSDvpFNb2HzWijE/ics?icsToken=DMk7sXsoFa5zP12M-wAALAAAAC43fiWPlGSR19UxF5GYW3-hcardNuY7NAbGrZ8lfnYJfI2wirC49UGypNfWFQRmIVjTO1WYC3GtucAeFzAwMDAwMg&meetingMasterEventId=KANIVnCvTtKGmxXoAb5smg)
- [List of class recordings](#class-recordings)

---

This is a problem-driven and technique-focused studio course — part hackathon, part production incubator — where you take a sample-level interactive audio synthesis idea from prototypes to finished, portfolio-ready products in software and/or hardware.

You can work solo or in groups, and develop final projects in a variety of possible forms:

🎛️ Hardware — Design your own device: a standalone instrument, a guitar pedal, a modular synthesos module, or an interactive art installation. In the course of this, get to know analog hardware and build embedded digital audio systems!  

🎮 Game Audio — Build adaptive sound and procedural foley systems that react live inside game engines such as Unity and Unreal. 

🔌 Plugins — Build real plugins that work with the audio software or video editors people already use such as Ableton Live or VCV Rack. 

🌐 Web & XR — Create generative audio for browser-based experiences, games and WebXR worlds. 

Instruction includes a blend of essential topic instruction with online resources, but mainly focuses on per-project supervision. 

Your progress is documented in a continuous development log, and final creative projects that can form part of a graduating portfolio. 

### Course software

We will work with the same tools many professional studios and hardware companies use to prototype sonic algorithms in the real world. To begin developing synthesis algorithms we will work using the **gen~** environment within [Cycling '74's Max](https://cycling74.com). 

> All students have access to a license for Max supported by the course fees. License codes should be coming to all students through the department after our first attendance check. The computers in ACW 102 also have Max installed and licensed, and students can come in to use them during open lab hours. Two of the machines in DM labs also have the RNBO license that you may need for the final project. 

### Evaluation

- **25% Dev Log**   
An online log of project design and the development progress, maintained throughout the course. It could be a Google Doc, a Notion doc, a Github page -- anything that can be shared online.

- **25% Presentation & Discussion**   
Presenting work-in-progress to the group, and generous contribution to discussion.

- **25% Final distributable project**   
A functional, professional embodiment of the sonic ideas in a specific application format such as: adaptive sound generators for video games; new embedded hardware for guitar pedals, modular synthesizers, or interactive art installations; embedding in web-native projects; creating plugins for desktop software.

- **10% Attendance (Undergraduate only)**

- **15% Website (Undergraduate only)**   
Documentation of the final project in the form of a web page with embedded video demonstration.

- **25% Research paper (Graduate only)**   
The final project implementation documented in research-appropriate writing, such as an academic paper suitable for submission to a conference such as NIME (New Instruments for Musical Expression), SMC (Sound Music Computing), or another comparable research document. 

### Related Courses

The course accompanies [DATT3074](https://alicelab.world/datt3074/) **Creative Generative Audio Signal Processing**, which focuses on sample-level audio synthesis algorithms. 

The course complements and supports Sonic Arts stream courses in Digital Media, including DATT4071/DIGM5071/6071 and DATT3070/4070/DIGM5070. The course may also directly contribute to project development in other courses such as DATT4700, DATT4520, and EECS4441.

[Back to top](#top)

# Week 1: Introduction
Sep 9 - [Class Recording](#class-recordings)

**Hello and welcome!**

Introduction to the course

*It's the 1st time to run this course, so the roadmap will be fleshed out more after I know more about what your interest foci are (after the 1st week's homework).*

Context: over a century of electronic sound synthesis & instrument design, intertwining creativity & technology 
  - Explore https://nodemusic.cc/horizon (Katerina Ryzhzh, 2026) + discussion
  - Mechanical, Analog, Digital, AI? 
  - Interconnectivity: Voltage, MIDI, plugins, networking, ...?
  - Mimicry, supernormal, alien
  - Physicality
  - Why is modular resurgent?
  - What's missing from this graph?

Presentation:

https://docs.google.com/presentation/d/147RoDVI9CexC3cXXdqOqc6ns1jGn0L_rGpgzSky1RvA/

- [Survey](https://docs.google.com/forms/d/e/1FAIpQLSfc-nzHniN77CjY7-6F_ik-i8j4uW_9yHiZzF3MV-fmJt_4pQ/viewform?usp=publish-editor)
- Attendance
- Max license question

- Open-ended demonstration: Modular, gen~, Oopsy & different Daisies :-)

## Homework week 1

Do some field research into reference videos about audio synthesis projects while thinking about what you would like to build. Collect the best 3 reference projects to your interest.

- They could be guitar pedals, modular synthesis modules, DIY instruments, VST plugins, sonic art installations, game audio, etc.  Keep their scope fairly narrow though -- modular modules, pedals and plugins are good choices because usually each one focuses on a single synthesis algorithm.
- All 3 should be different enough from each other so that they cover the different aspects of what you might want to do. For example:
  - One could be selected for what makes it interesting in terms of audio synthesis or generative algorithms
  - One could be selected for the interestingness of its interface 
  - At least one should be a project that explains how it was made (e.g. DIY, open source, tutorial video, etc.). Its OK if you don't fully understand it yet, or if it looks beyond what you think you can achieve. 

[Add these videos to slides in this presentation](https://docs.google.com/presentation/d/1xG5xHPcHTgD2Z7tH2E1d0mNjhQ2WEzrlkpEth35PLUI/edit?usp=sharing)

*Be careful not to accidentally overwrite one of your colleagues slides!*

For each one, think about how to answer these questions:
  - What is especially impressive or inspiring to you about it?  What makes it uniquely interesting? 
  - What surprised you in the details or implementation / what did you learn from it that you intend to apply?
  - Where do you think the project is weak, why, and how could it be better?

Put these answers into the slides (or presenter notes)

Can you sketch out what a hybrid between 2 or 3 of your references might look like?



**Also for next week: remember to bring headphones and/or portable speakers -- we will start flashing Daisies together**

# Week 2: Flashing Daisy

Setting up the Max / gen~ / Daisy workflow, and flashing Daisy on breadboards

Inspiration Slides: 

https://docs.google.com/presentation/d/1xG5xHPcHTgD2Z7tH2E1d0mNjhQ2WEzrlkpEth35PLUI/

# Class Recordings

Recordings of the weekly sessions will be here:

- [Week 1](https://yorku.zoom.us/rec/share/WvH17_lakNNvKvn-CyZ74cwDlYrRqHXntI-AFOhnvkXhUIDuh8ICQ0HSumcj2TCa.Q7j1bOMUS56nFRD3)