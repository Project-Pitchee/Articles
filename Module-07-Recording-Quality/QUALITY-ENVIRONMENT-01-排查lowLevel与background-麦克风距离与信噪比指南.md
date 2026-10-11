# 电平过低或背景干扰：让录音条件更可比

- **适用场景**：冒出 lowLevel 或 background 提示，或者换了个地方录，分数明显不一样了。
- **适用人群**：想固定一个靠谱的录音环境、让每次对比都可比的人。
- **核心目标**：分清"录音条件变了"和"声音变了"，找到稳定的录制方式。
- **修订日期**：2026-10-10

## 一、理解这项主题

dBFS 是数字信号相对满幅的电平（Audio Engineering Society, 2015）。它受麦克风灵敏度、距离、增益一路下来的影响，只回答"信号够不够强"这一个问题（Titze & Winholtz, 1993）。两台设备录出不同的 dBFS，原因在链路，不在嗓子（Jannetts et al., 2019）。

Pitchee 的两条检查线：语音电平中位数低于 −45 dBFS，提示 lowLevel；语音和"没说话的片段"电平差不到 10 dB，提示 background。这些都是帮你筛录音条件的工程阈值。注意两点：语音检测自己也可能认错（Ma & Nishihara, 2013），"没说话的片段"不一定真安静（Ma & Nishihara, 2013）；如果整段根本没有安静片段，背景就是"未知"，别拿最轻的语音段当环境底噪。背景这项检查值得认真对待：研究里信噪比低于 30 dB 时，环境噪声会盖过其他因素、成为左右分数的首要因素，正常声音都可能被分析判成异常（Deliyski et al., 2005）。

检查通过了，分数也只当参考就行（Deliyski et al., 2005）。

## 二、练习前的观察

先听：有没有风声、空调声、别人说话、碰设备的声音、房间里的回响（Deliyski et al., 2005）？正常呼吸、停一小会儿，仔细听环境。不用屏气，也不用拍手自测——以录音里实际听到的为准，别凭对房间的印象（Deliyski et al., 2005）。

确认声音是从哪个麦克风进来的。蓝牙耳机、USB 麦克风、手机自带麦，用的增益和处理完全不一样，换设备就等于换了整条链路（Jannetts et al., 2019）。

A/B 两次有没有换设备、换距离？就算都没报警，频率响应和自动增益的差别也会影响分数（Jannetts et al., 2019）。电平低推不出"声门漏气"，background 提示也解释不了自然分具体掉了多少——别过度解读，修好条件再说（Deliyski et al., 2005）。

## 三、可尝试的方法

找个相对安静、回响小的位置，躲开直吹麦克风的风口（Deliyski et al., 2005；Bottalico et al., 2020）。窗帘、沙发这些软的东西能吸一点反射，但别指望有统一标准，够用就行（Bottalico et al., 2020）。

用你平时说话的音量（NIDCD, n.d.）。声音太小，先把麦克风拿近一点（Titze & Winholtz, 1993），检查有没有挡住、是不是选对了输入设备；如果爆音多了，再稍微拿远或者避开气流（Titze & Winholtz, 1993）。能调增益的设备就按回听调，别靠喊去"达标"（NIDCD, n.d.）。

一次只改一个最明显的问题（Deliyski et al., 2006）：有风声就换个不迎风的位置；字清楚但声音小就查距离和设备；回声重就换个软家具多的房间。改完重读同一段，回听问题少没少。没改善再查下一项，别同时换设备、距离和发声方式。

找到清楚的录法之后，就固定下来：同一设备、同一位置、差不多的距离，用同一段话做对比（Jannetts et al., 2019；Titze & Winholtz, 1993）。换设备之后的记录单独放，别把链路变化当成进步或退步（Jannetts et al., 2019）。

## 四、参考文献

1. Deliyski, D. D., Shaw, H. S., & Evans, M. K. (2005). Adverse effects of environmental noise on acoustic voice quality measurements. *Journal of Voice*, *19*(1), 15–28. https://doi.org/10.1016/j.jvoice.2004.07.003
2. Bottalico, P., Codino, J., Cantor-Cutiva, L. C., et al. (2020). Reproducibility of voice parameters: The effect of room acoustics and microphones. *Journal of Voice*, *34*(2), 320–334. https://doi.org/10.1016/j.jvoice.2018.10.016
3. Titze, I. R., & Winholtz, W. S. (1993). Effect of microphone type and placement on voice perturbation measurements. *Journal of Speech and Hearing Research*, *36*, 1177–1190.
4. Jannetts, S., Schaeffler, F., Beck, J., & Cowen, S. (2019). Assessing voice health using smartphones: Bias and random error of acoustic voice parameters captured by different smartphone types. *International Journal of Language & Communication Disorders*, *54*(2), 292–305. https://doi.org/10.1111/1460-6984.12457
5. Ma, Y., & Nishihara, A. (2013). Efficient voice activity detection algorithm using long-term spectral flatness measure. *EURASIP Journal on Audio, Speech, and Music Processing*, *2013*, 21. https://doi.org/10.1186/1687-4722-2013-21
6. Audio Engineering Society. (2015). *AES17-2015: AES standard method for digital audio engineering—Measurement of digital audio equipment*.
7. National Institute on Deafness and Other Communication Disorders (NIDCD). (n.d.). Taking care of your voice. https://www.nidcd.nih.gov/health/taking-care-your-voice
8. Pitchee. (2026). 《引导练习、复测比较与可信趋势》（Docs/Guided-Practice.md）：lowLevel / background 判定规则与背景未知状态的产品文档。https://github.com/project-pitchee/Pitchee-ios/blob/61454c9d9cc5589073e85b42a3f1f0f5cdb0924d/Docs/Guided-Practice.md
9. Deliyski, D. D., Shaw, H. S., Evans, M. K., & Vesselinov, R. (2006). Regression tree approach to studying factors influencing acoustic voice analysis. *Folia Phoniatrica et Logopaedica*, *58*(4), 274–288. https://karger.com/fpl/article-abstract/58/4/274/140584/Regression-Tree-Approach-to-Studying-Factors
