# Cutting a new release

* Create a new release branch: `git checkout -b upgrade k8s-to-vx.x.x`
* Edit `k3s` version in [10-k3s/Dockerfile](images/10-k3s/Dockerfile):
```bash
ENV VERSION vx.x.x+xxx
```
* run `make`
* tag docker image with version label: `docker tag k3os:latest jeffherald/k3os:<release tag>`
* push to dockerhub: `docker push jeffherald/k3os:<release tag>`
* tag release in git: `git tag <releae tag>` ex. v0.28.5-k3s1r0
* push tag: `git push origin <release tag>`
* navigate to the github [releases](https://github.com/jeffherald/k3os/releases) page and click `Draft a new release`
* choose the release tag in `Choose a tag` dropdown, enter title and description and attach binaries and click `Publish release`
