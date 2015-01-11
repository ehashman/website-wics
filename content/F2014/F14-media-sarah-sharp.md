Title: Sarah Sharp and her USB 3.0 Success Story
Date: 2014-11-20 17:30
Category: Media
Tags: linux, open source, talks
Slug: sarah-sharp
Author: Elana Hashman
Summary: Sarah Sharp, Linux kernel developer, visits Waterloo to give a talk about getting involved with the Linux kernel and open source.

You can find more information about the event
[here](https://cs.uwaterloo.ca/events/talk-sarah-sharp-breaking-open-source-and-linux-usb-30-success-story).

<video width="320" height="240" controls>
  <source src="http://mirror.csclub.uwaterloo.ca/wics/sarah_sharp_low.mp4"
          type="video/mp4">
Your browser does not support the video tag.
</video>

**Video download:**
[Low (335MB)](http://mirror.csclub.uwaterloo.ca/wics/sarah_sharp_low.mp4)
[Med (730MB)](http://mirror.csclub.uwaterloo.ca/wics/sarah_sharp_med.mp4)
[High (1.2GB)](http://mirror.csclub.uwaterloo.ca/wics/sarah_sharp_hi.mp4)
**Slides download:** [PDF](/extra/F14-sarah-slides.pdf)
<br><br>

# Talk Transcript #

*Please note that the following transcript has been edited for clarity; it is
not intended to be a word-for-word transcript of the talk.*

**Elana:** Hello everyone! We're going to start now... and hopefully the
technical difficulties will sort themselves out.

The first announcement that I wanted to make is that today is the [Trans Day of
Remembrance](http://tdor.info/) for trans victims of violence, to memorialize
people that have been killed as the result of transphobia. Women in Computer
Science is obviously very concerned with diversity in technology and other
fields and we care very much about trans peoples' wellness, so I just wanted to
let you know about that in case you didn't already.

So, the format of the talk today: Sarah's going to speak, and then after the
talk we're going to have Q&A. There are two mics if you want to come down and
use the mic; if you want to just scream out your question and you can say it
loudly enough, that would be great as well.

I am going to invite Sandy Graham to the stage to introduce [Women in Computer
Science](http://cs.uwaterloo.ca/wics) (the committee as a whole), then I will
talk a little about [Women in Computer Science](/) (the undergraduate
committee), and I'm going to tell you a little bit about Sarah, and then we
will start. So, Sandy! [APPLAUSE]
<br><br>

**Sandy:** I just wanted to say a couple of words on behalf of Women in
Computer Science. The Faculty of Mathematics has had a [Women in Mathematics
Committee](http://math.uwaterloo.ca/women-in-mathematics/women-mathematics) for
more than two decades and it included computer science as part of the group
that it was supporting, but in 2007 it was felt that Women in Computer Science
needed to be formed as a separate committee because of the special concerns of
the number of women that were choosing computer science at all levels: in high
school, university, graduate, and in industry as well. Its purvue is to try to
support women that are in computer science at the University of Waterloo at the
undergraduate, graduate and faculty levels, as well as trying to encourage more
women to consider computer science, which quite honestly to me is an NP-hard
problem. [LAUGHTER]

We just really don't have enough resources to solve this problem, but we do our
best to try to encourage and support the women here on campus and do some
outreach activities as well, including things like inviting distinguished
speakers, and sending undergraduate students to the Grace Hopper conference,
and having some social activities just to support the well-being of the women
here.

One of the things I think is most important about the committee is that it
exists at all because it often times brings up the question "Why is there a
'Women in Computer Science' committee and not a 'Men in Computer Science'
committee?" We hear that question quite a bit. I'll just say that as part
of my job I do quite a bit of outreach and I visit lots of high school computer
science classes and I am very rarely encountering high school classes that have
more than one or two girls in them. And very often I'll walk into a classroom
and there will be no girls sitting in that room. So the fact that the committee
exists and this issue is being discussed I think is quite important and
hopefully in another ten years or maybe less&mdash;I don't expect that will be
true&mdash;we won't need the committee at all. So I will turn this over to
Elana and we'll move forward from here. Thank you. [APPLAUSE]
<br><br>

**Elana:** I should probably introduce myself as well.  I'm Elana Hashman, one
of the undergraduate representatives on the Women in Computer Science
Committee, and I want to tell you a little bit about the Women in Computer
Science Undergraduate Committee.  It seeks to support women interested in
computer science at the University of Waterloo, by running lectures like this
one, providing a mentorship program, organizing social and academic events for
individuals interested in computer science, advocating for diversity and more.

All of our events are subject to our [Code of
Conduct](/pages/code-of-conduct.html), which you can find on our website.  This
talk and the talk transcript will be recorded and made available on our website
as soon as possible.  If you like what you are seeing here today, please [let
us know](/pages/contact-us.html).  If you want to get involved we would also
like to hear from you.  To keep in touch with us, you can visit our website,
you can [send us an email](mailto:wics-ugrad@lists.uwaterloo.ca)&mdash;that's
the committee's email.  You can join our women-only [Facebook
group](https://www.facebook.com/groups/wicsUW) or subscribe to the public
[wics-announce mailing
list](https://lists.uwaterloo.ca/mailman/listinfo/wics-announce) and then you
can be informed directly about our events.

I'm excited to introduce Sarah Sharp, our speaker today.  She is a software
engineer at Intel's Open Source Technology Centre. Sarah is the author of the
Linux kenel USB3.0 driver and has participated in kernel development since
2006. She currently works as an embedded software developer with the [Yocto
Project](http://www.yoctoproject.org/).   Sarah volunteers as the coordinator
for the Linux kernel project within the [FOSS Outreach Program for
Women](https://live.gnome.org/OutreachProgramForWomen).  She herds kernel
mentors, finds funding, helps OPW applicants and writes documentation for
[getting started in Linux kernel
development](http://kernelnewbies.org/FirstKernelPatch).  She also has
participated in many open source projects, from open source and open hardware
[amateur rockets](http://psas.pdx.edu/) to [automated watering
systems](https://github.com/sarahsharp/GardenGeek) for her garden.  Without any
further delay, I would like to introduce our speaker, Sarah Sharp.  [APPLAUSE]
<br><br>

**Sarah:** Thank you so much for having me here.  It's been awesome to be in
Waterloo so far.  I will be talking and speaking and I'll be here for the next
two days if you want to try to meet up or chat more.

So when I was first asked to come to Waterloo, I had kind of an imposter
syndrome moment, where I was like "...why would they want to invite me here?"
And I was like, "No, you are awesome because you are a kernel developer, you
wrote the USB3 driver and speak at conferences across the world and have done
things like that Linux kernel developer panel with Linus Torvalds."  So when I
often speak at conferences I sometimes see that people are a little bit
intimidated by me and by some of the reall awesome things I have done, but  I
think that's because people compare what they see me as now and the goals I
have accomplished without looking at all of the different steps along the way
that led me there and all of the people that helped me along the way to get to
being a Linux kernel developer.  So I would like to share some of my journey of
how I started out as an undergraduate student and got into kernel development
and so you can see you can be awesome too and a leader in open source.
[APPLAUSE]

Twelve years ago I was a high school student in a very small town.  This
picture is my hometown.  Basically that's the main drag and it ends at that
hill over there, and that's it.   There's not that much to do in a small town,
so I spend a lot of the time online.  I played Neopets; I played computer games
like the Sims. And then in school, we didn't actually have a computer science
program in my high school.  We did have a program to introduce students to
computer engineering.  So there was a program called STRUT, Students Recycling
Used Technology, where we'd get donations of old computers and rip them apart
and we figured out what didn't work and we'd replace the parts and get them
working again and have whole computers to use in our schools and give to kids
around the community.

The other thing I did in high school is I did a little bit of web
programming.  I had a GeoCities website that was about haunted castles in
England.  And I was very proud: I got the tiling backgrounds and the pictures
centred! But this is all of the programming I did.  I didn't do any programming
in high school.  There was one class that I took that was an extracurricular
class that my mom drove me an hour to another city so I could take.  But when
we were pairing up, I was paired up with someone that stole the keyboard from
me and basically didn't get to program for the entire class.  So it wasn't
until college that I really took off programming-wise.

I didn't learn programming until I went to college and took my first CS class.
I went to [Portland State University](http://www.pdx.edu/) which is in
Portland, Oregon.  It's there that I met a bunch of different professors at the
university in computer engineering and electrical engineering, like Professor
Doug Hall.  He was interested in embedded systems and Linux.  I was going to go
into CS and he said, "oh no, go into computer engineering instead,"  because I
really liked writing software that touched the hardware.  I liked a little more
of the hardware side than the software side.

At college I also met my boyfriend (who is now my husband) who introduced me to
open source and Linux and amateur rockets.  So I got involved in the [Portland
State Aerospace Society](http://psas.pdx.edu/) which is an amateur rocketry
group. That's the 14 foot rocket that they built themselves and it runs all
open source software, and has open hardware; all the schematics for the
airframe are on our website and it's a really cool way to get involved.  So
getting involved with the Portland State aerospace society really introduced me
what it's like being in an open source community.

We had different people working together on different aspects of the rocket. We
had, you know, people who were pair programming on the flight computer
software, we had the EE's that were designing the boards and connecting them
and we had ME's that were building carbon fiber airframes to make sure that
everything was structurally sound so when you went past MACH-1 things wouldn't
break.  So you had all these people working on different parts of the system
but then they came together to have this awesome launch once a year.  And you
would have people who were out in the field who were setting up the rocket and
you would have people down at the ground control who were watching the
telemetry on the rocket come back, making sure that we could communicate via
wifi with the rocket.  It was awesome to see people come together and
collaborate even though they were all working on different parts.

Through the rocketry program I met a computer science professor, Prof. Bart
Massey.  He was really the one that got me into trying to do projects and get
class credit for projects.  When it was time to do my senior capstone for my
computer engineering background, he arranged that the Portland State Aerospace
Society was sponsoring a capstone.  They were building USB-based sensor nodes
for the rocket.  You would have a sensor node gathering information from
gyroscopes or GPS and transmitting that back to the flight computer to be able
to do real-time telemetry.  It was awesome to be able to get get engineering
senior capstone credit for something I was working on as sort of for a
part-time volunteer position.

There was one time I was really frustrated in a programming class that I was
taking, and I was like, oh, this is Yet Another Data Structures Assignment and
they're having us do this weird list of trees of something else, kind of thing.
And so my boyfriend and professor Bart Massey said, why don't you talk to the
professor and see if the data structures class assignment could kind of fit
into your own personal project.  And the personal project was: you've got a
microprocessor with a whole bunch of pins on it, and you can use the pins for
different functionality.  You can have SPI on pins 0 through 4 but you might
have it overlap with GPIO on pins 3 through 6.  If you want certain
functionality on your micro controller, you have to configure which pins.  I
did a combinatorial search program that said "I want this functionality, give
me the pin output for it."  I got to get class credit for two different classes
for that because I negotiated with the professors so I could get credit.

The lesson I took was basically rules can be bent.  Being able to talk with
your professors and being able to get extra credit for cool projects or do
projects with profs, that wasn't something I really thought of as this high
school student from this really small town that's trying to follow the rules.
It's fun to try to be able to find a project that you are passionate about and
see if people will help you work on it.

So in college, Professor Bart Massey beside helping me out with projects
also tried to into introduce me to the local tech scene. In Portland, there
is a large open source community.  And there are a bunch of Linux kernel
hackers that are there.  Every month they get together and have kernel beerings
where they have dinner at some particular restaurant and just sit around and
talk.  So that was like, oh, you should come to these, Sarah.  You should meet
these people.  I was kind of shy and said I don't know if I want to come, what
if I don't drink, is that okay?  He said that's fine.  You should come anyway.
Through that small gathering of tech people I met Greg KroahHartman who was the
USB subsystem maintainer in the Linux kernel.  And Greg was the one that said
to Bart, hey, you know, I have this project a student could work on this new
USB project.  Bart said, oh yeah, Sarah could totally work on this. Again, It
is mentors trying to advocate for you.  Bart helped me get ECE elective credit
to work on this project and got me an Intel undergraduate research grant so I
could get paid to work on the project.  The lesson from that is find a mentor
and do hands on projects as much as you can in college.

So the project I was working on was a basically a new kernel to user space USB
interface.  So you have got most of your kernel drivers, and usually USB
drivers are in the kernel and they talk directly to the USB core.  And then
it's an exception that there are some USB device drivers that are user space.
So they need to be able to pass buffers to transfer down to the USB devices or
read from the USB devices.  And they do that through an interface to the Linux
kernel.

So USBFS is basically that interface.  It is a bunch of system calls.  The
system calls, types it uses is actually Ioctls. And ioctls are like this really
weird system call that are like, if you can't find any other system call that
fits, then use this one.  Basically you just pass a blob down to it and it gets
munged and people fix it in the kernel and decode it.  So basically USBFS 2,
the goal of that was to replace these ioctl calls which were kind of ugly with
standard read-write system calls.  It fit you were sitting there and trying to
read data from the device or trying to write data to the device so it would
make sense to be able to actually use the read-write system calls.  And we
didn't want to make user space blocked so we wanted it to be able to submit
multiple buffers to read from the device so we could saturate the bus
bandwidth.  So we didn't want them to block on each submission.  We said, okay,
we need asynchronous completion of these buffers coming back from the devices.
And there is a Linux kernel API that's called asynchronous I/O and said oh,
wouldn't it be great if we could just use that.  So it is a software
engineering problem to find the right standard Linux kernel interfaces to try
to replace this ugly IOCTL.

So the problem that we ran into was technical debt.  It turns out that at the
time, the asynchronous I/O interface was only used by Oracle.  And it was used
in a very specific way.  They would only write block-sized chunks and they
would never try to cancel those reads or writes.  But The problem with USB
devices, is if the USB device stops responding, you have to cancel the buffer
you submitted to it otherwise you leak the buffer in the kernel.  We needed to
be able to use cancellation with asynchronous IO, but cancellation with
asynchronous IO was completely broken.  So basically We had set up this nice
big software engineering effort and it turned out technical debt stopped us
from actually implementing it in the way we wanted it to.  I was a little
bummed and didn't get the code into the kernel but I had submitted some RFCs
and got my code reviewed by Linux kernel developers.  So my professor Bart said
you should go and present this work at the O'Reilly Open Source Conference, and
I said it "oh, but it's not done, and it might not actually work" and he said
you should present it anyway.  It turned out that Kristen Accardi was on the
paper selection committee for the conference and she is a Linux kernel
maintainer.  And it turns out she was a Linux kernel developer, she was the hot
plug maintainer and she was one of Bart's master's degree students. So She
said, hey Bart, when is Sarah graduating?  We went in and I interviewed for a
job.

So they were looking for Linux kernel developers.  They were looking for
specific characteristics in, you know, open source and Linux kernel developers.
They were looking for someone that was meticulous, someone that would double
check their work before they sent out patches.  If they've got feedback on the
patches theyquickly try to address it and work with the people.  They were
looking for someone that had really good communication skills.  So most of the
open source development is done via mailing list and IRC channels and so you
have to be very clear and concise with your communication and really persuasive
in why you should take my code and take my patch.  They are also looking for
someone that was selflearner, someone that, you know, could go and find
documentation and read up on things before they went and they ask questions.
But also had that delicate balance of when they were stuck they actually knew
they should ask for help.  So it's a balance between being a selflearner and
asking questions.  They were also looking for someone that really preferred to
work in an open source manner, work on public mailing lists and work on IRC's
and comfortable with people looking at your code.  So basically I fit those
bill and I had worked with  I had worked with Bart on this project.  And they
had seen my work that I had done.  I had submitted it to the mailing list and
even though it didn't get accepted Kristen could look back at those mailing
list archives and say Sarah was totally trying to address feedback and trying
to make sure that her code was up to snuff before she sent it.

And so basically through my network, I got a job as a Linux kernel developer
when I graduated college.  And so when you're are thinking about trying to go
through school, try to network with professors, if there are meet ups that are
tech meetups, it is really useful to go to and try to make those connections
with people.  Go to open source conferences.  If your school offers you to pay
for you to go to a conference and present, it is a great opportunity to get to
know people and get to know people in the industry.

So in 2007 I was hired at Intel as a Linux kernel developer.  And the Linux USB
driver, USB3 driver didn't actually get submitted upstream until 2009.  So
there was a two-year period where we were working on the USB3.0 draft
specification.  Draft specification is very interesting because they are trying
to get the wording right so that people implement the hardware correctly and
then you write software to that hardware specification.  So working in draft
form is very much a back and forth of “well I thought I wanted it implemented
it that way but wait, you read it that way and we should clarify this.”  And
the hardware is still in FPGA and so you write some code and then you say “well
is it my code that's broken or is it your hardware that's broken or is it the
spec that's unclear, and it's all, you know, back and forth.

So I was writing the USB  3.0 host controller driver, so that's the orange box
below that basically sits at the very bottom of the kernel stack and it touches
the register interface to the USB host controller driver.  And it submits
packets down to the host controller driver and those eventually go out to the
wire.  A little bit about USB device topology.  If you look at the device
descriptor, there are a couple of different layers of USB.  So there's is a
configuration, there is an interface, and finally there is an alternate setting
that describes the endpoints on devices.  Those are things you send packets to.
It is either an in point that packets are coming into the host or out endpoint
the packets are going to the device and it also specifies how big of a packet
you send, the buffer size.  It specifies the interval.  If you have a periodic
interval how often do you send packets.

When you have something like a USB web cam and you're switching resolutions
and going from a lower resolution to a higher resolution on your USB web cam
you are reconfiguring that device so it sends more data at a more frequent
interval.  There is this configuration stage to go from low Res to high Res and
you have to negotiate with the device, and ask it to switch to the alternate
setting and the device says yes and you start sending packets.  The interesting
change between the USB 1.1 and 2.0 host vs. The USB 3.0 host is that the
USB 1.1 host and 2 host all of this scheduling of the packages on the bus was
done in software.  The host controller drivers were actually unaware of these
endpoints on the device.  It just saw a buffer arrives to me, I go and I put it
in somewhere in the bus schedule where I have space and life goes on.  So it
have this software scheduling.  The USB 3 host controller however supports
virtualization.  So each of the guests believe it is talking to just those
devices on the bus.  So you can't do scheduling in software if you have a
virtual host because each of the hosts could schedule packets at the same time.
So that means you have to do all of the scheduling in hardware which means that
you have a software problem to try to get the information about the device
endpoints down into the host controller driver.  So for this particular
instance, what I needed to do was I needed to take all of the information about
the device endpoints that was in the USB core and basically stuff it down into
the host controller driver.  I need to make completely new API's and go and
touch the USB core and add new API's that the host controller could talk to
which meant I had to deal with these guys.  So these are the USB Linux kernel
USB maintainer, Greg Kroah-Hartman was the overall USB maintainer.  He sends
all them to IS12.  And this is someone I met through the tech scene through
Bart.  And then the three that you see on the bottom on the far left is Alan
stern and he was the USB 1.1 host controller driver maintainer and he
maintained the USB core.  So he was the one that was reviewing my patches and
trying to make sure that the USB core patches were solid before they went in.
David Burnel had since passed was the USB 2 host controller maintainer.  He
also did review my patches as well.  Less so than Alan but some as well.  And
then Oliver Nicum was a developer at Suzay and he worked on device drivers and
power management and this guy could catch conditions just by looking at them.
He was good at you alley indicated this memory here but in this error path you
free it down here.  This was before a lot of the static analysis tools that we
use for the kernel as well.  So these were the USB maintainers that I needed to
deal with in order to make these new API and the USB core.  So being a Linux
kernel maintainer is really interesting.  You get a whole lot of emails every
day.  And it's a very rapid development cycle.  They release every eight weeks.
So you are basically releasing, you do bug fixes for the particular release
while you are getting new features ready for the next release all within an
eightweek period.  A Linux kernel maintainer is always looking at the long term
health of the project.  So is the code maintainable.  Is it usable by different
people, does it work across many different systems?  So they are really looking
at this code that they are going to maintain for five, ten, 15, maybe even 20
years.  When you submit new code to them, they are looking at it as I know you
are probably going to leave and leave me with this code but I am going to
maintain.  That's why they are so picky because they know they are going to end
up maintaining the code that you have.  So basically whenever they send your
code up, their reputation is on the line because they said when they take your
patch, when they take your code, they say I vetted this.  I think it's okay.  I
think it's not going to break anything.  I think it's mostly free of bugs and
usable.  Every time they send your patches up, they are putting their stamp of
approval on them.  So it takes a long time to get code Linux kernel.  Many of
the code, they take up to eight revisions to get to the kernel.  I think a
couple of my patch sets took, like, 10, 15 maybe and if a particular bit of
code touches multiple code systems it takes longer.  All of the coding
standards have to meet community coding style guidelines because people have to
maintain code across the kernel and we need it to be consistent.  Has to be
maintainable as well.  And complete.  So if you have a feature where you think
it's mostly done but maybe you are just missing polished edges on some things,
they want you to polish that.  As soon as it gets into the kernel they have to
maintain it.  If it breaks a system, they have to fix it or rip it out.  Often
when you are doing code submission for new code, the maintainer will say, oh,
well, I think that this particular subsystem could use this.  Could you make
your code more generic so you can both use it or maybe there is old code, could
you factor that because it would be better if you use this function rather than
just copy, paste things.  The important thing too is that when you get new
features in, you have to make sure that it doesn't break other users.  So if
you have got whiz bang new feature on a crumb book but then it breaks someone's
android phone, you can't have that feature.  You have to fix it or rip it out
basically.  So a lot of open source development is technical, but a lot of it
is social.  A lot of it is figuring out the cultural norms around the community
that you are in, the coding style, the tribal knowledge that's undocumented and
dealing with knowing who to send your patches to and knowing how to deal with
particular maintainers of open source communities.  And also it's about trust.
It's about building trust as a coder so that you prove that, you know, you can
write bug free code, that you can work in the style that they want you to, that
you can respond to feedback.  So it's a lot of building social trust and
building social status.  And you can do that in many different ways of open
source communities.  So you can do that by, you know, submitting bug reports
and following up on those.  You can do that by submitting very small patches to
start and working your way up to larger features and you can even do that by
adding documentation to the code that's already there that's undocumented.
Basically ways to show that you know that you have understood the code and you
also want to improve it and stick around in the community.  So eventually my
driver was accepted in 2009, and I got to be a Linux kernel maintainer.  And it
was interesting because I didn't realize how many new things I'd have to learn
as a kernel maintainer.  It wasn't just that I was writing code and maintaining
my own code, but now I had to go review other people's code which was something
completely foreign to me.  So I got to be the one on the other end saying, no,
I think that this is a little messy.  Let's re-factor this or this is not the
right way to do it.  This is interesting for me to go through the whole gamut
of contributing and now I get to take other people's contributions.  And
working with bug reporters is interesting because most of the bug reporters on
open source communities are remote.  So you learn interesting skills about, you
know, okay.  Well, how do I get information and how do I tell someone how to
use GDB or how to get a serial port or get net counsel running so I can get
messages running.  Or maybe I can send a picture of their crash and I have to
figure out how to decode this picture and narrowing it down to where the actual
bug is.  You say, okay, I know this is the system but try this one.  Try that
patch.  I think we have almost got it.  I think it will fix it.  Fix it, good.
Let's see if it fixes this other person that reported as well.  There is this
back and forth of trying to deal with bug reports.  I also learned a lot about
sending pole requests to different maintainers that mostly drag and I learned
how to do things to mark specific bug fixes so they go into the stable kernel
release so you can say, you know, this particular bug was introduced in this
commit which is in the kernel rev that was three kernels ago.  Make sure that
it goes  this fix goes in the kernels that are stable.  So sending pole
requests was making sure that my commits were right, figuring out when in the
release cycle that I could send new features versus when I should only be
sending bug fixes.  It was a lot of back and forth with the community.  So as I
got more confident in being a kernel maintainer and, you know, being the
USB 3.0 driver maintainer I spoke at a lot of conferences.  When I submitted
the driver I opened a video to Reddit, Linux is going to do USB 3 first.  There
is this cool person named Sarah and working on USB3 and you should get to know
her.  So I ended up speaking at a whole bunch of different conferences from
Japan to Australia, France, North American Europe, they were awesome enough to
pay for going to conferences and speak of the stuff I'm doing.  So I got to
promote myself as a leader in open source.  I got to go and speak at
conferences and talk with other kernel developers and really interact with them
and until they recognized that I was an awesome person in the kernel community
and they invited me to the Linux kernel which is only for top developers around
the world.  That was my journey of how I started from a high school student
that really didn't program at all until she went to college until now when I'm
a Linux kernel developer.  So I hope that by sharing this story that some of
you get inspired that there are many, many different steps of being a leader in
software.  I hope you look at where you are and realize it's a journey and I
hope you enjoy it.  So if you want to learn more about Linux kernel
development, there is a lot of different resources that I have included.  And I
am definitely available to answer questions.  So thank you very much.
[APPLAUSE]

## Q&A ##

**Sarah:** Alright.  If you have questions you can step up to the mic.  Don't
be shy.  I won't bite!

**Audience member:** Hi.  Can you talk about your work on Yocto and explain
what you are doing?

**Sarah:** So Yocto is an interesting project.  It's not a Linux distribution
but allows you to make an embedded Linux distribution.  So you can define
recipes that says I want this package of this software and this kernel version
and pull in these libraries and pull these patches on top of them and make you
a custom embedded distribution.  So there's a couple different things I'm
working on there.  One of them is getting it to work in windows because we will
have a Linux run in windows.  There is some interesting things about different
packet that is we want to move in and I am moving into Yocto now so learning
about the recipes and systems.  That's basically where I am on the Yocto
project.  There is cool people doing interesting stuff on Yocto.  There is John
Howley who is the minnow board advocate and really cool stuff that you can do
with Yocto.  And there is a Google plus group and Facebook group and check it
out.  There are cool demos.

I was briefly working on within the chrome group working on Linux graphics and
now I'm with the Yocto group.  So hence the short transition to the Yocto
group.
<br>

**Audience member:** Could you give a little bit more information on how
someone might get involved in open source&mdash;like, first steps?  It's a very
big world with all sorts of projects.  How might I get involved if I
wanted to?

**Sarah:** Sure.  There's lots of different ways to get involved in open
source.  One of the ways is to get sort of overview of all the different open
source projects out there or some of them anyway is you can go to openhatch.org
and projects you can register themselves and tell you you need these particular
skills to work on this project so here is a tutorial to learn those.  So
openhatch.org is a good way to get involved.  If you want to get involved and
get a paid internship to work on open source, there is a program called the
FOSS Outreach Program for women which is a three-month paid internship for
women and gender fluent and free individuals as well.  The application period
just closed but it runs twice a year.  So you can have your internship either
in the winter months or in the summer months.  The next application period is
in March.  So if you are interested in that, go to the kernel Newbies.org or
the OPW website at the bottom.  So you can actually get a three-month paid
internship.  It's 5,500.  You don't have to be a student either to be  to get
one of these OPW internships.  So if you know of other women in the community
that might be interested in being involved in open source that's a good way to
get involved.  Another way is to just poke around on the mailing list of a
project you are interested in.  Figure out what you are passionate about.
Maybe you are passionate of web Dev or kernel drivers.  All of these open
source communities have a mailing list that you can go and subscribe to.
Usually you can figure out people are talking about problems in this particular
area.  Maybe I can read that part of code and try to figure out what they are
doing.  Maybe you can ask questions on the mailing list or try to find
documentation on the project.  Most of the projects have everything on the web.
So you will be able to find documentation, tutorials and sometimes they will
have how to get into this first kind of first tutorials for you.

**Audience member:** I should also mention that there is anything at Waterloo
at UCOSP and that helps students get involved in open source as well.
<br>

**Audience member:** I had read somewhere that&mdash;I don't know if it was
you&mdash;that kernel developers were accused of being sexist or weren't open
to women developers or perhaps the community itself and not specific
developers.  Could you shed some light on that?

**Sarah:** So basically I thought that some of the there was some
communications on the mailing list that I felt were vaguely disrespectful to
people and some of them were quite blatantly disrespectful to people.  So we
had a conversation about basically community norms, behavioral norms within the
community.  Some of the cultural change takes a long time.  Some of that is
being addressed, some of it is being looked at.  it was sort of very  the kinds
of communication I was looking at were things like basically tearing people
down personally, just sort of ripping them apart.  And for me that kind of, you
know, of try to verbally tear someone down is not appropriate for mailing list.
It's not appropriate behaviour.  That's what I was trying to advocate for.  in
criticizing the patch, I think you said they would criticize a person
themselves or the patch or work of the person.  basically my stance has always
been you can be technically brutal and go and try to correct people's
behaviour.  But you can do that in a way that is personally respectful to them.
So that has been my viewpoint.  so were they like unprofessional to everyone or
especially to everyone.  I think it affects everyone but I think that women are
the canary in the coal mine.  People say we don't have a lot of minorities in
our community and perhaps that's why.  All right.  Other questions?
<br>

**Audience member:** [inaudible].

**Sarah:** see my mentor was awesome because Bart Massey introduced
me to all sorts of people in the industry.  He had an impact I got to
know in tech and networking and eventually leading up to my job.  I
really recommend highly getting a mentor.
<br>

**Audience member:** I just have a couple questions to ask you... first about
to refresh my memory, are you still, what was the position regarding the Linux
kernel... shoot.  I forget what it was.  Management or something, I forget.

**Sarah:** I was never a manager.  I was a Linux kernel maintainer.

**Audience member:** Okay!  Are you still in that position or...

**Sarah:** So I wanted to move and do something different than USB.  I actually
passed on that maintainership to Mateo Sniman which is in kernel.  But I think
that knowing you are going to get bored with technology with USB and come up
with a succession plan to get someone in after you is a really important thing
to do for your job or career in tech or even if you are a professor and you
need to take a sabbatical and do something different to refresh your skills in
industry or work at a different university, there is a lot of different things
you need to do to be sure to manage your time and try out new things.

**Audience member:** My other question is now that you have developed the
driver for USB 3.0, what's your next step?  Are you going to try to convince
Microsoft, apple, and all those developers to support that version of a USB?

**Sarah:** No.  So the driver that I wrote was written against the USB spec.
So basically I wrote a driver that said this is how  the spec said this is how
you talk to software.  So I wrote a driver that that was how I talked to
software.  Microsoft has their driver that talks exactly the same way to that
software.  So there is no reason for there to be one true driver that everyone
uses, you know, as long as the driver is writing written to the spec it doesn't
matter if Microsoft doesn't use mine or not.  will that actually make a
difference for phones.  so if you are running android and you have got host
mode and you have got a USB 3 host controller, you are running my code.  But if
someone has a windows phone that has a USB 3 host controller, they are running
the windows phone.
<br>

**Audience member:** Where do you find a mentor?  [LAUGHTER] [APPLAUSE]

**Sarah:** yes.  It's really hard to figure out.  So one of the things that I
did as an undergraduate, when I first started as an undergraduate I was shy
around my professors.  I don't want to go to office hours because they might
know that I don't know things.  And I don't know about trying to  these
professors, you put them on a pedestal and say I don't want to talk to them.
If you can actually realize that your professors are people too and get to know
them and figure out what interests them and maybe they have got a project that
is interesting to you.  So you can get mentors who are professors.  You can
always get involved in tech meet ups and things like that and you start hanging
out with other people in tech and you say  you never really ask someone to be a
mentor.  Maybe you just ask for their advice but you don't have formal things.
There are formal things like Intel has for women and leaders they have a
specific mentoring group and you can connect with mentors to what your careers
are.  There is no, like, be a mentor group on Facebook, you know.  So you just
kind of find them as you go along.
<br>

**Audience member:** hi, Sarah.  I really enjoyed your talk.  I am actually the
instructor for the operating course at the University of Waterloo.  Hopefully
some of my students are here.  I did advertise in my class.  I told them if
they like what they are doing in the course, they should come hear the talk
from a Linux kernel developer.  I guess my question is at Waterloo at least
currently we are using this more or less toy operating system to teach the
operating system course, the software 161 developed by Harvard.  I was
wondering, have you seen other schools or programs where they are able to use
Linux as a teaching tool rather than one of these, you know, less fully
featured operating systems?  Because I feel like a lot of the students are
excited to do this work but at the same time doing the project, I don't feel
comfortable saying go and hack the Linux kernel.  I was wondering if you had
advice.

**Sarah:** I have done the operating system where they had the toy OS.  I ran
into issues where I'm like the link thing doesn't do what I thought it would
do.  Because I have been reading on link list operations.  I don't understand
and I can't put this in multiple lists and why can't I do that.  I have done
the operating systems class where it was a toy IOS and it was frustrating and
you don't want to work on it after wards.  There is actually a professor at the
Portland state university Doug Hall who I mentioned and he teaches an embedded
operating system.  And he uses Linux and Intel atom boards and write a device
driver.  I think that's way more hands on.  I also took an advanced operating
systems internal class and making the character device and doing all sorts of
debugging and that's pact call.  If I had my druthers, the class would be
taught with the Linux kernel.

**Audience member:** I'm just going to sneak in here and let people know you do
have a class you can write an embedded operating system and people refer to it
as trains but it's real time operating system CS 452.
<br>

**Audience member:** so you mentioned that open source is equal parts technical
and social.  I thought that was interesting especially with regards to
harassment but in general interaction with people.  Do you think that some
harassment or less severe issues are  I don't know anything because people are
going to make fun of me because

**Sarah:** I think it's interesting that people in the Linux kernel are nice to
newcomers who are students.  As soon as they know you are paid to work in open
source they are harsh because you are paid to do professional development.  You
should be able to find a mentor to help you out.  If you are a student, they
are really nice to you guys.  Within the Linux kernel community there is a
project called the staging drivers and these are drivers they need a lot of
clean up.  The staging driver mailing list you can send little clean up patches
to and Greg KroahHartman is nice to those people in those drivers because they
are cleaning up crap.  I think too with open source because it's so much back
and forth written communication, sometimes you feel depersonalized because you
are typing all the time and you are just typing to a particular screen.  And
it's hard to also, you know, see nonverbal cues.  So if someone  you know, they
make a joke and you see that they make a joke.  It's hard to hear if people
make a joke on the Internet that's really subtle.  I also think that with open
source development, there's often so much email coming in.  Especially with
newcomers asking the same question, sometimes people get frustrated.  What I
have done is when I get a question with newcomers and they are asking the same
question, I will go make a FAQ on a Wiki and point them to that.  And try and
transfer the knowledge.  I think that a lot of open source developers are so
caught up in their every day lives of getting their jobs done it is difficult
to make time to make those Wiki's and FAQ to mentor people in there.  It is a
difficult situation because of how much time they spend doing open source
development.
<br>

**Audience member:** when you talked about being offered your first job or
interviewing your first job you talked about the qualities you had that the
person interviewing you thought would make meant so you would probably be a
good fit for open source development.  Are there qualities or habits or
something that would make you a bad fit for an open source community?

**Sarah:** the qualities that, you know, someone when I see this in people
interviewing the red flags, there is a certain type of person that you will
point them to a particular document, you asked a question and I think this
document answers it.  And they don't read the whole document before they ask
you, like, more questions.  And you can tell from the questions that they ask
that they haven't read it.  There is also the kind of person that  so that was
sort of the meticulous mind set if someone tells you, you should read the whole
thing or ask questions when you don't understand the documentation but don't
ask questions before you read the documentation.  There is also people you tell
them and give them feedback but they don't internalize the feedback so they
make the same mistake over and over again.  Those are the frustrations that
open source developers come across.  If you are responsive to feedback, if you
are trying, if you, you know, try to make a list of all the feedback that you
have gotten on a particular patch set and make sure the next time you submit
the patch set you go through and try to make sure you don't make the same
mistakes again.  If you make a new mistake, that's fine.  You didn't know about
that before.  That's sort of the two that are kind of regular flags for things
that make it difficult to be open source.  There's also people that if you
don't communicate well in English, then it's difficult to be an open source
developer.  Because most of the communication is written English.  More
questions.
<br>

**Audience member:** hi.  I just first of all like to thank you for coming.  My
question is I was thinking about what you were saying about the open source
community building you have to go through the process of building trust and
stuff like that, but also separating personal criticism and technical criticism
and you yourself were in a position to say this needs to be prettier or better
with different subsystems.  Do you think they are specifically the open source
or for profit development community has more power or ability or even just
willingness to embrace their ideas?  Do you think one community has more than
the other.

**Sarah:** Sorry, more of what?

**Audience member:** More... oomph.  I don't have a good word for it but more
oomph.

**Sarah:** So more oomph to get things more technically sound? Is that what
you're saying?

**Audience member:** Getting them into a real thing but also taking an abstract
idea, allowing someone who has that to refine it and build it into something
actually real.  Do you think, like, one has advantages over the other or is
better or just&mdash;what are your general thoughts on that?

**Sarah:** There are sort of trade offs between proprietary software and open
software.  Basically with proprietary software, if things are hacky, you get to
sweep that under the rug.  If it works, that's fine.  It maybe crashes but you
don't care because you don't get service from people because they are not
paying you.  Open source, because it's open, people are looking at the code and
so they are way more meticulous with open source development.  That's not to
say that open source doesn't have bugs.  It does.  With many eyes on the code
or because the code is out there, you still have bugs like the open cell bugs
that came out.  Even though that was out there for many, many years, bugs
existed.  If the right people are not working on the right open source
software, you will have bugs.  But I really like the open source methodology.
Because I feel like it gets me to work with people that are across the world
and I get different perspectives on code.  I also really like that open source
has a higher technical standard than proprietary software.  I like writing, you
know, meticulous code.  I like writing really good commit messages, because I
know that the next person that's going to take out my code or try to back port
my patches, I want to help them out.  Basically I feel like open source is
about help other people and collaborating with a community and I like that.
It's not better or worse than proprietary.  Because you can have a community
with proprietary, but I just like open source better.
<br>

**Audience member:** You mentioned some static analysis tools being used for
device drivers.  I know for a fact that Microsoft uses formal methods and
model-checking and condition detection.  I am wondering if there is a similar
effort for Linux?

**Sarah:** There are static analysis tools, COSNL is one to look at.  That is
Julia wall who is awesome.  It is to say I have a particular class of bug and
write a pattern and match that pattern throughout the code and figure out where
more bugs are.  You can add that script and run the COSNL.  Dan has a whole
bunch of different tools to do static analysis and also, you know, things like
snatch and what was the other one?  Things like sparse that do static analysis
checking as well.  In the Linux make C equals 1 it will run sparse and say
things like, well, you used this value uninitialized down here or you have, you
know, a switch statement with a nondefault flag or case basically, things like
that where, you know, there could be a bug in there and you really need to look
at it.  So one of the things that we try to require doing kernel patches is you
can't make more compiler warnings but they will run COS or sparse and there is
an automated infrastructure called the zero day infrastructure that one of my
coworkers a Intel works on where the Linux has their trees on kernel.org or
other place and the zero infrastructure pulls from those kernel trees and
automatically email them if they introduce a patch with these sparse warnings.
It's useful you are testing someone's code, push it to a branch and within ten
minutes you get an email saying you added extra warnings or sparse issues.
It's awesome.

I think that was the last question.  Thank you all for having me.  This was
fun!
