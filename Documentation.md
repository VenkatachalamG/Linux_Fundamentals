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

