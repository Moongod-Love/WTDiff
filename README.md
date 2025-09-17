# Title

**WTDiff: High-Fidelity Weather Translation with One-Step Diffusion**

*Zixuan Hua, Xun Fang, Xing Wei, Lihua Zhang*

## TODO

- [ ] train and test code release
- [ ] FID and DINO-Struct-Dist test code
- [ ] upload checkpoints for night, rainy, snowy and foggy

# Model Overview

![Pipeline](C:\Users\34110\Desktop\Pipeline.png)

# Image Results

![Qualitative](C:\Users\34110\Desktop\Qualitative.png)

# Getting Started

```
git clone https://github.com/Moongod-Love/WTDiff.git
```

# Dependencies

```
pip install -r requirements.txt
```

# Dataset Explanations

For the clear $\leftrightarrow$ foggy translation task, images should be placed under `/path_to_your_dataset/` in the following structure.

```
A: source images (e.g., clear images)
B: target images (e.g., foggy images)
```

# Dataset Folder Structure

```
/path_to_your_dataset/
    ├── train_A
    ├── train_B
    ├── test_A
    ├── test_B
    ├── fix_prompt_a.txt
    ├── fix_prompt_b.txt
```

# Training

Run in terminal.

```
sh train_{task}.sh
```

# Testing with pretrained model

1. Download the checkpoints.

2. Unzip the checkpoints.

3. Create folder Day2Night, Clear2Rainy, Clear2Snowy and Clear2Foggy under ./checkpoints.

   ```
   /WTDiff/
       ├── checkpoints
       │   ├── Day2Night
       │   ├── Clear2Rainy 
       |   ├── Clear2Snowy
       |   ├── Clear2Foggy
   ```

4. Run in terminal.

   ```
   sh test_{task}.sh
   ```

   