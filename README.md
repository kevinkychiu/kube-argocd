~~~ shell
kubectl annotate applicationset rke2-appset \
    argocd.argoproj.io/refresh=true \
    -n argocd --overwrite

kubectl rollout restart deployment argocd-applicationset-controller -n argocd
~~~

~~~ shell
kubectl annotate applicationset rke2-appset \
    argocd.argoproj.io/refresh=hard \
    -n argocd --overwrite

kubectl rollout restart deployment argocd-applicationset-controller -n argocd
~~~

~~~ shell
kubectl logs -n argocd deployment/argocd-applicationset-controller
~~~