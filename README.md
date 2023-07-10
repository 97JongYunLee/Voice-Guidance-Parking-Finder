# Voice-Guidance-Parking-Finder

주차장의 남은공간을 detecting 하여 주차장의 남은공간을 음성으로 알려주는 역할.

## Requirement

* (프로젝트를 실행시키기 위한 최소 requirement들에 대해 기술)

```
* 10th generation Intel® CoreTM processor onwards
* At least 32GB RAM
* Python 3.9.13
```

## Clone code

* (Code clone 방법에 대해서 기술)

```shell
git clone https://github.com/zzz/yyy/xxxx
```

## Prerequite

* (프로잭트를 실행하기 위해 필요한 dependencies 및 configuration들이 있다면, 설치 및 설정방법에 대해 기술)

```shell
python -m venv .venv
.venv/Scripts/activate

python -m pip install -U pip
python -m pip install wheel

python -m pip install openvino-dev
git clone --recurse-submodules https://github.com/openvinotoolkit/open_model_zoo.git

cd open_model_zoo
python -m pip install -r requirements.txt

cd open_model_zoo/demos/text_to_speech_demo/python
omz_downloader --name text-to-speech-en-0001-duration-prediction
omz_downloader --name text-to-speech-en-0001-generation
omz_downloader --name text-to-speech-en-0001-regression
omz_converter --name text-to-speech-en-0001-duration-prediction
omz_converter --name text-to-speech-en-0001-generation
omz_converter --name text-to-speech-en-0001-regression

cd open_model_zoo/demos/object_detection_demo/python
omz_downloader --name vehicle-detection-0202
omz_converter --name vehicle-detection-0202


## Steps to build

* (프로젝트를 실행을 위해 빌드 절차 기술)

```shell
cd ~/xxxx
.venv/Scripts/activate
cd open_model_zoo/demos/text_to_speech_demo/python/
make
make install
```

## Steps to run

* (프로젝트 실행방법에 대해서 기술, 특별한 사용방법이 있다면 같이 기술)

```shell
cd ~/xxxx
source .venv/bin/activate

cd /path/to/repo/xxx/
python demo.py -i xxx -m yyy -d zzz
```

## Output

![./images/result.jpg](./images/result.jpg)

## Appendix

* (참고 자료 및 알아두어야할 사항들 기술)
