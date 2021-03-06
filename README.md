# CSCI 466: Computer Networks

CSCI 466 - Networks - Montana State University - Fall 2021

## Links

- [CSCI 466: Computer Networks - Syllabus](https://docs.google.com/document/d/e/2PACX-1vSToCOvQShCN07u-9DrPyQN8cQCMv1iCgMoDx_0oLqyhqzk430dSkx_UXNP3FvHA9YFXNpv_jd6epVm/pub)
- [Course Schedule](https://docs.google.com/spreadsheets/d/e/2PACX-1vQ1ZO6jz-Y3k7JHQxofdxSlC7fjVH9h7WEgej-DTcPwE9fnbjmOft4t9M-KBn6_uC_XMXuwQDxkfBEO/pubhtml?gid=0&single=true)

> This is the tentative course schedule. We might move some topics around and make a few lecture substitutions due to my travel, or opportunities for interesting guest lectures. The programming assignment, homework, and lab deadlines are also tentative and meant to allow you to broadly plan your time. Please pay attention to deadlines posted for D2L assignments/quizzes - they are the official ones.

## Syllabus - Fall 2021

### Instructor

Mike Wittie

### Course Description

A computer network is an ecosystem of physical links and communication protocols that allow digital communications between distant computers. Networking technologies are a foundation for distributed systems, such as the Internet, and the Web. This course will investigate the fundamentals of network system design and explore some of the emerging trends in network communications including cloud computing and wide area wireless communications.

### Calendar

<table>
	<tbody>
		<tr>
			<th id="0R0"><div>1</div></th>
			<td>Week</td>
			<td>Topic</td>
			<td><div>Book Sections</div></td>
			<td>Assignments</td>
		</tr>
		<tr>
			<th id="0R1"><div>2</div></th>
			<td>8/25</td>
			<td>Course introduction</td>
			<td></td>
			<td></td>
		</tr>
		<tr>
			<th id="0R2"><div>3</div></th>
			<td>8/27</td>
			<td>OSI stack and Internet Topology</td>
			<td>1.5</td>
			<td></td>
		</tr>
		<tr>
			<th id="0R3"><div>4</div></th>
			<td>8/30</td>
			<td>Data forwarding and network performance</td>
			<td>1.3, 1.4</td>
			<td></td>
		</tr>
		<tr>
			<th id="0R4"><div>5</div></th>
			<td>9/1</td>
			<td>Internet history and application requirements</td>
			<td>1.7, 2.1</td>
			<td></td>
		</tr>
		<tr>
			<th id="0R5"><div>6</div></th>
			<td>9/3</td>
			<td>Socket Programming and HTTP</td>
			<td>2.2, 2.7</td>
			<td></td>
		</tr>
		<tr>
			<th id="0R6"><div>7</div></th>
			<td>9/6</td>
			<td>Labor Day - No Class</td>
			<td></td>
			<td></td>
		</tr>
		<tr>
			<th id="0R7"><div>8</div></th>
			<td>9/8</td>
			<td>PA 1 - Socket Communications</td>
			<td>2</td>
			<td><div>HW1 (Chapter 1) Due</div></td>
		</tr>
		<tr>
			<th id="0R8"><div>9</div></th>
			<td>9/10</td>
			<td>FTP, SMTP, DNS</td>
			<td>2.3, 2.4</td>
			<td></td>
		</tr>
		<tr>
			<th id="0R9"><div>10</div></th>
			<td>9/13</td>
			<td>CDNs</td>
			<td>2.6</td>
			<td></td>
		</tr>
		<tr>
			<th id="0R10"><div>11</div></th>
			<td>9/15</td>
			<td>P2P</td>
			<td>2.5</td>
			<td></td>
		</tr>
		<tr>
			<th id="0R11"><div>12</div></th>
			<td>9/17</td>
			<td>UDP</td>
			<td>3.1-3.3</td>
			<td></td>
		</tr>
		<tr>
			<th id="0R12"><div>13</div></th>
			<td>9/20</td>
			<td>RDT</td>
			<td>3.4</td>
			<td><div>Lab 1 (DNS) Due</div></td>
		</tr>
		<tr>
			<th id="0R13"><div>14</div></th>
			<td>9/22</td>
			<td>RDT</td>
			<td>3.4</td>
			<td></td>
		</tr>
		<tr>
			<th id="0R14"><div>15</div></th>
			<td>9/24</td>
			<td>Pipelining</td>
			<td>3.4</td>
			<td></td>
		</tr>
		<tr>
			<th id="0R15"><div>16</div></th>
			<td>9/27</td>
			<td>PA 2 - Reliable Transport</td>
			<td></td>
			<td><div>PA1 (HTTP server) Due</div></td>
		</tr>
		<tr>
			<th id="0R16"><div>17</div></th>
			<td>9/29</td>
			<td>TCP handshake and flow control</td>
			<td>3.5</td>
			<td></td>
		</tr>
		<tr>
			<th id="0R17"><div>18</div></th>
			<td>10/1</td>
			<td>TCP congestion control</td>
			<td>3.6, 3.7</td>
			<td></td>
		</tr>
		<tr>
			<th id="0R18"><div>19</div></th>
			<td>10/4</td>
			<td>TCP congestion control</td>
			<td>3.6, 3.7</td>
			<td></td>
		</tr>
		<tr>
			<th id="0R19"><div>20</div></th>
			<td>10/6</td>
			<td>Data forwarding methods</td>
			<td>4.1, 4.2, 4.4</td>
			<td><div>HW2 (Chapter 2, 3) Due</div></td>
		</tr>
		<tr>
			<th id="0R20"><div>21</div></th>
			<td>10/8</td>
			<td>IP addressing and DHCP</td>
			<td>4.3.1 - 4.3.3</td>
			<td><div>Lab 2 (TCP) Due</div></td>
		</tr>
		<tr>
			<th id="0R21"><div>22</div></th>
			<td>10/11</td>
			<td>NAT and IPv6</td>
			<td>4.3.4, 4.3.5</td>
			<td></td>
		</tr>
		<tr>
			<th id="0R22"><div>23</div></th>
			<td>10/13</td>
			<td>LS and DV routing</td>
			<td>5.1, 5.2</td>
			<td></td>
		</tr>
		<tr>
			<th id="0R23"><div>24</div></th>
			<td>10/15</td>
			<td>RDT Lab</td>
			<td></td>
			<td></td>
		</tr>
		<tr>
			<th id="0R24"><div>25</div></th>
			<td>10/18</td>
			<td>ICMP, RIP, OSPF, and BGP</td>
			<td>5.3, 5.4, 5.6</td>
			<td><div>PA2 (Reliable Data Transmission) Due</div></td>
		</tr>
		<tr>
			<th id="0R25"><div>26</div></th>
			<td>10/20</td>
			<td>PA 3 - Data Plane</td>
			<td></td>
			<td><div>HW3 (Chapter 4) Due</div></td>
		</tr>
		<tr>
			<th id="0R26"><div>27</div></th>
			<td>10/22</td>
			<td>Anycast, Broadcast, and Multicast</td>
			<td>5.4.4</td>
			<td></td>
		</tr>
		<tr>
			<th id="0R27"><div>28</div></th>
			<td>10/25</td>
			<td>Link layer introduction and class activity</td>
			<td>6.1</td>
			<td></td>
		</tr>
		<tr>
			<th id="0R28"><div>29</div></th>
			<td>10/27</td>
			<td>MAC protocols</td>
			<td>6.3</td>
			<td></td>
		</tr>
		<tr>
			<th id="0R29"><div>30</div></th>
			<td>10/29</td>
			<td>MAC protocols</td>
			<td>6.3</td>
			<td></td>
		</tr>
		<tr>
			<th id="0R30"><div>31</div></th>
			<td>11/1</td>
			<td>PA 4 - DV Routing</td>
			<td></td>
			<td><div>PA3 (Data Plane) Due</div></td>
		</tr>
		<tr>
			<th id="0R31"><div>32</div></th>
			<td>11/3</td>
			<td>Error Correction and ARP</td>
			<td>6.2, 6.4.1</td>
			<td></td>
		</tr>
		<tr>
			<th id="0R32"><div>33</div></th>
			<td>11/5</td>
			<td>Error Correction and ARP</td>
			<td></td>
			<td></td>
		</tr>
		<tr>
			<th id="0R33"><div>34</div></th>
			<td>11/8</td>
			<td>Ethernet and packet switching</td>
			<td>6.4.2</td>
			<td><div>Lab 3 (ARP) Due</div></td>
		</tr>
		<tr>
			<th id="0R34"><div>35</div></th>
			<td>11/10</td>
			<td>MPLS and Datacenter Networks</td>
			<td>6.5, 6.6</td>
			<td></td>
		</tr>
		<tr>
			<th id="0R35"><div>36</div></th>
			<td>11/12</td>
			<td>PA 5 - MPLS</td>
			<td></td>
			<td><div>PA4 (Control Plane) Due</div></td>
		</tr>
		<tr>
			<th id="0R36"><div>37</div></th>
			<td>11/15</td>
			<td>SDNs</td>
			<td>4.4</td>
			<td></td>
		</tr>
		<tr>
			<th id="0R37"><div>38</div></th>
			<td>11/17</td>
			<td>WiFi</td>
			<td>7.3</td>
			<td></td>
		</tr>
		<tr>
			<th id="0R38"><div>39</div></th>
			<td>11/19</td>
			<td>Cellular</td>
			<td>7.4</td>
			<td><div>HW4 (Chapter 5, 6) Due</div></td>
		</tr>
		<tr>
			<th id="0R39"><div>40</div></th>
			<td>11/22</td>
			<td>Thanksgiving Break - No Class</td>
			<td></td>
			<td></td>
		</tr>
		<tr>
			<th id="0R40"><div>41</div></th>
			<td>11/24</td>
			<td>Thanksgiving Break - No Class</td>
			<td></td>
			<td></td>
		</tr>
		<tr>
			<th id="0R41"><div>42</div></th>
			<td>11/26</td>
			<td>Thanksgiving Break - No Class</td>
			<td></td>
			<td></td>
		</tr>
		<tr>
			<th id="0R42"><div>43</div></th>
			<td>11/29</td>
			<td>IoT, Mobile IP, and Military Datalinks</td>
			<td></td>
			<td><div>Lab 4 (SDN) Due</div></td>
		</tr>
		<tr>
			<th id="0R43"><div>44</div></th>
			<td>12/1</td>
			<td>Multimedia Encoding</td>
			<td>9.1-9.3</td>
			<td></td>
		</tr>
		<tr>
			<th id="0R44"><div>45</div></th>
			<td>12/3</td>
			<td>Quality of Service</td>
			<td>9.5</td>
			<td></td>
		</tr>
		<tr>
			<th id="0R45"><div>46</div></th>
			<td>12/6</td>
			<td>Secure communications</td>
			<td>8.5-8.6</td>
			<td><div>HW5 (Chapter 7) Due</div></td>
		</tr>
		<tr>
			<th id="0R46"><div>47</div></th>
			<td>12/8</td>
			<td>Secure communications</td>
			<td>8.5-8.6</td>
			<td></td>
		</tr>
		<tr>
			<th id="0R47"><div>48</div></th>
			<td>12/10</td>
			<td>Firewalls and IDS</td>
			<td>8.9</td>
			<td><div>PA5 (MPLS) Due</div></td>
		</tr>
	</tbody>
</table>


#### Course Prerequisites

- CSCI 232: Data Structures and Algorithms
- CSCI 366: Computer Systems

### Goals

- __Course goals__:
  - List the __network layers__ and explain their function in end-to-end communications
  - Explain the tradeoff between hop-by-hop and end-to-end network mechanisms
  - Design and implement and networked application
  - Analyze network traffic
  - Measure network performance
  - Identify and describe network performance bottlenecks
  - Configure and troubleshoot a wide area network
- Criterion 3 Student Outcomes Addressed:
  - Outcome 2: Design, implement, and evaluate a computing-based solution to meet a given set of computing requirements in the context of the program???s discipline.
  - Outcome 5: Function effectively as a member or leader of a team engaged in activities appropriate to the program???s discipline.
  - Outcome 6: Apply computer science theory and software development fundamentals to produce computing-based solutions.

### Grading

I want this course to be engaging and productive in terms of the knowledge and skills you will acquire. To accomplish both tasks, I will ask you to do some work. I have structured the grade criteria to give you incentive to stay engaged and succeed in the course and to give you a solid background preparation to define and complete a network design project.

- Programming assignments - 40%
  - Designed to give you practical experience with protocol implementation
- Wireshark labs - 20%
  - Designed to give you practical experience with network tools
- Homeworks - 40%
  - Designed to give you practice on concepts
- Extra credit - ?%
  - We reserve the right to offer extra credit for particularly clever answers in-class problems.

Unless otherwise instructed, all assignments must be submitted by 11:59PM on the due date. Late assignments will lose 10% of total credit for missing the original deadline and then for every day they are late. Homework assignments must be completed individually. The project will be completed in pairs.

### Instruction

Lecture: MWF 12 - 12:50PM REID 202 in person

Course schedule, lecture slides, and assignments are posted on the course D2L page.

### Office Hours

Prof. Mike Wittie: Wednesdays 3:10PM - 6PM by appointment via: <https://www.montana.edu/scheduler/login/student/?fac=966>.
**Please select the earliest available appointment for any given day.**

Mr. Saidur Rahman (Course TA): Mondays 3:10PM - 4PM BARNAH 346

### Course Textbooks and Materials

[Computer Networking: A Top Down Approach 7th edition by Jim Kurose and Keith Ross](https://www.google.com/url?q=https://www.amazon.com/Computer-Networking-Top-Down-Approach-7th/dp/0133594149&sa=D&source=editors&ust=1629771194792000&usg=AOvVaw2nVE6cm6HJFHYWgXO9LaTn)

### Class Attendance

Class attendance is mandatory. You are responsible for the material covered in class. Prepare in advance for class by reading and studying the assigned text, and by making sure you understand the previous lecture.

### Policy on Academic Integrity

The integrity of the academic process requires that credit be given where credit is due. Accordingly, it is a breach of academic integrity to present the ideas or works of another as one's own work, or to permit another to present one's work without customary and proper acknowledgment of authorship. Students may collaborate with other students only as expressly permitted by the instructor. Students are responsible for the honest completion and representation of their work, the appropriate citation of sources and the respect and recognition of others' academic endeavors. According to Montana State University Conduct Guidelines and Grievance Procedures for Students, academic misconduct includes cheating, plagiarism, forgery, falsification, facilitation or aiding academic dishonesty; multiple submission, theft of instructional materials or tests; unauthorized access to, manipulation of or tampering with laboratory equipment, experiments, computer programs, or animals without proper authorization; alteration of grades or files; misuse of research data in reporting results; use of personal relationships to gain grades or favors, or otherwise attempting to obtain grades or credit through fraudulent means.

In other words, you may:

- Work out homework problems by yourself
- Work with your teammates on programming assignments/projects
- Share ideas (not answers) with other people
- Help other people debug (not write) their programs

You may NOT:

- Share code with other people
- Submit code that you (or your partner) did not write
- Modify someone else's solution and claim it as your own
- Fabricate results

Consequences, depending on the severity of violation:

- Zero on the assignment
- An `F` for the course and loss of permission to drop
- Suspension or expulsion from the university

Academic misconduct will be reported to the Department Chair and the Dean of Students Office
