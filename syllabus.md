# Syllabus

## Logistics

CU Boulder: CSCI 5636-002 (Spring 2025)

Meeting Time: MW 5:05-6:20 in ECEE 283

### Instructor: [Fruzsina Agocs](https://fruzsinaagocs.github.io), [`fruzsina.agocs@colorado.edu`](mailto:fruzsina.agocs@colorado.edu), ECOT 614

* Office hours: 

Every Wednesday, but alternating times and locations:
- Fruzsina: every other Wednesday starting 01/22, 3:50-4:50pm, ECOT 614
- Corey: every other Wednesday starting 01/15, 2-3pm, ECCS 114H (conference room inside CSEL)

:::{tip}
Chat sessions are important for asking questions, solving problems, discussion of broader academic and career strategy, and to provide feedback so I can make the class serve your needs and those of people with similar experiences and interests.
:::

## Overview

Partial differential equations (PDE) describe the behavior of fluids, structures, heat transfer, wave propagation, and other physical phenomena of scientific and engineering interest.
This course covers discretization of PDE using finite difference and collocation methods, finite volume methods, and finite element methods for elliptic, parabolic, and hyperbolic equations.
For each method, we will discuss boundary conditions, generalization to high order, robustness, and geometric complexity.
We will discuss foundational principles like will posedness, verification, and validation, as well as efficient methods for solution of the discretized equations and implementation in extensible software. 

## Organization

We will start with a brief refresher on numerical integration, approximation of functions, and numerical differentiation.  We will extend this to finite difference methods for elliptic problems (like heat and pressure equilibrium) and time integration, producing methods that converge with arbitrarily high orders of accuracy.  We will discover challenges when applying these methods to hyperbolic equations (which describe wave propagation and transport phenomena), especially nonlinear hyperbolic equations, and thus develop finite volume methods which rely on weaker assumptions.  We will learn about shocks, rarefactions, and Riemann solvers.  Finite volume methods are easy to use in complicated geometries and/or unstructured meshes, but achieving high order accuracy in such settings is unnatural and the methods can be awkward for elliptic and parabolic equations.  Finite element methods offer a flexible and robust analysis framework as well as modular implementation that allows arbitrary order of accuracy even in complicated domains.  We will introduce relevant concepts in continuum mechanics as we go.

In the second half of the semester, we will transition to more project-based learning.
You will choose an open source software package with an active community and give a presentation to the class about the choice of methods, stakeholders and community functioning, and identify opportunities for contribution.
You'll then form small teams of like interest and work on a contribution to be shared with the community.
(Such contributions can take many different shapes, and need not involve code.)

## Outcomes

Partial differential equations underly a broad range of high-fidelity models in science and engineering from atomic to cosmological scales.
Upon completing this course, students possess an ability to

* formulate problems in science and engineering in terms of partial differential equations
* understand the merits and limitations of the leading numerical methods used to solve PDE
* recognize and exploit structure to apply algorithms that improve performance and scalability
* select and use robust software libraries
* develop effective numerical software, taking into account stability, accuracy, and cost
* predict scaling challenges and computational costs when solving increasingly complex problems or attempting to meet real-time requirements
* interpret research papers and begin research in the field

## Grading

I'm here to be your partner, not your adversary, and I promise not to waste your time. The assignments in the class all serve the purpose of helping you in your future work and research. 

Your grade will be made up of the following assigments:
- Homeworks, to be submitted every 2 weeks: 30% total.
- Community project (second half of the semester): 60% total.
    - Community analysis proposal (7.5%): you'll write a one-page proposal (based on a template) where you identify the project you'll contribute to and find some information on it. 
    - Community analysis presentation (7.5%): a 5-minute presentation on your contirbution ideas.
    - Contribution proposal (15%): a more detailed written proposal of your contribution that you'll attempt to communicate upstream.
    - Your contribution itself (22.5%).
    - Contribution presentation (7.5%): lightning presentations and breakout group discussions about your contributions. 
- Portfolio: 10%. This is a journal to keep yourself organized, keep track of your goals, and collect ideas that relate to the class. It will take the form of a template repository, with detailed instructions and an example.

We will meet to reflect on your community project and portfolio. I will give constructive feedback and you will propose a grade.

## GitHub

We'll use Git with GitHub Classroom for managing activities and feedback. During the project-based learning later in the semester, you'll likely interact with open source communities using these tools.

You are encouraged to work together on assignments, but must give credit to peer contributions via the commit messages or Git history. For example, you would add

    Suggested-by: Friendly Neighbor <friendly.neighbor@colorado.edu>

to the commit message if that code incorporates an approach suggested by your neighbor. You should ensure that each assignment (pull request) contains some of your own meaningful intellectual contributions.

## Programming languages and environment

I will primarily use Julia and [Jupyter notebooks](https://jupyter.org/) for slides and activities in class.  This environment is convenient to work with, general purpose, and has extensive library support.  It is possible to write fast code in Julia, though performance implications can by mysterious. C, C++, and Fortran are popular languages for writing production numerical software, sometimes called from a higher level programming language like Python.  MATLAB is also popular for numerical computing, though it is a proprietary environment and lacks general-purpose libraries. Rust is an exciting young language, albeit with limited numerical library support at this time.

We will make use of libraries written in several languages, and I'll focus on the abstraction rather than minutia of the language. You don't need prior experience in any particular language, but please bring a growth mindset and ask for help as needed (from myself and peers -- GitHub discussions are a good place for this).

Most HPC facilities use a Linux operating system and many open source software packages and libraries will have the best documentation and testing on Linux systems. You can use any environment for your local development environment, or use the CS Department's JupyterHub [coding.csel.io](https://coding.csel.io/) to experiment and develop without a local install.

## Target audience

Graduate students in computer science or simulation-based science or engineering.  Suggested prereq: at least one of

* CSCI-2820 Linear Algebra
* CSCI-3656 Numerical Computation
* CSCI-4576 High-Performance Scientific Computing

## Resources (updated continuously)

* [SIAM Membership](http://www.siam.org/students/memberships.php) is free for CU students, 30% discount on SIAM books
* [LeVeque, *Finite Difference Methods for Ordinary and Partial Differential Equations*](https://faculty.washington.edu/rjl/fdmbook/) (CU students can [download free from SIAM](http://epubs.siam.org/doi/book/10.1137/1.9780898717839))
* [LeVeque, *Finite Volume Methods for Hyperbolic Problems*](https://depts.washington.edu/clawpack/book.html) and the [Clawpack software](http://www.clawpack.org/).
* [Toro, *Riemann Solvers and Numerical Methods for Fluid Dynamics*](https://link.springer.com/book/10.1007%2Fb79761#toc). (CU students can download free)
* [Logg, Mardal, Wells, *Automated Solution of Differential Equations by the Finite Element Method (The FEniCS Book)*](https://link.springer.com/book/10.1007%2F978-3-642-23099-8). (free download)
* [Trefethen, *Spectral Methods in MATLAB*](https://people.maths.ox.ac.uk/trefethen/spectral.html). (CU students can [download free from SIAM](http://epubs.siam.org/doi/book/10.1137/1.9780898719598))
* Elman, Silvester, Wathen, *Finite Elements and Fast Iterative Solvers with Applications in Incompressible Fluid Dynamics*

## Honor Code

All students enrolled in a University of Colorado Boulder course are responsible for knowing and adhering to the Honor Code. Violations of the Honor Code may include but are not limited to: plagiarism (including use of paper writing services or technology [such as essay bots]), cheating, fabrication, lying, bribery, threat, unauthorized access to academic materials, clicker fraud, submitting the same or similar work in more than one course without permission from all course instructors involved, and aiding academic dishonesty. Understanding the course's syllabus is a vital part in adhering to the Honor Code.
All incidents of academic misconduct will be reported to Student Conduct & Conflict Resolution: StudentConduct@colorado.edu. Students found responsible for violating the Honor Code will be assigned resolution outcomes from the Student Conduct & Conflict Resolution as well as be subject to academic sanctions from the faculty member. Visit Honor Code for more information on the academic integrity policy. 

## Accommodation for Disabilities, Temporary Medical Conditions, and Medical Isolation

If you qualify for accommodations because of a disability, please submit your accommodation letter from Disability Services to your faculty member in a timely manner so that your needs can be addressed.  Disability Services determines accommodations based on documented disabilities in the academic environment.  Information on requesting accommodations is located on the Disability Services website. Contact Disability Services at 303-492-8671 or DSinfo@colorado.edu  for further assistance.  If you have a temporary medical condition, see Temporary Medical Conditions on the Disability Services website.
If you have a temporary illness, injury or required medical isolation for which you require adjustment,
please contact the instructor in person or via fruzsina.agocs@colorado.edu (you are not required to state the nature of your illness/injury or provide a doctor’s note).

## Accommodation for Religious Obligations

Campus policy requires faculty to provide reasonable accommodations for students who, because of religious obligations, have conflicts with scheduled exams, assignments or required attendance. Please communicate the need for a religious accommodation in a timely manner by informing the instructor in person or in e-mail.

See the campus policy regarding religious observances for full details.

## Preferred Student Names and Pronouns

CU Boulder recognizes that students' legal information doesn't always align with how they identify. Students may update their preferred names and pronouns via the student portal; those preferred names and pronouns are listed on instructors' class rosters. In the absence of such updates, the name that appears on the class roster is the student's legal name.

## Classroom Behavior

Students and faculty are responsible for maintaining an appropriate learning environment in all instructional settings, whether in person, remote, or online. Failure to adhere to such behavioral standards may be subject to discipline. Professional courtesy and sensitivity are especially important with respect to individuals and topics dealing with race, color, national origin, sex, pregnancy, age, disability, creed, religion, sexual orientation, gender identity, gender expression, veteran status, marital status, political affiliation, or political philosophy.
For more information, see the classroom behavior policy, the Student Code of Conduct, and the Office of Institutional Equity and Compliance.

## Sexual Misconduct, Discrimination, Harassment and/or Related Retaliation

CU Boulder is committed to fostering an inclusive and welcoming learning, working, and living environment. University policy prohibits protected-class discrimination and harassment, sexual misconduct (harassment, exploitation, and assault), intimate partner abuse (dating or domestic violence), stalking, and related retaliation by or against members of our community on- and off-campus. The Office of Institutional Equity and Compliance (OIEC) addresses these concerns, and individuals who have been subjected to misconduct can contact OIEC at 303-492-2127 or email CUreport@colorado.edu. Information about university policies, reporting options, and OIEC support resources including confidential services can be found on the OIEC website.
Please know that faculty and graduate instructors are required to inform OIEC when they are made aware of incidents related to these concerns regardless of when or where something occurred. This is to ensure that individuals impacted receive outreach from OIEC about their options and support resources. To learn more about reporting and support for a variety of concerns, visit the Don’t Ignore It page.

## Mental Health and Wellness

The University of Colorado Boulder is committed to the well-being of all students. If you are struggling with personal stressors, mental health or substance use concerns that are impacting academic or daily life, please contact Counseling and Psychiatric Services (CAPS) located in C4C or call (303) 492-2277, 24/7.
Free and unlimited telehealth is also available through Academic Live Care. The Academic Live Care site also provides information about additional wellness services on campus that are available to students.

## Acceptable Use of AI in this Class

You may use generative AI in this course, but I ask that you do so
- carefully, always checking and testing their output and not accepting it unconditionally,
- as if you were consulting a colleague, i.e. cite and document your usage (the tool, the purpose of use, and the prompt). 
Generally, gen AI use in this course will not enhance your learning, nor serve the topic at hand.
