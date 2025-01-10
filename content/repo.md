


ubuntu에서 mirro 방법
```
debmirror --verbose \
  --method=http \
  --host=kr.archive.ubuntu.com \
  --root=ubuntu \
  --dist=jammy \
  --section=main,restricted \
  --arch=amd64 \
  --nosource \
  --ignore-release-gpg \
  /data/ubuntu
debmirror --verbose \
  --method=http \
  --host=kr.archive.ubuntu.com \
  --root=ubuntu \
  --dist=jammy \
  --section=main,restricted,universe,multiverse \
  --arch=amd64 \
  --nosource \
  --ignore-release-gpg \
  /data/ubuntu
```
