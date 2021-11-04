# SIMPLE GIT PUSHER

Usage:
```
push "this is my comment"
```

install
```
curl https://raw.githubusercontent.com/rhelsing/pusher/master/push -o /usr/local/bin/push
chmod 755 /usr/local/bin/push
# reload shell
```

script contents:
```
#!/bin/bash
git pull origin $(git symbolic-ref --short HEAD)
git add -A && git commit -am "$1"
git push origin $(git symbolic-ref --short HEAD)
```
