# ๐ฅHappyWhale - Dolphin and Whale

# Contents

#### &nbsp;&nbsp;&nbsp;&nbsp;**[๐ฌTask Description](https://github.com/thsckdduq/my_project/kaggle/happywhale#task-description-1)**

#### &nbsp;&nbsp;&nbsp;&nbsp;**[๐Project Result](https://github.com/thsckdduq/my_project/kaggle/happywhale#project-result-1)**

#### &nbsp;&nbsp;&nbsp;&nbsp;**[๐งCollaborate Tools](https://github.com/thsckdduq/my_project/kaggle/happywhale#collaborate-tools-1)**

#### &nbsp;&nbsp;&nbsp;&nbsp;**[๐งMy Experiment](https://github.com/thsckdduq/my_project/kaggle/happywhale#my-experiment-1)**
<br>

# Task Description

### Subject https://www.kaggle.com/competitions/happy-whale-and-dolphin 
<br>
์ด๋ฒ ๋ํ์ ์ฃผ์ ๋ ๋๊ณ ๋์ ๊ณ ๋์ ์ฌ์ง์ผ๋ก individual_id ๋ถ๋ฅํ๋ ๋ฌธ์ ์์ต๋๋ค.  ๋๊ณ ๋์ ๊ณ ๋์ ์ง๋๋ฌ๋ฏธ์ ์ฌ๋์ ์ง๋ฌธ๊ณผ ๊ฐ์ด ๊ฐ ๊ฐ์ฒด๋ฅผ ๋ถ๋ฅํ  ์ ์๋ ํน์ง์ด ์๋ค๊ณ  ์๊ฐํด ํด๋น ๋ฌธ์ ๋ฅผ object recognition ์ด๋ก ์ผ๋ก ์ ๊ทผํ์์ต๋๋ค.

<br>
๋๊ณ ๋์ ์ฌ์ง์ ์ง๋๋ฌ๋ฏธ์ ์ง๋๋ฌ๋ฏธ๋ฅผ ํฌํจํ ๋ชธํต์ผ๋ก object detection ์งํํ๊ณ , ํด๋น ์ด๋ฏธ์ง๋ฅผ ๊ฐ์ง๊ณ  ๊ฐ ๊ฐ์ฒด๋ฅผ ๋ถ๋ฅํ๋ ๋ชจ๋ธ์ ์์ฑํ์์ต๋๋ค.
<br>

### Data

- ํ๋ จ ๋ฐ์ดํฐ : 51033์ฅ์ ์ด๋ฏธ์ง์ ํด๋น ์ด๋ฏธ์ง์ ์ข๊ณผ individual_id

- ํ์คํธ ๋ฐ์ดํฐ : 27916์ฅ์ ์ด๋ฏธ์ง
<br>

### Metric

<img src="./img/metric.png" width='400px'/>
<br>

<img src="./img/metric_score.png" width='300px' height='180px' />
<br>

# Project Result

<div><img src=./img/rank.png?raw=true /></div>

- ์๋ฉ๋ฌ 47 ๋ฑ / 1,613 ํ

- Public LB Score: 0.85147 / Private LB Score: 0.81686

- Code : https://github.com/YDdreammaker/dl_whale_classification

- ์๋ฃจ์์ [์ด๊ณณ](https://www.notion.so/Solution-c1be44608fc941bd9442495587a8f1e1)์์ ํ์ธํ์ค ์ ์์ต๋๋ค.
<br>

# Collaboration Tools
<table>
    <tr height="200px">
        <td align="center" width="350px">	
            <a href="https://www.notion.so/b47246b96c204ca38f96c45888919525?v=f2ab615cde7342c78d3761641a828e5c"><img height="180px" width="320px" src="./img/notion.png?raw=true"/></a>
            <br/>
            <a href="https://www.notion.so/b47246b96c204ca38f96c45888919525?v=f2ab615cde7342c78d3761641a828e5c">Notion</a>
        </td>
        <td align="center" width="350px">	
            <a><img height="180px" width="320px" src="./img/wandb.png?raw=true"/></a>
            <br />
            <a>WanDB</a>
        </td>
    </tr>
</table>

# My Experiment

- Annotation ์์์ ํตํ Yolo๋ฅผ ๋๋ฆฌ๊ธฐ ์ํ ๋ฐ์ดํฐ ์์ฑ
- Inference Code ์์ฑ (๊ธฐ์กด ์ฝ๋ 20๋ถ ๊ฐ๋ ์์ -> 7๋ถ ์์๋๋ ์ฝ๋ ๊ตฌํ)
    - ๊ธฐ์กด์ pandas๋ก ์ด๋ฃจ์ด์ ธ ์๋ ์ฝ๋๋ฅผ numpy๋ก ์์ ํ์ฌ ์์ ์๊ฐ ๋จ์ถ
    - embedding ๊ฐ์ผ๋ก ensemble์ ํ๊ธฐ์ํ ์ฝ๋ (Arcface Embedding๊ฐ์ ๋ฐ์์ ์งํ)
    - logit ๊ฐ์ผ๋ก ensemble ํ๊ธฐ์ํ ์ฝ๋ (ArcFace Cosine๊ฐ์ ๋ฐ์์ ์งํ)
- ์ข์ ๋ถ๋ฅํ๊ธฐ ์ํ Model ์คํ
    - ํด๋น Task์์ Species๋ฅผ ํตํ ์ ๋ต์ ๋์ถ์ด ์ค์ํ ํค์๋๋ผ ์๊ฐํ๊ณ  Species๋ฅผ ๋ถ๋ฅํ๋ ๋ชจ๋ธ์ ์ํ ์คํ
    - Species๋ฅผ ๋ถ๋ฅํ๋ Model์ ์์ฑ ํ Inference ๊ณผ์ ์์ Species๋ฅผ ํตํ Masking ํ Inference ํ๋ ์ฝ๋ ์์ฑ - Model์ด ์ ๊ตํ ๋๋ ๊ณผ์ ์์ Species๋ฅผ ํตํ Masking์ด ํจ๊ณผ๊ฐ ์์ด์ง
    - ๋ง์ง๋ง Inference ๊ณผ์ ์์ ์ข๋ณ๋ก ๋ถํฌ๊ฐ ์์ดํ ๊ฒ์ ํ์ธํ๊ณ  ์ข๋ณ๋ก new_individual์ ์ ํ๋ Threshold๋ฅผ ๊ตฌํ๋ ๊ณผ์ ์ ์ฌ์ฉ๋จ
- ์ข๋ณ๋ก label smoothing
    - ๋ชจ๋ธ์ ํ์ตํ๋ ๊ณผ์ ์์ Species ๋ณ๋ก ๋ค์ํ feature๋ฅผ ๊ตฌ๋ถํ  ์ ์์ผ๋ฉด ์ข์ ๊ฒ ๊ฐ๋ค๋ ์๊ฐ์ผ๋ก Label Smoothing์ Species ๋ณ๋ก ์ ์ฉํ์ฌ ํ์ต - ์ค์ ๋ก ํ์ธํด๋ณธ ๊ฒฐ๊ณผ ๊ธฐ์กด ArcFace ๋ชจ๋ธ๊ณผ ํ์ตํ ๋ด์ฉ์ด ๋งค์ฐ ์์ดํ์
    - ๋ณธ๋์ ArcFace Model๊ณผ Ensemble์ ์งํํ ๊ฒฐ๊ณผ ์ฑ๋ฅ์ด ์ํญ ์์น
- Global Feature์ Local Feature๋ฅผ ํ์ตํ๊ธฐ ์ํ ๋ฐฉ๋ฒ ๊ตฌํ
