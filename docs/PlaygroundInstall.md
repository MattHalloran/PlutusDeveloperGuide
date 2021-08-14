# Plutus Playground Installation
The Plutus Playground is required to complete the Plutus Pioneers Program.

For the most up-to-date information, see the [official Plutus repo README](https://github.com/input-output-hk/plutus)

## Instructions  
1. First, Nix must be set up. In a terminal, enter `curl -L https://nixos.org/nix/install | sh`  
    Note: To remove Nix, simply enter `rm -rf /nix`
2. Open /etc/nix/nix.conf and add the following lines:  
    ```
    substituters        = https://hydra.iohk.io https://iohk.cachix.org https://cache.nixos.org/
    trusted-public-keys = hydra.iohk.io:f/Ea+s+dFdN+3Y/G+FDgSq+a5NEWhJGzdjvKNGv0/EQ= iohk.cachix.org-1:DpRUyj7h7V830dp/i6Nti+NEO2/nhblbov/8MW7Rqoo= cache.nixos.org-1:6NCHdD59X431o0gWypbMrAURkbJ16ZPMQFGspcDShjY=
    ```
    Note: If using MacOS, also add the following lines:
    ```
    sandbox = true
    extra-sandbox-paths = /System/Library/Frameworks /System/Library/PrivateFrameworks /usr/lib /private/tmp /private/var/tmp /usr/bin/env
    ```
3. Next, Plutus must be set up. In a terminal, navigate to where you want the Plutus code to live. Then enter `git clone https://github.com/input-output-hk/plutus`  
    Note: If you already have Plutus downloaded, make sure to git pull the latest changes.
4. In the Plutus directory, enter `nix build -f default.nix plutus.haskell.packages.plutus-core.components.library`