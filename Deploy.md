# 构建
- 在 gr.py3.utils/grutils/__init__.py 更新版本号
```shell
# 安装wheel(python3 setup.py bdist_wheel 指令需要)
# pip install wheel

# 清除./dist/*, 并重新构建
rm -rf ./build && \
rm -rf ./dist && \
rm -rf ./grutils.egg-info && \
python3 setup.py sdist bdist_wheel
```

# 发布到pypi.org
```shell
# 安装twine
#pip install twine

# 现在不能使用密码来发布包(https://pypi.org/manage/account/token/)
# 需要使用api token
# 提示username时填写: __token__
# 提示password时填写网站上设置的api token
twine upload --repository pypi dist/*
```
