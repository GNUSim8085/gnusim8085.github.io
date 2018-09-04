---
layout: default
title: Download
---
<script>
var xmlhttp = new XMLHttpRequest();
var release_binaries = "https://api.github.com/repos/GNUSim8085/GNUSim8085/releases/12172069/assets";

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
        if (arr[i].name.lastIndexOf("installer.exe") >= 0) {
            document.getElementById("wingtk32").parentNode.innerHTML += ' Downloads: ' + arr[i].download_count;
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
|[Debian/Ubuntu 32 bit (i386)](https://github.com/GNUSim8085/GNUSim8085/releases/download/1.4.1/gnusim8085_1.4.1-0.upstream1_i386.deb){:id="deb32"}|SHA256: 6ad56a8cf0cc450d47eacad1cadc2df21693a1812d461567d4f3169a43b99315, Compatible with Debian >= 8.0, Ubuntu >= 14.04|
|[Debian/Ubuntu 64 bit (amd64)](https://github.com/GNUSim8085/GNUSim8085/releases/download/1.4.1/gnusim8085_1.4.1-0.upstream1_amd64.deb){:id="deb64"}|SHA256: 1bfc8949312181a4ace612267d3c922fcb46228fc68343814138fa5273ed9786, Compatible with Debian >= 8.0, Ubuntu >= 14.04|
|[Windows 32 bit](https://github.com/GNUSim8085/GNUSim8085/releases/download/1.4.1/gnusim8085-1.4.1-installer.exe){:id="wingtk32"}|SHA256: dee03d81fd72e12bbc7e332640ff640000891359f936b5d38daa2d0f6dcb730e, Please uninstall any old versions before installing this.|
|[Arch Linux](https://aur.archlinux.org/packages/gnusim8085/){:target="_blank"}|Package avaialble from AUR. If it works well for you do not forget to vote for it.|
|[Source](https://github.com/GNUSim8085/GNUSim8085/releases/download/1.4.1/gnusim8085-1.4.1.tar.gz){:id="targz"}|SHA256: 4af0797afa90490a2d236c4bb2053e30676cd14a9c9a4b4e1eeba9c9808ea017, Compatible with Debian >= 8.0, Ubuntu >= 14.04|

