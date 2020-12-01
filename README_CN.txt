# Update For Azure China

### mainTemplate.json

1、_artifactsLocation: "https://costmanagement.s3.cn-northwest-1.amazonaws.com.cn/azure-marketplace/src/"（GitHub原始地址的usercontent DNS解析不稳定）
2、esVersion： 增加“7.9.3”和“7.10.0”版本支持，修改defaultValue为 “7.9.3”
3、vmSizeKibana、vmSizeMasterNodes、vmSizeDataNodes的defaultValue修改为：Standard_A2_v2



**ps：部署前请注意**

* _artifactsLocation在项目执行过程中可以替换为自己的私有地址，脚本文件能被azure portal公开访问即可。
* vmSize* 参数，请在实际部署时，核对目标区域是否支持该实例类型。
* 部署时尽量采用新创建资源组的方式，便于撤销操作等
* 若部署出现问题，可检查具体报错内容，手动进行集群选举即可。
* adminPassword 该参数虽然未加*标志，但是为必填项目

