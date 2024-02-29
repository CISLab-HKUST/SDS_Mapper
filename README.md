# An Implemention of Variational Mapper on SDS based on ThreeStudio

## Implemented based on `LODS` and `ThreeStudio` 
### [LODS](https://yangxiaofeng.github.io/demo_diffusion_prior/)
### [ThreeStudio](https://github.com/threestudio-project/threestudio)




## Updates
- 29/2/2024: Code Released.


## TODO List

- [x] Implement improved SDS Loss (Variational Mapper)

- [ ] Apply improved SDS Loss on 3D Avatar Generation

- [ ] ID Driven 3D Avatar Generation

## Installation

- Install PyTorch and torch vision
```sh
# torch1.12.1+cu113
pip install torch==1.12.1+cu113 torchvision==0.13.1+cu113 --extra-index-url https://download.pytorch.org/whl/cu113
# or torch2.0.0+cu118
pip install torch torchvision --index-url https://download.pytorch.org/whl/cu118
```


- Install dependencies:
```sh
pip install -r requirements.txt
```

- Install 3DGS and Shap-E:
```sh
pip install ninja
pip install ./gaussiansplatting/submodules/diff-gaussian-rasterization
pip install ./gaussiansplatting/submodules/simple-knn

git clone https://github.com/openai/shap-e.git
cd shap-e
pip install -e .
```

If you have any problem with the installation, you may search the issues in these two repos first.
Also feel free to open a new issue here.

## Quickstart


### Run Variational Mapper + 3D Gaussian Splatting
```
python launch.py --config configs/t3aga-gs-mapper.yaml --train --gpu 0 system.prompt_processor.prompt="a DSLR image of a hamburger"
```


## Credits

This code is built on the following open-source projects:
- **[ThreeStudio](https://github.com/threestudio-project/threestudio)** Main Framework
- **[LODS](https://yangxiaofeng.github.io/demo_diffusion_prior/)** Clear Framework based on ThreeStudio
- **[GaussianDreamer](https://github.com/hustvl/GaussianDreamer)** 3D Gaussian Splatting
- **[3D Gaussian Splatting](https://github.com/graphdeco-inria/gaussian-splatting)** 3D Gaussian Splatting

Credits from ThreeStudio
- **[Lightning](https://github.com/Lightning-AI/lightning)** Framework for creating highly organized PyTorch code.
- **[OmegaConf](https://github.com/omry/omegaconf)** Flexible Python configuration system.
- **[NerfAcc](https://github.com/KAIR-BAIR/nerfacc)** Plug-and-play NeRF acceleration.

