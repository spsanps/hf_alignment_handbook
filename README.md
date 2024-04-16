This is a fork from https://github.com/huggingface/alignment-handbook. Please refer to the repo there.

This is for running a series of sft experiments.

Steps I take to run experiments:

```
git clone https://github.com/spsanps/hf_alignment_handbook.git
cd hf_alignment-handbook
python -m pip install .
```

```
python -m pip install flash-attn==2.3.6 --no-build-isolation
```

```
apt update
apt instal git-lfs
```

```
pip install wandb
wandb login
```

```
huggingface-cli login
```

```
ACCELERATE_LOG_LEVEL=info accelerate launch --config_file recipes/accelerate_configs/deepspeed_zero3.yaml scripts/run_sft.py recipes/zephyr-7b-beta/custom_gutenberg/config_full.yaml
```


