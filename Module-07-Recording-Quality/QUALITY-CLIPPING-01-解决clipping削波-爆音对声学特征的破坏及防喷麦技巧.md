# 录音提示可能削波：先调整采集，再比较声音

- **适用场景**：录到 clipping 提示，或者回听时某些字有爆音、沙沙的失真。
- **适用人群**：怀疑麦克风没摆对、想先修好录音再练的人。
- **核心目标**：搞定削波和喷麦，录到干净、可比较的样本。
- **修订日期**：2026-10-10

## 一、理解这项主题

削波就是声音太大，超过了某个环节能处理的上限，波形顶端被"削平"了（Xia & Hansen, 2018）。它跟"动态压缩/限幅"不是一回事——那是主动控制音量的，这里是直接爆掉了（Xia & Hansen, 2018）。

爆掉的波形会多出本来没有的谐波和杂音（Xia & Hansen, 2018），后面的分析（音高、音色分、自然分）都会受影响，但分数具体会怎么变、变多少，事先说不准（Xia & Hansen, 2018）。

Pitchee 的规则是：至少 1% 的采样点顶到头（绝对值不小于 0.999）就提示可能削波。这是帮你发现采集问题的工程检查线，别拿它当嗓子好坏的标准（Bottalico et al., 2020）。它也可能漏掉一些情况——比如失真发生在前级、后面又被压小了。提示出现了就先处理；没出现的话，回听确认一下更稳。

## 二、练习前的观察

先回听，定位杂音：是只在某些送气音（比如 p、t）上爆，还是句首突然大声，还是整段都有？先分一下类：喷麦是爆破音的气流直冲振膜，出来的是偏低频的"噗"声；数字削波是音量顶到上限，出来的是刺耳的失真。气流冲击麦克风产生的噪声本来就集中在低频（Sun et al., 2026），所以听着闷的先查位置和气流，听着刺的先查增益和电平。几种情况也可能混在一起，稳妥起见还是一个个排查（Deliyski et al., 2006）。

确认现在用的是哪个麦克风：手机、耳机还是外接？进音孔有没有被手或手机壳挡住？蓝牙和有线用的可能不是同一个麦克风，换了设备要重新看（Parsa et al., 2001）。

再问自己：刚才是不是为了让 App 收到声音，不自觉喊起来了？平常说话的音量能录清楚，就别加力（NIDCD, n.d.）。如果已经觉得疼、紧或者哑，先停（NIDCD, n.d.）——这是嗓子累了的信号，先休息，调麦克风解决不了。

## 三、可尝试的方法

先别动发声，只动麦克风。保持平常说话的音量，把麦克风拿远一点，或者挪到气流不直接喷到的位置（Titze & Winholtz, 1993）。从大概一掌的距离试起，录一句短的听听，再微调（Titze & Winholtz, 1993）。

做一次"只查采集"的对比：位置 A（原来）录一遍，位置 B（移开）录同一句。只看杂音少没少、字清不清楚、提示还在不在——这一轮分数变了也不算数，因为你改的是录音条件，不是发声（Bottalico et al., 2020）。

如果设备能调输入增益，适当调低一点，给比较响的字留点余量（Xia & Hansen, 2018）。一次只改一个条件，这样才知道是哪个调整起的作用（Deliyski et al., 2006）。

有防喷罩就用上：网面把集中的气流打散，低频"噗"声就小很多（Sun et al., 2026）。还是不行的话，换个安静的位置（Bottalico et al., 2020）、检查插线，或者换个靠谱的麦克风（Parsa et al., 2001；Titze & Winholtz, 1993）。录清楚了，再回去比声音。

## 四、参考文献

1. Xia, W., & Hansen, J. H. L. (2018). Speaker recognition with nonlinear distortion: Clipping analysis and impact. In *Proceedings of Interspeech 2018* (pp. 746–750). https://doi.org/10.21437/Interspeech.2018-2430
2. Titze, I. R., & Winholtz, W. S. (1993). Effect of microphone type and placement on voice perturbation measurements. *Journal of Speech and Hearing Research*, *36*, 1177–1190.
3. Parsa, V., Jamieson, D. G., & Pretty, B. R. (2001). Effects of microphone type on acoustic measures of voice. *Journal of Voice*, *15*(3), 331–343. https://doi.org/10.1016/S0892-1997(01)00035-2
4. Bottalico, P., Codino, J., Cantor-Cutiva, L. C., et al. (2020). Reproducibility of voice parameters: The effect of room acoustics and microphones. *Journal of Voice*, *34*(2), 320–334. https://doi.org/10.1016/j.jvoice.2018.10.016
5. Deliyski, D. D., Shaw, H. S., Evans, M. K., & Vesselinov, R. (2006). Regression tree approach to studying factors influencing acoustic voice analysis. *Folia Phoniatrica et Logopaedica*, *58*(4), 274–288. https://karger.com/fpl/article-abstract/58/4/274/140584/Regression-Tree-Approach-to-Studying-Factors
6. National Institute on Deafness and Other Communication Disorders (NIDCD). (n.d.). Taking care of your voice. https://www.nidcd.nih.gov/health/taking-care-your-voice
7. Pitchee. (2026). 《引导练习、复测比较与可信趋势》（Docs/Guided-Practice.md）：采集质量规则、削波比例阈值与基线排除行为的产品文档。https://github.com/project-pitchee/Pitchee-ios/blob/61454c9d9cc5589073e85b42a3f1f0f5cdb0924d/Docs/Guided-Practice.md
8. Sun, C., Wei, S., & Liu, B. (2026). Experimental investigation of a tubular front cavity for wind noise suppression in MEMS microphones of mobile devices. *Micromachines*, *17*(3), 357. https://doi.org/10.3390/mi17030357
