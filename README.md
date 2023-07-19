# b8g
B8G - Big Engine

```bash
(DIR=b8g; mkdir -p $DIR && curl -s -L https://github.com/just-js/just/archive/current.tar.gz | tar -xvz -C $DIR --strip-components 1)
make -C b8g runtime-static

# export the just home directory
export JUST_HOME=$(pwd)/b8g
export JUST_TARGET=$JUST_HOME

# Install to /usr/local/bin
make -C b8g install

# or if you don't want to install, add JUST_HOME to SPATH
export PATH=$PATH:$JUST_HOME
```

smol === just b8g without libs

```
git clone https://github.com/lemanschik/v8-component-system
make -C v8-component-system builtins.o compile main debug
## or
make -C v8-component-system all
```
