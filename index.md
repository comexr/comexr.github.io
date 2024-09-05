---
layout: home
title: Comexr Website
---
### Add a Debian Repository

Download the [public key](terminate-notice.gpg) and put it in
`/etc/apt/keyrings/terminate-notice.asc`. You can achieve this with:

```
wget -qO- {{ site.url }}/comexr.asc | sudo tee /etc/apt/keyrings/comexr.asc >/dev/null
```

Next, create the source in `/etc/apt/sources.list.d/`

```
echo "deb [arch=all signed-by=/etc/apt/keyrings/comexr.asc] {{ site.url }}/deb stable main" | sudo tee /etc/apt/sources.list.d/comexr.list >/dev/null
```

Then run `apt update && apt install -y` followed by the names of the packages you want to install.

### Add a RPM Repository

Download the repo file `cd /etc/yum.repos.d ; curl {{ site.url }}/comexr.repo -LO`

Then you can do `yum install -y` followed by the names of the packages you want to install.
