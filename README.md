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
bind = $mainMod, RETURN, exec, ~/dotfiles/.settings/terminal.sh
bind = $mainMod, F, exec, ~/dotfiles/.settings/browser.sh
bind = $mainMod, S, exec, chromium spotify.com
bind = $mainMod, N, exec, chromium notion.so
bind = $mainMod, B, exec, google-chrome-stable luna.amazon.com
# Windows
bind = $mainMod, Q, killactive
bind = $mainMod, T, fullscreen
bind = $mainMod, E, exec, ~/dotfiles/scripts/filemanager.sh
bind = $mainMod, G, togglefloating
bind = $mainMod SHIFT, T, exec, ~/dotfiles/hypr/scripts/toggleallfloat.sh
bind = $mainMod, C, togglesplit
bind = $mainMod, H, movefocus, l
bind = $mainMod, L, movefocus, r
bind = $mainMod, K, movefocus, u
bind = $mainMod, J, movefocus, d
bind = $mainMod SHIFT, J, movewindow, d
bind = $mainMod SHIFT, H, movewindow, l
bind = $mainMod SHIFT, L, movewindow, r
bind = $mainMod SHIFT, K, movewindow, u
bindm = $mainMod, mouse:272, movewindow
bindm = $mainMod, mouse:273, resizewindow
bind = $mainMod SHIFT, right, resizeactive, 100 0
bind = $mainMod SHIFT, left, resizeactive, -100 0
bind = $mainMod SHIFT, up, resizeactive, 0 -100
bind = $mainMod SHIFT, down, resizeactive, 0 100

# Actions
bind = $mainMod, PRINT, exec, ~/dotfiles/hypr/scripts/screenshot.sh
bind = $mainMod, M, exec, wlogout
bind = $mainMod SHIFT, W, exec, ~/dotfiles/hypr/scripts/wallpaper.sh
bind = $mainMod CTRL, W, exec, ~/dotfiles/hypr/scripts/wallpaper.sh select
bind = $mainMod, SPACE, exec, rofi -show drun
bind = $mainMod CTRL, H, exec, ~/dotfiles/hypr/scripts/keybindings.sh
bind = $mainMod SHIFT, B, exec, ~/dotfiles/waybar/launch.sh
bind = $mainMod SHIFT, R, exec, ~/dotfiles/hypr/scripts/loadconfig.sh
bind = $mainMod CTRL, F, exec, ~/dotfiles/scripts/filemanager.sh
bind = $mainMod CTRL, C, exec, ~/dotfiles/scripts/cliphist.sh
bind = $mainMod, V, exec, ~/dotfiles/scripts/cliphist.sh
bind = $mainMod CTRL, T, exec, ~/dotfiles/waybar/themeswitcher.sh
bind = $mainMod CTRL, S, exec, alacritty --class dotfiles-floating -e ~/dotfiles/hypr/start-settings.sh

# Workspaces
bind = $mainMod, 1, workspace, 1
bind = $mainMod, 2, workspace, 2
bind = $mainMod, 3, workspace, 3
bind = $mainMod, 4, workspace, 4
bind = $mainMod, 5, workspace, 5
bind = $mainMod, 6, workspace, 6
bind = $mainMod, 7, workspace, 7
bind = $mainMod, 8, workspace, 8
bind = $mainMod, 9, workspace, 9
bind = $mainMod, 0, workspace, 10
bind = $mainMod SHIFT, 1, movetoworkspace, 1
bind = $mainMod SHIFT, 2, movetoworkspace, 2
bind = $mainMod SHIFT, 3, movetoworkspace, 3
bind = $mainMod SHIFT, 4, movetoworkspace, 4
bind = $mainMod SHIFT, 5, movetoworkspace, 5
bind = $mainMod SHIFT, 6, movetoworkspace, 6
bind = $mainMod SHIFT, 7, movetoworkspace, 7
bind = $mainMod SHIFT, 8, movetoworkspace, 8
bind = $mainMod SHIFT, 9, movetoworkspace, 9
bind = $mainMod SHIFT, 0, movetoworkspace, 10
bind = $mainMod, mouse_down, workspace, e+1
bind = $mainMod, mouse_up, workspace, e-1
bind = $mainMod CTRL, down, workspace, empty

# Fn keys
bind = , XF86MonBrightnessUp, exec, brightnessctl -q s +10%
bind = , XF86MonBrightnessDown, exec, brightnessctl -q s 10%-
bind = , XF86AudioRaiseVolume, exec, pactl set-sink-volume @DEFAULT_SINK@ +5%
bind = , XF86AudioLowerVolume, exec, pactl set-sink-volume @DEFAULT_SINK@ -5%
bind = , XF86AudioMute, exec, wpctl set-mute @DEFAULT_AUDIO_SINK@ toggle
bind = , XF86AudioPlay, exec, playerctl play-pause
bind = , XF86AudioPause, exec, playerctl pause
bind = , XF86AudioNext, exec, playerctl next
bind = , XF86AudioPrev, exec, playerctl previous
bind = , XF86AudioMicMute, exec, pactl set-source-mute @DEFAULT_SOURCE@ toggle
bind = , XF86Calculator, exec, qalculate-gtk
bind = , XF86Lock, exec, swaylock
bind = , XF86Tools, exec, alacritty --class dotfiles-floating -e ~/dotfiles/hypr/settings/settings.sh

# Passthrough SUPER KEY to Virtual Machine
#bind = $mainMod, P, submap, passthru
#submap = passthru
#bind = SUPER, Escape, submap, reset
#submap = reset


HHH
monitor=HDMI-A-1, 1920x1080, 0x0, 1 #HKC
monitor=DP-1, 2560x1080@100.00, 1920x0, 1
monitor=HDMI-A-2, 1920x1080, 4480x0, 1 #22cwa


HHV
monitor=HDMI-A-1, 1920x1080, 0x0, 1, #HKC
monitor=DP-1, 2560x1080@100.00, 1920x0, 1
monitor=HDMI-A-2, 1920x1080, 4480x0, 1, transform, 3 #22cwa


VHH
monitor=HDMI-A-1, 1920x1080, 0x0, 1, transform, 1 #HKC
monitor=DP-1, 2560x1080@100.00, 1080x0, 1
monitor=HDMI-A-2, 1920x1080, 3640x0, 1 #22cwa



VHV
monitor=HDMI-A-1, 1920x1080, 0x0, 1, transform, 1 #HKC
monitor=DP-1, 2560x1080@100.00, 1080x0, 1
monitor=HDMI-A-2, 1920x1080, 3640x0, 1, transform, 3 #22cwa
