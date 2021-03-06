---
title: Troubleshooting
---
<br />

<br />

# Troubleshooting

<br />

Over the past year, we've noticed a few errors (or noticed ourselves making user errors) when using POSM. Here's a quick list of these issues and how to solve them.

<br />

<br />

### First-time POSM install fails

Did you prepare the USB stick, plug it into POSM, and try to boot... only to get an error message? This can be an issue if your USB stick has an overall folder that contains everything that you extracted from the POSM `.iso` file. It can also be an issue if you extracted the files and then moved them manually onto the USB stick. There are hidden files in the package which will not follow if you try to manually move the contents. You can fix this by using an extraction tool (like The Unarchiver for Mac or 7-Zip for Windows) to extract the contents directly onto the USB stick.

### Re-installing the core POSM software

Let's say there's a new version of the POSM stack and you want to upgrade. You can do this by following the normal first-time install process: download software, prep USB stick, install onto POSM. The software will overwrite and previous versions.

### I'm connected to POSM. When I try to reach any website, it should redirect me to posm.io but it sometimes doesn't

Secure websites (ie websites whose URL starts with https:// instead of http://) will not redirect to the posm.io homepage. So, if you click any link in your bookmarks, it may not redirect to posm.io.

### Multiple deployments are buggy

POSM sometimes has a hard time dealing with multiple deployments - it may struggle when making MB tiles, or when first loading a deployment onto phones. We've solved this by just trying those processes again. It is also a good idea to keep the POSM "clean" by deleting old deployments that are no longer needed.

### How do I delete an old deployment?

To do this, you will need to use an FTP client like [Cyberduck](https://cyberduck.io/?l=en) (or command line) to connect (or "SSH") into POSM.

Power up the POSM and connect to it from your computer. Launch Cyberduck and start a new connection with the following parameters:
* Type: `SSH`
* Server: `posm.local`
* Username: `root`
* Password: (blank)

![](cyberduck.png)

The file structure looks like this: (needs completion + screenshot)

You can find a deployment...


### How do I access the file structure behind POSM?

To do this, you will need to use an FTP client like [Cyberduck](https://cyberduck.io/?l=en) (or command line) to connect (or "SSH") into POSM.

Power up the POSM and connect to it from your computer. Launch Cyberduck and start a new connection with the following parameters:
* Type: `SSH`
* Server: `posm.local`
* Username: `root`
* Password: (blank)

![](cyberduck.png)

The file structure looks like this: (needs completion + screenshot)


### Can I push OMK/ODK data to the server through a cell connection or actual internet?

Yes... but it's a little tricky. This would involve creating a parallel server in the cloud and then integrating this data back into the POSM server. If doing this is worth it (or just interesting) to you, then [here are the instructions](https://hackmd.io/EYFhA4DYDMFMEYC0BDEBmYiSXmx4BOAY0iwHZoAGAVnnFkrICYyg).

- Deleting a deployment (and when)
- MB tiles take forever
- Directory structure
- Why can't I connect to the wireless (bug)
- Can I connect to the internet through POSM? (bridge mode, Android tethering)
- Why can't I see anything in FieldPapers? (wrong centerpoint; clear cookies). Why does everything look different
- How do I add downloads
- How do I change the password on POSM? (wifi, SSH)
