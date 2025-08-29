# OHSINT - TRYHACKME_CHALLENGE
A short solution and walk through on the Ohsint challenge room on tryhackme.com an engaging problem that helps showcase the use of Exiftool(an osint tool) to solve this problem

# What is Osint
Open-Source Intelligence (OSINT) is the process of collecting publicly available data from sources like social media, websites, and documents to assess security risks. In cybersecurity, OSINT is crucial for uncovering vulnerabilities, tracking threats, and performing reconnaissance without engaging in illegal activities.

# What is this challenge about
an image (windows xp wallpaper) is given to you to find information and give the correct answers to the questions asked(challenge)
link to the challenge: https://tryhackme.com/room/ohsint ![taskfile](ohsint.jpg)
image link: https://tryhackme.com/room/ohsint?taskNo=1

# Questions given to be answered
1: What is this user's avatar of?\
2: What is the SSID of the WAP he connected to?\
3: What is his personal email address?\
4: What site did you find his email address on?\
5: Where has he gone on holiday?\
6: What is the person's password?\

# Solutions and walkthrough
for each questions i'll be giving answers with graphical examples of how i go to the answers

# Attacking the problem
first of all i obtained the task file: ![taskfile](1.png)(https://github.com/LuckyboyJay/OSINT/blob/339a6b28a5680f4ec8dba3f422bd1deb2eb10e8b/ohsint.jpg)\
if you tap the above link you will see that the image is a wallpaper from the windows XP with not much to see. but the information needed to solve
the problem is hidden within this seemingly empty image file.\
Now you might want to ask; what exactly are we looking for? by perusing the metadata of this image file, we will find the needed infomation to get what we're looking for\
Another question would be; How do we get this metadata? in OSINT we have different tools for metadata extraction. tools like: Exiftool, Geosetter, PhotoDNA etc. for this challenge, we'll be
using the Exiftool (that has already been preinstalled in my kali linux terminal).\
By using exiftool we will get the metadata; https://github.com/LuckyboyJay/OSINT/blob/503ca3384841f27b969d385776c0f3c2ca0cd7ef/1.png \
The information gotten from the metadata will be helpfull in solving this challenge

# Question 1: What is this user's avatar of?
from the information gotten from the metadata, we know this image file is copyrighted to the name " Owoodflint ", a simple google search of the name would bring another list of information that would
be helpfull in answering this question and the rest that follows.\
searching the name brings out a list of information that includes; the owners X handle, wordpress page and github account. https://github.com/LuckyboyJay/OSINT/blob/840550dd8544bb750bc2b90d9fe4b766daf328d5/2.png \
Checking his X(formerly twitter) would automatically show us his profile picture. https://github.com/LuckyboyJay/OSINT/blob/50081a3fcc034c67bbda80970ddd1412b827bb04/3.png this shows his profile in detail, which consist of his profile picture, bio and some few tweet he made \
This way we've answered the first question. CAT

# Question 2: What is the SSID of the WAP he connected to?
To answer this question we need to know what SSID means. SSID (Service Set Identifier)is simply the name given to a Wi-Fi network, it is a label that tells you which Wi-Fi/network you're connecting to.\
from the information gotten from the metadata, there's no mention of an SSID, neither is it writeen on his  X page, github or wordpress page. but we do find a BSSID (Basic Service Set Identifier), while an SSID is
a Wi-Fi's name, BSSID is a Wi-Fi's router ID\
You can use BSSID to get a routers SSID and with the help of WIGLE.net (Users around the world use WiGLE to scan Wi-Fi networks and even cell towers logging details like network names (SSIDs), unique identifiers (BSSIDs), GPS location, and encryption status. All this gets uploaded into the WiGLE database)\
https://github.com/LuckyboyJay/OSINT/blob/1a1aad8e7990ccabfb78fb4ec3016e94b863788c/6.png \
https://github.com/LuckyboyJay/OSINT/blob/1a1aad8e7990ccabfb78fb4ec3016e94b863788c/7.png \
With the help of WIGLE, the SSID is gotten to UnileverWIFI

# Question 3: What is his personal email address?
as aforestated, the information gotten from the metadata does'nt include obvious answeres for our challenge. we use information from the metadata to find answeres to our question. Now, to tackle this, we need to go through what we got from
searching his copyright name " Owoodflint " on  google. Going through his github, in one of his repository, a readme.md file is attached that has his email amd other information clearly stated there for our convenience.\
his email Owoodflint@gmail.com\
https://github.com/LuckyboyJay/OSINT/blob/2e8f6fb0087b0fdc3dab8ab2116892cc1034180a/8.png\

# Question 4: What site did you find his email address on?
The email address was found on Github

# Question 5: Where has he gone on holiday?
From the information gotten from his Github and also with the help of WIGLE.net we know he esides in London, but there was no mention of where he went on holiday on these sites, also going through his X profile
has proved futile. the only page/site we've yet to check out is his Wordpress blog. investigating his wordpress blog indicates that he is currently in the state of NewYork for his vacation\
https://github.com/LuckyboyJay/OSINT/blob/328b5b879ea3a9e8b58e4612412984dfa91f80e2/9.png

# Question 6: What is the person's password?
in all our ivestigations, this would seem to be the most difivult, because people usually do not leave their passwords out in the open, because it would put them at rist of their personal information to be stollen, but with the help of osint,
we'll try our best to get this right too. going through his public pages on X, github and wordpress did'nt seeem to bring out anything, but from experience, it is always advisable to check out the source code for all web pages when running an investigation just like this. futher inspection on the source code of the wordpress site shows that his password was hidden in a line of code.\
https://github.com/LuckyboyJay/OSINT/blob/735cb3f06e08f4c34a8f3949f3d30015f90667d4/10.png\
this shows that the password was hidden in plainsight and highlighting the web page would have also shown us the password\
https://github.com/LuckyboyJay/OSINT/blob/33664eef8dac94b54f8e3275dac0f18b46e7f853/11.png


























