cd /usr/local/src
git clone https://github.com/shinsakukataoka/arm-memcached.git
Do not do this: ln -s /lib/aarch64-linux-gnu/libevent-2.1.so.7.0.1 /lib/aarch64-linux-gnu/libevent-2.1.so.6
cd /usr/local/src/arm-memcached
cd memcached
./memcached -d -t 2 -m 2040 -n 550 -u nobody
cd ../memcached-loadtester
chmod +x entrypoint.sh
./enetrypoint.sh --m="W" --S=28 --D=10240 --w=8 --T=2
