# Super Mario Land 2 DX v1.8.1 FPGA Hardware Compatibility Patch

This patch fixes major compatibility problems between Super Mario Land 2 DX v1.8.1 and FPGA-based Game Boy hardware, especially the ModRetro Chromatic when used with certain flash cartridges.

<p align="center">
  <img src="docs/SML2DX_Before_After.gif" width="900">
</p>

<p align="center">
  <em>Original FPGA sprite corruption versus SML2DX_FPGA_v33 compatibility patch.</em>
</p>

This release improves compatibility with FPGA-based Game Boy hardware, specifically:
- ModRetro Chromatic
- InsideGadgets MBC5 FRAM Flash Cart
- Other FPGA Game Boy / flash cart configurations

The original Super Mario Land 2 DX hack may exhibit:
- severe sprite corruption
- invisible enemies/items
- overworld corruption
- gameplay instability
- DMA/OAM rendering issues

This patch restructures sprite DMA staging behavior to restore stable gameplay on affected hardware.

--------------------------------------------------
REQUIRED FILES
--------------------------------------------------

1. Base ROM:
   Super Mario Land 2 - 6 Golden Coins (UE) (V1.0)

2. Required Patch:
   Super Mario Land 2 DX v1.8.1

3. This Patch:
   SML2DX_FPGA_v33.ips

--------------------------------------------------
PATCHING ORDER
--------------------------------------------------

STEP 1:
Apply the official Super Mario Land 2 DX v1.8.1 patch to your legally obtained Super Mario Land 2 - 6 Golden Coins (UE) (V1.0) ROM.

STEP 2:
Apply SML2DX_FPGA_v33.ips to the patched Super Mario Land 2 DX v1.8.1 ROM.

--------------------------------------------------
FINAL RESULT
--------------------------------------------------

- Fixed sprite rendering
- Stable gameplay on Chromatic / FPGA hardware
- Restored enemy/item visibility
- Corrected overworld rendering

--------------------------------------------------
FEATURES
--------------------------------------------------

- Restores correct sprite rendering
- Fixes invisible enemies/items
- Fixes major overworld corruption
- Resolves major gameplay instability
- Preserves original gameplay behavior

--------------------------------------------------
KNOWN ISSUES
--------------------------------------------------

- Minor graphical corruption may appear during the ending credits sequence.
- Gameplay itself is stable and fully playable.

--------------------------------------------------
TECHNICAL NOTES
--------------------------------------------------

This patch modifies OAM DMA staging behavior using switchable WRAM bank staging to improve compatibility with FPGA-based Game Boy hardware implementations.

Public release builds use:
- WRAM Bank 3 staging
- DMA compatibility hook
- Preserved register state
- Restored SVBK handling

--------------------------------------------------
CREDITS
--------------------------------------------------

Shout out to toruzz for creating this beautiful ROM hack. This project was truly a labor of love, all driven by the desire to experience this amazing Super Mario Land 2 ROM hack on my own hardware. Thanks for breathing new life into a classic!

--------------------------------------------------
LEGAL
--------------------------------------------------

This package does NOT contain copyrighted Nintendo ROM data.

Only patch files are distributed.
