
# Increasing ParC-Net’s Performance with Half-blocks

Project created for the CISC 867 class of Prof. Hazem Abbas, in Fall '23 at Queen's University - Canada, by <a href="https://github.com/dashtiali">@dashtiali</a>, <a href="https://github.com/MahaK21">@MahaK21</a> and <a href="https://github.com/MahatKC">@MahatKC</a>.

---

Fork from the [original repository](https://github.com/hkzhang-git/ParC-Net) for the paper "ParC-Net: Position Aware Circular Convolution with Merits from ConvNets and Transformer". Our changes are mainly to the `cvnets/modules/edgeformer_block.py` file, specifically the `forward` function on line 489.

Our goal here was to increase the performance of the original ParC-Net architecture by reducing redundancy. For that matter, we designed the ParC-Half blocks, which do convolution only for the even-indexed rows/columns of the input, which are shown in the image below.

<img src="https://raw.githubusercontent.com/MahatKC/ParC-Net-HalfBlocks/main/readme_images/HalfBlockV.png" align="middle" width="800" ></a>

Then, using the proposed ParC-Half blocks, we did 3 experiments to compare our approach with the approach from the paper:

<img src="https://raw.githubusercontent.com/MahatKC/ParC-Net-HalfBlocks/main/readme_images/Experiments.png" align="middle" width="550" ></a>

The following results were achieved, which are compared to the pre-trained model of the paper (provided in their repository):

<img src="https://raw.githubusercontent.com/MahatKC/ParC-Net-HalfBlocks/main/readme_images/TestResults.png" align="middle" width="400" ></a>

Therefore, we were able to improve upon the accuracy of the original model while decreasing its cost.
