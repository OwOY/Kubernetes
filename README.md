<p align="center">
    <img src="img/logo.png">
</p>

# Introduction
..待補

# How to use
## AKS Setting
1. 登入  
    ```
    az login --tenant <TenantID>
    ```
2. 取得受控 Kubernetes 叢集的存取認證  
    --resource-group > 資源群組的名稱  
    --name > 受控叢集的名稱
    ```
    az aks get-credentials --resource-group <MyGroup> --name <MyCluster>
    ```
## K8S Use
- 執行操作  
    ## kubectl config  
    - 取得所有Context
    ```
    kubectl config get-contexts
    ```
    - 使用指定Context
    ```
    kubectl config use-context <ContextName>
    ```
    - 查看當前Context
    ```
    kubectl config current-context
    ```
    ## kubectl get
    - 取得所有pods
    ```
    kubectl get pods -A
    ```
    ## kubectl log
    - 查看log
    ```
    kubectl logs -f <PodName> -n <NameSpace>
    ```
