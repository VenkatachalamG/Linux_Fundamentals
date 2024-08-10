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

<h2>The Command Line</h2>

![Command Line Terminal](https://github.com/user-attachments/assets/4ced0c8f-ab7c-4c92-8d1b-2ac87707dead)
<strong><p>Command Line </p></strong>
<p>Most input lines entered at the shell prompt have three basic elements:</p>
<ul>
    <li>Command</li>
    <li>Options</li>
    <li>Arguments</li>
</ul>
<p>The command is the name of the program or script you are executing. It may be followed by one or more options (or switches) that modify what the command may do. Options usually start with one or two dashes, for example, <code>-p</code> or <code>--print</code>, in order to differentiate them from arguments, which represent what the command operates on.</p>
<p>However, plenty of commands have no options, no arguments, or neither. In addition, other elements (such as setting environment variables) can also appear on the command line when launching a task.</p>

<h3>sudo</h3>
<p>All the demonstrations created have a user configured with <code>sudo</code> capabilities to provide the user with administrative (admin) privileges when required. <code>sudo</code> allows users to run programs using the security privileges of another user, generally root (superuser).</p>
<p>On your own systems, you may need to set up and enable <code>sudo</code> to work correctly. To do this, you need to follow some steps that we will discuss but not explain in much detail right now. Many distributions, including Ubuntu, configure <code>sudo</code> for you during installation. On other Linux distributions, you will need to configure <code>sudo</code> to work properly after the initial installation.</p>

<h4>NOTE: Steps for Setting Up and Running <code>sudo</code></h4>
<ol>
    <li>
        <p>You will need to make modifications as the administrative, or superuser, root. While <code>sudo</code> will become the preferred method of doing this, we do not have it set up yet, so we will need to use <code>su</code> instead. At the command line prompt, type <code>su</code> and press <code>Enter</code>. You will then be prompted for the root password, so enter it and press <code>Enter</code>. You will notice that nothing is printed; this is so others cannot see the password on the screen. You should end up with a different looking prompt, often ending with ‘#’. For example:</p>
        <pre>$ su<br>Password:<br>#</pre>
    </li>
    <li>
        <p>Now, you need to create a configuration file to enable your user account to use <code>sudo</code>. Typically, this file is created in the <code>/etc/sudoers.d/</code> directory with the name of the file the same as your username. For example, for this demo, let’s say your username is <code>student</code>. After doing step 1, you would then create the configuration file for <code>student</code> by doing this:</p>
        <pre># echo "student ALL=(ALL) ALL" > /etc/sudoers.d/student</pre>
    </li>
    <li>
        <p>Finally, some Linux distributions will complain if you do not also change permissions on the file by doing:</p>
        <pre># chmod 440 /etc/sudoers.d/student</pre>
    </li>
</ol>
<p>That should be it. For the rest of this course, if you use <code>sudo</code> you should be properly set up. When using <code>sudo</code>, by default you will be prompted to give a password (your own user password) at least the first time you do it within a specified time interval.</p>

<h3>Turning Off the Graphical Desktop</h3>
<p>Linux distributions can start and stop the graphical desktop in various ways. The exact method differs among distributions and between versions. For the newer system-based distributions, the display manager is run as a service, and you can stop the GUI desktop with the <code>systemctl</code> utility. In addition, most distributions will also work with the <code>telinit</code> command, as in:</p>
<pre>$ sudo systemctl stop gdm (or sudo telinit 3)</pre>
<p>and restart it (after logging into the console) with:</p>
<pre>$ sudo systemctl start gdm (or sudo telinit 5)</pre>

<h3>Logging In and Out</h3>
<p>An available text terminal will prompt for a username (with the string <code>login:</code>) and password. When typing your password, nothing is displayed on the terminal (not even a <code>*</code> to indicate that you typed in something), to prevent others from seeing your password. After you have logged into the system, you can perform basic operations.</p>
<p>Once your session is started (either by logging into a text terminal or via a graphical terminal program), you can also connect and log into remote systems by using Secure SHell (SSH). For example, by typing <code>ssh student@remote-server.com</code>, SSH would connect securely to the remote machine (<code>remote-server.com</code>) and give <code>student</code> a command line terminal window, using either a password (as with regular logins) or cryptographic key to sign in without providing a password to verify the identity.</p>

![loginout](https://github.com/user-attachments/assets/94bffffb-c531-4cf2-b9d6-405794523677)
<strong><p>Logging in and out</p></strong>

<h3>Rebooting and Shutting Down</h3>
<p>The preferred method to shut down or reboot the system is to use the <code>shutdown</code> command. This sends a warning message, and then prevents further users from logging in. The <code>init</code> process will then control shutting down or rebooting the system. It is important to always shut down properly; failure to do so can result in damage to the system and/or loss of data.</p>
<p>The <code>halt</code> and <code>poweroff</code> commands issue <code>shutdown -h</code> to halt the system; <code>reboot</code> issues <code>shutdown -r</code> and causes the machine to reboot instead of just shutting down. Both rebooting and shutting down from the command line requires superuser (root) access.</p>
<p>When administering a multi-user system, you have the option of notifying all users prior to shutdown, as in:</p>

<h3>Locating Applications</h3>
<p>Depending on the specifics of your particular distribution's policy, programs and software packages can be installed in various directories. In general, executable programs and scripts should live in the <code>/bin</code>, <code>/usr/bin</code>, <code>/sbin</code>, <code>/usr/sbin</code> directories, or somewhere under <code>/opt</code>. They can also appear in <code>/usr/local/bin</code> and <code>/usr/local/sbin</code>, or in a directory in a user's account space, such as <code>/home/student/bin</code>.</p>
<p>One way to locate programs is to employ the <code>which</code> utility. For example, to find out exactly where the <code>diff</code> program resides on the filesystem:</p>

<h3>Accessing Directories</h3>
<p>When you first log into a system or open a terminal, the default directory should be your home directory. You can see the exact location by typing <code>echo $HOME</code>. However, most Linux distributions open new graphical terminals in <code>$HOME/Desktop</code> instead.</p>

<h4>Table: Commands useful for directory navigation</h4>
<table>
    <tr>
        <th>COMMAND</th>
        <th>RESULT</th>
    </tr>
    <tr>
        <td><code>pwd</code></td>
        <td>Displays the present working directory</td>
    </tr>
    <tr>
        <td><code>cd ~</code> or <code>cd</code></td>
        <td>Change to your home directory; shortcut name is <code>~</code> (tilde)</td>
    </tr>
    <tr>
        <td><code>cd ..</code></td>
        <td>Change to parent directory (<code>..</code>)</td>
    </tr>
    <tr>
        <td><code>cd -</code></td>
        <td>Change to previous working directory; <code>-</code> (minus)</td>
    </tr>
</table>

<h3>Understanding Absolute and Relative Paths</h3>
<h4>Absolute pathname</h4>
<p>An absolute pathname begins with the root directory (<code>/</code>) and follows the tree, branch by branch, until it reaches the desired directory or file. Absolute paths always start with <code>/</code>.</p>

![absrelpath](https://github.com/user-attachments/assets/372fcc04-078f-4aad-b1ff-5c5505b769b4)
<strong><p>Absolute and Relative Paths</p></strong>

<h4>Relative pathname</h4>
<p>A relative pathname starts from the present working directory. Relative paths never start with <code>/</code>.</p>
<p>Multiple slashes (<code>/</code>) between directories and files are allowed, but all but one slash between elements in the pathname is ignored by the system. While <code>////usr//bin</code> is valid, it is seen as just <code>/usr/bin</code> by the system.</p>
<p>Most of the time, it is most convenient to use relative paths, which require less typing. Usually, you take advantage of the shortcuts

 <code>.</code> (current directory) and <code>..</code> (parent directory) when specifying relative paths. However, in shell scripts and programs, it is wise to use absolute paths to avoid unexpected results.</p>

<h3>Copying Files and Directories</h3>
<p>To copy a file or directory, the <code>cp</code> command is used. This command takes at least two arguments: the name of the source file or directory, and the name of the destination file or directory.</p>
<p>To create a backup copy of <code>file1</code>, you could run:</p>
<pre>$ cp file1 file1.bak</pre>
<p>To copy <code>file1</code> to <code>/tmp</code> you could run:</p>
<pre>$ cp file1 /tmp</pre>
<p>To copy multiple files to another directory, the destination must be a directory:</p>
<pre>$ cp file1 file2 file3 directory/</pre>
<p>When copying directories, you must specify the <code>-r</code> (recursive) option:</p>
<pre>$ cp -r dir1 dir2</pre>

<h3>Moving and Renaming Files</h3>
<p>To move files or directories, or to rename them, the <code>mv</code> command is used. This command takes at least two arguments: the name of the source file or directory, and the name of the destination file or directory.</p>
<p>To rename <code>file1</code> to <code>file2</code>:</p>
<pre>$ mv file1 file2</pre>
<p>To move <code>file1</code> to <code>/tmp</code>:</p>
<pre>$ mv file1 /tmp</pre>
<p>To move multiple files to another directory:</p>
<pre>$ mv file1 file2 file3 directory/</pre>
<p>To rename a directory:</p>
<pre>$ mv dir1 dir2</pre>

<h3>Removing Files and Directories</h3>
<p>To remove a file, the <code>rm</code> command is used. This command takes at least one argument: the name of the file to remove. To remove multiple files, simply specify all the filenames as arguments:</p>
<pre>$ rm file1 file2 file3</pre>
<p>To remove a directory, the <code>rmdir</code> command is used. This command takes at least one argument: the name of the directory to remove. However, <code>rmdir</code> can only be used to remove empty directories. To remove a non-empty directory, you must use the <code>rm</code> command with the <code>-r</code> option:</p>
<pre>$ rm -r dir1</pre>

<h3>Creating Files and Directories</h3>
<p>To create a file, the <code>touch</code> command is used. This command takes at least one argument: the name of the file to create. To create multiple files, simply specify all the filenames as arguments:</p>
<pre>$ touch file1 file2 file3</pre>
<p>To create a directory, the <code>mkdir</code> command is used. This command takes at least one argument: the name of the directory to create. To create multiple directories, simply specify all the directory names as arguments:</p>
<pre>$ mkdir dir1 dir2 dir3</pre>

<h3>Viewing Files</h3>
<p>To view the contents of a file, the <code>cat</code> command is used. This command takes at least one argument: the name of the file to view. To view multiple files, simply specify all the filenames as arguments:</p>
<pre>$ cat file1 file2 file3</pre>
<p>To view the contents of a file one page at a time, the <code>less</code> command is used. This command takes at least one argument: the name of the file to view. To view multiple files, simply specify all the filenames as arguments:</p>
<pre>$ less file1 file2 file3</pre>

<h3>Editing Files</h3>
<p>To edit a file, the <code>nano</code> command is used. This command takes at least one argument: the name of the file to edit. To edit multiple files, simply specify all the filenames as arguments:</p>
<pre>$ nano file1 file2 file3</pre>
<p>To edit a file with the <code>vim</code> command, you can use:</p>
<pre>$ vim file1</pre>

<h2>File Management</h2>

<h3>Hard Links</h3>
<p>The <code>ln</code> utility is used to create hard links and (with the <code>-s</code> option) soft links, also known as symbolic links or symlinks. These two kinds of links are very useful in UNIX-based operating systems.</p>
<p>Suppose that <code>file1</code> already exists. A hard link, called <code>file2</code>, is created with the command:</p>
<pre>$ ln file1 file2</pre>
<p>Note that two files now appear to exist. However, a closer inspection of the file listing shows that this is not quite true.</p>
<pre>$ ls -li file1 file2</pre>
<p>The <code>-i</code> option to <code>ls</code> prints out in the first column the inode number, which is a unique quantity for each file object. This field is the same for both of these files; what is really going on here is that it is only one file, but it has more than one name associated with it, as is indicated by the 2 that appears in the <code>ls</code> output. Thus, there was already another object linked to <code>file1</code> before the command was executed.</p>


![hardlinks](https://github.com/user-attachments/assets/db6302e6-bbba-41aa-a9c4-def6757af418)
<strong><p>Hard links</p></strong>

<h3>Soft (Symbolic) Links</h3>
<p>Soft (or Symbolic) links are created with the <code>-s</code> option, as in:</p>
<pre>$ ln -s file1 file3</pre>
<p>Symbolic links take no extra space on the filesystem (unless their names are very long). They are extremely convenient, as they can easily be modified to point to different places. Unlike hard links, soft links can point to objects even on different filesystems, partitions, and/or disks and other media, which may or may not be currently available or even exist. In the case where the link does not point to a currently available or existing object, you obtain a dangling link.</p>

<h3>Navigating Through Directory History</h3>
<p>The <code>cd</code> command remembers where you were last and lets you get back there with <code>cd -</code>. For remembering more than just the last directory visited, use <code>pushd</code> to change the directory instead of <code>cd</code>; this pushes your starting directory onto a list. Using <code>popd</code> will then send you back to those directories, walking in reverse order (the most recent directory will be the first one retrieved with <code>popd</code>). The list of directories is displayed with the <code>dirs</code> command.</p>

<h3>Creating and Modifying Files with touch</h3>
<p>The <code>touch</code> command is often used to set or update the access, change, and modify times of files. By default, it resets a file's timestamp to match the current time. However, you can also create an empty file using <code>touch</code>:</p>
<pre>$ touch filename</pre>
<p>This is normally done to create an empty file as a placeholder for a later purpose. The <code>-t</code> option allows you to set the date and timestamp of the file to a specific value:</p>
<pre>$ touch -t 12091600 myfile</pre>
<p>This sets the <code>myfile</code> file's timestamp to 4 p.m., December 9th (12 09 1600).</p>

<h3>Creating and Removing Directories</h3>
<p>The <code>mkdir</code> command is used to create a directory:</p>
<pre>$ mkdir sampdir</pre>
<p>It creates a sample directory named <code>sampdir</code> under the current directory.</p>
<pre>$ mkdir /usr/sampdir</pre>
<p>It creates a sample directory called <code>sampdir</code> under <code>/usr</code>.</p>
<p>Removing a directory is done with <code>rmdir</code>. The directory must be empty or the command will fail. To remove a directory and all of its contents you have to use <code>rm -rf</code>.</p>

<h3>Standard File Streams</h3>
<p>When commands are executed, by default there are three standard file streams (or descriptors) always open for use: standard input (stdin), standard output (stdout), and standard error (stderr).</p>
<table>
  <tr>
    <th>NAME</th>
    <th>SYMBOLIC NAME</th>
    <th>VALUE</th>
    <th>EXAMPLE</th>
  </tr>
  <tr>
    <td>standard input</td>
    <td>stdin</td>
    <td>0</td>
    <td>keyboard</td>
  </tr>
  <tr>
    <td>standard output</td>
    <td>stdout</td>
    <td>1</td>
    <td>terminal</td>
  </tr>
  <tr>
    <td>standard error</td>
    <td>stderr</td>
    <td>2</td>
    <td>log file</td>
  </tr>
</table>

<h3>I/O Redirection</h3>
<p>We can redirect the three standard file streams so that we can get input from either a file or another command, instead of from our keyboard, and we can write output and errors to files or use them to provide input for subsequent commands.</p>
<p>To redirect input from a file:</p>
<pre>$ do_something < input-file</pre>
<p>To redirect output to a file:</p>
<pre>$ do_something > output-file</pre>
<p>To redirect both input and output:</p>
<pre>$ do_something < input-file > output-file</pre>
<p>To redirect stderr to a file:</p>
<pre>$ do_something 2> error-file</pre>

<h3>Pipes</h3>
<p>The UNIX/Linux philosophy is to have many simple and short programs (or commands) cooperate together to produce quite complex results. Extensive use of pipes is made to combine the actions of several commands into one. To pipe the output of one command into another as its input:</p>
<pre>$ command1 | command2 | command3</pre>

![pipes](https://github.com/user-attachments/assets/43f7e672-6077-4304-aa82-3fd5a1070231)
<strong><p>Pipes</p></strong>

<h3>Search Utilities</h3>

<h4>locate</h4>
<p>The <code>locate</code> utility performs a search while taking advantage of a previously constructed database of files and directories on your system, matching all entries that contain a specified character string. To get a shorter list, use <code>grep</code> as a filter:</p>
<pre>$ locate zip | grep bin</pre>

<h4>find</h4>
<p>The <code>find</code> utility recurses down the filesystem tree from any particular directory (or set of directories) and locates files that match specified conditions. The default pathname is always the present working directory. Commonly used options include <code>-name</code>, <code>-iname</code>, and <code>-type</code>. To search for files and directories named <code>gcc</code>:</p>
<pre>$ find /usr -name gcc</pre>
<p>To search only for directories named <code>gcc</code>:</p>
<pre>$ find /usr -type d -name gcc</pre>

🚀<b>Snapshots for Linux Command Line Tools : <a link href="Snapshots/Command Line Tools">Click here</a></b>

<h2>What Is a Process?</h2>
<p>A <strong>process</strong> is simply an instance of one or more related tasks (threads) executing on your computer. It is not the same as a <strong>program</strong> or a <strong>command</strong>. A single command may actually start several processes simultaneously. Some processes are independent of each other and others are related. A failure of one process may or may not affect the others running on the system.</p>

![image](https://github.com/user-attachments/assets/2f2a558b-40c5-4532-91c5-b2d92b07b70b)
<strong><p>Process Overview</p></strong>

<h3>Processes</h3>
<p>Processes use many system resources, such as memory, CPU (central processing unit) cycles, and peripheral devices, such as network cards, hard drives, printers, and displays. The operating system (especially the kernel) is responsible for allocating a proper share of these resources to each process and ensuring overall optimized system utilization.</p>

<h4>Process Type</h4>
<table>
  <tr>
    <th>Process Type</th>
    <th>Description</th>
    <th>Examples</th>
  </tr>
  <tr>
    <td>Interactive Processes</td>
    <td>Need to be started by a user, either at a command line or through a graphical interface such as an icon or a menu selection.</td>
    <td>bash, firefox, top, Slack, LibreOffice</td>
  </tr>
  <tr>
    <td>Batch Processes</td>
    <td>Automatic processes which are scheduled from and then disconnected from the terminal. These tasks are queued and work on a FIFO (First-In, First-Out) basis.</td>
    <td>updatedb, ldconfig</td>
  </tr>
  <tr>
    <td>Daemons</td>
    <td>Server processes that run continuously. Many are launched during system startup and then wait for a user or system request indicating that their service is required.</td>
    <td>httpd, sshd, libvirtd, cupsd</td>
  </tr>
  <tr>
    <td>Threads</td>
    <td>Lightweight processes. These are tasks that run under the umbrella of a main process, sharing memory and other resources, but are scheduled and run by the system on an individual basis. An individual thread can end without terminating the whole process and a process can create new threads at any time. Many non-trivial programs are multi-threaded.</td>
    <td>dconf-service, gnome-terminal-server</td>
  </tr>
  <tr>
    <td>Kernel Threads</td>
    <td>Kernel tasks that users neither start nor terminate and have little control over. These may perform actions like moving a thread from one CPU to another, or making sure input/output operations to disk are completed.</td>
    <td>kthreadd, migration, ksoftirqd</td>
  </tr>
</table>

<h4>Process Scheduling and States</h4>
<p>A critical kernel function called the <strong>scheduler</strong> constantly shifts processes on and off the CPU, sharing time according to relative priority, how much time is needed and how much has already been granted to a task.</p>
<p>When a process is in a so-called <strong>running</strong> state, it means it is either currently executing instructions on a CPU, or is waiting to be granted a share of time (a time slice) so it can execute. All processes in this state reside on what is called a run queue and on a computer with multiple CPUs, or cores, there is a run queue on each. As noted, the word running is a little misleading as the process may actually be swapped out, waiting its turn to get back in the race.</p>
<p>However, sometimes processes go into what is called a <strong>sleep</strong> state, generally when they are waiting for something to happen before they can resume, perhaps for the user to type something. In this condition, a process is said to be sitting in a wait queue.</p>
<p>There are some other less frequent process states, especially when a process is terminating. Sometimes, a child process completes, but its parent process has not asked about its state. Amusingly, such a process is said to be in a <strong>zombie state</strong>; it is not really alive, but still shows up in the system's list of processes.</p>

![image](https://github.com/user-attachments/assets/68dbfb9f-94b3-4a1a-bd1f-9d26c38790ce)
<strong><p>Process Scheduling</p></strong>

<h4>Process and Thread IDs</h4>
<p>At any given time, there are always multiple processes being executed. The operating system keeps track of them by assigning each a unique process ID (PID) number. The PID is used to track process state, CPU usage, memory use, precisely where resources are located in memory, and other characteristics.</p>
<p>New PIDs are usually assigned in ascending order as processes are born. Thus, PID 1 denotes the <strong>init</strong> process (system initialization process), and succeeding processes are gradually assigned higher numbers.</p>

<h4>User and Group IDs</h4>
<p>Many users can access a system simultaneously, and each user can run multiple processes. The operating system identifies the user who starts the process by the Real User ID (RUID) assigned to the user.</p>
<p>The user who determines the access rights for the users is identified by the Effective UID (EUID). The EUID may or may not be the same as the RUID.</p>
<p>Users can be organized into enumerated groups. Each group is identified by the Real Group ID (RGID). The access rights of the group are determined by the Effective Group ID (EGID). Each user can be a member of one or more groups.</p>
<p>Most of the time we ignore these details and just talk about the User ID (UID) and Group ID (GID).</p>

![image](https://github.com/user-attachments/assets/95cc3512-8c2f-4cea-af18-ac91410a9a52)
<strong><p>Process Scheduling</p></strong>

<h4>Load Averages</h4>
<p>The <strong>load average</strong> is the average of the <strong>load number</strong> for a given period of time. It takes into account processes that are:</p>
<ul>
  <li>Actively running on a CPU.</li>
  <li>Considered runnable, but waiting on the run queue for a CPU to become available.</li>
  <li>Sleeping: i.e. waiting for some kind of resource (typically, I/O) to become available.</li>
</ul>
<p>NOTE: Linux differs from other UNIX-like operating systems in that it includes the sleeping processes. Furthermore, it only includes so-called <strong>uninterruptible</strong> sleepers, those which cannot be awakened easily.</p>

<h4>Interpreting Load Averages</h4>
<p>The load average is displayed using three numbers (0.45, 0.17, and 0.12) in the below screenshot. Assuming our system is a single-CPU system, the three load average numbers are interpreted as follows:</p>
<ul>
  <li>0.45: For the last minute the system has been 45% utilized on average.</li>
  <li>0.17: For the last 5 minutes utilization has been 17%.</li>
  <li>0.12: For the last 15 minutes utilization has been 12%.</li>
</ul>
<p>If we saw a value of 1.00 in the second position, that would imply that the single-CPU system was 100% utilized, on average, over the past 5 minutes; this is good if we want to fully use a system. A value over 1.00 for a single-CPU system implies that the system was over-utilized: there were more processes needing CPU than CPU was available.</p>
<p>If we had more than one CPU, say a quad-CPU system, we would divide the load average numbers by the number of CPUs. In this case, for example, seeing a 1 minute load average of 4.00 implies that the system as a whole was 100% (4.00/4) utilized during the last minute.</p>
<p>Short-term increases are usually not a problem. A high peak you see is likely a burst of activity, not a new level. For example, at start up, many processes start and then activity settles down. If a high peak is seen in the 5 and 15 minute load averages, it may be cause for concern.</p>

<h4>Background and Foreground Processes</h4>
<p>Linux supports background and foreground <strong>job processing</strong>. A job in this context is just a command launched from a terminal window. Foreground jobs run directly from the shell, and when one foreground job is running, other jobs need to wait for shell access (at least in that terminal window if using the GUI) until it is completed. This is fine when jobs complete quickly. But this can have an adverse effect if the current job is going to take a long time (even several hours) to complete.</p>
<p>In such cases, you can run the job in the background and free the shell for other tasks. The background job will be executed at lower priority, which, in turn, will allow smooth execution of the interactive tasks, and you can type other commands in the terminal window while the background job is running. By default, all jobs are executed in the foreground. You can put a job in the background by suffixing <code>&</code> to the command, for example: <code>updatedb &</code>.</p>
<p>You can use <code>CTRL-Z</code> to suspend a foreground job (i.e., put it in background) and <code>CTRL-C</code> to terminate it. You can
<h3>The <code>ps</code> Command (System V Style)</h3>
<p><code>ps</code> (process status) provides information about currently running processes keyed by PID. If you want a periodic update of this status, you can use <code>top</code> or other commonly installed variants (such as <code>htop</code>, <code>atop</code>, or <code>btop</code>) from the command line, or invoke your distribution's graphical system monitor application (such as <code>gnome-system-monitor</code> or <code>ksysguard</code>).</p>
<p><code>ps</code> has many options for specifying exactly which tasks to examine, what information to display about them, and precisely what output format should be used.</p>
<ul>
    <li><strong>Default Behavior</strong>: Without options, <code>ps</code> will display all processes running under the current shell.</li>
    <li><strong>-u Option</strong>: Use <code>ps -u &lt;username&gt;</code> to display information of processes for a specified username.</li>
    <li><strong>-ef Option</strong>: The command <code>ps -ef</code> displays all the processes in the system in full detail.</li>
    <li><strong>-eLf Option</strong>: The command <code>ps -eLf</code> goes one step further and displays one line of information for every thread (remember, a process can contain multiple threads).</li>
</ul>

<h3>The <code>ps</code> Command (BSD Style)</h3>
<p><code>ps</code> has another style of option specification, which stems from the BSD variety of UNIX, where options are specified without preceding dashes. For example, the command <code>ps aux</code> displays all processes of all users. The command <code>ps axo</code> allows you to specify which attributes you want to view.</p>
<p>The screenshot shows a sample output of <code>ps</code> with the <code>aux</code> and <code>axo</code> qualifiers.</p>

<h3>The <code>top</code> Command</h3>
<p>While a static view of what the system is doing is useful, monitoring the system performance live over time is also valuable. One option would be to run <code>ps</code> at regular intervals, say, every few seconds. A better alternative is to use <code>top</code> to get constant real-time updates (every two seconds by default), until you exit by typing <code>q</code>. <code>top</code> clearly highlights which processes are consuming the most CPU cycles and memory (using appropriate commands from within <code>top</code>).</p>

![image](https://github.com/user-attachments/assets/4afb17a2-2462-4a01-b632-a0f175243d78)
<strong><p>Top command</p></strong>

<h4>First Line of the <code>top</code> Output</h4>
<p>The first line of the <code>top</code> output displays a quick summary of what is happening in the system, including:</p>
<ul>
    <li>How long the system has been up</li>
    <li>How many users are logged on</li>
    <li>What is the load average</li>
</ul>
<p>The load average determines how busy the system is. A load average of 1.00 per CPU indicates a fully subscribed, but not overloaded, system. If the load average goes above this value, it indicates that processes are competing for CPU time. If the load average is very high, it might indicate that the system is having a problem, such as a runaway process (a process in a non-responding state).</p>

<h4>Second Line of the <code>top</code> Output</h4>
<p>The second line of the <code>top</code> output displays the total number of processes, the number of running, sleeping, stopped, and zombie processes. Comparing the number of running processes with the load average helps determine if the system has reached its capacity or perhaps a particular user is running too many processes. The stopped processes should be examined to see if everything is running correctly.</p>

<h4>Third Line of the <code>top</code> Output</h4>
<p>The third line of the <code>top</code> output indicates how the CPU time is being divided between the users (us) and the kernel (sy) by displaying the percentage of CPU time used for each.</p>
<p>The percentage of user jobs running at a lower priority (niceness - ni) is then listed. Idle mode (id) should be low if the load average is high, and vice versa. The percentage of jobs waiting (wa) for I/O is listed. Interrupts include the percentage of hardware (hi) vs. software interrupts (si). Steal time (st) is generally used with virtual machines, which has some of its idle CPU time taken for other uses.</p>

<h4>Fourth and Fifth Lines of the <code>top</code> Output</h4>
<p>The fourth and fifth lines of the <code>top</code> output indicate memory usage, which is divided in two categories:</p>
<ul>
    <li>Physical memory (RAM) – displayed on line 4.</li>
    <li>Swap space – displayed on line 5.</li>
</ul>
<p>Both categories display total memory, used memory, and free space.</p>
<p>You need to monitor memory usage very carefully to ensure good system performance. Once the physical memory is exhausted, the system starts using swap space (temporary storage space on the hard drive) as an extended memory pool, and since accessing disk is much slower than accessing memory, this will negatively affect system performance.</p>
<p>If the system starts using swap often, you can add more swap space. However, adding more physical memory should also be considered.</p>

<h4>Process List of the <code>top</code> Output</h4>
<p>Each line in the process list of the <code>top</code> output displays information about a process. By default, processes are ordered by highest CPU usage. The following information about each process is displayed:</p>
<ul>
    <li>Process Identification Number (PID)</li>
    <li>Process owner (USER)</li>
    <li>Priority (PR) and nice values (NI)</li>
    <li>Virtual (VIRT), physical (RES), and shared memory (SHR)</li>
    <li>Status (S)</li>
    <li>Percentage of CPU (%CPU) and memory (%MEM) used</li>
    <li>Execution time (TIME+)</li>
    <li>Command (COMMAND)</li>
</ul>

<h3>The <code>cron</code> Command</h3>
<p><code>cron</code> is a time-based scheduling utility program. It can launch routine background jobs at specific times and/or days on an ongoing basis. <code>cron</code> is driven by a configuration file called <code>/etc/crontab</code> (cron table), which contains the various shell commands that need to be run at the properly scheduled times. There are both system-wide <code>crontab</code> files and individual user-based ones. Each line of a <code>crontab</code> file represents a job, and is composed of a so-called CRON expression, followed by a shell command to execute.</p>
<p>Typing <code>crontab -e</code> will open the crontab editor to edit existing jobs or to create new jobs. Each line of the <code>crontab</code> file will contain 6 fields:</p>

<table>
    <tr>
        <th>Field</th>
        <th>Description</th>
        <th>Values</th>
    </tr>
    <tr>
        <td>MIN</td>
        <td>Minutes</td>
        <td>0 to 59</td>
    </tr>
    <tr>
        <td>HOUR</td>
        <td>Hour field</td>
        <td>0 to 23</td>
    </tr>
    <tr>
        <td>DOM</td>
        <td>Day of Month</td>
        <td>1-31</td>
    </tr>
    <tr>
        <td>MON</td>
        <td>Month field</td>
        <td>1-12</td>
    </tr>
    <tr>
        <td>DOW</td>
        <td>Day of Week</td>
        <td>0-6 (0 = Sunday)</td>
    </tr>
    <tr>
        <td>CMD</td>
        <td>Command</td>
        <td>Any command to be executed</td>
    </tr>
</table>

<p>Examples:</p>
<ul>
    <li>The entry <code>* * * * * /usr/local/bin/execute/this/script.sh</code> will schedule a job to execute <code>script.sh</code> every minute of every hour of every day of the month, and every month and every day in the week.</li>
    <li>The entry <code>30 08 10 06 * /home/sysadmin/full-backup</code> will schedule a full-backup at 8.30 a.m., 10-June, irrespective of the day of the week.</li>
</ul>

<h3>The <code>sleep</code> Command</h3
<h3>The <code>sleep</code> Command</h3>
<p>Sometimes, a command or job must be delayed or suspended. Suppose, for example, an application has read and processed the contents of a data file and then needs to save a report on a backup system. If the backup system is currently busy or not available, the application can be made to sleep (wait) until it can complete its work. Such a delay might be to mount the backup device and prepare it for writing. An even simpler and frequent case is one where a system process needs to run periodically to take care of any work that has been queued up for it to deal with and then has to lurk in the background until it is needed again.</p>
<p><code>sleep</code> suspends execution for at least the specified period of time, which can be given as the number of seconds (the default), minutes, hours, or days. After that time has passed (or an interrupting signal has been received), execution will resume.</p>
<p>The syntax is:</p>

<pre><code>sleep NUMBER[SUFFIX]...</code></pre>

<p>where <code>SUFFIX</code> may be:</p>
<ul>
    <li><code>s</code> for seconds (the default)</li>
    <li><code>m</code> for minutes</li>
    <li><code>h</code> for hours</li>
    <li><code>d</code> for days</li>
</ul>

🚀<b>Snapshots for Linux Processes (System and User) : <a link href="Snapshots/Processes">Click here</a></b>
