# Pure Arch

## Spirit of the repository
*Pure Arch Linux is Arch Linux*

1. Pure Arch philosophy: follow Arch defaults where feasible
2. Pure arch packages (no AUR; no URLs or URIs)
3. Pure archiso (runs off base arch iso with no modifications)
4. Pure bash
5. Bleeding edge philosophy: Priority support for modern hardware using simple configurations. Support for legacy hardware and configurations takes a back seat to reducing system complexity. For example, this tool only supports systems that support UEFI firmware and gpt disks.

## Usage Instructions

### Full recovery
*wipes a single drive on a system to replace with a pure-arch setup*

1. boot archiso
2. git clone this repository
3. run `gen_settings.bash`
4. populate the target-device file
4. run `full_recovery.bash`

### Other scripts

TODO

## System Documentation

- Every script under `recovery` is executable by users, and should load the Pure Arch bash library with the following code:
	`source $PWD/rec-script-preamble.bash`
- Every script under `recovery` is executable by users, and should have the execute bit set in the file system.
- The basic system configuration leaves the user with two fully separate OS, called `arch` and `recovery`. `arch` is the default boot environment. The `recovery` boot environment has a copy of this repository under $HOME/pure-arch and a copy of the recovery working directory under $HOME/recovery-files

`
