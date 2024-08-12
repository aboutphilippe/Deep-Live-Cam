# install models

mkdir -p models
curl -L -o models/GFPGANv1.4.pth https://huggingface.co/hacksider/deep-live-cam/resolve/main/GFPGANv1.4.pth
curl -L -o models/inswapper_128_fp16.onnx https://huggingface.co/hacksider/deep-live-cam/resolve/main/inswapper_128.onnx

(choppy on m1 https://github.com/hacksider/Deep-Live-Cam/issues/120)

# install brew dependencies

brew install ffmpeg
brew install tcl-tk
brew install python-tk@3.11

# run in venv

python3.11 -m venv venv
source venv/bin/activate

pip install -r requirements.txt

python run.py --keep-fps --execution-provider coreml

# To replace feed on yout Webcam

https://obsproject.com/

Add source from Window and Select
Start Virtual Camera
