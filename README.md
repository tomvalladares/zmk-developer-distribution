# ZMK Corne Keyboard Configuration

This configuration provides optimized layouts for the Corne keyboard with support for both macOS and Windows, including integration with AeroSpace window manager.

## Features

- **Dual OS Support**: Dedicated layouts for macOS and Windows
- **AeroSpace Integration**: Hyper key modifier function for window management
- **Bluetooth Management**: Easy switching between 5 devices
- **Media Controls**: Volume, playback, and navigation
- **Function Keys**: Full F1-F12 support
- **Number Pad**: Dedicated numpad on lower layer

## Layer Overview

### Layer 0: Default (Mac)
```
┌─────┬─────┬─────┬─────┬─────┬─────┐       ┌─────┬─────┬─────┬─────┬─────┬─────┐
│ TAB │  Q  │  W  │  E  │  R  │  T  │       │  Y  │  U  │  I  │  O  │  P  │BSPC │
├─────┼─────┼─────┼─────┼─────┼─────┤       ├─────┼─────┼─────┼─────┼─────┼─────┤
│LSHFT│  A  │  S  │  D  │  F  │  G  │       │  H  │  J  │  K  │  L  │  ;  │  '  │
├─────┼─────┼─────┼─────┼─────┼─────┤       ├─────┼─────┼─────┼─────┼─────┼─────┤
│LGUI │  Z  │  X  │  C  │  V  │  B  │       │  N  │  M  │  ,  │  .  │  /  │HYPER│
└─────┴─────┴─────┼─────┼─────┼─────┤       ├─────┼─────┼─────┼─────┴─────┴─────┘
                  │LALT │ LWR │SPACE│       │ENTER│ RSE │RALT │
                  └─────┴─────┴─────┘       └─────┴─────┴─────┘
```

### Layer 1: Lower (Navigation & Numbers)
```
┌─────┬─────┬─────┬─────┬─────┬─────┐       ┌─────┬─────┬─────┬─────┬─────┬─────┐
│ ESC │VOL+ │HOME │ UP  │ END │  [  │       │  ]  │  7  │  8  │  9  │  0  │BSPC │
├─────┼─────┼─────┼─────┼─────┼─────┤       ├─────┼─────┼─────┼─────┼─────┼─────┤
│LSHFT│MUTE │LEFT │DOWN │RIGHT│  (  │       │  )  │  4  │  5  │  6  │  .  │ DEL │
├─────┼─────┼─────┼─────┼─────┼─────┤       ├─────┼─────┼─────┼─────┼─────┼─────┤
│LGUI │VOL- │PREV │PLAY │NEXT │  {  │       │  }  │  1  │  2  │  3  │     │HYPER│
└─────┴─────┴─────┼─────┼─────┼─────┤       ├─────┼─────┼─────┼─────┴─────┴─────┘
                  │LCTRL│     │SPACE│       │ENTER│ CFG │LALT │
                  └─────┴─────┴─────┘       └─────┴─────┴─────┘
```

### Layer 2: Raise (Symbols & Function Keys)
```
┌─────┬─────┬─────┬─────┬─────┬─────┐       ┌─────┬─────┬─────┬─────┬─────┬─────┐
│ TAB │  !  │  @  │  #  │  $  │  %  │       │  ^  │  &  │  *  │  (  │  )  │BSPC │
├─────┼─────┼─────┼─────┼─────┼─────┤       ├─────┼─────┼─────┼─────┼─────┼─────┤
│LSHFT│ F1  │ F2  │ F3  │ F4  │ F5  │       │  -  │  =  │  [  │  ]  │  \  │  `  │
├─────┼─────┼─────┼─────┼─────┼─────┤       ├─────┼─────┼─────┼─────┼─────┼─────┤
│LGUI │ F6  │ F7  │ F8  │ F9  │ F11 │       │  _  │  +  │  {  │  }  │  |  │  ~  │
└─────┴─────┴─────┼─────┼─────┼─────┤       ├─────┼─────┼─────┼─────┴─────┴─────┘
                  │LCTRL│ CFG │SPACE│       │ENTER│     │RALT │
                  └─────┴─────┴─────┘       └─────┴─────┴─────┘
```

### Layer 3: Config (Bluetooth & System)
```
┌─────┬─────┬─────┬─────┬─────┬─────┐       ┌─────┬─────┬─────┬─────┬─────┬─────┐
│BTCLR│     │     │     │     │     │       │     │     │     │     │     │PSCRN│
├─────┼─────┼─────┼─────┼─────┼─────┤       ├─────┼─────┼─────┼─────┼─────┼─────┤
│ WIN │ MAC │ BT2 │ BT3 │ BT4 │     │       │     │     │     │     │     │     │
├─────┼─────┼─────┼─────┼─────┼─────┤       ├─────┼─────┼─────┼─────┼─────┼─────┤
│EPOFF│     │     │     │     │     │       │     │     │     │     │     │HYPER│
└─────┴─────┴─────┼─────┼─────┼─────┤       ├─────┼─────┼─────┼─────┴─────┴─────┘
                  │LCTRL│     │SPACE│       │ENTER│     │RALT │
                  └─────┴─────┴─────┘       └─────┴─────┴─────┘
```

## Windows Layers (4-7)

Windows versions of the above layers with modified modifier keys:
- **Layer 4**: Windows Default (LCTRL instead of LGUI)
- **Layer 5**: Windows Lower
- **Layer 6**: Windows Raise
- **Layer 7**: Windows Config

## Special Features

### Hyper Key
The `&kp LC(LA(LGUI))` modifier function sends `Ctrl+Alt+Cmd` simultaneously, perfect for AeroSpace window management shortcuts without conflicts. This uses ZMK's modifier functions to properly maintain the key combination state.

### Bluetooth Management
- **BT CLR**: Clear all bluetooth pairings
- **WIN/MAC**: Switch between Windows and Mac modes with automatic bluetooth profile
- **BT0-4**: Select specific bluetooth profiles

### Media Controls
- Volume up/down/mute
- Play/pause, previous/next track
- Located on lower layer for easy access

### Power Management
- **EP OFF**: Turn off external power to save battery

## AeroSpace Integration

This keyboard works seamlessly with the provided AeroSpace configuration. The hyper key triggers window management commands:

- `Hyper + H/J/K/L`: Focus windows
- `Hyper + 1-9`: Switch workspaces  
- `Hyper + Shift + H/J/K/L`: Move windows
- `Hyper + Shift + 1-9`: Move windows to workspaces

## Usage

1. Flash the `corne.keymap` to your Corne keyboard
2. Install AeroSpace and use the provided configuration
3. Use the config layer to switch between Mac/Windows modes
4. Pair up to 5 bluetooth devices using BT0-BT4

## Layer Access

- **Lower**: Hold left thumb key (Layer 1/5)
- **Raise**: Hold right thumb key (Layer 2/6) 
- **Config**: Hold both Lower + Raise simultaneously (Layer 3/7)

## Customization

The keymap can be easily modified for personal preferences. Key areas for customization:

- Modifier key positions
- Symbol layer arrangements
- Media control placement
- Bluetooth profile assignments