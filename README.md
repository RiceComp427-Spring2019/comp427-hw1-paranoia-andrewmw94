# <img src="http://www.rice.edu/_images/rice-logo.jpg" width=180> Comp427, Spring 2018, Homework 1
## Rational Paranoia
The homework specifications, as well as the corresponding course slide decks,
can be found on the [Comp427 Piazza](https://piazza.com/class/jqifhp864b37ju).
This assignment is due **Thursday, January 17 at 6 p.m.**

You will do this homework by editing the _README.md_ file. It's in
[MarkDown format](https://guides.github.com/features/mastering-markdown/)
and will be rendered to beautiful HTML when you visit your GitHub repo.

## Student Information
Please also edit _README.md_ and replace your instructor's name and NetID with your own:

_Student name_: Andrew WELLS

_Student NetID_: aw34

Your NetID is typically your initials and a numeric digit. That's
what we need here.

_If you contacted us in advance and we approved a late submission,
please cut-and-paste the text from that email here.**

## Problem 1
- Scenario: **Grading**
- Assumptions:
  - This is something that I actually do, so my assumptions will be the set of true propositions for COMP 382.
  - Among these assumptions, we're assuming the grading platform is "as secure as it will get." This hold because I don't have influence over canvas. 
- Assets:
  - Approximately thirty undergrads and grad students with a passion for justice and a nose for illicit cooperation.
  - Approximately 8 hrs per week per TA (so 240 man hours per week).
- Threats:
  - Unscrupulous undergrads that want to pass a required class.
  - Inquisitive undergrads who want to see what they can get away with?
  - Inconsistent grading caused by subjective factors.
  - An obligation to respond to all emails complaining about the class.
- Countermeasures:
  - Rather than assigning **n** assignments to each TA, give each TA **k x n** instances of problems to grade. Thus the grading is as consistent as possible across assignments (no assignment is entirely graded by one TA). This can be done easily with a software package.
  - Randomly shuffle pairings of TA's and student's. (I.e., don't use alphabetical.) This could be handled by the same software package.
  - Have the TA's grade in random order to avoid subjective bias. (e.g., the first assignment may be graded more harshly on average.) The software package could present assignments in a random order.
  - Have the student's identity hidden from the TA's. The software package can hide the student's names. Other identifying information would be difficult to detect/remove.
  - Use a tool such as MOSS to detect plagiarism in code. This can be automated fairly easily for each assignment.
  - Have some limit to students' regrade requests to prevent incessant emailing. This is hard to do in a fair, one-size-fits-all manner. Maybe have some possible penalty for regrading (e.g., can lose points or gain them) to discourage it.
  - Attempt to characterize problems into some small number of classes. Then have TA's communicate to attempt consistent grading and detect plagiarism. This is very hard to do in a robust way. Grades will probably have a fair amount of randomness due to subjective factors. Having enough assignments throughout the semester will hopefully cause the information to outweigh the noise.

## Problem 2
- Scenario: **Stadium**
- Assumptions:
  - With D1 schools spending up to 50 million dollars on their football teams in a given year, it seems evident that some people care about these teams a lot. The ultimate goal of each team is presumably to win the national championship game. We will assume that attempts to do this will not utilize resources on the nation-state level (e.g., satellites will not be used to spy on opposing teams' practices). We will not assume morality (i.e., we will assume that there is at least a small group of people that are happy to cheat to help a given team win.), but we will assume that there is no one willing to risk life in prison to hurt a given team (e.g., no assassination attempts).
- Assets:
  - A small portion of the 50 million dollar budget. Let's say 5 million.
  - A large staff, say 97 people not counting the players. We'll also assume we can hire a few new employees (say 3 people).
- Threats:
  - We'll use www.yourteamcheats.com to find common ways teams cheat and try to cover those. Additionally, we'll try to look at new ways teams could use technology to cheat:
  - Disqualification. Anything from academic probation to performance enhancing drug (PED) use can disqualify a player. NFL teams don't have academic probation, but PEDs have resulted in suspensions. While this would give some short-term benefit to our players, we will assume that the net result for our team is negative as such acts are likely to be detected and punished.
  - Illicitly taping the other team. Games are open to the public, but practices are not supposed to be taped by opposing teams. Historically, this has been a person attending practice with a camcorder. We would also like to prevent people recording using cell phones and "fans" placing small cameras around the stadium prior to the practice.
  - Placing radios in helmets would be useful, but it is illegal. We would like to detect any opposing team that uses such radios.
- Countermeasures:
  - To deal with disqualification, we will encourage "appropriate" behavior by having our players shadowed. Note that this is already done at major schools (players have individual "tutors" ensuring they attend class etc.) so it does not cost additional resources. Hopefully this also discourages PED use. We won't *actually* perform drug tests because we don't want to catch our players. We just hope they don't get caught by anyone.
  - To deal with taping, we would essentially need to prevent the use of electronics within the stadium. While we could use EMPs to destroy them, this would damage other systems and probably not be worth the cost. Instead, we can try to exclude non-team members from the stadium during practices and task a small number of team staff members to look for people holding cameras / phones during practice among the few people we do allow in the stadium. To deal with small cameras, we could assume they use common communication protocols and monitor for unusual signals. If these signals are detected, it should be possible to locate the source using a kalman filter or similar.
  - Placing radios in helmets would be difficult to detect, but again monitoring for unusual signals could detect this form of cheating.

## Problem 3
- Scenario: **Research on My Computer**
- Assumptions:
  - Again, this is a real scenario that I face, so my assumptions are the set of true statements concerning computer security at NASA.
  - Specifically, we assume I'm powerless to change any security policies implemented by IT.
- Assets:
  - My assets are myself, spending approximately 8 hours per day.
  - Hardware I am given / bring. This includes a NASA desktop and my personal laptop.
  - NASA has an internal network that is (hopefully) secure from the outside world. The NASA desktop is on this network. My personal laptop is connected to the world-wide web.
  - I also have access to very expensive hardware. Code I write can be run on this hardware, but it is not connected to a network while it runs.
- Threats:
  - Here, we will divide threats into two classes. First we will consider threats from overtly malicious entities. Then we will consider threats from the IT department.
  - For overtly malicious entities, we have other actors (e.g., the Chinese) who apparently think NASA code is worth stealing. Based on my experience, these people are more to be pitied than feared, but I signed something saying I'd protect NASA secrets, so I'll get in trouble if I don't.
  - The presumed attacks would be attempts to access the NASA network or to read secrets I place on a device connected to the world-wide web.
  - Non-approved USB drives are forbidden at the workplace, but this rule is not generally followed. Hopefully all such drives are quarantined to their respective networks. (Personal drives only used with personal computers. NASA drives only with NASA computers.)
  - A malicious entity could destroy the robot hardware by modifying low-level controllers for e.g., the motors or cooling systems.
  - For the IT department, the goal seems to be preventing anything from happening. If nothing happens then nothing bad happens. This approach is foolproof.
- Countermeasures:
  - External software (e.g., Linux) is installed from NASA approved USB drives. I don't know how it got there, but that's not my fault. If my computer is compromised by this, then so is everyone else's, so the additional risk is negligible.
  - Internal software is installed from internal servers. Again, if these are compromised, then my computer isn't going to make things worse.
  - For some external software that is not hosted, I need to build it from source. Here I'm assuming that the software is not malicious, that the compiler I'm using is correct, and that the means of obtaining the software that I use is safe. The first assumption seems reasonable, because the software packages are widely used and the creators have no reason to expect them to be used at NASA. If the compiler provided by the USB stick is compromised, again I am not making things worse. The weakest point is probably my means of obtaining the software. I download it, comparing the hash against the reported hash for the download. This makes it unlikely that the software is compromised.
  - To protect the robot hardware, all software is reviewed by at least three people before it is run on the robot. Additionally, the robot is not connected to the network while it runs. The damage that could be caused is fairly large (approximately 3 million dollars of hardware), but the probability that malicious code would make it past the inspection process and operate while not connected to a network seems small. Additionally, code for low-level controllers has a separate review process, safety systems are two-fault tolerant, and the robot is always run with a human read to press the E-stop.
  - In general, the theme here is "I'm not making things worse than they already are." This is a useful reduction to avoid worrying about a variety of things.
  - There are no known countermeasures to the IT department. They install a key logger and remote administration tool on your computer (and presumably other stuff, but they just say there is "no reasonable expectation of privacy."). If needed, I could send requests to the IT department to host executable for other software packages on the NASA network, but it seems easier to install them from source.
