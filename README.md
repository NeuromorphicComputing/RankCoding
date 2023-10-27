# Rank Coding
_This open source project is not an official Huawei product. Huawei is not expected to provide support for this project._
## Spike-inspired Rank Coding for Fast and Accurate Recurrent Neural Networks

This repository contains a sample of the code corresponding to [this ICLR 2022 paper](https://openreview.net/forum?id=iMH1e5k7n3L), which has been accepted as a Spotlight paper. 

_Authors:_ Alan Jeffares, Qinghai Guo, Pontus Stenetorp, Timoleon Moraitis

_TL;DR:_ Fast inference through partly spiking LSTMs, outperforming other SNNs, and applied in keyword spotting.

## Abstract
Biological spiking neural networks (SNNs) can temporally encode information in their outputs, e.g. in the rank order in which neurons fire, whereas artificial neural networks (ANNs) conventionally do not. As a result, models of SNNs for neuromorphic computing are regarded as potentially more rapid and efficient than ANNs when dealing with temporal input. On the other hand, ANNs are simpler to train, and usually achieve superior performance. Here we show that temporal coding such as rank coding (RC) inspired by SNNs can also be applied to conventional ANNs such as LSTMs, and leads to computational savings and speedups.
In our RC for ANNs, we apply backpropagation through time using the standard real-valued activations, but only from a strategically early time step of each sequential input example, decided by a threshold-crossing event. Learning then incorporates naturally also when to produce an output, without other changes to the model or the algorithm. Both the forward and the backward training pass can be significantly shortened by skipping the remaining input sequence after that first event. RC-training also significantly reduces time-to-insight during inference, with a minimal decrease in accuracy. The desired speed-accuracy trade-off is tunable by varying the threshold or a regularization parameter that rewards output entropy. We demonstrate these in two toy problems of sequence classification, and in a temporally-encoded MNIST dataset where our RC model achieves 99.19% accuracy after the first input time-step, outperforming the state of the art in temporal coding with SNNs, as well as in spoken-word classification of Google Speech Commands, outperforming non-RC-trained early inference with LSTMs.

## Cite
To cite this work please use the following reference:

    @inproceedings{
    jeffares2022spikeinspired,
    title={Spike-inspired rank coding for fast and accurate recurrent neural networks},
    author={Alan Jeffares and Qinghai Guo and Pontus Stenetorp and Timoleon Moraitis},
    booktitle={International Conference on Learning Representations},
    year={2022},
    url={https://openreview.net/forum?id=iMH1e5k7n3L}
    }

## Demo
To get started, see a demo of applying our method in Demo.ipynb.
