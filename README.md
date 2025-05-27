# PolNet-CR: Spatial-channel collaborative interaction network for PolSAR incremental information-assisted optical satellite imagery cloud removal
## Jiangong Xu, Xiaoyu Yu, Jun Pan*, Liwen Cao, Mi Wang
![p1](https://github.com/user-attachments/assets/7643014c-698d-4173-bb91-203a4492eaaa)

## Dataset Overview
In this study, we propose a novel method to address the critical challenge of cloud contamination in optical remote sensing imagery. Our method, PolNet-CR, leverages polarimetric synthetic aperture radar (PolSAR) data to aid in the removal of clouds from optical images. This approach not only addresses domain gaps between the imaging mechanisms of PolSAR and optical data but also efficiently reduces the impact of speckle noise inherent in PolSAR data through a multi-modal feature interaction network.
We also developed the first public dataset, LuojiaSET-PolCR, which explicitly introduces PolSAR polarimetric scattering characteristics into cloud-contaminated optical satellite image reconstruction to advance research in this field.The LuojiaSET-PolCR dataset encompasses 45 non-overlapping ROIs. Each ROI has an average size of approximately 10980×10980 pixels, which, with a ground sampling distance of 10 meters, corresponds to a ground coverage area of 109.8×109.8 km. To make the acquired imagery more suitable for input into networks based on deep learning methods, a sliding window of sensor-specific dimensions is used to divide each ROI into smaller patches of 256×256 pixels, with a stride of 64 pixels. This means there is a 25% overlap between adjacent patches. 
![p2](https://github.com/user-attachments/assets/c89fb398-8c96-4fc0-b59d-306342bbe7a0)

## Data Structure
We divide all the patches into three subdatasets, namely, training set, validation set, testing, and write the division in a .csv file as:
```
1	Sen-1_auxiliary-Alpha	Sen-1_auxiliary-Anisotropy	Sen-1_auxiliary-C11	Sen-1_auxiliary-C12_imag	Sen-1_auxiliary-C12_real	Sen-1_auxiliary-C22	Sen-1_auxiliary-Entropy	Sen-2_cloudy	Sen-2_reference	ROIs_40_p_4790.tif
2	Sen-1_auxiliary-Alpha	Sen-1_auxiliary-Anisotropy	Sen-1_auxiliary-C11	Sen-1_auxiliary-C12_imag	Sen-1_auxiliary-C12_real	Sen-1_auxiliary-C22	Sen-1_auxiliary-Entropy	Sen-2_cloudy	Sen-2_reference	ROIs_09_p_3372.tif
3	Sen-1_auxiliary-Alpha	Sen-1_auxiliary-Anisotropy	Sen-1_auxiliary-C11	Sen-1_auxiliary-C12_imag	Sen-1_auxiliary-C12_real	Sen-1_auxiliary-C22	Sen-1_auxiliary-Entropy	Sen-2_cloudy	Sen-2_reference	ROIs_37_p_0903.tif
```
Here label is a number and 1 represents training set, 2 represents validation set and 3 represents testing set. 
Then build the file structure in your computer as the folder dataset shown.
```
./
+-- LuojiaSET-PolCR
    +--	Sen-1_auxiliary
        +-- Alpha
        |   +-- patch_ROIs_01_name.tif
        |   +-- ...
        +-- Anisotropy
        |   +-- patch_ROIs_01_name.tif
        |   +-- ...
        +-- C11
        |   +-- patch_ROIs_01_name.tif
        |   +-- ...
        +-- C12_imag
        |   +-- patch_ROIs_01_name.tif
        |   +-- ...
        +-- C12_real
        |   +-- patch_ROIs_01_name.tif
        |   +-- ...
        +-- C22
        |   +-- patch_ROIs_01_name.tif
        |   +-- ...
        +-- Entropy
        |   +-- patch_ROIs_01_name.tif
        |   +-- ...
     +-- Sen-2_cloudy
        |   +-- patch_ROIs_01_name.tif
        |   +-- ...
     +-- Sen-2_reference
        |   +-- patch_ROIs_01_name.tif
        |   +-- ...
```

## Instructions
Links to **[here](https://www.wenjuan.com/s/uQVZnag/#)** download the data.

If you have any questions about this work please concat me. E-mail: panjun1215@whu.edu.cn, dd_xjg@whu.edu.cn

## License and Citation
```
Copyright WHU-LIESMARS. All Rights Reserved.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
If you find our work and datasets useful for your research, please cite our paper.
```
@article{xxx,
  title={PolNet-CR: Spatial-channel collaborative interaction network for PolSAR incremental information-assisted optical satellite imagery cloud removal},
  author={Jiangong Xu, Xiaoyu Yu, Jun Pan*, Liwen Cao, Mi Wang},
  journal={{Information Fusion}},
  year={xxxx}
}
```
