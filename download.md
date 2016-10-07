---
layout: default
title: Download
---
<script>
var xmlhttp = new XMLHttpRequest();
var release_binaries = "https://api.github.com/repos/GNUSim8085/GNUSim8085/releases/4220919/assets";

xmlhttp.onreadystatechange = function() {
    if (this.readyState == 4 && this.status == 200) {
        var assetArr = JSON.parse(this.responseText);
        parseAssets(assetArr);
    }
};

xmlhttp.open("GET", release_binaries, true);
xmlhttp.send();

function parseAssets(arr) {
    var i;
    for(i = 0; i < arr.length; i++) {
        if (arr[i].name.lastIndexOf("i386.deb") >= 0) {
            document.getElementById("deb32").parentNode.innerHTML += ' Downloads: ' + arr[i].download_count;
        }
        if (arr[i].name.lastIndexOf("amd64.deb") >= 0) {
            document.getElementById("deb64").parentNode.innerHTML += ' Downloads: ' + arr[i].download_count;
        }
        if (arr[i].name.lastIndexOf("powerpc.deb") >= 0) {
            document.getElementById("debpowerpc").parentNode.innerHTML += ' Downloads: ' + arr[i].download_count;
        }
        if (arr[i].name.lastIndexOf("with-gtk-installer.exe") >= 0) {
            document.getElementById("wingtk32").parentNode.innerHTML += ' Downloads: ' + arr[i].download_count;
        }
        if (arr[i].name.lastIndexOf("without-gtk-installer.exe") >= 0) {
            document.getElementById("winnogtk32").parentNode.innerHTML += ' Downloads: ' + arr[i].download_count;
        }
        if (arr[i].name.lastIndexOf("tar.gz") >= 0) {
            document.getElementById("targz").parentNode.innerHTML += ' Downloads: ' + arr[i].download_count;
        }
    }
}

</script>

# Downloads

GNUSim8085 is available in repository of most Linux distributions. If the latest version is not available then you can download source or binaries we provide. Please note that we do not provide binaries for all distributions.

|File|Notes|
|:--:|:---:|
|[Debian/Ubuntu 32 bit (i386)](https://github.com/GNUSim8085/GNUSim8085/releases/download/1.3.7/gnusim8085_1.3.7-1.hardy1_i386.deb){:id="deb32"}|MD5: 45180d7bc235f0a0affb6e3a0acb799c, Compatible with Debian >= 5.0, Ubuntu >= 8.04|
|[Debian/Ubuntu 64 bit (amd64)](https://github.com/GNUSim8085/GNUSim8085/releases/download/1.3.7/gnusim8085_1.3.7-1.hardy1_amd64.deb){:id="deb64"}|MD5: 05712fd939217ff06586c1a81c9ebe1f, Compatible with Debian >= 5.0, Ubuntu >= 8.04|
|[Debian/Ubuntu powerpc](https://github.com/GNUSim8085/GNUSim8085/releases/download/1.3.7/gnusim8085_1.3.7-1.hardy1_powerpc.deb){:id="debpowerpc"}|MD5: 663d118ba2cdcb7ac4a41a00b942ff00, Compatible with Debian >= 5.0, Ubuntu >= 8.04|
|[Windows 32 bit + GTK installer](https://github.com/GNUSim8085/GNUSim8085/releases/download/1.3.7/gnusim8085-1.3.7-with-gtk-installer.exe){:id="wingtk32"}|MD5: 4dc96458af974f04fed626efc0bd650c, GTK+ runtime 2.12 included. Choose this installer only if you don't already have GTK+ runtime >= 2.12 installed.|
|[Windows 32 bit](https://github.com/GNUSim8085/GNUSim8085/releases/download/1.3.7/gnusim8085-1.3.7-without-gtk-installer.exe){:id="winnogtk32"}|MD5: 9b6a3085f8e457a9e5b3964db4f5f4b1, GTK+ runtime >= 2.12 needs to be installed separately if not installed already. Download it from [here](http://gtk-win.sourceforge.net/home/index.php/en/Downloads).|
|[Source](https://github.com/GNUSim8085/GNUSim8085/releases/download/1.3.7/gnusim8085-1.3.7.tar.gz){:id="targz"}|MD5: 6baabf2d32685a3447a6c1382589ea84, Compatible with Debian >= 5.0, Ubuntu >= 8.04|

