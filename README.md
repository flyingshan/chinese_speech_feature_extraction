Because this repo is mainly focused on improving the chinese speech feature extraction, so I will use chinese then

## 思路

将"models--jonatasgrosman--wav2vec2-large-xlsr-53-chinese-zh-cn"提取出的中文ASR概率分布特征，分解为拼音声母、韵母级别的特征，从而能够提取出对于中文语音来说更加有表征能力的特征：

## 步骤

1. 使用models--jonatasgrosman--wav2vec2-large-xlsr-53-chinese-zh-cn模型提取出形状为(B, 16, 3503)的特征
2. 使用本仓库的viseme.py, 将3503维特征转为109维特征
3. 将AudioNet的输入从44维改为使用109，使用109维特征训练、测试


## else

对你有帮助的话请点个star！
