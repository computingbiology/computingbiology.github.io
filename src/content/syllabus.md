+++
date = "22 Aug 2022"
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

The version as posted on the first day of class is available [here](https://github.com/computingbiology/computingbiology.github.io/blob/2605d186b00a12fedb87cf110837ee3d5b7a24a1/syllabus/index.html), and [history of changes](https://github.com/computingbiology/computingbiology.github.io/commits/main/syllabus/index.html).
</div>

## Overview

**Course Description:** This course will look at connections between
computing and biology, with a focus on DNA. It will include
computational methods used in biology focusing on how computing can be
used to analyze and design DNA, as well as opportunities to use
biological materials to compute.

**Course Objectives:** Students who succeed in the course will:

- Understand at a high (but deep) level how life works, and why
  certain aspects of known life on Earth seem to have evolved with
  common, robust mechanisms.

- Be able to implement and reason about algorithms for analyzing DNA
  including algorithms for genome assembly, genome alignment, and
  phylogeny.

- Connect theoretical understanding of computing to biological
  mechanisms, including information theoretic understanding of genomes
  and immune systems and algorithmic perspectives on evolutionary
  processes.

- Learn to think like a computational biologist.

- Be able to read and understand some research papers in computational
  biology, and present key ideas in biomedical work in ways that are
  understandable to computer scientists.

<a name="meetings"></a>

**Class Meetings:** The full class meetings of the course are
  scheduled for Tuesdays and Thursdays, 12:30pm &ndash; 1:45pm in Olsson Hall 120.

## Preparation

**Official Prerequisites:** Students entering this course are expected
  to have successfully completed cs2130, and at least one of cs3100 or
  cs3120, or comparable experience. 

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
  determine if it would be better to post a message the github
  discussions instead of by personal email). 

Office hours (in Rice 507):
Mondays, 1:30-2:45pm  
To schedule other times, use [_https://davidevans.youcanbook.me/_](https://davidevans.youcanbook.me/)

**Teaching Assistants:**  
[Ashley Gao](https://www.cs.virginia.edu/~yg9ca/), PhD student studying affective computing and transfer learning.  
&nbsp;&nbsp;&nbsp;Office Hours (in Link Lab Arena area, second floor of Olsson): Wednesdays, noon-1pm; Fridays, noon-1pm

[Jack Heavey](https://www.linkedin.com/in/jack-heavey), PhD student studying computational epidemiology.  
&nbsp;&nbsp;&nbsp;Office Hours (in Rice 414): Mondays, 11am-noon; Wednesdays, 2-3pm

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

**Github Discussions:** We will use [github
  discussions](https://github.com/computingbiology/fall2022/discussions)
  for course discussions. You should use the github discussions if you
  have questions about concepts in the class, assignments, and
  readings.

## Assignments

The course will include two structured project assignments, and a large open-ended final project.

The schedule for the two projects is:

**Project 1: Assembling Genomes** (due Monday, 5 September, 8:59pm)

**Project 2: Genome Alignment and Phylogeny** (due Wednesday, 21 September, 8:59pm)

**Final Project:** The final project will be open-ended, and could
involve either explaning a topic or recent result in biology, doing an
original research project, or something else of value and relevant to
the course. There will be a series of separate deliverables and
deadlines for the final project, leading up to project paper
submissions on 7 November. You will get a preliminary grade on your
project and feedback on these submissions, and an opportunity to
revise them, to submit a final project paper the last day of class (6
December).

## Quizzes

To see how well students are understanding concepts in the course, and
incentivize students to do preparation readings when assigned, we will
have a few short quizzes.

These are tentatively scheduled for:

**Quiz 1:** Tuesday, 11 October  
**Quiz 2:** Thursday, 27 October  
**Quiz 3:** Tuesday, 15 November

(Depending on how things are going and other scheduling issues, there
might be a Quiz 4 on 1 December.)

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
students and the course staff).

In general, I don't have a single, simple, formula that is a
function that takes in point values for all assignments and outputs a
grade, but instead will analyze all of your performance in the course
in several different ways to determine a grade that best reflects your
overall learning and contributions to the course.

You can ensure an "A" grade in the course by doing any one of these:

- Doing a great job on the final project, and demonstrating an
  acceptable level of effort on the structured projects and quizzes.

- Doing reasonably well on the final project, and doing at or above
expectations on both of the structured projects, and doing well on at
least two of the quizzes.

- Putting a reasonable effort into a project but ultimately not
succeeding in producing a satisfactory project, but doing above
expectations on both of the structured projects and well on all of the
quizzes.

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
required to read, understand, and agree to the [course
pledge](/pledge)**. If you are not willing to agree to any of the
expectations there, please let Prof. Evans know. On your [course
registration survey](https://forms.gle/96eqfeZnA26rpWiw6), you will be
expected to virtually sign acceptance of the course pledge.
 
## Additional Information

This is standard information that is probably included in most of your
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


