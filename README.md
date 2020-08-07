# wpatent
write patent

## 思路
1. 自动把思路稿转为方案书初稿。
    * 把标题，框架，常用术语定义好。
    * 把内容分布填充在合适的位置。
    * 留出补充内容的位置。
    * 生成填空类型的模板，为直接生成权利要求书做准备。
    * 抽象出顺序步骤的叙述方法，做好完形填空的模板。
    * 提示填充内容的角度。

2. 自动把方案书转为权利要求书。
    * 把标题，框架，常用术语定义好。
    * 抽取方案书的内容填充权利要求书的内容。
    * 自动识别术语的指代，做文本转换。
    * 生成接近终稿的权利要求书。

## 方案思考

* 让用户填写的方案书的形式是怎样的？
    - 问答题的形式，一道题一道题回答，回答到指定位置。
    - 生成权利要求书的时候则直接用答案即可。
    - 生成方案书直接用答案拼接即可。
    - 问答题的形式，即问答卷。

* 首先定义问答题的问题，这些问题对完成方案书和权利要求书都能自动生成。
* 然后自动冲思路稿中抽取内容回答各个问题，形成问答卷初稿。
* 最后人工核对补充内容，修改内存，形成问答卷终稿。
* 自动从问答卷中抽取内容，生成方案稿。方案稿即终稿，不用人工修改。
* 自动从问答卷中抽取内容，生成权利要求书。权利要求书需要人工核对修改。
* 填写问答卷的时候需要明确的标示步骤的关系，明确输入和输出。
* 用唯一标记表示各个步骤的输入输出，及连接关系。


## 问答卷设计
### 框架
1. 标题

2. 背景技术
    * 背景介绍。
    * 问题描述。
    * 引用专利。
    * 有益效果。

3. 步骤
    * 步骤序号。
    * 步骤一句话介绍。
    * 步骤概述。
    * 步骤详细介绍。
    * 步骤举例。

### 框架说明
1. 标题

2. 背景技术
    * 背景介绍。
        - 时代背景。
        - 技术背景。
    * 问题描述。
        - 需求问题。
        - 技术缺陷问题。
        - 不够好的问题。
    * 引用专利。
        * 引用专利的简介。
            - 专利号和专利名称。
            - 专利方法流程。
        * 引用专利的优点。
            - 专利的好处。
            - 专利解决的问题。
        * 引用专利的缺点。
            - 专利没有解决但是本方法可以解决的问题。
            - 专利没有达到的效果。
        * 需要本方法的原因。
            - 当前方法达不到的效果。
            - 引用专利忽视的问题。
    
    * 有益效果
        * 本方法的优点。
        * 本方法解决的问题。
        * 本方法达到的效果。

3. 步骤
    * 步骤序号。
    * 步骤一句话描述。
        - 表达清楚输入和输出。
        - 一句话介绍怎样从输入处理到输出。
    * 步骤概述。
        - 步骤一句话描述的具体介绍。
        - 介绍清楚输入来源和特点。
        - 叙述怎样处理输入得到输出。
        - 介绍清楚明确的输出。
    * 步骤详细介绍。
        - 步骤概述的具体化。
        - 补充说明技术细节。
        - 说明操作的原因和达到的效果。
    * 步骤举例。
        - 举例具体的输入，有具体的数量，具体的特点。
        - 具体的数据流向过程，具体的数字计算结果。
        - 具体得到的输出，输出的数量。
        - 必要情况，举例细节例子，例如一条数据的流向。
        - 如果有多个分支，举例各个分支的例子。


## 工作流程
1. 人工微调思路稿，按照问题的答案分句分段。
    * 避免一个句号的内容包含两个问题的答案，如果这样，则需人工在合适的地方把逗号改为句号。
    * 一个段回答一个问题，人工敲换行键换行。
    * 在每个大问题前加关键字，如果已经有关键字则不需重复加。
        - 关键字有：标题，背景技术，有益效果，步骤。
        - 如果标题在第一行，则标题关键字可以不加。

2. 把微调的思路稿输入问答卷转换系统，转换为问答卷初稿。
3. 人工完善问答卷初稿内容，补充内容，修改错位的答案，调整顺序。
4. 把问答卷输入方案稿转换系统，转换为方案稿终稿。
5. 把问答卷输入专利交底书转换系统，转换为专利交底书初稿。
6. 人工检查内容，增删改查。
