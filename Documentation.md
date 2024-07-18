<h2>LINUX PHILOSOPHY AND CONCEPTS</h2>

![Picture1](https://github.com/user-attachments/assets/158b538f-c525-4ab5-9302-a8aa92e43b15)
<strong><p>Symbol of Linux</p></strong>

<p>Linux, heavily influenced by UNIX, leverages many of its concepts. It accesses features and services primarily through files and file-like objects, providing a multi-tasking, multi-user environment with integrated networking and daemon services.</p>

<p>Developed by a global collaboration of developers led by Linus Torvalds, Linux encourages participation based on technical skill and a desire to contribute. The Linux community includes a vast ecosystem of developers, vendors, and users who support and advance the operating system.</p>

<p>Key Linux terms include kernel, distribution, boot loader, service, filesystem, X Window system, desktop environment, and command line. A complete Linux distribution comprises the kernel and various software tools for file operations, user management, and software package management.</p>

<h2>LINUX BASICS AND SYSTEM STARTUP</h2>

<p>A partition is a logical segment of a disk, allowing data to be grouped and separated for better organization and protection. A filesystem, which is a method of storing and locating files on a hard disk, operates within these partitions. By partitioning a disk, any failure or mistake is contained within the affected partition, preserving data on other partitions.</p>

<p>The Linux boot process involves multiple steps: starting with BIOS, which triggers the boot loader to launch the Linux kernel. This leads to invoking the initramfs filesystem, which then triggers the init program to complete the startup process.</p>

<p>Selecting the appropriate Linux distribution requires aligning your system's specific needs with the capabilities of various distributions.</p>

![Picture2](https://github.com/user-attachments/assets/d0de47ea-f330-40da-9ccc-0e6a26b12397)

<strong><p>Linux Booting Process Flow Diagram</p></strong>

<h2>Graphical Desktop</h2>
<p>Linux can be used through either a Command Line Interface (CLI) or a Graphical User Interface (GUI).</p>
<ul>
    <li><strong>CLI:</strong> Requires knowledge of specific commands and programs. It's efficient for repetitive tasks and allows quick access to information about command usage and options.</li>
    <li><strong>GUI:</strong> Easier to navigate with graphical icons and screens, making it user-friendly for those who don't remember commands or perform tasks infrequently.</li>
</ul>
<p>We will focus on managing sessions using the GUI for three Linux distributions: Red Hat (CentOS, Fedora), SUSE (openSUSE), and Debian (Ubuntu, Mint). Since we're using the GNOME-based variant of openSUSE, the experience across these distributions will be similar. Note that if you use KDE or other desktops like XFCE, your experience may vary slightly.</p>

![Picture1](https://github.com/user-attachments/assets/b14f2e5e-565e-4399-88ab-f86cd8504359)
<strong><p>Linux is a Seamless Desktop Environment</p></strong>

<h3>X Window System</h3>
<p>Loading the graphical desktop is one of the final steps in the Linux boot process. Traditionally, this was managed by the X Windows System (X), which dates back to the mid-1980s.</p>
<ul>
    <li><strong>Display Manager:</strong> Manages displays, loads the X server (providing graphical services to applications), handles graphical logins, and starts the appropriate desktop environment after user login.</li>
</ul>
<p>X has limitations on modern systems, particularly with security. It is gradually being replaced by Wayland, a newer system that is now the default for Fedora, RHEL, and other recent distributions. Wayland looks similar to X for users but has significant differences under the hood.</p>

<p>A desktop environment consists of a session manager, which starts and maintains the components of the graphical session, and the window manager, which controls the placement and movement of windows, window title-bars, and controls.</p>
<p>Although these can be mixed, generally a set of utilities, session manager, and window manager are used together as a unit, and together provide a seamless desktop environment.</p>
<p>If the display manager is not started by default in the default runlevel, you can start the graphical desktop in a different way, after logging on to a text-mode console, by running <code>startx</code> from the command line. Or, you can start the display manager (gdm, kdm, xdm, etc.) manually from the command line. This differs from running <code>startx</code> as the display managers will project a sign-in screen. We discuss them next.</p>

<h3>GNOME Desktop Environment</h3>

![Picture2](https://github.com/user-attachments/assets/4511f533-c5ca-499e-b931-a47b0d4b5e23)
<strong><p>Linux Desktop Environment</p></strong>

<p>GNOME is a popular, user-friendly desktop environment and the default for many Linux distributions, including RHEL, Fedora, CentOS, SUSE, Ubuntu, and Debian. It features menu-based navigation, making it accessible for Windows users. However, its appearance can vary across distributions.</p>
<p>Another important desktop environment is KDE, commonly used with SUSE and openSUSE. Other options include Unity (used in older Ubuntu versions), XFCE, and LXDE. Most desktop environments are similar to GNOME, and we will primarily focus on GNOME to maintain simplicity.</p>
<p><strong>NOTE:</strong> To change the Desktop Background: Right-Click on Desktop Screen → Change Background</p>

<h3>gnome-tweaks</h3>
<p>Most common settings, both personal and system-wide, can be found by clicking on the gear or similar icon in the upper right corner of your Linux distribution. However, the default settings utility in GNOME-based distributions is limited, making it hard to customize your system.</p>
<p>To access more settings, use <code>gnome-tweaks</code>. This utility provides additional options and allows you to install third-party extensions. It may not be installed by default, but you can add it (previously known as <strong>gnome-tweak-tool</strong>). Launch it with <code>Alt-F2</code> and typing its name, and consider adding it to your Favorites.</p>
<p>Recent distributions have moved many features from <code>gnome-tweaks</code> to <code>gnome-extensions-app</code>.</p>

<h3>Locking the Screen</h3>
<p>Locking your screen is a good way to prevent unauthorized access while you're away from your computer. Note that this doesn't suspend the computer; all applications and processes continue running.</p>
<p>There are two ways to lock your screen:</p>
<ul>
    <li><strong>Graphical Interface:</strong> Click the upper-right corner of the desktop, then click the lock icon.</li>
    <li><strong>Keyboard Shortcut:</strong> Press <code>SUPER-L</code> (or <code>SUPER-Escape</code>). The SUPER key is also known as the Windows key. You can modify this shortcut in keyboard settings, which may vary by distribution.</li>
</ul>
<p>To unlock, simply enter your password. The screenshot below shows how to lock the screen on Ubuntu; details are similar across modern distributions.</p>

<h3>Shutting Down and Restarting on GNOME</h3>

![Picture3](https://github.com/user-attachments/assets/b7aea1b4-d0c2-4084-b80c-71f9ef8a49a3)
<strong><p>Linux GUI for Shutting Down the System</p></strong>

<p>To shut down the computer in any recent GNOME-based Linux distribution, perform the following steps:</p>
<ol>
    <li>Click either the Power or the Gear icon in the upper-right corner of the screen.</li>
    <li>Click on Power Off, Restart, or Cancel. If you do nothing, the system will shut down in 60 seconds.</li>
</ol>
<p>Shutdown, reboot, and logout operations will ask for confirmation before going ahead. This is because many applications will not save their data properly when terminated this way.</p>
<p>Always save your documents and data before restarting, shutting down, or logging out.</p>

<h3>Locating Applications</h3>
<p>Unlike other operating systems, a Linux installation typically comes with a wide range of applications and access to software archives with thousands of programs. Most key tasks have a default application already installed, but you can always install more.</p>
<p>For example, Firefox is often the default browser, while alternatives like Epiphany, Konqueror, and Chromium are available from software repositories. Proprietary browsers such as Opera and Chrome are also available.</p>
<p>Finding applications in GNOME and KDE is easy, as they are organized in functional submenus.</p>

<h3>File Manager</h3>
<p>Each distribution implements the Nautilus (File Manager) utility, which is used to navigate the file system. It can locate files and, when a file is clicked upon, either it will run if it is a program, or an associated application will be launched using the file as data. This behavior is completely familiar to anyone who has used other operating systems.</p>
<p>To start the file manager, you will have to click on its icon (a file cabinet), which is easily found, usually under Favorites or Accessories. It will have the name <strong>Files</strong>.</p>
<p>This will open a window with your Home directory displayed. The left panel of the File Manager window holds a list of commonly used directories, such as Desktop, Documents, Downloads, and Pictures.</p>
<p>You can click the magnifying glass icon on the top-right to search for files or directories (folders).</p>

<h3>Editing a File</h3>
<p>Editing any text file through the graphical interface is easy in the GNOME desktop environment. Simply double-click the file on the desktop or in the Nautilus file browser window to open the file with the default text editor.</p>
<p>The default text editor in GNOME is <code>gedit</code>. It is simple yet powerful, ideal for editing documents, making quick notes, and programming. Although gedit is designed as a general-purpose text editor, it offers additional features for spell-checking, highlighting, file listings, and statistics.</p>

🚀<b>Snapshots for Linux Systemctl commands, Linux GUI, File viewing, Boot process diagram, Locating Applications, Swicthing User, Shutting Down : <a link href="Snapshots/Linux Basic Boot Process and GUI operations with system and files">Click here</a></b>

<h2>System Settings</h2>
<p>The System Settings panel allows you to control most of the basic configuration options and desktop settings, such as specifying the screen resolution, managing network connections, or changing the date and time of the system.</p>
<p>For the GNOME Desktop Manager, one clicks on the upper right-hand corner and then selects the tools image (screwdriver crossed with a wrench or a gear). Depending on your distribution, you may find other ways to get into the settings configuration as well.</p>

![image](https://github.com/user-attachments/assets/993db969-e8f3-4b11-af02-2fbe50c10dd5)
<strong><p>System settings in Linux</p></strong>

<h3>gnome-tweaks</h3>
<p>A lot of personalized configuration settings do not appear on the settings menus. Instead, you have to launch a tool called either <em>gnome-tweaks</em> (or <em>gnome-tweak-tool</em> on older Linux distributions). We have not really discussed working at the command line yet, but you can always launch a program such as this by doing <em>Alt-F2</em> and typing in the command. Some distributions have a link to the tweaks menus in the settings, but for some mysterious reason, many obscure this tool's existence, and it becomes hard to discover how to modify even rather basic desktop attributes and behavior.</p>
<p>Important things you can do with this tool include selecting a theme, configuring extensions which you can get from your distribution or download from the Internet, control fonts, modify the keyboard layout, and set which programs start when you login.</p>
<p>The most recent GNOME versions have removed a lot of the functionality of <em>gnome-tweaks</em>; extensions now have to be configured using a new app called <em>gnome-extensions-app</em>.</p>

<h3>Display Settings</h3>
<p>Clicking on <em>Settings > Displays</em> (or <em>Settings > Devices > Displays</em>) will expose the most common settings for changing the desktop appearance. You can also bring this up by right-clicking anywhere on the desktop and selecting <em>Display Settings</em>. These settings function independently of the specific display drivers you are running. The exact appearance will depend enormously on how many monitors you have and other factors, such as Linux distribution and particular version.</p>
<p>If your system uses a proprietary video card driver (usually from nVidia or AMD), you will probably have a separate configuration program for that driver. This program may give more configuration options, but may also be more complicated, and might require sysadmin (root) access. If possible, you should configure the settings in the Displays panel rather than with the proprietary program.</p>
<p>On systems utilizing the X Window system, the server which actually provides the GUI, uses <em>/etc/X11/xorg.conf</em> as its configuration file if it exists; In modern Linux distributions, this file is usually present only in unusual circumstances, such as when certain less common graphic drivers are in use. Changing this configuration file directly is usually for more advanced users.</p>

![Screen Display Settings](https://github.com/user-attachments/assets/a90fe23f-3493-4f03-b6c3-ce041e783335)
<strong><p>System Display settings in Linux</p></strong>

<h3>Date and Time Settings</h3>
<p>By default, Linux always uses Coordinated Universal Time (UTC) for its own internal timekeeping. Displayed or stored time values rely on the system time zone setting to get the proper time. UTC is similar to, but more accurate than, Greenwich Mean Time (GMT).</p>
<p>If you click on the time displayed on the top panel, you can adjust the format with which the date and time is shown; on some distributions, you can also alter the values.</p>
<p>The more detailed date and time settings can be selected from the Date & Time window in the System Settings Menu.</p>

<h3>Network Time Protocol</h3>
<p>The Network Time Protocol (NTP) is the most popular and reliable protocol for setting the local time by consulting established Internet servers. Linux distributions always come with a working NTP setup, which refers to specific time servers run or relied on by the distribution. This means that no setup, beyond "on" or "off", is generally required for network time synchronization.</p>


![picture1](https://github.com/user-attachments/assets/b5bf66aa-f48e-4b02-a10f-ad68fc4907e2)
<strong><p>Sample Networking Diagram</p></strong>

<h3>Network Configuration</h3>
<p>All Linux distributions have network configuration files, but file formats and locations can differ from one distribution to another. Hand editing of these files can handle quite complicated setups, but is not very dynamic or easy to learn and use. <em>Network Manager</em> was developed to make things easier and more uniform across distributions. It can list all available networks (both wired and wireless), allow the choice of a wired, wireless, or mobile broadband network, handle passwords, and set up Virtual Private Networks (VPNs). Except for unusual situations, it is generally best to let Network Manager establish your connections and keep track of your settings.</p>
<p>Wireless networks are usually not connected by default. You can view the list of available wireless networks and see which one (if any) you are currently connected to by using Network Manager. You can then add, edit, or remove known wireless networks, and also specify which ones you want connected by default when present.</p>

![List of available networks](https://github.com/user-attachments/assets/b4bbfc63-549a-45f3-9bb9-e766f40e648c)
<strong><p>List of all available Wireless Connections</strong></p>

<p>To configure a wireless network in any recent GNOME-based distribution:</p>
<ol>
    <li>Click on the upper-right corner of the top panel, which brings up a settings and/or network window. While the exact appearance will depend on Linux distribution and version, it will always be possible to click on a <em>Wi-Fi</em> sub-menu, as long as the hardware is present. Here is an example from a RHEL 8 system:</li>
    <li>Select the wireless network you wish to connect to. If it is a secure network, the first time it will request that you enter the appropriate password. By default, the password will be saved for subsequent connections.</li>
</ol>
<p>If you click on <em>Wi-Fi Settings</em>, you will bring up the third screenshot. If you click on the Gear icon for any connection, you can configure it in more detail.</p>

![Confiiguring Connected Networks](https://github.com/user-attachments/assets/61a5a738-231b-4185-8ed5-011d2d683e09)
<p><strong>Configuring the Network of Your Choice</strong>p></strong>

<h3>Installing and Updating Software</h3>
<p>Each package in a Linux distribution provides one piece of the system, such as the Linux kernel, the C compiler, utilities for manipulating text or configuring the network, or for your favorite web browsers and email clients.</p>
<p>Packages often depend on each other. For example, because your email client can communicate using SSL/TLS, it will depend on a package that provides the ability to encrypt and decrypt SSL and TLS communication and will not install unless that package is also installed at the same time.</p>
<p>All systems have a lower-level utility that handles the details of unpacking a package and putting the pieces in the right places. However, most of the time, you will be working with a higher-level utility that knows how to download and install packages directly from the Internet and can manage dependencies and groups for you.</p>

<h3>Debian Packaging</h3>
<p>Let’s look at the package management for the Debian family system.</p>
<p><em>dpkg</em> is the underlying package manager for these systems. It can install, remove, and build packages. Unlike higher-level package management systems, it does not automatically download and install packages and satisfy their dependencies.</p>
<p>For Debian-based systems, the higher-level package management system is the Advanced Package Tool (APT) system of utilities. Generally, while each distribution within the Debian family uses APT, it creates its own user interface on top of it (for example, apt and apt-get, synaptic, gnome-software, Ubuntu Software Center, etc). Although apt repositories are generally compatible with each other, the software they contain generally is not. Therefore, most repositories target a particular distribution (like Ubuntu), and often software distributors ship with multiple repositories to support multiple distributions.</p>

![picture2](https://github.com/user-attachments/assets/2bcc9cac-3ba9-48d0-b4f1-9a8c1cd21080)
<strong><p>Debian Packaging Diagram</p></strong>

<h3>Package Management in the Debian Family System</h3>

<h3>Red Hat Package Manager (RPM)</h3>
<p>Red Hat Package Manager (RPM) is the other package management system popular on Linux distributions. It was developed by Red Hat and adopted by a number of other distributions, including Fedora, CentOS, SUSE/openSUSE, Oracle Linux, and others.</p>
<p>The higher-level package manager differs between distributions. Red Hat family distributions historically use RHEL/CentOS, and Fedora uses <em>dnf</em>, while SUSE family distributions such as openSUSE also use RPM but use the <em>zypper</em> interface.</p>

🚀<b>Snapshots for Linux System Settings, Display Settings, Date and Time, Wireless Network Configurations : <a link href="Snapshots/Linux Graphical System Interface">Click here</a></b>

<div>
    <h2>Network-Aware Applications</h2>
    <p><strong>FileZilla:</strong> An intuitive graphical FTP client that supports FTP, Secure File Transfer Protocol (SFTP), and FTP Secured (FTPS). It is used to transfer files to and from FTP servers.</p>
    <p><strong>Pidgin:</strong> A versatile messaging application that allows access to various messaging networks, including GTalk, AIM, ICQ, MSN, and IRC.</p>
    <p><strong>HexChat:</strong> A user-friendly application for accessing Internet Relay Chat (IRC) networks.</p>
</div>

![filezilla](https://github.com/user-attachments/assets/620a8843-6dcf-481e-ae40-9085acac1cec)
<strong><p>Filezilla</p></strong>

<div>
    <h2>Office Applications</h2>
    <p>Most day-to-day computer systems have productivity applications (sometimes called office suites) available or installed. Each suite is a collection of closely coupled programs used to create and edit different kinds of files:</p>
    <ul>
        <li>Text (articles, books, reports, etc.) → Using LibreOffice Writer</li>
        <li>Spreadsheets → Using LibreOffice Calc</li>
        <li>Presentations → Using LibreOffice Impress</li>
        <li>Graphical objects → Using LibreOffice Draw</li>
    </ul>
    <p>Most Linux distributions offer LibreOffice, an open source office suite that started in 2010 and has evolved from OpenOffice. In addition, Linux users have full access to Internet-based office suites such as Google Docs and Microsoft Office 365.</p>
</div>

![libreofficecomp](https://github.com/user-attachments/assets/4548a0e3-2873-4b0f-86fb-fb45c0d23ffe)
<strong><p>Libre Office Components</p></strong>

<div>
    <h2>Development Applications</h2>
    <p>Linux distributions come with a comprehensive set of applications and tools for developing and maintaining both user applications and the kernel. These tightly integrated tools include:</p>
    <ul>
        <li>Advanced Editors: Customized for programmers, such as vi and Emacs.</li>
        <li>Compilers: For various languages, including gcc and clang (C/C++) as well as newer languages like Golang and Rust.</li>
        <li>Debuggers: Tools like gdb, graphical front ends, and Valgrind.</li>
        <li>Performance Tools: Programs for measuring and monitoring performance, ranging from user-friendly interfaces to advanced tools for experienced engineers.</li>
        <li>Version Control Systems: Git (with interfaces like GitHub and GitLab) and older systems like Apache Subversion.</li>
        <li>Integrated Development Environments (IDEs): Complete setups like Eclipse and Visual Studio Code.</li>
    </ul>
    <p>Unlike other operating systems where these tools often need to be purchased and installed separately, on Linux they are available at no cost through standard package installation systems or direct downloads from maintainers.</p>
</div>

![eclipse](https://github.com/user-attachments/assets/4ed79f13-a485-443b-ae31-ed7eaeb608a7)
<strong><p>Eclipse IDE</p></strong>

<div>
    <h2>Sound Players</h2>
    <p><strong>Amarok:</strong> A mature MP3 player with a graphical interface that plays audio and video files, and streams online audio. It allows you to create playlists and uses a database to store information about your music collection.</p>
    <p><strong>Audacity:</strong> A simple interface application used to record and edit sounds.</p>
    <p><strong>Audacious:</strong> Another versatile audio media player.</p>
    <p><strong>Rhythmbox:</strong> Supports various digital music sources, including streaming Internet audio and podcasts. It offers a search function for audio in a library and supports smart playlists with an automatic update feature based on specified criteria.</p>
</div>

![amarok](https://github.com/user-attachments/assets/1424b276-1aaa-4abc-b0b1-af9ef5a7de77)
<strong><p>Amarok</p></strong>

<div>
    <h2>Movie Editors</h2>
    <p><strong>Blender:</strong> A professional tool for creating 3D animation and design, starting with modeling. It includes powerful tools for camera capture, recording, editing, enhancing, and creating video, each with a specific focus.</p>
    <p><strong>Cinelerra:</strong> Allows you to capture, compose, and edit audio and video.</p>
    <p><strong>FFmpeg:</strong> A versatile tool for recording, converting, and streaming audio and video. It serves as a format converter and includes additional tools like ffplay and ffserver.</p>
</div>

![blender](https://github.com/user-attachments/assets/d9e164b4-4a26-4c8e-a697-2eaff7865769)
<strong><p>Blender</p></strong>

<div>
    <h2>GIMP (GNU Image Manipulation Program)</h2>
    <p>Graphic editors allow you to create, edit, view, and organize images of various formats, like JPEG, PNG, GIF, and TIFF. The GNU Image Manipulation Program (GIMP) is a feature-rich image retouching and editing tool similar to Adobe Photoshop. Some features of GIMP include:</p>
    <ul>
        <li>It can handle any image file format.</li>
        <li>It has many special purpose plugins and filters.</li>
        <li>It provides extensive information about the image, such as layers, channels, and histograms.</li>
    </ul>
</div>

![gimpeditor](https://github.com/user-attachments/assets/e1c6796a-6bd0-40e8-a9be-f21542ba5155)
<strong><p>GIMP Editor</p></strong>

<div>
    <h2>Image and Document Editing Tools</h2>
    <p><strong>Eye of Gnome (eog):</strong> An image viewer with slide show capabilities and basic editing tools like rotate and resize. It allows easy navigation through images in a directory.</p>
    <p><strong>Inkscape:</strong> A feature-rich image editor that works with layers and transformations, often compared to Adobe Illustrator.</p>
    <p><strong>Convert:</strong> A command-line tool (part of the ImageMagick suite) for modifying image files. It offers file format conversion and numerous image modifications, such as blur, resize, and despeckle.</p>
    <p><strong>Scribus:</strong> A WYSIWYG document creation tool for publishing, providing numerous editing tools for professional document design.</p>
</div>

![inkspace](https://github.com/user-attachments/assets/d16cb698-e04b-4c32-98aa-85efb80b8d20)
<strong><p>Inkspace</p></strong>

🚀<b>Snapshots for Linux System Common Applications : <a link href="Snapshots/Common Applications">Click here</a></b>
