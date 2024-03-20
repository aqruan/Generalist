# Generalist: Decoupling Natural and Robust Generalization

Official implementation for CVPR'23 paper "Generalist: Decoupling Natural and Robust Generalization"



## Prerequisites

- Python (>=3.7)
- Pytorch (>=1.5)
- Torchvision
- CUDA
- Numpy
- [AutoAttack](https://github.com/fra31/auto-attack)



## 备注
代码在pycharm中进行了修改，修改后可以直接运行

## Training and Testing

- Train ResNet-18 on CIFAR10:

```
  $ CUDA_VISIBLE_DEVICES={your GPU number} python3 main.py 
```

- Train WRN-32-10 on CIFAR10

```
  $ CUDA_VISIBLE_DEVICES={your GPU number} python3 main.py --arch 'WRN32'
```

Then, it will automatically run all the robustness evaluation in our paper, including NAT, PGD20/100, MIM, CW, APGD<sub>ce</sub>, APGD<sub>dlr</sub>, APGD<sub>t</sub>, FAB<sub>t</sub>, Square and AutoAttack.

[Pretrained model](https://drive.google.com/file/d/1mbxSoTOUb4bfGDiJo46oKINqj42kgZyY/view?usp=drive_link)


## Citation

If you are interested in our work, please consider citing the related paper:

```
@inproceedings{wang2023simple,
  title={Generalist: Decoupling Natural and Robust Generalization},
  author={Hongjun Wang and Yisen Wang},
  booktitle={CVPR},
  year={2023}
}

@inproceedings{wang2022selfensemble,
  title={Self-ensemble Adversarial Training for Improved Robustness},
  author={Hongjun Wang and Yisen Wang},
  booktitle={ICLR},
  year={2022}
}
```
