# Gain-MLP: Improving HDR Gain Map Encoding via a Lightweight MLP, ICCV 2025
Trevor D. Canham <sup>1</sup>, SaiKiran Tedla <sup>1</sup>, Michael J. Murdoch <sup>2</sup>, Michael S. Brown <sup>1</sup>

<sup>1</sup>York University  <sup>2</sup>Rochester Institute of Technology

[Paper](https://arxiv.org/abs/2503.11883), [Video](https://www.youtube.com/watch?v=u7OTgVeZur4), [Dataset](https://www.dropbox.com/scl/fo/uskvi9evls91uax00f4cx/AOm20-zZSq_08JHuuq0ewBg?rlkey=cdgufhmh3cvm4t1ifh5vwx5or&st=vl5p7hm7&dl=0), [code](https://github.com/trevorcanham/Gain-MLP.git)

Gain maps are a new encoding paradigm which allow images mastered for different displays (e.g., standard vs. high dynamic range) to be embedded together. While the new standard  for this encoding scheme ([ISO 21496](https://www.iso.org/standard/86775.html)) recommends using traditional compression techniques (JPEG, HEIC etc.) these methods suffer from blocking and quantization artifacts. We show in this work that by replacing this compression step with an implicit neural representation (INR) based strategy, these artifacts can be avoided while reducing bit rates.

![](https://raw.githubusercontent.com/trevorcanham/Gain-MLP/refs/heads/main/teaser_gh.png)

New displays are capable of showing brighter and more vivid colors, so images must be encoded and edited differently to take advantage of the extended dynamic range. This editing generally takes the form of global non-linear changes to pixel intensity but can also involve local processes like frequency filters and masking.

![](https://raw.githubusercontent.com/Gain-MLP/Gain-MLP.github.io/refs/heads/main/tmICCV.png)

![](https://raw.githubusercontent.com/Gain-MLP/Gain-MLP.github.io/refs/heads/main/overviewICCV.png)

![](https://raw.githubusercontent.com/Gain-MLP/Gain-MLP.github.io/refs/heads/main/architectureICCV.png)

![](https://github.com/Gain-MLP/Gain-MLP.github.io/blob/main/resultsICCV.png?raw=true)


