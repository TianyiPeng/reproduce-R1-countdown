# reproduce-R1-countdown
Reproducing a mini Deepseek R1 for the countdown game (https://www.philschmid.de/mini-deepseek-r1)

Check the tutorial here: https://www.philschmid.de/mini-deepseek-r1

Install the dependencies:
```
pip install -r requirements.txt
```

Run the experiment: 
```
accelerate launch --num_processes 7 --config_file deepspeed_zero3.yaml run_r1_grpo.py --config grpo-qwen-2.5-3b-deepseek-r1-countdown.yaml
```

Using tensorboard to monitor the training
```
tensorboard --logdir=runs/qwen-2.5-3b-r1-countdown/runs --port=6006 --bind_all 
```