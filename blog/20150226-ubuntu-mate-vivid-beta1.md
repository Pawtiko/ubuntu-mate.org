<!--
.. title: Ubuntu MATE 15.04 Beta1
.. slug: ubuntu-mate-vivid-beta1
.. date: 2015-02-26 17:30:37 UTC
.. tags: Ubuntu,MATE,Vivid,beta
.. link:
.. description:
.. type: text
.. author: Martin Wimpress
-->

<div class="bs-component">
    <div class="jumbotron">
        <h1>Achievement Unlocked!</h1>
        <p>Ubuntu MATE 15.04 is now an official member of the Ubuntu family.</p>
        <p><img class="centered" src="/Ubuntu-MATE-Remix.png" alt="Ubuntu MATE" /></p>
    </div>
</div>

Yes, we finally made it! Ubuntu MATE 15.04 Beta1 is now available
for official download. This official release builds on Ubuntu MATE Alpha2,
introduces some new features and is officially official `:-D`

## What works?

People tell us that Ubuntu MATE is stable. You may, or may not, agree.

## What changed since the Ubuntu MATE 15.04 Alpha2 release?

Well, the big change is largely backend stuff as Ubuntu MATE has transitioned
from our unofficial iso build servers to the official Canonical build
infrastructure. From Ubuntu MATE 15.04 onward images are now built alongside the
other members of the Ubuntu family.

I'd like to say a big ***"Thank You"*** to the following Ubuntu developers who
have helped make this possible:

  * [Mathieu Trudel-Lapierre](https://launchpad.net/~mathieu-tl)
  * [Colin Watson](https://launchpad.net/~cjwatson)
  * [Iain Lane](https://launchpad.net/~laney)
  * [Adam Conrad](https://launchpad.net/~adconrad)
  * [Adam Stokes](https://launchpad.net/~adam-stokes)
  * [Didier Roche](https://launchpad.net/~didrocks)
  * [Martin Pitt](https://launchpad.net/~pitti)
  * [Daniel Holbach](https://launchpad.net/~dholbach)

It is also worth mentioning that the [Xubuntu](http://xubuntu.org/) team
have been ever so welcoming and great collaborators. Some new features
in Ubuntu MATE have come directly from Xubuntu development efforts. As always,
I can't thank [Mike Gabriel](https://alioth.debian.org/users/sunweaver/) and
[Vangelis Mouhtsis](https://alioth.debian.org/users/gnugr-guest/) enough for
their help working the MATE packages through Debian and fixing bugs. A
large percentage of the Ubuntu MATE development is actually taking place in
Debian.

Here what changed since Ubuntu MATE 15.04 Alpha2:

  * Added everything required to build Ubuntu MATE 15.04 to the official Ubuntu archive.
  * Added PowerPC as an officially supported architecture for Ubuntu MATE 15.04.
    * Running Linux on PowerPC can require some tinkering and the following are useful references.
    * [PowerPC Known Issues](https://wiki.ubuntu.com/PowerPCKnownIssues)
    * [PowerPC FAQ](https://wiki.ubuntu.com/PowerPCFAQ)
  * Added an interface layout switcher to MATE Tweak, see the video below.

<div align="center"><iframe width="480" height="360" src="https://www.youtube.com/embed/YI4IWO_SpiI&html5=1" frameborder="0" allowfullscreen></iframe></div>

  * Added [Plank](https://launchpad.net/plank).
    * Plank is not enabled by default, but can be activated via the *Eleven* layout in MATE Tweak.
  * Added [Folder Colors](http://foldercolor.tuxfamily.org/).
  * Added menu categories to *System -> Preferences*.
  * Added OEM Install.
    * This is as a result of achieving official status.
  * Updated [LightDM GTK Greeter](http://smdavis.us/projects/lightdm-gtk-greeter/) to 2.0.0 which now includes a MATE logo in the session switcher.
  * Updated [LightDM GTK Greeter Settings](https://launchpad.net/lightdm-gtk-greeter-settings) 1.10. Thanks to [Sean M. Davis](http://smdavis.us)
  * Updated Yuyo GTK theme to better support GTK 3.14. Thanks to [Sam Hewitt](http://snwh.org/).
  * [Fixed GTK+ 2.x]( https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=777142) so it better supports multi monitor under MATE. Thanks to [Vlad Orlov](https://github.com/monsta) (MATE Core Dev).
    * This was then merge upstream. Thanks [Wolfgang Ulbrich](https://github.com/NiceandGently) (MATE Core Dev)
    * This resulted in GTK 2.24.26 being released which is now included in Ubuntu 15.04.
  * Fixed uninstalling packages from the Ubuntu MATE meta packages.
    * This is as a result of achieving official status.
  * Fixed being an unofficial Ubuntu flavour.
    * This is as a result of achieving official status `;-)`
  * Merged [MATE Compatibility integration into upstream Compiz](https://code.launchpad.net/~ubuntu-mate-dev/compiz/compiz-mate/+merge/249578)
    * While Compiz is installed by default, it is not enabled by default.
    * MATE Tweak includes an option to switch between Marco and Compiz, no log out/in required.

<div class="bs-component">
    <div class="jumbotron">
        <h1>Ubuntu MATE 15.04 Download</h1>
        <p>Join the fun and experience a retrospective future.</p>
        <a href="/vivid/" class="btn btn-primary btn-lg">Download</a>
        </p>
    </div>
</div>

## Known Issues

It is not all good news however. Here are the known issues.

  * MATE 1.8x is not fully compatible with `glibc` >= 2.43.1 which now features
  in Ubuntu 15.04. The MATE team have been working on patches but they have not yet
  made there way into the official Ubuntu archive. Therefore the following
  PPA should be enabled to get the fixes. You *really* want to do this:

    sudo apt-add-repository ppa:ubuntu-mate-dev/vivid-mate
    sudo apt-get update
    sudo apt-get dist-upgrade

  * The "Notification Area" crashes on first start, and then at random intervals there after but only for the **i386** build.
    * [LP: #1425401](https://bugs.launchpad.net/ubuntu/+source/mate-panel/+bug/1425401)
    * When the `"Notification Area"` has quit unexpectedly` dialogue appears click **Reload**.
  * Live switching between Compiz and Marco is somewhat experimental and may result in
  no window decorations on some older GPUs.
  * Virtualbox guests may only get a resolution of 640x480
    * [LP: #1368784](https://bugs.launchpad.net/ubuntu/+source/virtualbox/+bug/1368784/), see [comment #13](https://bugs.launchpad.net/ubuntu/+source/virtualbox/+bug/1368784/comments/13) for a work around.
  * Running an Ubuntu MATE live session as a Virtualbox guest may corrupt the video
  output of the guest.
    * You can correct the video display by pressing `Host+F1` to switch
    VT in the guest and then press `Host+F7` to switch back which will
    correct the video output.
  * The .iso images are a little bigger than they need to be and include some unnecessary
  packages. This is due to the transition from unofficial to official builds and will be
  addressed for Beta 2 or the Release Candidate.
  * Some packages schedule for inclusion in Ubuntu MATE 15.04 have not yet made it into
  the official archive. Hopefully this can be addressed before Beta 2.

You'll also want to check the Ubuntu MATE bug tracker to see what has already
been reported. These issues will be addressed in due course.

  * [Ubuntu MATE Bug Tracker](https://bugs.launchpad.net/ubuntu-mate)

## Useful Information

You may find the following information useful, which is why we titled 
the section *Useful Information* since the information presented here
is mostly useful.

  * [Ubuntu MATE 15.04 Useful Information](https://ubuntu-mate.community/t/ubuntu-mate-14-10-and-15-04-useful-information/24)

## Feedback

Is there anything you can help with or want to be involved in? Maybe you just
want to discuss your experiences or ask the maintainers some questions. Please
[come and talk to us](https://ubuntu-mate.community/).
