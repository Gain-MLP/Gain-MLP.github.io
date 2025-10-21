# Gain-MLP: Improving HDR Gain Map Encoding via a Lightweight MLP, ICCV 2025
Trevor D. Canham <sup>1</sup>, SaiKiran Tedla <sup>1</sup>, Michael J. Murdoch <sup>2</sup>, Michael S. Brown <sup>1</sup>

<sup>1</sup>York University  <sup>2</sup>Rochester Institute of Technology

[Paper](https://arxiv.org/abs/2503.11883), [Video](https://www.youtube.com/watch?v=u7OTgVeZur4), [Dataset](https://www.dropbox.com/scl/fo/uskvi9evls91uax00f4cx/AOm20-zZSq_08JHuuq0ewBg?rlkey=cdgufhmh3cvm4t1ifh5vwx5or&st=vl5p7hm7&dl=0), [code](https://github.com/trevorcanham/Gain-MLP.git)

![](https://raw.githubusercontent.com/Gain-MLP/Gain-MLP.github.io/refs/heads/main/teaserICCV.png)

Gain maps are a new encoding paradigm which allow images mastered for different displays (e.g., standard vs. high dynamic range) to be embedded together. While the new standard  for this encoding scheme ([ISO 21496](https://www.iso.org/standard/86775.html)) recommends using traditional compression techniques (JPEG, HEIC etc.) these methods suffer from blocking and quantization artifacts. We show in this work that by replacing this compression step with an implicit neural representation (INR) based strategy, these artifacts can be avoided while reducing bit rates.

## Tone Mapping

![](https://raw.githubusercontent.com/Gain-MLP/Gain-MLP.github.io/refs/heads/main/tmICCV.png)

New displays are capable of showing brighter and more vivid colors, so images must be encoded and edited differently to take advantage of the extended dynamic range. This editing generally takes the form of global non-linear changes to pixel intensity but can also involve local processes like frequency filters and masking.

## Gain Maps

![](https://raw.githubusercontent.com/Gain-MLP/Gain-MLP.github.io/refs/heads/main/overviewICCV.png)

Gain maps are computed by dividing the High Dynamic Range (HDR) image version by its SDR counterpart, represented in the HDR display space. The gain values are normalized and encoded with traditional compression techniques.

## Proposed Method

![](https://raw.githubusercontent.com/Gain-MLP/Gain-MLP.github.io/refs/heads/main/architectureICCV.png)

### Gamma maps 
Our prior work demonstrated that the use of exponential residuals resulted in better reconstruction quality than the conventional gain map workflow. Here, we show this result holds for MLP based encoding techniques.

### Gain-MLP
In this work, we show that implicit neural representations (INR) benefit from base/residual frameworks like gain maps. By passing the SDR image as input, the networks can be quickly optimized to achieve high reconstruction quality.

### Synthetic Initialization images 
We also demonstrate in this work that INR representations can be initialized with synthetic noise images which cover the display gamut and are filtered to achieve 1/𝑓^2 power spectrum properties, consistent with natural image statistics.

## Experiments

Employing these three findings, the proposed MLP-based gain map encoding methodology outperforms both traditional and INR based encoding techniques and has robust rate-distortion performance.

![](https://raw.githubusercontent.com/Gain-MLP/Gain-MLP.github.io/refs/heads/main/table1iccv.png)

![](https://raw.githubusercontent.com/Gain-MLP/Gain-MLP.github.io/refs/heads/main/rdICCV.png)

![](https://github.com/Gain-MLP/Gain-MLP.github.io/blob/main/resultsICCV.png?raw=true)

Here the results are demonstrated in terms of \Delta E<sub>00</sub>

![](https://github.com/Gain-MLP/Gain-MLP.github.io/blob/main/resultsDEiccv.png?raw=true)


