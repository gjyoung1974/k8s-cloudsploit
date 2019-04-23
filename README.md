## ACME cloudsploit scanner
CloudSploit is a security and configuration scanner that can detect hundreds of threats in your AWS account. Don't let a single misstep compromise your entire infrastructure.
## Installing the Chart

```
cd ACME.charts; ops/helm-package.sh;
helm install ./charts/k8s-cloudsploit-1.0.1.tgz --name cloudsploit --namespace=cloudsploit -f ./charts/k8s-cloudsploit/values.yaml
```

## Upgrade installed Chart

```
cd ACME.charts;
ops/helm-package.sh; helm upgrade cloudsploit -f ./charts/k8s-cloudsploit/values.yaml ./charts/k8s-cloudsploit-1.0.1.tgz
```

## Delete Chart

```
helm delete --purge cloudsploit;
```
or purge version as well
```
helm delete cloudsploit --purge
```

## List deployed Charts

```
helm list
```
or all
```
helm list -a
```

## Misc

These app runs in `cloudsploit`.    
The deployment script will create the namespace.


List kubernetes stuff   
```
kubectl get all --namespace cloudsploit 
```

2018 Gordon Young - gjyoung1974@gmail.com
