ares, a cross-platform, multi-system emulator
=============================================

ares runs games for a variety of classic computers and game consoles
on modern PCs. It currently emulates the following systems: Famicom, Famicom
Disk System, Super Famicom, Super Game Boy, Game Boy, Game Boy Color, Game Boy
Advance, Game Boy Player, SG-1000, SC-3000, Master System, Game Gear, Mega
Drive, Mega CD, PC Engine, SuperGrafx, MSX, MSX2, ColecoVision, Neo Geo Pocket,
Neo Geo Pocket Color, WonderSwan, WonderSwan Color, SwanCrystal, Pocket
Challenge V2.

ares currently runs on Windows, Linux, and FreeBSD, with an experimental port to
macOS.

History
-------

In 2004, a programmer calling themselves byuu had been working on fan
translations of Super Famicom games. They became frustrated by inaccuracies
in Super Famicom emulators of the time, and began working on their own emulator
designed for hardware accuracy and homebrew development, rather than just
running commercially-published games. The first versions of byuu's
SNES/Super Famicom emulator, *bsnes*, were released in late 2004.

bsnes quickly achieved top-tier emulation of the SNES base unit, and slowly
began adding support for more esoteric hardware.

  - In 2009, bsnes v046 became the first SNES emulator to properly support the
    Super Game Boy, adding a Game Boy emulation core based on the *gambatte*
    emulator.
  - In 2010, bsnes v060 added support for the fictional MSU-1 co-processor,
    allowing the creation of SNES games with streaming CD-quality audio and
    full-motion video. The MSU-1 would later be implemented in an FPGA by Ikari,
    allowing MSU-1 games to be played on original hardware.
  - Also in 2010, bsnes v073 became the first SNES emulator to support low-level
    emulation of the DSP co-processors included with some of the most popular
    SNES games. This fixed a number of emulation bugs in those games, and was
    the first time *SD Gundam GX* was playable at all.
  - In 2011, bsnes v074 replaced gambatte-based Super Game Boy emulation with
    a new Game Boy emulation core called bgameboy.
  - Also in 2011, bsnes v083 added NES emulation.
  - In 2012, bsnes v087 became the first SNES emulator to support the ST018
    co-processor used in *Hayazashi Nidan Morita Shougi 2*, which turned out
    to be an ARM-based CPU.
  - Also in 2012, bsnes v088 added support for Game Boy Advance emulation,
    since it already supported Game Boy hardware and an ARM-based CPU.
  - With support for four different consoles (plus the temporary addition of
    *dasShiny*, a Nintendo DS emulator), the name "bsnes" was increasingly
    inaccurate, and at version v091 *bsnes* was renamed to *higan*.
  - In 2016, higan v098 added support for the WonderSwan and WonderSwan Color
    handheld consoles.
  - Also in 2016, higan v099 removed the "balanced" and "performance" versions
    of the SNES emulation core, leaving only the "accuracy" core.
  - In 2017, higan v102 added basic emulation of the Sega Master System,
    Sega Game Gear, Sega Mega Drive (Genesis), and NEC PC Engine
    (TurboGrafx-16).
  - In 2019, byuu had a new idea for efficient SNES emulation. It wouldn't be
    appropriate for the accuracy-oriented higan (and besides, higan's
    user-interface was getting very complex), so byuu decided to resurrect
    the "bsnes" name for a standalone SNES-focussed emulator. This new bsnes
    was based on higan v106, but with a fresh new user-interface that included
    many of the quality-of-life features dropped from previous higan versions
    because they could not be implemented consistently for every core.
  - In late 2019, higan v107 added support for the ColecoVision, Coleco Adam,
    the Mega CD add-on for the Sega Mega Drive, the Neo Geo Pocket, and the Neo
    Geo Pocket Color.
  - In early 2020, buoyed by the popularity of the new bsnes and tired of the
    complexity of the higan user-interface, byuu created a new simplified
    interface. As he was growing tired of the name "byuu" (Japanese for "to make
    a mistake"), he named the new interface "byuu" and took the new name Near
    for himself.
  - In March 2020, after fifteen years of continuous development, Near decided
    to retire from the emulation scene, and released higan v110, as his final
    version for the community to maintain and build on.
  - In April 2020, the global pandemic caused Near to be confined to his house,
    and to keep himself occupied he resumed his emulation work as a hobby.
    To distinguish his work from the community around higan, he renamed it
    "ares".
  - In June 2020, Near made the first public release of ares, v114, under a
    Creative Commons Non-Commercial licence. It added support for the PC Engine
    CD, and CPU-only emulation for the Nintendo 64.
  - In July 2020, Near decided to retire for real, and released ares v115.

Name changes
------------

Ares' components have been renamed numerous times over the years. Here's a quick
guide:

| Component              | Current name | Previous names             |
|------------------------|--------------|----------------------------|
| Whole project          | ares         | higan, bsnes               |
| Advanced interface     | lucia        | higan                      |
| Simple interface       | luna         | byuu                       |
| Game analyzer/importer | mia          | icarus, purify, snespurify |
