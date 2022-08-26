[![Build Status](https://shields.cosanostra-cloud.de/drone/build/alcapone1933/docker-ward?logo=drone&server=https%3A%2F%2Fdrone.docker-for-life.de)](https://drone.docker-for-life.de/alcapone1933/docker-ward)
[![Build Status Branch Master](https://shields.cosanostra-cloud.de/drone/build/alcapone1933/docker-ward/master?logo=drone&label=build%20%5Bbranch%20master%5D&server=https%3A%2F%2Fdrone.docker-for-life.de)](https://drone.docker-for-life.de/alcapone1933/docker-ward/branches)
[![Docker Pulls](https://shields.cosanostra-cloud.de/docker/pulls/alcapone1933/ward?logo=docker&logoColor=blue)](https://hub.docker.com/r/alcapone1933/ward/tags)
![Docker Image Version (latest semver)](https://shields.cosanostra-cloud.de/docker/v/alcapone1933/ward?sort=semver&logo=docker&logoColor=blue&label=dockerhub%20version)

<h3 align = "center">
    <img src = "images/logo.png" alt = "Logo" />
</h3>

---

### About

Ward is a simple and and minimalistic server monitoring tool. Ward supports adaptive design system. Also it supports dark theme.
It shows only principal information and can be used, if you want to see nice looking dashboard instead looking on bunch of numbers and graphs.
Ward works nice on all popular operating systems, because it uses [OSHI](https://github.com/oshi/oshi).

**All features tested on:** `Windows` `Linux`

<p align = "center">
    <img src = "images/preview.png" alt = "Preview Image" />
    <h7 align = "center">Preview Image</h7>
</p>

---

### Features

<table>
    <tr>
        <td width = "600.5">Processor name</td>
        <td rowspan = "5">
            <img src = "images/cpu.png" alt = "Card 1" align = "center" />
        </td>
    </tr>
    <tr>
        <td>Processor utilization percentage</td>
    </tr>
    <tr>
        <td>Processor cores count (Logical and physical ones)</td>
    </tr>
    <tr>
        <td>Current frequency of the processor</td>
    </tr>
    <tr>
        <td>Does the processor supports 64-bit instructions</td>
    </tr>
</table>

<br>

<table>
    <tr>
        <td width = "600.5">Type of operating system and it's version</td>
        <td rowspan = "5">
            <img src = "images/host.png" alt = "Card 2" align = "center" />
        </td>
    </tr>
    <tr>
        <td>RAM utilization percentage</td>
    </tr>
    <tr>
        <td>Amount of total installed RAM</td>
    </tr>
    <tr>
        <td>Generation of the installed RAM (If you have dmidecode)</td>
    </tr>
    <tr>
        <td>Current processes count</td>
    </tr>
</table>

<br>

<table>
    <tr>
        <td width = "600.5">Host0 storage name</td>
        <td rowspan = "5">
            <img src = "images/hdd.png" alt = "Card 3" align = "center" />
        </td>
    </tr>
    <tr>
        <td>Storage utilization percentage</td>
    </tr>
    <tr>
        <td>Total current storage installed (Including external drives)</td>
    </tr>
    <tr>
        <td>Installed disks count</td>
    </tr>
    <tr>
        <td>Total amount of virtual memory (Swap in Linux)</td>
    </tr>
</table>

<br>

<table>
    <tr>
        <td width = "916.5">
            <img src = "images/time-diagramm.png" alt = "Card 4" align = "center" />
        </td>
    </tr>
    <tr>
        <td>
            This block contain uptime and chart sections. Uptime represent time since last boot on Linux, and time between hard resets on Windows.
            Also it have paginator which can be useful to get author contacts.
            Chart section display last fifteen seconds of server utilization. (Proccesor, ram, storage)
            You can hide separated datasets by clicking on rectangles on the top right corner of chart section.
        </td>
    </tr>
</table>

---

### Installation
    Create your own jar

    1. Clone the project
    2. Import project in your IDE as Maven project
    3. mvn clean package
    4. jar will be in the target folder

<br>

    Run jar file

    1. Create you own jar as described above
    2. Execute jar on Windows or Linux with administrative rights
    3. Enter localhost:4000 and set up application

<br>

    Build for Docker or Pull 

    1. Clone the project
    2. git clone https://github.com/alcapone1933/Ward.git or docker pull ghcr.io/alcapone1933/ward:latest or docker pull alcapone1933/ward:latest
    3. docker build --tag ward . 
    4. docker run --rm -it --name ward -p 4000:4000 -p <application port>:<application port> --privileged ward
    5. Go to localhost:4000 in web browser, input the same application port
    6. If you get error after being redirected to application port try hitting refresh
