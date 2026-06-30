# sc3tools

A CLI tool for extracting and modifying text in .scx and .msb scripts found in visual novels based on MAGES. engine. It's meant to be a replacement for the old, overly complicated tool which had the same name and was part of the now-abandoned [SciAdv.Net project](https://github.com/CommitteeOfZero/SciAdv.Net).

## Supported games

- STEINS;GATE (Steam)
- STEINS;GATE ELITE (Steam & Switch)
- CHAOS;HEAD Love Chu☆Chu! (PS3 & Impacto)
- ROBOTICS;NOTES ELITE
- STEINS;GATE: Linear Bounded Phenogram (Steam)
- CHAOS;CHILD (Steam & GOG)
- STEINS;GATE 0 (Steam)
- CHAOS;CHILD Love Chu☆Chu!! (PS4 & Impacto)
- ROBOTICS;NOTES DaSH
- 11eyes CrossOver (Xbox 360)

## Usage

Run `./sc3tools` with no arguments to see the list of the avaliable commands, as well as the list of the supported games and their aliases (such as `sg0` for Steins;Gate 0).

Run `./sc3tools help <command>` to see the help message for a specific command.

Here's an example of how you can extract text from the Robotics;Notes scripts:

`./sc3tools extract-text C:/src/CoZ/rne-msb/*.msb rn`

The output files will be placed in a subfolder named `txt` (in this case, `C:/src/CoZ/rne-msb/txt`).

## Compilation
Install the Rust toolchain for Windows from [rustup.rs](https://rustup.rs).

Clone the repository using Git: `git clone https://github.com/ThePlayer14/sc3tools_mod.git`

Navigate to the cloned folder `sc3tools_mod` and open the context menu / righclick menu in File Explorer and click on "Open in Terminal"

From this point you can run `cargo build` to build a "dev" (debug) release, or run `cargo build --release` to make a "release" build.
 
## Known issues
* This tool currently does not handle color setting in dialogue correctly (such as in the case of 11eyes CrossOver), and it will leave a truncated script if that is happened.

  Example of the telltale sign:
```
  Processing "D:\\script\\SC000.scr"... 
  Error: SC000.scr, line 73: expected more input.
```
