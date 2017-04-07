## 游戏对局数据获取

#### 国服：腾讯游戏平台非官方API - http://www.games-cube.com/

|游戏版本|游戏模式|艾欧尼亚|诺克萨斯|黑色玫瑰|扭曲丛林|合计|数据预处理|
| ------- | ------------ | -------- | -------- | -------- | -------- | -------- | ------------------------------ |
|6.23|极地大乱斗|108155|67753|-|209911|385819|去除未满级对局|
|6.24|极地大乱斗|187479|130584|-|191964|510027|去除未满级对局<br>去除战绩异常对局|
|7.4|无限乱斗|10335|-|7681|18587|36603|去除战绩异常对局|

#### 外服：Riot开发者平台API - https://developer.riotgames.com/

|游戏版本|游戏模式|美服|西欧服|韩服|合计|数据预处理|
| ------- | ------------ | -------- | -------- | -------- | -------- | ------------------------------ |
|7.6|排位赛(单/双排)|56240|70154|66113|192507|去除开局掉线投降对局|
|7.6|经典匹配|44666|47303|34778|126747|去除开局掉线投降对局|
|7.6|极地大乱斗|35372|37318|30152|102842|-|

## 游戏对局胜负预测

### 根据双方英雄阵容，预测获胜方的准确率（%）

|游戏版本|游戏模式|随机森林|AdaBoost|XGBoost|支持向量机|Logistic回归|神经网络|
| ------ | ------------ | -------- | -------- | -------- | -------- | -------- | -------- |
|6.23|极地大乱斗| 65.8 | 67.9 | 68.0 | 68.0 | 67.9 | **69.2** |
|6.24|极地大乱斗| 65.5 | 67.3 | 67.5 | 67.3 | 67.3 | **68.6** |
|7.4|无限乱斗| 61.8 | 64.4 | 63.3 | 64.1 | 64.2 | **64.5** |
|7.6|排位赛(单/双排)| 52.8 | 54.8 | 54.7 | 54.7 | 54.9 | 54.8 |
|7.6|经典匹配| 52.9 | 54.4 | 54.3 | 54.3 | 54.5 | 54.5 |
|7.6|极地大乱斗| 63.9 | 66.2 | 65.5 | 66.0 | 66.2 | **66.9** |

### 只根据本方英雄阵容，预测本方能否获胜的准确率（%）				

|游戏版本|游戏模式|随机森林|AdaBoost|XGBoost|支持向量机|Logistic回归|神经网络|
| ------ | ------------ | -------- | -------- | -------- | -------- | -------- | -------- |
|6.23|极地大乱斗| 59.7 | 62.2 | 62.3 | - | 62.2 | **62.9** |
|6.24|极地大乱斗| 59.3 | 61.8 | 62.0 | - | 61.8 | **62.3** |
|7.4|无限乱斗| 58.3 | 60.5 | 60.0 | 60.6 | 60.6 | **60.6** |
|7.6|排位赛(单/双排)| 51.3 | 53.4 | 53.0 | - | 53.4 | 53.4 |
|7.6|经典匹配| 51.6 | 53.5 | 53.4 | - | 53.5 | 53.8 |
|7.6|极地大乱斗| 59.0 | 61.3 | 61.3 | - | 61.3 | **62.1** |
