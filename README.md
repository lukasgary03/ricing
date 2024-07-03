** NOTE: When making rofi-wayland, uninstall that using yay then install it with yay as just rofi. IDK why installer chooses the wayland version when general works great

# ricing

Putting all my designs and process of creating a linux desktop environment in this repo


Additional notes: 
minecraft using fabric-loader

https://app.3dprintforce.com/dashboard?v=3dmodels
https://www.paypal.com/shiplabel/home 
https://www.chunkbase.com/apps/seed-map#-4649662074261581818

 BetterF3-9.0.0-Fabric-1.20.4.jar                   Zoomify-2.12.0.jar
 blur-3.1.1.jar
 entity_model_features_fabric_1.20.4-1.3.jar
 entity_texture_features_fabric_1.20.4-5.2.3.jar
 fabric-api-0.96.4+1.20.4.jar
 fabric-language-kotlin-1.10.18+kotlin.1.9.22.jar
 freecam-fabric-modrinth-1.2.3+1.20.4.jar
 iris-mc1.20.4-1.6.17.jar
 modmenu-9.0.0.jar
 MouseTweaks-fabric-mc1.20-2.25.jar
 shulkerboxtooltip-fabric-4.0.8+1.20.4.jar
 sodium-fabric-0.5.8+mc1.20.4.jar
 yet-another-config-lib-fabric-3.3.2+1.20.4.jar


    // Clock
    "clock": {
        // "timezone": "America/New_York",
        "tooltip-format": "<big>{:%Y %B}</big>\n<tt><small>{calendar}</small></tt>",
        "format": "{:%I:%M}",
        // START CLOCK FORMAT
        "format-alt": "{:%Y-%m-%d}"
        // END CLOCK FORMAT
    },

# ----------------------------------------------------- 
# Key bindings
# name: "Default"
# ----------------------------------------------------- 

# SUPER KEY
$mainMod = SUPER

# Applications
bind = $mainMod, RETURN, exec, ~/dotfiles/.settings/terminal.sh # Open the terminal
bind = $mainMod, F, exec, ~/dotfiles/.settings/browser.sh # Open the browser
bind = $mainMod, S, exec, spotify # Open spotify
bind = $mainMod, N, exec, chromium notion.so # Open notion
bind = $mainMod, N, exec, chromium luna.amazon.com # Open fortnite online
bind = $mainMod, O, exec, obsidian # Open obsidian

# Windows
bind = $mainMod, Q, killactive # Kill active window
bind = $mainMod, T, fullscreen # Set active window to fullscreen
bind = $mainMod, G, togglefloating # Toggle active windows into floating mode
bind = $mainMod, E, exec, ~/dotfiles/.settings/filemanager.sh # Open the filemanager
bind = $mainMod SHIFT, T, exec, ~/dotfiles/hypr/scripts/toggleallfloat.sh # Toggle all windows into floating mode
bind = $mainMod, C, togglesplit # Toggle split
bind = $mainMod, H, movefocus, l # Move focus left
bind = $mainMod, L, movefocus, r # Move focus right
bind = $mainMod, K, movefocus, u # Move focus up
bind = $mainMod, J, movefocus, d # Move focus down
bind = $mainMod SHIFT, H, movewindow, l # Move focus left
bind = $mainMod SHIFT, L, movewindow, r # Move focus right
bind = $mainMod SHIFT, K, movewindow, u # Move focus up
bind = $mainMod SHIFT, J, movewindow, d # Move focus down
bindm = $mainMod, mouse:272, movewindow # Move window with the mouse
bindm = $mainMod, mouse:273, resizewindow # Resize window with the mouse
bind = $mainMod SHIFT, right, resizeactive, 100 0 # Increase window width with keyboard
bind = $mainMod SHIFT, left, resizeactive, -100 0 # Reduce window width with keyboard
bind = $mainMod SHIFT, down, resizeactive, 0 100 # Increase window height with keyboard
bind = $mainMod SHIFT, up, resizeactive, 0 -100 # Reduce window height with keyboard
bind = $mainMod, G, togglegroup # Toggle window group

# Actions
bind = $mainMod SHIFT, A, exec, ~/dotfiles/hypr/scripts/toggle-animations.sh # Toggle animations
bind = $mainMod, PRINT, exec, ~/dotfiles/hypr/scripts/screenshot.sh # Take a screenshot
bind = $mainMod, M, exec, wlogout # Start wlogout
bind = $mainMod SHIFT, W, exec, waypaper --random # Change the wallpaper
bind = $mainMod CTRL, W, exec, waypaper # Open wallpaper selector
bind = $mainMod, SPACE, exec, rofi -show drun -replace -i # Open application launcher
bind = $mainMod CTRL, H, exec, ~/dotfiles/hypr/scripts/keybindings.sh # Show keybindings
bind = $mainMod SHIFT, B, exec, ~/dotfiles/waybar/launch.sh # Reload waybar
bind = $mainMod CTRL, B, exec, ~/dotfiles/waybar/toggle.sh # Toggle waybar
bind = $mainMod SHIFT, R, exec, ~/dotfiles/hypr/scripts/loadconfig.sh # Reload hyprland config
bind = $mainMod, V, exec, ~/dotfiles/scripts/cliphist.sh # Open clipboard manager
bind = $mainMod CTRL, T, exec, ~/dotfiles/waybar/themeswitcher.sh # Open waybar theme switcher
bind = $mainMod CTRL, S, exec, ~/dotfiles/apps/ML4W_Dotfiles_Settings-x86_64.AppImage # Open ML4W Dotfiles Settings app
bind = $mainMod SHIFT, S, exec, ~/dotfiles/hypr/scripts/hyprshade.sh # Toggle screenshader
bind = $mainMod ALT, G, exec, ~/dotfiles/hypr/scripts/gamemode.sh # Toggle game mode

# Workspaces
bind = $mainMod, 1, workspace, 1 # Open workspace 1
bind = $mainMod, 2, workspace, 2 # Open workspace 2
bind = $mainMod, 3, workspace, 3 # Open workspace 3
bind = $mainMod, 4, workspace, 4 # Open workspace 4
bind = $mainMod, 5, workspace, 5 # Open workspace 5
bind = $mainMod, 6, workspace, 6 # Open workspace 6
bind = $mainMod, 7, workspace, 7 # Open workspace 7
bind = $mainMod, 8, workspace, 8 # Open workspace 8
bind = $mainMod, 9, workspace, 9 # Open workspace 9
bind = $mainMod, 0, workspace, 10 # Open workspace 10
bind = $mainMod SHIFT, 1, movetoworkspace, 1 # Move active window to workspace 1
bind = $mainMod SHIFT, 2, movetoworkspace, 2 # Move active window to workspace 2
bind = $mainMod SHIFT, 3, movetoworkspace, 3 # Move active window to workspace 3
bind = $mainMod SHIFT, 4, movetoworkspace, 4 # Move active window to workspace 4
bind = $mainMod SHIFT, 5, movetoworkspace, 5 # Move active window to workspace 5
bind = $mainMod SHIFT, 6, movetoworkspace, 6 # Move active window to workspace 6
bind = $mainMod SHIFT, 7, movetoworkspace, 7 # Move active window to workspace 7
bind = $mainMod SHIFT, 8, movetoworkspace, 8 # Move active window to workspace 8
bind = $mainMod SHIFT, 9, movetoworkspace, 9 # Move active window to workspace 9
bind = $mainMod SHIFT, 0, movetoworkspace, 10 # Move active window to workspace 10
bind = $mainMod, mouse_down, workspace, e+1 # Open next workspace
bind = $mainMod, mouse_up, workspace, e-1 # Open previous workspace
bind = $mainMod CTRL, down, workspace, empty # Open the next empty workspace

# Passthrough SUPER KEY to Virtual Machine
bind = $mainMod, P, submap, passthru # Passthrough SUPER key to virtual machine
submap = passthru
bind = SUPER, Escape, submap, reset # Get SUPER key back from virtual machine
submap = reset

# Fn keys
bind = , XF86MonBrightnessUp, exec, brightnessctl -q s +10% # Increase brightness by 10%
bind = , XF86MonBrightnessDown, exec, brightnessctl -q s 10%- # Reduce brightness by 10%
bind = , XF86AudioRaiseVolume, exec, pactl set-sink-volume @DEFAULT_SINK@ +5% # Increase volume by 5%
bind = , XF86AudioLowerVolume, exec, pactl set-sink-volume @DEFAULT_SINK@ -5% # Reduce volume by 5%
bind = , XF86AudioMute, exec, wpctl set-mute @DEFAULT_AUDIO_SINK@ toggle # Toggle mute
bind = , XF86AudioPlay, exec, playerctl play-pause # Audio play pause
bind = , XF86AudioPause, exec, playerctl pause # Audio pause
bind = , XF86AudioNext, exec, playerctl next # Audio next
bind = , XF86AudioPrev, exec, playerctl previous # Audio previous
bind = , XF86AudioMicMute, exec, pactl set-source-mute @DEFAULT_SOURCE@ toggle # Toggle microphone
bind = , XF86Calculator, exec, qalculate-gtk # Open calculator
bind = , XF86Lock, exec, hyprlock # Open screenlock
bind = , XF86Tools, exec, alacritty --class dotfiles-floating -e ~/dotfiles/apps/ML4W_Dotfiles_Settings-x86_64.AppImage # Open ML4W Dotfiles Settings app



HHH
monitor=HDMI-A-1, 1920x1080, 0x0, 1 #HKC
monitor=DP-2, 2560x1080@100.00, 1920x0, 1 #wide
monitor=HDMI-A-2, 1920x1080, 4480x0, 1 #22cwa


HHV
monitor=HDMI-A-1, 1920x1080, 0x0, 1 #HKC
monitor=DP-2, 2560x1080@100.00, 1920x0, 1 #wide
monitor=HDMI-A-2, 1920x1080, 4480x0, 1, transform, 3 #22cwa


VHH
monitor=HDMI-A-1, 1920x1080, 0x0, 1, transform, 1 #HKC
monitor=DP-2, 2560x1080@100.00, 1080x0, 1
monitor=HDMI-A-2, 1920x1080, 3640x0, 1 #22cwa



VHV
monitor=HDMI-A-1, 1920x1080, 0x0, 1, transform, 1 #HKC
monitor=DP-2, 2560x1080@100.00, 1080x0, 1
monitor=HDMI-A-2, 1920x1080, 3640x0, 1, transform, 3 #22cwa


yt dlp something like that
