# 音高够了、音色分不够：59 分上限是怎么回事

- **适用场景**：女性向结果里看到 high_f0_male_cap，分数被压在 59 以下。
- **适用人群**：音高已经提上去了、但分数还是上不去，想知道卡在哪一项的人。
- **核心目标**：看懂这条 59 分上限在说什么，决定要不要、以及从哪开始探索音色。
- **修订日期**：2026-10-10

## 一、理解这项主题

先说规则本身：当音高 >165 Hz、自然分 ≥50、但音色分 <50 时，女性向会匹配 high_f0_male_cap，最终分最高 59。规则名里的 male 只是代码里的标识符，不是 App 在判断你的性别，不用在意这个命名。

这条规则的意思是：光靠高音高，补不上音色分。所以它会先提示你去听听音色——继续往上飙音高，解不开这个上限。

音高和音色本来就可以不同步：听者判断声音时同时参考基频和共振峰（共鸣）两套线索，在连续说话里，共振峰甚至是更相关的那一套（Gelfer & Bennett, 2013）。两段录音平均音高差不多，一段听起来明亮，一段听起来厚实，这很常见。音色分是模型给的整体印象分，当个参考就行；自然分高也只说明"听起来像日常说话"，不代表嗓子状态。

**技术细节**：high_f0_male_cap 匹配条件为 F0 > 165 Hz、自然分 ≥ 50、音色分 < 50，最终分上限 59（实际可能更低）。

## 二、练习前的观察

先问自己一个问题：你喜欢现在这个声音吗？如果日常交流够用、自己也顺耳，完全可以留着它，不用为了冲破 59 分去改。

如果想探索音色，找一句话，听听里面的元音：是偏明亮、偏柔和，还是偏厚实？同时记下说的时候费不费力。听感描述就够了，不用去想身体结构的事。

## 三、可尝试的方法

1. 用舒服的音高和日常音量说"你好，明天见"，这是原版，后面都用这句比。
2. 轻轻对比"衣""啊""乌"三个元音，听听音色怎么变。它们本来就需要不同口型，不用把所有元音固定成一个形状。
3. 如果其中某种听感你有兴趣，在"你好"的开头试着接近它，再把整句说完。每个字都要听得清，口舌跟着字词自然动。
4. 回听原版和尝试版，比较"你""好"两个字的音色，看句子是不是还说得清楚。听不出差别就记"这次没听出来"，很正常。
5. 别用这些方法去"折腾喉头"：不用手压，不用吞咽保持，不用刻意挤窄咽部（ASHA, n.d.）。目标是找到喜欢的听感，不是跟算法较劲。

## 四、参考文献

1. Project Pitchee. (n.d.). scoring.cpp. project-pitchee/Core. https://github.com/project-pitchee/Core/blob/e84d9c9a22401f5f25504a2e4348e50ed2db00bf/src/scoring.cpp —— 本文规则与公式按源码核对。

2. Project Pitchee. (n.d.). analyzer.cpp. project-pitchee/Core. https://github.com/project-pitchee/Core/blob/e84d9c9a22401f5f25504a2e4348e50ed2db00bf/src/analyzer.cpp —— 可查看音高有效帧筛选与音色分计算。

3. Gelfer, M. P., & Bennett, Q. E. (2013). Speaking fundamental frequency and vowel formant frequencies: Effects on perception of gender. *Journal of Voice*, *27*(5), 556–566. https://doi.org/10.1016/j.jvoice.2012.11.008 —— 基频与共振峰是两套相对独立的性别感知线索，音高相同的情况下共鸣仍可不同。

4. American Speech-Language-Hearing Association. (n.d.). Gender affirming voice and communication. ASHA Practice Portal. https://www.asha.org/practice-portal/professional-issues/gender-affirming-voice-and-communication/ —— 介绍以个人目标为中心的多维声音与交流支持。
