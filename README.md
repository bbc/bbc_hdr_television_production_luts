# BBC HDR Television Production LUTS

## Description

Conversion LUTs are available for the following video transformations.  

| LUT number | Description |
| --- | --- |
|  1 | BT.2100 PQ 1000 cd/m<sup>2</sup> to BT.2100 HLG  |
|  2 | BT.2100 PQ 4000 cd/m<sup>2</sup> to BT.2100 HLG  |
|  3 | BT.709 to BT.2100 HLG direct-mapping (display-light) |
|  4 | BT.709 to BT.2100 HLG direct-mapping (scene-light) |
|  5 | BT.709 to BT.2100 HLG up-mapping (display-light)  |
|  6 | BT.709 to BT.2100 HLG up-mapping (scene-light)  | 
|  7 | BT.2100 HLG to BT.2100 PQ 1000 cd/m<sup>2</sup>  |
|  8 | BT.2100 HLG to BT.709 CAM-based down-mapping (display-light)  |
|  9 | BT.2100 HLG to BT.709 down-mapping (display-light) with SDR super-whites  |
|  10 | S-Log3 (100%) to BT.2100 HLG (Scene-Light)  |
|  11 | S-Log3 (200%) to BT.2100 HLG (Scene-Light)  |
|  12 | BT.2100 HLG to BT.709 down-mapping (scene-light)   |
|  13 | Test LUTs  |
|  14 | PQ P3D65 1000 cd/m<sup>2</sup> to BT.2100 HLG  |
|  15 | BT.2100 HLG to PQ P3D65 1000 cd/m<sup>2</sup>  |
|  16 | BT.2100 HLG to X'Y'Z' PQ at 108 cd/m<sup>2</sup> (used for cinema displays)  |
|  17 | BT.2020 to BT.2100 HLG direct-mapping (display-light)  |
|  18 | BT.2020 to BT.2100 HLG up-mapping (display-light)  |
|  19 | BT.2100 HLG traditional camera look-LUT – increases saturation and hue shift  |
|  20 | sRGB to BT.2100 HLG direct-mapping (display-light)  |
|  21 | BT.2100 HLG to SDR BT.2020 (Wide Colour Gamut) down-mapping (display-light)  |
|  22 | BT.709 SDR camera shading LUT. Combines LUT 4 followed by LUT 9 into a single LUT  |

### BT.709 Strict Implementation

During early productions, it was found that some camera manufacturers strictly implemented BT.709 whilst others approximated BT.709 using a square root function.  Strict and square root versions of scene-light conversions from BT.709 are provided.

### Incorrect Matrices

Early hardware LUT video processors assumed that both the input and output matrices (which are used to convert the signal to and from R'G'B') were ITU-R BT.709.  LUT files are provided with a compensation for incorrect matrices.  These should only be used with a device that uses the incorrect matrices - this is usuually obvious because there is no user interface to choose or indication of the matrices in use.

### Narrow-range vs Full-range

Versions of each CUBE LUT are provided for processing of narrow-range input and output, full-range input and output, and for situations where a conversion between the two is required (e.g. converting a theatrical release for insertion in an ITU-R BT.2100 HLG programme).

The output of the LUTs which are designed for use with narrow-range output signals will exhibit excursions in to the below-nominal-black and above-nominal-white regions.

### LUT Formats

At present, only Adobe CUBE format LUTs are available.

## Documentation

## Licensing

These LUTs are licensed under the Apache 2.0 licence. A copy of the licence is visible at [LICENSE](https://www.apache.org/licenses/LICENSE-2.0)

## Repository Update History

| Date | Update Description | LUTS Affected |
| --- | --- | --- |
| Sept 2026 | Moved LUT licensing model to Apache 2.0 and incremented version number to 1.8.  No changes to LUT functionality compared to version 1.7. | CUBE LUTs v1.8 |