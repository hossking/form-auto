# 今日校园疫情上报表单自动填写
## 介绍
- 该脚本适用于今日校园自动疫情上报，基于https://github.com/Itswag/cpdaily_submit 开发优化，在此基础上修改了请求host和对应的表单内容。
- 深信息的学生只需要修改学号和密码即可使用，其他学校的学生修改参数也可以使用。
- 如果问卷内容改变，需对第152行至163行的表单过滤进行修改。
## 使用说明
### 深信息学生：
- 修改第22、23行的学号和信息门户密码,
```
xh = 'xxx'  # 学号 自行修改
pwd = 'xxx'  # 密码 自行修改
```
- 在装有python环境的机器运行以下命令
```
pip install -r requirements.txt
python form-auto.py
```
### 其他学校学生：
- 替换学号和密码
- 将代码中的'sziit'全局替换为自己学校的host
- 抓包获取上报表单的相关参数，相关教程可以自行baidu/google，参考https://github.com/ZimoLoveShuang/auto-submit

## 注意
- 可搭配windows计划任务或者linux定时任务实现自动填写提交
- 学校下发的问卷内容有时会改变，建议设置自动填写时间为发布的后两小时
- 代码仅供学习参考，不得用于其他用途

