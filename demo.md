---
title: Monokai theme demo
version: 1.0.0
theme: monokai
header: Monokai Classic Marp theme
footer: brayevalerien
paginate: true
marp: true
math: mathjax
---

# Monokai Classic

A dark theme for [Marp](https://marp.app) inspired by the Monokai Classic theme.

Adapted from the Dracula theme by *Daniel Nicolas Gisolfi*.

![bg left](./abstract.png)

---

# Equations

There is support for inline equations which allow to define $z \hookrightarrow \mathcal{N}(0, \mathbf{I})$, and use it in a follow up display equation like the following.

$$
\begin{align}
x_t &= \sqrt{\bar{\alpha}_t} x_0 + \sqrt{1 - \bar{\alpha}_t} z \\
x_{t-1} &= \frac{1}{\sqrt{\alpha_t}} \left( x_t - \frac{1 - \alpha_t}{\sqrt{1 - \bar{\alpha}_t}} z \right) + \sigma_t \epsilon
\end{align}
$$
Note that this document uses `mathjax` but `katex` can be used too, changing the properties at the top of the source code.

---

# Tables

Tables are inspired by the clean $\LaTeX$ tables.

| Country | Industry      | Tool             | Daily active users |
| ------- | ------------- | ---------------- | ------------------ |
| USA     | Technology    | ChatGPT          | 2461               |
| France  | Manufacturing | Midjourney       | 8496               |
| UK      | Agriculture   | Stable Diffusion | 1124               |
| Brazil  | Agriculture   | Midjourney       | 3267a              |
| USA     | Healthcare    | Bard             | 4265               |
| China   | Retail        | Midjourney       | 613                |

*[source](https://www.kaggle.com/datasets/tfisthis/global-ai-tool-adoption-across-industries)*

---

# Figures

Images are resized to fit the page, but it still isn't optimal. Add more lines here to see how the image can go out of the slide.

![Example image](https://fastly.picsum.photos/id/328/1280/720.jpg?hmac=LsGKysj6LwtqeYLwAhHbEMgnyZkDkpprxhH1GxRNnIQ)

---

# Multiple figures

Use html and css as a hacky way to get multiple figures next to each others.

<style>
.noborder tbody tr:last-child td {
    border-bottom: none !important;
}
</style>
<table class="noborder" style="border-collapse: collapse; width: 100%; border: none;">
  <tr>
    <td style="border: none; padding: 0; margin: 0;"><img src="https://fastly.picsum.photos/id/743/1280/720.jpg?hmac=6q5cVCPLG7Z2UT22COPlJA63uPQdVyZODV_b-qUIKic"/></td>
    <td style="border: none; padding: 0; margin: 0;"><img src="https://fastly.picsum.photos/id/634/1280/720.jpg?hmac=s-kfmL1yZuJUYra7m42xOhnm5nDitQpvy810fXn8cSk"/></td>
  </tr>
</table>

This isn't the best solution, if you have anything better please [open an issue](https://github.com/brayevalerien/Marp-monokai-classic/**issues**).

---

# Blockquotes

As a wise man (Einstein) once said,
> Pure mathematics is, in its way, the poetry of logical ideas.

Multi-line quotes are supported too:
> I wonder where I'll float next?
> 
> — The barrel boy

---

# Lists
## Unordered
Unordered lists with nesting are supported.
- CNNs
  - Convolution layers
    - Edge detection filters
    - Feature maps
  - Pooling layers
    - Max pooling
    - Average pooling
- Data augmentation
  - Rotation
  - Flipping

---

## Ordered
Ordered lists with nesting are supported too.
1. Preprocessing
   1. Normalization
   2. Augmentation
2. Feature Extraction
   1. Edge Detection
   2. Texture Analysis
3. Models
   1. CNN
      1. Conv Layers
      2.  Pooling Layers
   2.  Transfer Learning


---

# Code formating

Surround text with backticks like `theme.set("monokai")` or use tripple backticks.

```python
import torch.nn as nn
import torch

conv = nn.Conv2d(in_channels=3, out_channels=16, kernel_size=3, stride=1, padding=1)
x = torch.randn(1, 3, 64, 64) 
out = conv(x)
print(out.shape)  # Expect torch.Size([1, 16, 64, 64])
```

Language can be specified after the first triple backticks.