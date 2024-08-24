## Installation

### [Prerequsites](https://aios.readthedocs.io/en/latest/get_started/installation.html#prerequsites) : Met 

* Anaconda 

* Python: 3.9-3.11 :: 3.11

* Git : Y


### Build from source[#](https://aios.readthedocs.io/en/latest/get_started/installation.html#build-from-source "Permalink to this heading")

```bash
# Prep: Git Enabled
# ---
(base) dp@P920:~/Documents/GitHub/AIOS$ ll
total 20
drwxrwxr-x 3 dp dp 4096 Aug 24 17:48 ./
drwxrwxr-x 3 dp dp 4096 Aug 24 17:45 ../
drwxrwxr-x 8 dp dp 4096 Aug 24 17:45 .git/
-rw-rw-r-- 1 dp dp   66 Aug 24 17:45 .gitattributes
-rw-rw-r-- 1 dp dp  137 Aug 24 17:49 installation_with_ollama.md
```

Git clone AIOS repository

```bash
# Created conda environment
# ---
(base) dp@P920:~/Documents/GitHub/AIOS$ conda create -n aios python=3.11
...
Preparing transaction: done
Verifying transaction: done
Executing transaction: done
#
# To activate this environment, use
#
#     $ conda activate aios
#
# To deactivate an active environment, use
#
#     $ conda deactivate

# Cloned source resository
# ---
(base) dp@P920:~/Documents/GitHub/AIOS$ git clone https://github.com/agiresearch/AIOS.git
Cloning into 'AIOS'...
remote: Enumerating objects: 3110, done.
remote: Counting objects: 100% (872/872), done.
remote: Compressing objects: 100% (367/367), done.
remote: Total 3110 (delta 649), reused 557 (delta 501), pack-reused 2238 (from 1)
Receiving objects: 100% (3110/3110), 3.24 MiB | 12.03 MiB/s, done.
Resolving deltas: 100% (1682/1682), done.

(base) dp@P920:~/Documents/GitHub/AIOS$ ll
total 24
drwxrwxr-x  4 dp dp 4096 Aug 24 17:57 ./
drwxrwxr-x  3 dp dp 4096 Aug 24 17:45 ../
drwxrwxr-x 12 dp dp 4096 Aug 24 17:57 AIOS/
drwxrwxr-x  8 dp dp 4096 Aug 24 17:45 .git/
-rw-rw-r--  1 dp dp   66 Aug 24 17:45 .gitattributes

## Activated conda
(base) dp@P920:~/Documents/GitHub/AIOS$ conda activate aios
```

Install from requirements-cuda.txt if you have cuda environment
```
(aios) dp@P920:~/Documents/GitHub/AIOS$ cd AIOS/
(aios) dp@P920:~/Documents/GitHub/AIOS/AIOS$ pip install -r requirements-cuda.txt
Collecting google-generativeai (from -r requirements.txt (line 1))
  Using cached google_generativeai-0.7.2-py3-none-any.whl.metadata (4.0 kB)
Collecting openai==1.20.0 (from -r requirements.txt (line 2))
  Using cached openai-1.20.0-py3-none-any.whl.metadata (21 kB)
  ...
  ...
ferencing-0.35.1 regex-2024.7.24 requests-2.32.3 rpds-py-0.20.0 rsa-4.9 safetensors-0.4.4 sentencepiece-0.2.0 six-1.16.0 sniffio-1.3.1 starlette-0.38.2 sympy-1.13.2 tiktoken-0.7.0 tokenizers-0.19.1 torch-2.4.0 torchvision-0.19.0 tqdm-4.66.5 transformers-4.44.2 triton-3.0.0 typing-extensions-4.12.2 tzdata-2024.1 uritemplate-4.1.1 urllib3-2.2.2 uvicorn-0.30.6 uvloop-0.20.0 vllm-0.5.4 vllm-flash-attn-2.6.1 watchfiles-0.23.0 websockets-13.0 xformers-0.0.27.post2 xxhash-3.5.0 yarl-1.9.4 zipp-3.20.0
(aios) dp@P920:~/Documents/GitHub/AIOS/AIOS$  
```

## Quickstart

### Out of Box
```bash
(aios) dp@P920:~/Documents/_POCs/AIOS/AIOS$ python main.py --llm_name ollama3
[🤖ollama3] AIOS LLM successfully loaded.
...
[Scheduler] example/academic_agent is executing. 

[🤖ollama3] example/academic_agent is switched to executing.

[example/academic_agent] At step 4, An unexpected error occurred: [Errno 111] Connection refused
```

### @TODO: set OPEN API Key, copy/create agent  task from example


