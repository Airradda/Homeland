# **Homeland**

A collection of instructions and scripts to take back the $HOME directory on linux machines from rampant dot files. 

*These instructions assume you are running an __Arch-based__ system, if you are not, please consult the manuals and wikis for your system about some of the referenced files and variables.

# Folders

## .nv
---
The .nv file belongs to [**NVIDIA**](http://us.download.nvidia.com/XFree86/FreeBSD-x86/319.32/README/) as part of the [OpenGL Shader Disk Cache](http://us.download.nvidia.com/XFree86/FreeBSD-x86/319.32/README/openglenvvariables.html).

>The NVIDIA OpenGL driver utilizes a shader disk cache. This optimization benefits some applications, by reusing shader binaries instead of compiling them repeatedly...By default, caches are stored in $HOME/.nv/GLCache.

To fix this we will need to set the `__GL_SHADER_DISK_CACHE_PATH` as an environment variable for the either per user or entire system.

__User__ (*Suggested*): Put `export __GL_SHADER_DISK_CACHE_PATH="/home/$USER/.local/share/nvidia/cache/"` in the `.bashrc` in the HOME directory (if it is not there, make it)

__System Wide__: Put `export __GL_SHADER_DISK_CACHE_PATH="/home/$USER/.local/share/nvidia/cache/"` in proper shell script form in `/etc/profile/` (may also be `/etc/profile.d/`)

References:

https://wiki.archlinux.org/index.php/Environment_variables

http://us.download.nvidia.com/XFree86/FreeBSD-x86/319.32/README/

## .persepolis
---

As the folder name suggest, .persepolis belongs to the Persepolis Download Manager and is the default temporary download folder. To change it, simple go to `Edit>Preferences>Save as` and change the `Temporary Download Folder` to what ever you want. Finally, you can simply delete the old folder.