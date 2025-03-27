https://docs.astral.sh/uv/guides/integration/pytorch/

0. 가장 먼저 내 그래픽카드가 지원하는 CUDA toolkit의 버전을 확인한다. 
   CUDA의 GPUs supported status은, https://en.wikipedia.org/wiki/CUDA에서 확인가능하다. 
   
   CUDA를 버전에 맞게 설치하자.

1. 그 다음으로 python, torch, torchvision을 따라서 버전을 확인한다. 

   CUDA 버전에 맞는 
   Pytorch version, Python version 확인:  
   Pytorch 공식 github에 있는 Compatibility Matrix를 확인한다.(https://github.com/pytorch/pytorch/blob/main/RELEASE.md#release-compatibility-matrix)

   torchvision version 확인
   (https://github.com/pytorch/vision)

2. 터미널에 `uv --init python 3.12` 실행.

3. 'pyproject.toml' 작성 (내가 이미 작성한 pyproject.toml 참조)

4. 'uv sync'

5. vs code에서 활용하기 위해 다음을 참고한다. 
   'Using Jupyter from VS Code'
   https://docs.astral.sh/uv/guides/integration/jupyter/
   'uv add --dev ipykernel'
   'code .'

6. 아무 python .py 파일이나, .ipynb 파일에서 import torch 등등을 하고,
   torch.cuda.is_available()을 입력, 간절히 기도한다.

7. 성공!
