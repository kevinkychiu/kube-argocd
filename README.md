~~~ shell
kubectl annotate applicationset rke2-appset \
    argocd.argoproj.io/refresh=true \
    -n argocd --overwrite

kubectl rollout restart deployment argocd-applicationset-controller -n argocd
~~~
