# project
# 练习项目
# 正则应用
import re
html = '''
<div><p>九霄龙因惊天变</p></div>
<div><p>风云机会潜水游</p></div>
'''
# 贪婪匹配
pattern = re.compile('<div><p>.*</p></div>',re.S)
r = pattern.findall(html)
print(r)
# 非贪婪匹配
pattern = re.compile('<div><p>.*?</p></div>',re.S)
r = pattern.findall(html)
print(r)
