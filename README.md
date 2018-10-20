# -import requests

str = input("请输入需要翻译的内容")
data = {
    "i": str,
    "from":"AUTO",
    "to": "AUTO",
    "smartresult": "dict",
    "client":" fanyideskweb",
    "salt": "1539957487998",
    "sign": "80130c361c4de659ba0dd16de3599282",
    "doctype": "json",
    "version": "2.1",
    "keyfrom": "fanyi.web",
    "action": "FY_BY_REALTIME",
    "typoResult": "false",
    }
res = requests.post("http://fanyi.youdao.com/translate?smartresult=dict&smartresult=rule",data)
print(res.json()["translateResult"][0][0]["tgt"])
