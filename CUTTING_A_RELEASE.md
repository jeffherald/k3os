# Cutting a new release

* Create a new release branch: `git checkout -b upgrade k8s-to-vx.x.x`
* Edit `k3s` version in [10-k3s/Dockerfile](images/10-k3s/Dockerfile):
```bash
ENV VERSION vx.x.x+xxx
```