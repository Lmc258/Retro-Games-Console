# Retro-Games-Console


<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
        <li><a href="#adding-games-roms">Adding Games - ROMs</a></li>
      </ul>
    </li>
    <li><a href="#additional-consoles">Additional Consoles</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>

<!-- ABOUT THE PROJECT -->
## About The Project

![RaspberryPi-RetroPie][product-screenshot]

Retro gaming console. This console is run using RetroPie and is operating on a Raspberry Pi 5. This console has the ability to run variaty of game from  an array of different retro consoles, such as, PS1, Nintendo DS, Nintendo 64 or MAME. 

This project utilises existing tools such as the Retro Pi OS. The aim of this project description is to allow the reader to recreate the same console with a simple step by step guide.


<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- GETTING STARTED -->
## Getting Started

This is an example of how you may give instructions on setting up your project locally.
To get a local copy up and running follow these simple example steps.

### Prerequisites

#### Required

Before you get started you will need the following components.
* Raspberry pi 4 or higher (for this project I used a Raspberry Pi 5).
* MicroSD card (bigger the better).
* Power source
  * 5.1V 5A for pi 5
  * 5.1V 3A for pi 4
* Monitor or TV connected through MicroHDMI → HDMI
* Keyboard

#### Optional

* Raspberry Pi Case - Here is the one I used, <a href="https://www.aliexpress.com/item/1005006648075701.html?spm=a2g0o.order_list.order_list_main.57.72801802hiR6IR">GeeekPi Game 5Pi Case</a>. I picked this one as it fits the asthetic of a Retro Console.
* USB Controlers - This is up to you. I choose some which fit the Retro asthetic I was going for but I would recommend getting controllers with at least 15 buttons. An PlayStation/Xbox controller with triggers and bumbers will do the trick. As long as your controller connects via USB you should be fine.


### Installation

To begin your instalation of Retro Pi, you will first need to boot up your Pi with Raspberry Pi OS, and open the terminal. This will require you to have git installed. If you don't have git installed you can download git at [https://git-scm.com/downloads](https://git-scm.com/downloads) or type the following into terminal ```sh sudo apt install git lsb-release```.

1. Download the RetroPie-Setup script
   ```sh
   cd
   git clone --depth=1 <https://github.com/RetroPie/RetroPie-Setup.git>
   ```
2. Then execute the follow script to get into the RetroPie-Setup
   ```sh
   cd RetroPie-Setup
   chmod +x retropie_setup.sh
   sudo ./retropie_setup.sh
   ```

<p align="right">(<a href="#readme-top">back to top</a>)</p>



### Adding Games - ROMs 

By now you should have the RetroPie working. BUT, your missing something... you need games, otherwise what's the point? You will need to source your own game files or ROMs but I can tell you how to get them on to your RetroPie. 


#### Formating ROMS

Once you have your ROMs (games files) on your computer you need to format these files to how the RetroPi formats ROMs. Game files or ROMs will need to be stored in folders which match the console they have come from **make sure these folder names are correct**.

![ROM_Formatting_image]

To check the folder names are correct you can go to "FILE MANAGER" in "RETROPIE". From here go to "RetroPie", and "roms". This will show you how the RetroPie stores/formats ROMs. See image below.

![RetroPie-filemanager]


#### Adding ROMs to RetroPi

To transfer games to the Retro Pi you can use SCP (Secure Copy) to transfer over wifi. This wil require you to have set up the wifi on your Pi.
1. Right-click your “roms” folder and choose “copy as path”
2. Copy over your ROMs with the following command.
```sh
scp -r <roms folder path>\\* <username>@<pi ip address>:~/RetroPie/roms/
```

<p align="right">(<a href="#readme-top">back to top</a>)</p>




<!-- ADDITIONAL CONSOLES -->
## Additional consoles
Personally, I found that most of the nostalgic games I remember come from Nintendo DS or PlayStation. These consoles are not by default enabled/downloaded on the RetroPie system. Here are a list of steps you can follow to add these consoles to your Pi.

### Nintendo DS

### PlayStation 1

<p align="right">(<a href="#readme-top">back to top</a>)</p>




<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

I'd like to acknowledge the following resources. These are the real heros!

* [Retro Pie: A Raspberry Pi Gaming Machine](https://youtu.be/AaseHnf0k2o?si=gGENro9Kp6qdv0rq)
* [Best-README-Template](https://github.com/othneildrew/Best-README-Template)
* [RetroPie Website](https://retropie.org.uk/)


<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[product-screenshot]: raspberry-pi-4-retro-gaming-case.jpg
[ROM_Formatting_image]: Pi_roms_amiga_folder2-2051483879.png
[RetroPie-filemanager]: raspberry-pi-imager-retropie-file-manager-2-3729658751.jpg
