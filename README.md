# 🎮 Apex Legends Autoexec Generator (📆 Outdated)

### 🧩 Description

This desktop application was developed using Java 8 (Swing) in NetBeans to simplify the creation and editing of autoexec configuration files for Apex Legends. This was to resolve an issue of game downtime when editing Autoexec files for the game.

During peak competitive play, advanced techniques like tap-strafing and custom keybind optimization required manual editing of .cfg files. This process was repetitive and error-prone especially as in game meta's changed and code changed within the game where certains aspects where disabled.

The goal of this application was to provide a fast, user-friendly interface to generate and customize autoexec files without needing to manually write configurations when changing between AutoExec config files. 

****
### 🖼️ Layout
<img width="952" height="529" alt="image" src="https://github.com/user-attachments/assets/55eb3fc5-f0bd-419c-88c1-779e41aa4b3d" />

## Files generated
<details>
  <summary><strong>Autoxec.cfg</strong></summary

```Java
   //AutoExec Setup EXECUTE AUTOEXEC if fails to run on start
      bind_US_standard "F12" "exec autoexec" 0
     
  //Show Ingame POS,Speed
    bind_US_standard "." "toggle cl_showpos 1 0"
  
  //FOV 120 SCALE
    cl_fovScale "1.7"
     
  //NETWORK LAG FIXES
  //Should almost always be 0 to reduce artificial latency (0 syncs with server)
    cl_interp 0
  // use 1 if you have no packet loss, use 2 if you have light packet loss, use 3 or 4 if you have heavy packet loss
    cl_interp_ratio 1
  // using higher values makes no sense because apex server tick is locked at 20Hz
    cl_updaterate 128
     
  //SOUND SETTINGS
    miles_occlusion_server_sounds_per_frame "20"
    miles_occlusion "0"
    miles_occlusion_force "0"
    miles_occlusion_partial "0"
    snd_mixahead "0.05"
    snd_surround_speakers 8
    snd_headphone_pan_exponent "8"
    snd_musicvolume "0.8"
    snd_setmixer PlayerFootsteps vol 0.09
    snd_setmixer GlobalFootsteps vol 5.0
    miles_channels 8
     
  //Multiple CFG's Below
    exec ScrollAtk.cfg
    exec Legend.cfg
    exec Strafer.cfg
```
    
</details>

<details>
  <summary><strong>ScrollAtk.cfg</strong></summary

```Java
  //GUN GO BRRRRTTT
    bind_US_standard "mwheelup" "+attack" 0
    bind_US_standard "mwheeldown" "+attack" 0
    bind_US_standard "/" "exec Strafer.cfg" 0
    bind_US_standard "," "exec Legend.cfg" 0
```
    
</details>

<details>
  <summary><strong>Legend.cfg</strong></summary

```Java
  //Become a Legend
    bind_US_standard "mwheeldown" "+use; +use_long; +jump" 0
    bind_US_standard "mwheelup" "+forward; +jump" 0
    bind_US_standard "," "exec ScrollAtk.cfg" 0
    bind_US_standard "/" "exec Strafer.cfg" 0
```
    
</details>

<details>
  <summary><strong>Strafer.cfg</strong></summary

```Java
  //Strafe Backwards your MAD
    bind_US_standard "mwheeldown" "+backward; +jump" 0
    bind_US_standard "mwheelup" "+forward; +jump" 0
    bind_US_standard "/" "exec Legend.cfg" 0
    bind_US_standard "," "exec ScrollAtk.cfg" 0
```
    
</details>

## 🚀 Features
#### 🎯 Radio button-based selection for key settings (ensures valid input)
#### ⚙️ Generate .cfg autoexec files instantly
#### 🎮 Supports configuration for:
  - Keybinds
  - Scripts (Switching Config File mid game)
  - Audio settings
  - Video settings
  - Performance tweaks
#### 🖥️ Built with Java Swing for a lightweight desktop experience
#### 💾 One-click file generation and saving
