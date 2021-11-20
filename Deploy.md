# 构建
```shell
# 安装wheel(python3 setup.py bdist_wheel 指令需要)
# pip install wheel

# 清除./dist/*, 并重新构建
rm -rf ./build && \
rm -rf ./dist && \
rm -rf ./grutils.egg-info && \
python3 setup.py sdist bdist_wheel && \
cp -r dist /Users/liuleidong/Downloads/SharedFromMac/grutils/
```

# 发布到pypi.org
```shell
# 安装twine
#pip install twine

twine upload --repository pypi dist/*
```
