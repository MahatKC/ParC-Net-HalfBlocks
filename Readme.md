
# Increasing ParC-Net’s Performance with Half-blocks

Project created for the CISC 867 class of Prof. Hazem Abbas, in Fall '23 at Queen's University - Canada, by <a href="https://github.com/dashtiali">@dashtiali</a>, <a href="https://github.com/MahaK21">@MahaK21</a> and <a href="https://github.com/MahatKC">@MahatKC</a>.

---

Fork from the [original repository](https://github.com/hkzhang-git/ParC-Net) for the paper "ParC-Net: Position Aware Circular Convolution with Merits from ConvNets and Transformer". Our changes are mainly to the `cvnets/modules/edgeformer_block.py` file, specifically the `forward` function on line 489.

Our goal here was to increase the performance of the original ParC-Net architecture by reducing redundancy. For that matter, we designed the ParC-Half blocks, which do convolution only for the even-indexed rows/columns of the input.

<!---images half block, architecture, result table--->
