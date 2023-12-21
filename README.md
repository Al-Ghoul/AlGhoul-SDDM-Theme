# Intro
This theme is based on [Sugar Candy](https://framagit.org/MarianArlt/sddm-sugar-candy) by MarianArlt; refer to [NixOS-Conf/alghoul-sddm-theme.nix](https://github.com/Al-Ghoul/NixOS-Conf/blob/main/modules/nix-os/alghoul-sddm-theme.nix) for an example, you'll also need to set the following attr as follows
```bash
    services.xserver.displayManager.sddm.theme = "AlGhoul-SDDM-Theme";
```
and call the package in ur *configration.nix* or *flake.nix* as follows:
```bash
    environment.systemPackages = with pkgs; [
      pkgs.libsForQt5.qt5.qtgraphicaleffects # This lib is a REQUIREMENT for this theme.
      (callPackage ./modules/nix-os/alghoul-sddm-theme.nix {})
    ];
```

## Preview
![A preview of the theme](/preview.png)
