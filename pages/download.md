<!--
.. title: Download
.. slug: download
.. date: 2017-07-06 10:00:00 UTC
.. tags: Ubuntu,MATE,download
.. link:
.. description: Download a copy of Ubuntu MATE
.. type: text
.. author: Luke Horwell
-->

<link href="/assets/css/downloads.css" rel="stylesheet" type="text/css">

<noscript>
    <div class="alert alert-danger">
        <strong>Please enable JavaScript to use this page.</strong>
        <br/>
        Alternately, you can accquire downloads for the desktop version from the
        <a href="http://cdimage.ubuntu.com/ubuntu-mate/">CD Image Server</a>.
    </div>
</noscript>

<!----------------------------
 1. Architecture Selection
----------------------------->
<div id="arch-list">
    <h2>Choose your architecture</h2>
    <div class="row">
        <div class="col-xs-12 col-md-6">
            <button class="download-option arch-option" id="amd64" onclick="setArch('amd64', '64-bit')">
                <div class="icon">
                    <span class="fa fa-laptop"></span>
                </div>
                <div class="details">
                    <h3>64-bit</h3>
                    <p>
                        Ideal for computers with:
                        <ul>
                            <li>More than 3 GB of RAM.</li>
                            <li>64-bit capable Intel and AMD processors</li>
                            <li>UEFI PCs booting in CSM mode.</li>
                            <li>Modern Intel-based Apple Macs</li>
                        </ul>
                    </p>
                </div>
            </button>
        </div>

        <div class="col-xs-12 col-md-6">
            <button class="download-option arch-option" id="i386" onclick="setArch('i386', '32-bit')">
                <div class="icon">
                    <span class="fa fa-laptop"></span>
                </div>
                <div class="details">
                    <h3>32-bit</h3>
                    <p>
                        Ideal for computers with:
                        <ul>
                            <li>Less than 2 GB of RAM.</li>
                            <li>Intel and AMD processors.</li>
                            <li>Ageing PCs with low-RAM resources.</li>
                            <li>Older Intel-based Apple Macintosh systems.</li>
                        </ul>
                    </p>
                </div>
            </button>
        </div>
    </div>

    <div class="row">
        <div class="col-xs-12 col-md-6">
            <button class="download-option arch-option" id="powerpc" onclick="setArch('powerpc', 'PowerPC')">
                <div class="icon">
                    <span class="fa fa-desktop"></span>
                </div>
                <div class="details">
                    <h3>PowerPC</h3>
                    <p>
                        For hardware like:
                        <ul>
                            <li>Apple Macintosh G3, G4 and G5</li>
                            <li>Apple iBooks and PowerBooks</li>
                            <li>IBM OpenPower 7xx Machines</li>
                        </ul>
                    </p>
                </div>
            </button>
        </div>

        <div class="col-xs-12 col-md-6">
            <button class="download-option arch-option" id="armhf" onclick="setArch('armhf', 'Raspberry Pi')">
                <div class="icon">
                    <img src="/images/logos/raspberry-pi-download.png" />
                </div>
                <div class="details">
                    <h3>Raspberry Pi</h3>
                    <p>
                        For aarch32 (ARMv7) computers, like:
                        <ul>
                            <li>Raspberry Pi 2</li>
                            <li>Raspberry Pi 3</li>
                        </ul>
                    </p>
                </div>
            </button>
        </div>
    </div>
</div>


<!----------------------------
 2. Release Selection
----------------------------->
<div id="release-list" hidden>
    <h2>
        Which release would you like?
        <br/>
        <small>for a <span class="arch-choice"></span> system</small>
    </h2>

    <div class="row">
        <div class="col-xs-12 col-md-6">
            <button class="download-option release-option" id="xenial" onclick="setRelease('xenial')">
                <div class="icon">
                    <img src="/assets/img/downloads/releases/xenial.svg" />
                </div>
                <div class="details">
                    <h3>16.04.3 LTS "Xenial"</h3>
                    <p>Recommended for stability and mission critical systems.</p>
                    <div class="support-ends">Supported until April 2019</div>
                </div>
            </button>
        </div>
        <div class="col-xs-12 col-md-6">
            <button class="download-option release-option" id="zesty" onclick="setRelease('zesty')">
                <div class="icon">
                    <img src="/assets/img/downloads/releases/zesty.svg" />
                </div>
                <div class="details">
                    <h3>17.04 "Zesty"</h3>
                    <p>Interm release for users desiring the latest features and applications.</p>
                    <div class="support-ends">Supported until January 2018</div>
                </div>
            </button>
        </div>
    </div>
    <div class="row">
        <div class="col-xs-12 col-md-6">
            <button class="download-option release-option" id="artful" onclick="setRelease('artful')">
                <div class="icon">
                    <img src="/assets/img/downloads/releases/artful.svg" />
                </div>
                <div class="details">
                    <h3>17.10 "Artful"</h3>
                    <p>For early testers of the next release.</p>
                    <div class="support-preview">Beta 1</div>
                </div>
            </button>
        </div>
    </div>
    <div class="row">
        <h4><button class="btn btn-link" onclick="goBackToArch()">Choose a different architecture</button></h4>
    </div>
</div>


<!----------------------------
 3. Download Selection
----------------------------->
<div id="details-list" hidden>
    <div class="row">
        <div id="artwork-background" class="col-xs-12">
            <div class="logo hidden-xs">
                <img src="/assets/img/logos/ubuntu-mate.svg"/>
            </div>
            <div class="text">
                <div id="title">Ubuntu MATE <span id="selected-release"></span></div>
                <a id="release-notes" href="#" class="btn btn-primary btn-lg">Release Notes</a>
            </div>
        </div>
        <br/>
        <div class="col-xs-12" style="text-align:center;">
            <button class="btn btn-link" onclick="goBackToRelease()" style="padding:1em 0; display:block; margin:auto;">Choose a different release</button>
            <div id="pre-release-warning" class="alert alert-danger" style="text-align:left" hidden>
                <span class="fa fa-warning"></span>
                <strong>This is a development pre-release</strong>
                <br/>
                It is better suited for developers and testers who want to help with Ubuntu MATE QA, or to provide testing feedback and file bug reports.
            </div>
        </div>
    </div>
    <hr/>
    <div class="row">
        <div class="col-xs-3">
            <div class="text-center">
                <img src="/assets/img/downloads/torrent.png" alt="BitTorrent">
            </div>
        </div>
        <div class="col-xs-9">
            <h3>Download Links</h3>
            <p>If you can spare the bytes, a torrent is the recommended method to download Ubuntu&nbsp;MATE.</p>
            <a id="torrent-download" href="#" class="btn btn-primary"><span class="fa fa-download"></span> <var></var></a>
            <a id="magnet-download" href="#" class="btn btn-default"><span class="fa fa-magnet"></span> Magnet Link</a>
            <div class="help-tooltip" title="Magnet links directly open your BitTorrent client. For Raspberry Pi downloads, this excludes the web seeds, reducing the bandwidth costs.">
                <span class="fa fa-info-circle"></span>
            </div>
            <br/>
            <a id="direct-download" href="#" class="btn btn-default"><span class="fa fa-download"></span> <var></var></a>
            <br/>
            <table>
                <tr>
                    <th>Download Size</th>
                    <td id="download-size">1.7 GB</td>
                </tr>
                <tr>
                    <th>SHA256SUM Checksum</th>
                    <td><code id="sha256sum"></code></td>
                </tr>
            </table>
            <br/>
            <a href="/how-to-verify-downloads"><span class="fa fa-question-circle"></span> How to verify downloads</a>
        </div>
    </div>
    <hr/>
    <div class="row">
        <div class="col-xs-3">
            <div class="text-center">
                <img src="/assets/img/downloads/download-tips.png" alt="Piggy Bank"/>
            </div>
        </div>
        <div class="col-xs-9">
            <h3>Download Tip</h3>
            <p><strong>A little bit goes a long way.</strong>  If everyone who downloaded Ubuntu MATE donated $2.50
            it would fund the full-time development of Ubuntu MATE and MATE Desktop. <u>Please help both projects
            flourish by showing your support with a tip.</u></p>

            <!-- Tip $2.50 -->
            <form name="single" class="form-horizontal" action="https://www.paypal.com/cgi-bin/webscr" method="post">
                <fieldset>
                    <button type="submit" class="btn btn-primary">
                        Tip us <strong>$2.50</strong>
                    </button>
                </fieldset>
                <input type="hidden" name="cmd" value="_xclick">
                <input type="hidden" name="business" value="6282B4CZGVCB6">
                <input class="tip-name" type="hidden" name="item_name" value="Ubuntu MATE Tip">
                <input type="hidden" name="no_shipping" value="1">
                <input type="hidden" name="no_note" value="1">
                <input type="hidden" name="charset" value="UTF-8">
                <input type="hidden" name="amount" value="2.50">
                <input type="hidden" name="currency_code" value="USD">
                <input type="hidden" name="src" value="1">
                <input type="hidden" name="sra" value="1">
                <input type="hidden" name="return" value="https://ubuntu-mate.org/donation-completed/">
                <input type="hidden" name="cancel_return" value="https://ubuntu-mate.org/donation-cancelled/">
            </form>

            <!-- Tip $5 -->
            <form name="single" class="form-horizontal" action="https://www.paypal.com/cgi-bin/webscr" method="post">
                <fieldset>
                    <button type="submit" class="btn btn-primary">
                        Tip us <strong>$5</strong>
                    </button>
                </fieldset>
                <input type="hidden" name="cmd" value="_xclick">
                <input type="hidden" name="business" value="6282B4CZGVCB6">
                <input class="tip-name" type="hidden" name="item_name" value="Ubuntu MATE Tip">
                <input type="hidden" name="no_shipping" value="1">
                <input type="hidden" name="no_note" value="1">
                <input type="hidden" name="charset" value="UTF-8">
                <input type="hidden" name="amount" value="5">
                <input type="hidden" name="currency_code" value="USD">
                <input type="hidden" name="src" value="1">
                <input type="hidden" name="sra" value="1">
                <input type="hidden" name="return" value="https://ubuntu-mate.org/donation-completed/">
                <input type="hidden" name="cancel_return" value="https://ubuntu-mate.org/donation-cancelled/">
            </form>

            <!-- Tip $10 -->
            <form name="single" class="form-horizontal" action="https://www.paypal.com/cgi-bin/webscr" method="post">
                <fieldset>
                    <button type="submit" class="btn btn-primary">
                        Tip us <strong>$10</strong>
                    </button>
                </fieldset>
                <input type="hidden" name="cmd" value="_xclick">
                <input type="hidden" name="business" value="6282B4CZGVCB6">
                <input class="tip-name" type="hidden" name="item_name" value="Ubuntu MATE Tip">
                <input type="hidden" name="no_shipping" value="1">
                <input type="hidden" name="no_note" value="1">
                <input type="hidden" name="charset" value="UTF-8">
                <input type="hidden" name="amount" value="10">
                <input type="hidden" name="currency_code" value="USD">
                <input type="hidden" name="src" value="1">
                <input type="hidden" name="sra" value="1">
                <input type="hidden" name="return" value="https://ubuntu-mate.org/donation-completed/">
                <input type="hidden" name="cancel_return" value="https://ubuntu-mate.org/donation-cancelled/">
            </form>

            <!-- Tip $20 -->
            <form name="single" class="form-horizontal" action="https://www.paypal.com/cgi-bin/webscr" method="post">
                <fieldset>
                    <button type="submit" class="btn btn-primary">
                        Tip us <strong>$20</strong>
                    </button>
                </fieldset>
                <input type="hidden" name="cmd" value="_xclick">
                <input type="hidden" name="business" value="6282B4CZGVCB6">
                <input class="tip-name" type="hidden" name="item_name" value="Ubuntu MATE Tip">
                <input type="hidden" name="no_shipping" value="1">
                <input type="hidden" name="no_note" value="1">
                <input type="hidden" name="charset" value="UTF-8">
                <input type="hidden" name="amount" value="20">
                <input type="hidden" name="currency_code" value="USD">
                <input type="hidden" name="src" value="1">
                <input type="hidden" name="sra" value="1">
                <input type="hidden" name="return" value="https://ubuntu-mate.org/donation-completed/">
                <input type="hidden" name="cancel_return" value="https://ubuntu-mate.org/donation-cancelled/">
            </form>
            <br/>
            <h5>Powered by &nbsp;<img src="/assets/img/logos/pp-logo-100px.png" alt="Powered by PayPal" /></h5>
            <p>To donate more, donate with <strong>BitCoin</strong> or become an Ubuntu MATE <strong>Patron</strong>,
            <a href="/donate/">please visit the donate page</a>.</p>
        </div>
    </div>
    <hr/>
    <div id="sponsor1" class="row">
        <div class="col-xs-3">
            <div class="text-center">
                <br/><br/>
                <img src="/images/sponsors/osdisc.png" alt="OSDisc.com">
            </div>
        </div>
        <div class="col-xs-9">
            <h3>Purchase DVDs and USBs</h3>
            <h4><b>OSDisc.com</b></h4>
            <p>OSDisc.com is a leading source for Linux DVDs and USBs. Purchase ready-to-use bootable
            DVDs and memory sticks that come pre-installed with Ubuntu MATE and have persistent storage.</p>
            <a href="https://www.osdisc.com/products/ubuntumate?affiliate=ubuntumate" class="btn btn-primary">
                <span class="fa fa-shopping-cart"></span> Purchase
            </a>
        </div>
    </div>
    <br/>
    <div id="sponsor2" class="row">
        <div class="col-xs-3">
            <div class="text-center">
                <br/>
                <img src="/images/merch/hellotux/flash-drive.png" alt="HelloTux Flash Drive">
            </div>
        </div>
        <div class="col-xs-9">
            <h4><b>HELLOTUX</b></h4>
            <p>HELLOTUX sell an Ubuntu MATE branded 8GB Metallic Unibody USB stick that is just 41 mm
            long and less than 5 mm thick. It’s the perfect flash drive for your key ring, always
            with you. HELLOTUX will also help you to upgrade your flash drive to the next version
            of Ubuntu MATE, absolutely free.</p>
            <a href="https://www.hellotux.com/ubuntumate1510_flash_drive" class="btn btn-primary">
                <span class="fa fa-shopping-cart"></span> Purchase
            </a>
        </div>
    </div>
    <hr/>
    <div id="getting-started" class="row">
        <div class="row">
            <div class="col-xs-3">
            <div class="text-center">
                <br/>
                <img src="/assets/img/downloads/getting-started.png" alt="Getting Started">
            </div>
        </div>
        <div class="col-xs-9">
            <h3>Getting Started</h3>
            <p>The following resources may be useful to help get you up and running.</p>
            <ul>
                <li><a href="/how-to-create-bootable-usb-drive"><span class="fa fa-usb"></span> Creating a bootable USB on Windows, Mac and GNU/Linux</a></li>
                <li><a href="https://help.ubuntu.com/community/BurningIsoHowto"><span class="fa fa-dot-circle-o"></span> Burning a DVD on Windows, Mac and GNU/Linux</a></li>
                <li><a href="/about/#hardware_requirements"><span class="fa fa-laptop"></span> Check your System Requirements</a></li>
            </ul>
        </div>
    </div>
    <hr/>
    <div id="mirrors" class="row">
        <div class="col-xs-3">
            <div class="text-center">
                <br/>
                <img src="/assets/img/logos/i18n-small.png" alt="Mirrors and Other Options">
            </div>
        </div>
        <div class="col-xs-9">
            <h3>Mirrors and Other Options</h3>
            <p>You might prefer to find a DVD image on a mirror server that is geographically
            close to you in order to achieve a faster download.</p>
            <a target="_blank" rel="noopener" href="https://launchpad.net/ubuntu/+cdmirrors" class="btn btn-default">
                <span class="fa fa-globe"></span> Official Mirrors
            </a>
            <a id="other-downloads" href="#" target="_blank" rel="noopener" class="btn btn-default">
                <span class="fa fa-bookmark"></span> Other Downloads
            </a>
        </div>
    </div>
</div>

<script src="/assets/js/jquery-1.12.2.min.js"></script>
<script src="/assets/js/downloads.js"></script>

<script>
// http://netnix.org/2014/04/27/tracking-downloads-with-google-analytics/
window.onload = function() {
var a = document.getElementsByTagName('a');
for (i = 0; i < a.length; i++) {
if (a[i].href.match(/^https?:\/\/.+\.(bz2|deb|gz|iso|pdf|torrent|xz|zip)$/i)) {
a[i].setAttribute('target', '_blank');
a[i].onclick = function() {
ga('send', 'event', 'Downloads', 'Click', this.getAttribute('href'));
};
}
}
}
</script>
