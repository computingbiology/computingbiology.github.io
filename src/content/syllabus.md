+++
date = "16 Jan 2022"
draft = false
title = "Syllabus"
slug = "syllabus"
+++

   <div class="yellownote">

This syllabus is a "semi-living document" (i.e., more like a virus
than a bacterium) subject to change as we adapt during the
semester. The course website is managed through a [public github
repository](https://github.com/computingbiology/computingbiology.github.io),
so you can see past versions and changes there.

The version as posted on the first day of class is [here](TODO)
</div>

## Overview

**Course Description:** This course will look at connections between
computing and biology, with a focus on DNA. It will include
computational methods used in biology focusing on how computing can be
used to analyze and design DNA, as well as opportunities to use
biological substances and ideas to compute.

**Course Objectives:** Students who succeed in the course will:

- Understand at a high (but deep) level how life works, and why
  certain aspects of known life on Earth seem to have evolved with
  common, robust mechanisms.

- Be able to implement and reason about algorithms for analyzing DNA
  including algorithms for genome assembly, genome alignment, and
  phylogeny, as well as algorithms used to try and understand genetic
  factors in diseases.

- Gain understanding how mRNA vaccines are developed, and what
  scientists have learned about SARS-CoV-2.

- Connect theoretical understanding of computing to biological
  mechanisms, including information theoretic understanding of genomes
  and immune systems and algorithmic perspectives on evolutionary
  processes.

- Be able to read and understand some research papers in computational
  biology, and present key ideas in biomedical work in ways that are
  understandable to computer scientists.

<a name="meetings"></a>

**Class Meetings:** The full class meetings of the course are
  scheduled for Mondays and Wednesday, 12:30 &ndash; 1:45pm in Olsson
  Hall 018. 

**Pandemic Policies.** The challenges we are facing with the current pandemic
places our community under tremendous stress, and we appreciate that
many of our students are dealing with extreme personal challenges this
semester. You should prioritize your own physical and mental health,
and the well-being of your friends and family, over any class. We want
the class to be a low stress, high value experience for everyone. 

Following current University policies, classes will be held in person
  and designed to maximize their value to students able to attend in
  person. This means we will use some of the class time for small
  group discussions and sometimes have graded activites in class. We
  will provide all the course materials (e.g., lecture slides and
  notes) openly on this website, but will not be routinely recording
  or live-streaming classes since doing this can diminish the value of
  the class to attendees (at a minimum, it divides the instructor's
  attention, and precludes any activites that expect student
  participation). Students who are not able to make it to class for
  medical, family, or personal reasons will not be impacted negatively
  by not participating in any in-class graded activities. 

I will do everything I can to accommodate students varying situations,
and to ensure that every student has the best opportunity possible to
succeed in the class and have a good experience.  Please communicate
with me about difficulties you are facing, or anything I can do to
make things better for you.

I will expect everyone associated with the class (including the
instructor, TAs, and students) to follow [University
policies](https://uvapolicy.virginia.edu/policy/SEC-045) regarding
health and safety requirements. These regulations may change during
the semester.  The ones currently in effect as of 16 January 2022
state that "all students who live, learn, or work in person at the
University of Virginia during the 2021-2022 academic year must be
fully vaccinated" and "masks are required for all people (students,
faculty, staff, contractors, and visitors), both vaccinated and
unvaccinated, who enter UVA properties."  This applies to all indoor
spaces, including our classroom. Following these regulations is both
important for your own health and for the safety and comfort for
everyone in the community, including many who may have different risk
profiles than your own such as living with elderly relatives or
children too young to be vaccinated.

## Preparation

**Official Prerequisites:** Students entering this course are expected
  to have successfully completed cs2150, and at least one of cs3102 or
  cs4102, or comparable experience. 

**Expected Background:** We expect all students in the class to be
  living human beings and to have been curious observers of the life
  that surrounds us, but do not expect an previous formal background
  in biology. 

We expect students to have solid understanding of core ideas in
theoretical computer science and be comfortable using asymptotic
notation and talking about computational complexity. To check your
understanding and refresh your memory, read the post on [Computer Science
Background](/computer-science-background).

We expect students to be able to program in Python, and to be able to
read and write programs with a few thousand lines of code, and to be
able to figure out how to use libraries and APIs from their provided
documentation and other resources. We expect students to have
experience with software engineering practices, and to be able to
write readable programs and test them systematically.


## Course Staff

**Instructor:** The course is taught by [David
  Evans](https://www.cs.virginia.edu/evans)
  (_evans@virginia.edu_). Feel free to contact me with any questions
  about the course, computer science, or anything else you think I can
  help with (but please read the section below on communications to
  determine if it would be better to post a message in slack or github
  discussions instead of by personal email). I have been [teaching at
  UVA](https://www.cs.virginia.edu/~evans/courses/) for more than 20
  years, but this is my first computational biology course. The last
  formal biology course I took was in high school (long before any of
  you were born), but I did previously teach a seminar on
  [_Biologically-Inspired
  Computing_](http://www.cs.virginia.edu/~evans/bio-seminar/), have given talks on [_What Biology Can (and Can't) Teach Us About Security_](http://www.cs.virginia.edu/~evans/talks/usenix04/), and published a [few](http://www.cs.virginia.edu/~evans/pubs/ssrs-abstract.html) [minor](https://www.cs.virginia.edu/~evans/pubs/whenantsattack.pdf) [papers](https://www.cs.virginia.edu/~evans/pubs/woss-abstract.html) that connect computing and biology. Most of my research is in [security and privacy](https://uvasrg.github.io/).

**Teaching Assistants:**  
[Hyun Jae Cho](https://hyunjaecho94.github.io/), PhD student working in biology and machine learning.  
[Anshuman Suri](https://www.anshumansuri.me/), PhD student working on privacy risks of machine learning.

**Office Hours:** A full schedule of office hours will be posted on the course website later. For the first week of the semester, Dave will hold office hours after class Wednesday. 

## Learning Materials
    
There is no required textbook to purchase for the course.

We will be using chapters from three open books:

- Bert Hubert’s [_The Technology of Life: A DNA-centric tour of
  biology_](https://berthub.eu/dna-book/). This is a new book
  currently under development. The author has graciously agreed to
  share an early version of the book with us. You will need a password
  to access this, which will be distributed through the collab mailing
  list.

- Phillip Compeau and Pavel Pevzner's [_Bioinformatics
  Algorithms_](https://www.bioinformaticsalgorithms.org/). Several
  chapters of the book are [freely
  available](https://www.bioinformaticsalgorithms.org/read-the-book),
  and we will only assign these chapters for reading. The [full
  book](https://www.bioinformaticsalgorithms.org/shop) is available as
  a printed book ($90), but is not necessary to purchase for the
  course. (There is also an [on-line
  course](https://stepik.org/course/55789/promo) ($90) connected to
  this book, which you may find useful and interesting.)

- Manolis Kellis' [_Computational Biology - Genomes, Networks, and
  Evolution_](https://bio.libretexts.org/Bookshelves/Computational_Biology/Book%3A_Computational_Biology_-_Genomes_Networks_and_Evolution_(Kellis_et_al.)). (Transcriptions
  of lectures from [MIT 6.047
  course](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-047-computational-biology-fall-2015/). Various
  versions of this course, and recorded videos of the lectures, are
  available on-line, and we will use some of these materials.)

The three books are all excellent and cover much of the same material,
but are quite different in style, expected background, and technical
depth. We will often assign readings from one or two of the books, and
suggest additional optional readings from the others for students who
want more depth or prefer a different kind of presentation.

In addition to these main texts, we will be reading papers
(distributed as PDFs through this website) and occasionally viewing
videos and other available materials.


## Communication

We will primarily use the course website for one-to-many
communications (posting course materials), use the course slack for
"real-time" messages and immediate course announcements, and use
github discussions for discussions.

**Course Website:** We will post all course materials on the course
website,
[_https://computingbiology.github.io/_](https://computingbiology.github.io/),
except for ones that we cannot post publicly, which will be shared
using collab or other mechanisms.  

**Slack:** We will use a slack workspace for immediate and real-time
  communications. All students in the course should join the slack
  workspace:
  [_https://computingbiology.github.io/slack/_](https://computingbiology.github.io/slack/).You
  should be able to join directly yourself using a `@virginia.edu`
  email address (let the course staff know if you have any problems
  joining). You will also be able to use slack to form channels for
  teams.

**Github Discussions:** We will use [github
  discussions](https://github.com/computingbiology/spring2022/discussions)
  for more persistent and structured discussions. You should use the
  github discussions if you have questions about concepts in the
  class, assignments, and readings.

**Email:** Managing email for a large class like this is difficult,
  and we prefer to use the course slack and github discussions for
  most communications relevant to the class. Please use direct
  messages in slack if you have personal, course-related questions for
  the instructor (e.g., requesting an extension or exemption). You
  should feel free to use email for messages peripherally related to
  the course (e.g., emailing an instructor about interest in their
  research). You should also use email if you post a question on slack
  or github discussions but don't receive an adequate response within
  24 hours.

## Assignments

The main assignments for the course, and where we expect students will
do the most learning, is a series of projects where students
implement, analyze, and extend computational biology algorithms.

Because this is a new course, we do not want to commit to the specific
topics and deadlines in the pre-semester syllabus, but expect there to
be four structured projects, approximately two weeks each, and one
longer open-end project for the final 5 weeks of the semester.

The rough schedule and planned topics (which are likely to change) are:

**Project 1: Assembling Genomes** (out Monday, 24 January, due Sunday 6 February)

**Project 2: Genome Alignment and Analysis** (out Monday 7 February, due Sunday 20 February)

**Project 3: Engineering a Covid Vaccine** (out Monday 21 February, due Friday 4 March) (Spring break is March 7-11, we will not have any assignments over spring break.)

**Project 4: Computing with Biology** (out Monday 14 March, due Sunday 27 March)

**Final Project** (final projects due Monday 2 May, last day of class,
with several intermediate deliverables and short presentations). The
final project will be open-ended, and could involve either explaning
a topic or recent result in biology, doing an original research
project, or something else of value and relevant to the course.

## Quizzes

To see how well students are understanding concepts in the course, and
incentivize students to do preparation readings when assigned, we
might have occasional, short quizzes. The details on these quizzes,
and how they will be scheduled, will depend on how the class is going.


## Grading

Since this is an upper-level elective, we hope students are not overly
stressed about grading and mostly focused on learning and doing
worthwhile things. That said, we understand students are often
stressed about grading and understandably want to know where they
stand in a class without having to rely just on the judgment of the
course instructor.  We aim to grade in a way that is useful (provides
students with accurate measure of how well they understood what they
should), motivating (encourages the behaviors we prefer, including
hard but not obsessive work), fair (assigned higher grades to more
deserving students), robust (arbitrary small perturbations do not have
a material impact on someone's grade), and low stress (for both
students and the course staff). You will get grades for the projects
that make it clear how well you have met our expectations, and will
get informative grades for any quizzes.

The final grade in the course will be determined based mostly on the
grades on your projects throughout the semester. If you do well on all
the projects, you'll get an A in the course. If you do exceptionally
well on the final project, this will more than make up for any
mediocre grades on the early projects. Performance on quizzes and
other contributions to the class may also be used to adjust student's
grades. In general, I don't have a single, simple, formula that is a
function that takes in point values for all assignments and outputs a
grade, but instead will analyze all of your performance in the course
in several different ways to determine a grade that best reflects your
overall learning and contributions to the course.  

**Accommodations:** It is the University's long-standing policy and
  practice to reasonably accommodate students so that they do not
  experience an adverse academic consequence when sincerely held
  religious beliefs or observances conflict with academic
  requirements. Although University policy only recognizes religious
  accomodations, the course instructor believes they are many other
  valid reasons for accomdations that are at least as justifiable as
  ones for religious observance and consider family obligations,
  personal crises, and extraordinary opportunities to all be
  potentially valid reasons for accomodations.

In general, I don't think I should make value judgements about this -
  what matters is that it is _something important to you_, that you
  have _little scheduling control over_, and that you _make the
  request_ as early as you should be able to know an accomodation is
  necessary and are flexible in working with me to find an
  alternative.

## Honor Expectations

We believe strongly in the value of a community of trust, and expect
all of the students in this class to contribute to strengthening and
enhancing that community.

The course will be better for everyone if everyone can assume everyone
is trustworthy. The course staff starts with the assumption that all
students at the university deserve to be trusted.

To ensure that expectations are clear to everyone, **all students are
required to read, understand, and sign (virtually on your [registration
survey](/survey)) the [course pledge](/pledge)**.

**Collaboration Policy:** Many of the assignments in this course will
require or allow you to work with others; some may require you to work
on your own.  The collaboration policy will be described on each
assignment document. The main expectation is that you do not
misrepresent others work as your own, or do things that obviously
violate the intent of the stated collaboration policy. We aim to make
the language describing the policy as clear and unambiguous as
possible, but if anything is ever unclear about the stated policy for
an assignment, please clarify with the course staff. The penalty for
policy violations will be considered on a case-by-case basis, with a
penalty commensurate the severity of the offense.

## Additional Information

This is generic information that is probably included in most of your
course syllabi.

**Special Circumstances:** The University of Virginia strives to
  provide accessibility to all students. If you require an
  accommodation to fully access this course, please contact the
  Student Disability Access Center (SDAC) at (434) 243-5180 or
  `sdac@virginia.edu`. If you are unsure if you require an
  accommodation, or to learn more about their services, you may
  contact the SDAC at the number above or by visiting their website
  [https://studenthealth.virginia.edu/sdac](https://studenthealth.virginia.edu/sdac)

**Safe Environment:** The University of Virginia is dedicated to
  providing a safe and equitable learning environment for all
  students. To that end, it is vital that you know two values that we
  and the University hold as critically important:
 
  1. Power-based personal violence will not be tolerated. 
  2. Everyone has a responsibility to do their part to maintain a safe community on grounds (including in virtual environments).

If you or someone you know has been affected by power-based personal
violence, more information can be found on the UVA Sexual Violence
website that describes reporting options and resources available:
[https://www.virginia.edu/sexualviolence](https://www.virginia.edu/sexualviolence).
   
As your professor and as a human, know that I care about you and your
well-being and stand ready to provide support and resources as I
can. As a faculty member, I am a _responsible employee_, which means
that I am required by University policy and federal law to report what
you tell me to the University's Title IX Coordinator. The Title IX
Coordinator's job is to ensure that the reporting student receives the
resources and support that they need, while also reviewing the
information presented to determine whether further action is necessary
to ensure survivor safety and the safety of the University
community. If you would rather keep this information confidential,
there are Confidential Employees you can talk to on Grounds (see
[https://eocr.virginia.edu/chart-confidential-resources](https://eocr.virginia.edu/chart-confidential-resources)
). The worst possible situation would be for you or your friend to
remain silent when there are so many here willing and able to help.

**Student Support Team:** You have many resources available to you
  when you experience academic or personal stresses. In addition to
  your professor, the School of Engineering and Applied Science has
  three staff members located in Thornton Hall who you can contact to
  help manage academic or personal challenges (students in the College
  or other schools may have additional resources available to you
  through your enrolled school, but since this course is offered
  through SEAS, these resources are available to any student in this
  class). Please do not wait until the end of the semester to ask for
  help!

_Lisa Lampe_, Director of Undergraduate Education (academic), ll4uu@virginia.edu  
_Blake Calhoun_, Director of Undergraduate Success (academic), bic4sc@virginia.edu  
_Alex Hall_, Assistant Dean of Students (non-academic issues), aec5d@virginia.edu  

In addition to having an Assistant Dean of Students embedded in
Engineering, we are also fortunate to have two CAPS counsellors
embedded in SEAS. You may schedule time with Elizabeth Ramirez-Weaver
or Katie Fowler through Student Health
(https://www.studenthealth.virginia.edu/getting-started-caps). You are
also urged to use TimelyCare for either scheduled or on-demand 24/7
mental health care.

Finally, the Center for Diversity in Engineering facilitates free
tutoring during the academic year, helps students locate internships
and research opportunities, and connects students with the many
organizations on Grounds that provide information and support. The
center also engages with student organizations, particularly those
serving students who are traditionally underrepresented in
engineering.


