# CSCI 466: Lab 1 - DNS

Complete the following assignment in your project groups. Submit your work into the Dropbox on D2L into the “Lab 1” folder. All group members will submit the same solution.

## Assignment

In this assignment you will learn to use Wireshark traffic monitor to gain a deeper understanding of DNS. Besides working with DNS, knowing how to use Wireshark is an essential skill in administration, network experimentation, and distributed system implementation.

The assignment is composed of two labs. The first lab introduces Wireshark; the second lab explores DNS.

### Part One

- [5 points] Find a partner.
Submit `partner.txt` with your partner’s first and last name. If you’re working by yourself, include the word “solo” in `partner.txt`.

### Part Two

- [5 points] Work through the “[Wireshark Lab: Getting Started](wireshark-files/Wireshark_Intro.pdf)” [:file_folder:](https://www.google.com/url?q=https://drive.google.com/file/d/1Uz6lqTxp4mdoLYcmM17ieqZD0ADVYuFW/view?usp%3Dsharing&sa=D&source=editors&ust=1632164402995000&usg=AOvVaw1vtVFYxl_wAiP5DEh5AmQc) lab and answer the following questions.
  - [1 point] ] List 3 different protocols that appear in the protocol column in the unfiltered packet-listing window in step 7.
  - [1 point] How long did it take from when the HTTP GET message was sent until the HTTP OK reply was received? (By default, the value of the Time column in the packet-listing window is the amount of time, in seconds, since Wireshark tracing began. To display the Time field in time-of-day format, select the Wireshark View pull down menu, then select Time Display Format, then select Time-of-day.)
  - [1 point] What is the Internet address of the gaia.cs.umass.edu (also known as www- net.cs.umass.edu)? What is the Internet address of your computer?
  - [1 point] Print the two HTTP messages (GET and OK) referred to in question 2 above. To do so, select Print from the Wireshark File command menu, and select the “Selected Packet Only” and “Print as displayed” radial buttons, and then click OK.

Submit your answers as `wireshark_intro.txt`.

### Part Three

- [20 points] Work through the “[Wireshark Lab: DNS](wireshark-files/Wireshark_DNS.pdf)” [:file_folder:](https://www.google.com/url?q=https://drive.google.com/file/d/12BMudLR3oX2qyNKOKr_pC5Jf2qqMTPzO/view?usp%3Dsharing&sa=D&source=editors&ust=1632174974460000&usg=AOvVaw15Zca0W5ezut1gkKzVhBHK) and answer questions 1-23, except 15, 19, and 23.

> **Note**: The lab asks you to use `bitsy.mit.edu`. That server is no longer available. Instead use Google’s DNS server at `8.8.8.8`, or any other [open DNS server](https://www.google.com/url?q=https://public-dns.info/&sa=D&source=editors&ust=1632174974461000&usg=AOvVaw0akDvm9L84dEIgS3pp6unB). You may also use an open DNS server to answer question 3 in the DNS lab.

> **Note**: The lab gives you an option to download zipped Wireshark traces. I want you to capture the traces yourselves, instead of downloading one, if possible. If you do run into problems running Wireshark you can get the wireshark traces [here](../../wireshark-traces). [:file_folder:](https://www.google.com/url?q=https://drive.google.com/file/d/1376xXffFs0B48SrxTc39kFPAZA2WJDrz/view?usp%3Dsharing&sa=D&source=editors&ust=1632174974461000&usg=AOvVaw1-UrVTB5pGhraQJh_bpoah)

Submit your answers as `wireshark_dns.txt`.

### Bonus

- [2 points] Speeding up DNS performance is an active research area. Find two conference publications from the last four years that describe how to speed up DNS lookups. Cite the papers and summarize their approaches in your own words.

Submit your answers as `bonus.txt`.
