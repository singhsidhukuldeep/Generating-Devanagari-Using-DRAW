# Generating-Devanagari-Using-DRAW
PyTorch implementation of [DRAW: A Recurrent Neural Network For Image Generation](https://arxiv.org/abs/1502.04623) on the task of generating [Devanagari](https://en.wikipedia.org/wiki/Devanagari) Characters.

Deep Recurrent Attentive Writer (DRAW) is a neural network architecture for image generation. DRAW networks combine a novel spatial attention mechanism that mimics the foveation of the human eye, with a sequential variational auto-encoding framework that allows for the iterative construction of complex images. The system substantially improves on the state of the art for generative models on MNIST, and, when trained on the Street View House Numbers dataset, it generates images that cannot be distinguished from real data with the naked eye.

<p align="center">
<img src="images/devanagari_generate.gif" title="Generated Data Animation" alt="Generated Data Animation">
</p>

## Articles
### Blog Post: [http://kuldeepsinghsidhu.blogspot.com](http://kuldeepsinghsidhu.blogspot.com)

Articles: https://kuldeepsinghsidhu.blogspot.com/2019/01/generating-devanagari-using-draw.html

## Difference

| With Attention  | Without Attention |
| ------------- | ------------- |
| <img src="images/mnist_attn.gif" width="100%"> | <img src="images/mnist_noattn.gif" width="100%"> |

## Training
Download the data and place it in the **data/** directory. Run **`train.py`** to start training. To change the hyperparameters of the network, update the values in the `param` dictionary in `train.py`.

**Loss Curve**
<p align="center">
<img src="images/Devanagari_Loss_Curve.png" title="Training Loss Curves" alt="Training Loss Curves">
</p>

## Generating New Images
To generate new images run **`generate.py`**.
```sh
python3 evaluate.py -load_path /path/to/pth/checkpoint -num_output n
```
The checkpoint file for the model trained for 50 epochs is present in **checkpoint/** directory.

## Results
<table align='center'>
<tr align='center'>
<th> Devanagari Training Data </th>
<th> Generated Devanagari After 50 Epochs</th>
</tr>
<tr>
<td><img src = 'images/Devanagari_Training_Data.png'>
<td><img src = 'images/Devanagari_Generated_Image.png'>
</tr>
</table>
<table align='center'>
<tr align='center'>
<th> Devanagari Numbers Only Training Data </th>
<th> Generated Devanagari Numbers After 50 Epochs</th>
</tr>
<tr>
<td><img src = 'images/devanagari_num_Training_Data.png'>
<td><img src = 'images/devanagari_num_epoch_50_generated_image.png'>
</tr>
</table>

### Some more generated images:
<img src = 'images/Generated_Image144_1.png'>

## References
1. **Karol Gregor, Ivo Danihelka, Alex Graves, Danilo Jimenez Rezende, Daan Wierstra.** *DRAW: A Recurrent Neural Network For Image Generation.* [[arxiv](https://arxiv.org/abs/1502.04623)]
2. **ericjang/draw** [[repo](https://github.com/ericjang/draw)]
3. **What is DRAW (Deep Recurrent Attentive Writer)?** [[blog](http://kvfrans.com/what-is-draw-deep-recurrent-attentive-writer/)]

## Data
The Devanagari Character dataset is available on kaggle. ([Source](https://www.kaggle.com/rishianand/devanagari-character-set))


## CREDITS

>Kuldeep Singh Sidhu

Github: [github/singhsidhukuldeep](https://github.com/singhsidhukuldeep)
`https://github.com/singhsidhukuldeep`

Website: [Kuldeep Singh Sidhu (Website)](http://kuldeepsinghsidhu.com)
`http://kuldeepsinghsidhu.com`

LinkedIn: [Kuldeep Singh Sidhu (LinkedIn)](https://www.linkedin.com/in/singhsidhukuldeep/)
`https://www.linkedin.com/in/singhsidhukuldeep/`
