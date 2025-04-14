```run.sh
#!/bin/bash
set -e
source tutorial-env/bin/activate
cd MU-LLaMA
unset http_proxy https_proxy
HF_ENDPOINT=https://hf-mirror.com   python gradio_app.py --model ./ckpts/checkpoint.pth --llama_dir ./ckpts/LLaMA
# python demo1.py
```



test 
```
import torchaudio
waveform, sr = torchaudio.load("./examples_piano.wav")
print(waveform.shape)
print("-------torchaudio load------\n")
```



```
ls ckpts
-rw-r--r-- 1 root root 2.5G Nov 27 18:52 7B.pth
-rw-r--r-- 1 root root  17G Nov 27 19:11 checkpoint.pth
-rw-r--r-- 1 root root  13G Nov 27 20:12 knn.index
drwxr-xr-x 3 root root 4.0K Nov 27 19:22 LLaMA
-rw-r--r-- 1 root root  266 Nov 27 18:49 README.md

d1b833424ced327378ad14cfa747ac51  7B.pth


cd LLaMA
ls 
total 504K
drwxr-xr-x 2 root root 4.0K Nov 27 19:22 7B
-rw-r--r-- 1 root root 1.9K Nov 27 18:49 llama.sh
-rw-r--r-- 1 root root   50 Nov 27 18:49 tokenizer_checklist.chk
-rw-r--r-- 1 root root 489K Nov 27 18:49 tokenizer.model

cd 7B
ls
checklist.chk  consolidated.00.pth  params.json  test.txt

cat params.json 
{"dim": 4096, "multiple_of": 256, "n_heads": 32, "n_layers": 32, "norm_eps": 1e-05, "vocab_size": -1}

```
