# AF-
一个自定义填充化学式特征的即时软件
使用说明：


声明：本软件为学术交流所用，运行密码为ICQMSicqms，不允许以任何形式用于商业用途，所有学术用户拥有使用权，欢迎加入AF，提出修改意见和一起完善。



①本软件写成简单实用的exe程序，不需要其他支持环境，可在Win系统上直接使用。
②本软件为提取简单化学式特征使用，暂不支持-----”化学式中有括号，水合物符号，电子价等符号参与的化学式“若有特殊需求可联系作者，联系方式见控制台。
③特征维度的限制为1000维度，维度是自己定制的(维度跟随你的特征文件)，10000是每行最多的字符，可以使用我们提供的元素物理基本性质的特征文件，也可以自定义自己添加想要使用的特征。
④元素物理基本性质的特征文件，以magpie.csv为例(mapie的参考文献https://www.nature.com/articles/npjcompumats201628，这个csv我们采集了magpie中给出的元素基本物理量，具体特征见magpe原文）,请严格参照magpie.csv的文件输入格式，并在进行填充之前更正csv文件的名字为：Fillfeature.csv。
⑤确保Fillfeature.csv(特征文件)和data.csv(要求里面只有化学式这一列，无其他多余字符)与exe软件处在同一个文件夹中。
⑥运行软件，输入ICQMSicqms，得到out.csv文件，即提取化学式特征完成。
⑦本软件产生的特征为加权求和标量版，即对化学式中的元素基本性质根据化学计量数进行求和，可仿照example中有输入案例，将exe复制入文件夹运行，得到out文件。
⑧注意，当data.csv文件中出现了Fillfeature.csv没有的特征无法进行提取时，我们使用常见的填0的办法进行填充。
⑨特征文件中的特征填充请使用数字，如有字符等，请先自行分类用数字进行表征。





写在后面：
       在S2.0版本中我们考虑了加入一些数学上的平均值，均差值等特征指示，如有其他需要添加和更新的性质将在后续版本中更新；
       基于结构对特征采用独热编码的将仅制作在T(Tensor)版，该版本S(Scalar)版本，目标在于不考虑结构标量通用的描述符,T版本是为ABO3钙钛矿或者ABC型半哈斯勒等特定结构定制。
       有想要做出ST(structure)版本的想法，功能为可以读取DFT计算输入文件POSCAR来提取结构上的环境信息，将Coulomb matrix，SOAP等作为输出文件,但这些都在S和T版本稳定后再做打算。
