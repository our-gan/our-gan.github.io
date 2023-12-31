## OUR-GAN: One-shot Ultra-high-Resolution Generative Adversarial Networks - Demo

### Abstract
We propose a one-shot ultra-high-resolution (UHR) image synthesis framework, OUR-GAN, that generates non-repetitive 16K (16,384 x 8,644) images from a single training image and is trainable on a single GPU. OUR-GAN generates an initial image that is visually consistent and varied in shape at low resolution, then gradually increases the resolution by adding detail through super-resolution. Since OUR-GAN learns from a real UHR image, it can synthesize large-scale shapes with fine details while maintaining long-range coherence, which is difficult with conventional generative models that rely on the patch distribution learned from relatively small images. OUR-GAN can synthesize high-quality 4K images with only 8GB of GPU memory and 16K images with 12.5GB, as it synthesizes a UHR image part by part through seamless subregion-wise super-resolution, preventing discontinuity at the subregion boundary. Additionally, OUR-GAN improves visual coherence while maintaining diversity by applying vertical positional convolution. In experiments on the ST4K and RAISE datasets, OUR-GAN exhibited improved fidelity, visual coherency, and diversity compared with the baseline one-shot synthesis models. To the best of our knowledge, OUR-GAN is the first one-shot image synthesizer that generates non-repetitive UHR images on a single GPU.
<br>
<br>


### Notice
Loading UHR images may take time because the files are large. \
Therefore, we've posted downsampled versions of the images on this page for faster image loading. \
**Click on the images to access the full-size raw images.** 

The images may look distorted depending on the viewer since the image resolution is very high. \
So, please download samples, then evaluate the quality. \
Download all samples (including all sections) - [link](https://drive.google.com/drive/folders/1YUweukIe356ZwmrEqNmCu07N_WA5iWxJ?usp=sharing)\
<br>

### ST4K
To train and evaluate OUR-GAN, we built a new UHR image dataset, **S**cenery and **T**exture-**4K** (**ST4K**), consisting of high-quality 4K scenery and texture images. \
The ST4K dataset includes a total of 50 copyright-free images collected from the Internet with a minimum resolution of 4,096 × 2,160 pixels. \
Download ST4K - [link](https://drive.google.com/drive/folders/1-be9tPTWJ2swRTohv5dzKoZVYyAkTioW?usp=sharing)
<br>
<br>

### 1. 16K (16,384 x 10,912) image synthesized by OUR-GAN trained with a single 4K training image.
OUR-GAN can synthesize UHR image with higher resolution than that of the training image. \
The resolution of this image is 16K, whereas that of the training image is only 4K. \
OUR-GAN synthesize high-fidelity UHR images, preserving even fine details. \
Download Sec 1. samples - [link](https://drive.google.com/drive/folders/1-QNA3SqVN0kunzwI43x3DH49zCfXB1CH?usp=sharing)

<br>


<table>
<thead>
  <tr>
    <th><a href="https://drive.google.com/file/d/1KnUvKsokhtQTjrsukftC9rcJ8BIDfuN6/view?usp=sharing" target="_blank"><img src="/assets/images/downsampled/16k_stonehenge_downsampled.png" alt="16k_our"></a></th>
  </tr>
</thead>
<tbody>
 <tr>
    <td><div align=center><b>16K (16,384 x 10,912) image synthesized by OUR-GAN</b></div></td>
 </tr>
</tbody>
</table>


<table>
<thead>
  <tr>
    <th><a href="https://drive.google.com/file/d/1s1GiUl2gQnySx9iCVr2HAKPJzovs-eAI/view?usp=sharing" target="_blank"><img src="/assets/images/downsampled/4k_gt_stonehenge_downsampled.png" alt="4k_train"></a></th>
  </tr>
</thead>
<tbody>
 <tr>
    <td><div align=center><b>4K (4,096 x 2,728) training image</b></div></td>
 </tr>
</tbody>
</table>



<table>
<thead>
  <tr>
    <th><a href="https://drive.google.com/file/d/1OjRdTokqMlMkP4QptHvC9c47rj2w9JXb/view?usp=sharing" target="_blank"><img src="/assets/images/downsampled/8k_stonehenge_0_downsampled.png" alt="8k_our_0"></a></th>
    <th><a href="https://drive.google.com/file/d/1locTavVIL-gzAC5HRXuSIekqxnDeiO6z/view?usp=sharing" target="_blank"><img src="/assets/images/downsampled/8k_stonehenge_1_downsampled.png" alt="8k_our_1"></a></th>

  </tr>
</thead>
<tbody>
 <tr>
    <td colspan="2"><div align=center><b>8K (8,192 x 5,456) image synthesized by OUR-GAN</b></div></td>
 </tr>
</tbody>
</table>

<br>


### 2. Improving visual coherence
For one-shot image synthesis, achieving visual coherence while maintaining diversity is challenging. \
HP-VAE-GAN[1] synthesizes diverse images but fails to catch global coherence, as shown below. \
OUR-GAN, applied vertical coordinate convolution to HP-VAE-GAN, significantly improves the global coherence of patterns still generating diverse patterns.\
Download Sec 2. samples - [link](https://drive.google.com/drive/folders/1wCenETIRuku1CoVIhfSPqH3XStsRv7G0?usp=sharing)
<br>

<table>
<thead>
  <tr>
    <th><a href="https://drive.google.com/file/d/10GEWIesF0H_Dt3XDO7bmtErdAGq-nQCF/view?usp=sharing" target="_blank"><img src="assets/images/coherence/hp-vae-gan/1K_0_0.png" alt="coherence_hp_0_0"></a></th>
    <th><a href="https://drive.google.com/file/d/17xryGUAxk09uKfucEaX6OyeNYIKMZw8C/view?usp=sharing" target="_blank"><img src="assets/images/coherence/hp-vae-gan/1K_0_1.png" alt="coherence_hp_0_1"></a></th>
    <th><a href="https://drive.google.com/file/d/1by3AH8Nw3yxwb5rj0hAqiolEl7KoZlEY/view?usp=sharing" target="_blank"><img src="assets/images/coherence/our-gan/1K_0_0.png" alt="coherence_our_0_0"></a></th>
    <th><a href="https://drive.google.com/file/d/1OkcvaJhA-IwbnZwLk5Hp0I2kurb4ggcj/view?usp=sharing" target="_blank"><img src="assets/images/coherence/our-gan/1K_0_1.png" alt="coherence_our_0_1"></a></th>
   

 </tr>
</thead>
<tbody>
 <tr>
    <th><a href="https://drive.google.com/file/d/10UBBH9TJ-ZGcypkFggHXpITVOvBoPzE3/view?usp=sharing" target="_blank"><img src="assets/images/coherence/hp-vae-gan/1K_1_0.png" alt="coherence_hp_1_0"></a></th>
    <th><a href="https://drive.google.com/file/d/1Reb5MZF3Vm9seVGV_8wW0e3jkH2TS8P3/view?usp=sharing" target="_blank"><img src="assets/images/coherence/hp-vae-gan/1K_1_1.png" alt="coherence_hp_1_1"></a></th>
    <th><a href="https://drive.google.com/file/d/1ThvvpuyirB-ATfjSDerRzxheR3pL7Tr0/view?usp=sharing" target="_blank"><img src="assets/images/coherence/our-gan/1K_1_0.png" alt="coherence_our_1_0"></a></th>
    <th><a href="https://drive.google.com/file/d/1uUzcJcrrRWacpvXV03rRmqZjGrZkE5tK/view?usp=sharing" target="_blank"><img src="assets/images/coherence/our-gan/1K_1_1.png" alt="coherence_our_1_1"></a></th>
 </tr>
 <tr>
    <td colspan="2"><div align=center><b>HP-VAE-GAN</b></div></td>
    <td colspan="2"><div align=center><b>OUR-GAN (proposed) <br> [HP-VAE-GAN + <br> Vertical coordinate convolution] </b></div></td>
 </tr>
</tbody>
</table>



<br>

### 3. Large-scale shape generation 

For UHR image synthesis, models that learns from small patch images like InfinityGAN[2] are hard to synthesize large-scale shapes.\
But, OUR-GAN can synthesize globally coherent large-scale objects such as buildings.\
You can download full-size InfinityGAN samples in the [InfinityGAN project page](https://hubert0527.github.io/infinityGAN/).\
Download Sec 3. samples - [link](https://drive.google.com/drive/folders/1a4GeqOu2rET6ys45R_dreqmWVVz9Hl3A?usp=sharing)\
<br>


<table>
<thead>
  <tr>
    <th><a href="https://drive.google.com/file/d/1gCqqCaIP_yFMkt5zrreh8smXB-NLlTlQ/view?usp=sharing" target="_blank"><img src="/assets/images/large/our_1k_0.png" alt="large_our_0"></a></th>
   <th><a href="https://drive.google.com/file/d/1rYitkLTsLlINzruv1m_I9565SxOPO6tP/view?usp=sharing" target="_blank"><img src="/assets/images/large/our_1k_1.png" alt="large_our_1"></a></th>
 </tr>
</thead>
<tbody>
  <tr>
    <td colspan="2"><div align=center><b>OUR-GAN (proposed)</b></div></td>
  </tr>
</tbody>
</table>

<br>



<table>
<thead>
  <tr>
    <th><img src="assets/images/large/inf_1k_0.png" alt="large_inf_0"></th>
    <th><img src="assets/images/large/inf_1k_1.png" alt="large_inf_1"></th>
    <th><img src="assets/images/large/inf_1k_2.png" alt="large_inf_2"></th>
 </tr>
</thead>
<tbody>
  <tr>
    <td colspan="3"><div align=center><b>InfinityGAN</b></div></td>
  </tr>
</tbody>
</table>



<br>

### 4. 16K (16,384 x 10,912) image synthesized by OUR-GAN trained with a single 16K training image.
OUR-GAN-16K can synthesize 16K images from a single 16K training image with a single GPU. \
We further increased the resolution of OUR-GAN by applying an additional subregion-wise super-resolution step, referred to as OUR-GAN-16K. \
OUR-GAN-16K successfully synthesized non-repetitive high-fidelity 16K images maintaining both visual coherence and fine details. \
% The size of the biggest island at the rigth of the image is approximately 7,083 × 4,388. \
Download Sec 4. samples - [island](https://drive.google.com/drive/folders/1GSX8vqHFDmKvvXODMl5YtmIdEOZd51I_?usp=sharing), [forest](https://drive.google.com/drive/folders/1OSTy3EBKcA9lWJr4HGa4JmhjPGKd9Q9W?usp=sharing)



<br>


<table>
<thead>
  <tr>
    <th><a href="https://drive.google.com/file/d/1M9Vg5MbhA7ieT7MBwVocEJciOwbLjKxi/view?usp=share_link" target="_blank"><img src="/assets/images/downsampled/our_island_16K_1_downsampled.png" alt="16k_our_island"></a></th>
  </tr>
</thead>
<tbody>
 <tr>
    <td><div align=center><b>16K (16,384 x 9,152) island image synthesized by OUR-GAN</b></div></td>
 </tr>
</tbody>
</table>


<table>
<thead>
  <tr>
    <th><a href="https://drive.google.com/file/d/1Dl-Vn00yzv4YCcNzzKgmw_02QyNgqsrI/view?usp=share_link" target="_blank"><img src="/assets/images/downsampled/16K_island_GT_downsampled.png" alt="16k_train_island"></a></th>
  </tr>
</thead>
<tbody>
 <tr>
    <td><div align=center><b>16K (16,329 x 9,185) island training image</b></div></td>
 </tr>
</tbody>
</table>

<br>


<table>
<thead>
  <tr>
    <th><a href="https://drive.google.com/file/d/1MISvmIiM2SAlzpWghHrGcos2NyRwoxES/view?usp=share_link" target="_blank"><img src="/assets/images/downsampled/our_forest_16K_0_downsampled.png" alt="16k_our_forest"></a></th>
  </tr>
</thead>
<tbody>
 <tr>
    <td><div align=center><b>16K (16,384 x 10,880) forest image synthesized by OUR-GAN</b></div></td>
 </tr>
</tbody>
</table>


<table>
<thead>
  <tr>
    <th><a href="https://drive.google.com/file/d/14lJWmP6qo8wBtiwtvBAMcbqJJNvGqitX/view?usp=share_link" target="_blank"><img src="/assets/images/downsampled/16K_forest_GT_downsampled.png" alt="16k_train_forest"></a></th>
  </tr>
</thead>
<tbody>
 <tr>
    <td><div align=center><b>16K (16,384 x 10,880) forest training image</b></div></td>
 </tr>
</tbody>
</table>

### References

<b>[1] Shir Gur, Sagie Benaim, and Lior Wolf. Hierarchical patch vae-gan: Generating diverse videos from a single
sample. In H. Larochelle, M. Ranzato, R. Hadsell, M. F. Balcan, and H. Lin, editors, Advances in Neural
Information Processing Systems, volume 33, pages 16761–16772. Curran Associates, Inc., 2020.
</b>

<b>[2] Chieh Hubert Lin, Yen-Chi Cheng, Hsin-Ying Lee, Sergey Tulyakov, and Ming-Hsuan Yang. InfinityGAN:
Towards infinite-pixel image synthesis. In International Conference on Learning Representations, 2022.
</b>


<!-- <br>

### 4K scenery images synthesized by OUR-GAN
OUR-GAN successfully synthesized high-quality non-repetitive images with visually coherent shapes with fine details.

| [![4K_scenery_0_0](/assets/images/downsampled/11000_0_downsampled.png)](/assets/images/4K/11000_0.png) | [![4K_scenery_0_1](/assets/images/downsampled/11000_17_downsampled.png)](/assets/images/4K/11000_17.png) |
|---|---|
| [![4K_scenery_1_0](/assets/images/downsampled/11015_17_downsampled.png)](/assets/images/4K/11015_17.png) | [![4K_scenery_1_1](/assets/images/downsampled/11015_28_downsampled.png)](/assets/images/4K/11015_28.png) |
| [![4K_scenery_2_0](/assets/images/downsampled/11021_0_downsampled.png)](/assets/images/4K/11021_0.png) | [![4K_scenery_2_1](/assets/images/downsampled/11021_18_downsampled.png)](/assets/images/4K/11021_18.png) |
| [![4K_scenery_3_0](/assets/images/downsampled/11013_44_downsampled.png)](/assets/images/4K/11013_44.png) | [![4K_scenery_3_1](/assets/images/downsampled/11013_46_downsampled.png)](/assets/images/4K/11013_46.png) |

<br>

### 4K texture images synthesized by OUR-GAN
OUR-GAN successfully synthesized high-quality texture images with diverse patterns.

| [![4K_texture_0_0](/assets/images/downsampled/21000_52_downsampled.png)](/assets/images/4K/21000_52.png) | [![4K_texture_0_1](/assets/images/downsampled/21000_66_downsampled.png)](/assets/images/4K/21000_66.png) |
|---|---|
| [![4K_texture_1_0](/assets/images/downsampled/21022_52_downsampled.png)](/assets/images/4K/21022_52.png) | [![4K_texture_1_1](/assets/images/downsampled/21022_83_downsampled.png)](/assets/images/4K/21022_83.png) | -->

<!-- You can use the [editor on GitHub](https://github.com/anonymous-62348/anonymous-62348.github.io/edit/main/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/anonymous-62348/anonymous-62348.github.io/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
 -->
