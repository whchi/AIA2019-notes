[sli.do](https://app.sli.do/event/sfblyz4p/live/questions)

自建平台最基本的問題是資料是否可以上雲端
1. 政府法規
2. 公司同意

jupyter 底層用 zeroMQ 跟 kernel 溝通, kernel 相當於一個在 python daemon
storage 用 ceph
* ceph 的機制在如果 storage 沒有全壞的情況下指責其他 ceph
* [最小安裝](https://github.com/jupyterhub/the-littlest-jupyterhub), 彈性小
* [kubeflow](https://github.com/kubeflow/)
* [primeHub](https://github.com/InfuseAI/primehub)
