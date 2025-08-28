# OHSINT - TRYHACKME_CHALLENGE
A short solution and walk through on the Ohsint challenge room on tryhackme.com an engaging problem that helps showcase the use of Exiftool(an osint tool) to solve this problem

# What is Osint
Open-Source Intelligence (OSINT) is the process of collecting publicly available data from sources like social media, websites, and documents to assess security risks. In cybersecurity, OSINT is crucial for uncovering vulnerabilities, tracking threats, and performing reconnaissance without engaging in illegal activities.

# What is this challenge about
an image (windows xp wallpaper) is given to you to find information and give the correct answers to the questions asked(challenge)
link to the challenge: https://tryhackme.com/room/ohsint
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
first of all i obtained the task file: https://github.com/LuckyboyJay/OSINT/blob/339a6b28a5680f4ec8dba3f422bd1deb2eb10e8b/ohsint.jpg \
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
Checking his X(formerly twitter) would automatically show us his profile picture. https://github.com/LuckyboyJay/OSINT/blob/50081a3fcc034c67bbda80970ddd1412b827bb04/3.png this shows his profile in detail, which
consist of his profile picture, bio and some few tweet he made \
This qay we've answered the first question. Ans CAT

# Question 2: What is the SSID of the WAP he connected to?
