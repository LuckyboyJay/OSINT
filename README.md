# OHSINT - TRYHACKME_CHALLENGE
A short solution and walk through on the Ohsint challenge room on tryhackme.com an engaging problem that helps showcase the use of Exiftool(an osint tool) to solve this problem

# What is Osint
Open-Source Intelligence (OSINT) is the process of collecting publicly available data from sources like social media, websites, and documents to assess security risks. In cybersecurity, OSINT is crucial for uncovering vulnerabilities, tracking threats, and performing reconnaissance without engaging in illegal activities.

# Whai is this challenge about
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
Now you might waht to ask; what exactly are we looking for? by perusing the metadata of this image file, we will find the needed infomation to get what we're looking for\
Another question would be; How do we get this metadata? in OSINT we have tools for metadata extraction. tools like: Exiftool, Geosetter, PhotoDNA etc. for this challenge, we'll be
using the Exiftool (hat has already been preinstalled in my kali linux terminal)
