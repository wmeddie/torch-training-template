# Torch Training Template

## Set-up

Run the following commands to install all the dependencies into a virtualenv.

Linux/Mac Bash:
```
python3 -m venv venv

source venv/bin/activate
pip install -r requirements.txt
```

Windows Cmd:
```
python3 -m venv venv

.\venv\Scripts\activate
pip install torch===1.6.0 torchvision===0.7.0 -f https://download.pytorch.org/whl/torch_stable.html
pip install -r requirements.txt
```

## Training

Run the train.py script with different arguments to create experiments.

```
python train.py \
    --name simple_experiment \
    --train_dataset /Users/egonzalez/Downloads/train \
    --val_dataset /Users/egonzalez/Downloads/val \
    --batch_size 32 \
    --seed 42 \
    --epochs 100
```

After training, you'll find the saved model, config, and evaluation results inside `experiments/$name`

