# Network Diagnostic Test

* Download the file.


* Make the file executable
chmod 777 ndt-server

It should resemble below
bin$ ls -l ndt-server 
-rwxr-xr-x 1 aloswain eng 20070320 Feb  7 01:20 ndt-server


* Execute file
bin$ ./ndt-server -ndt5.protocol.verbose=true
2020/02/17 19:58:57 argsfromenv.go:38: Argument cert=
2020/02/17 19:58:57 argsfromenv.go:38: Argument datadir=/var/spool/ndt
2020/02/17 19:58:57 argsfromenv.go:38: Argument key=
2020/02/17 19:58:57 argsfromenv.go:38: Argument ndt5.protocol.verbose=true
2020/02/17 19:58:57 argsfromenv.go:38: Argument ndt5_addr=:3001
2020/02/17 19:58:57 argsfromenv.go:38: Argument ndt5_ws_addr=127.0.0.1:3002
2020/02/17 19:58:57 argsfromenv.go:38: Argument ndt5_wss_addr=:3010
2020/02/17 19:58:57 argsfromenv.go:38: Argument ndt7_addr=:443
2020/02/17 19:58:57 argsfromenv.go:38: Argument prometheusx.listen-address=:9990
2020/02/17 19:58:57 argsfromenv.go:38: Argument uuid-prefix-file=rch-ads-210_1556553491_unsafe
2020/02/17 19:58:57 ndt-server.go:134: About to listen for unencrypted ndt5 NDT tests on 127.0.0.1:3002
2020/02/17 19:58:57 ndt-server.go:170: Cert="" and Key="" means no TLS services will be started.


* If fails check all libraries are properly linked
/bin$ ldd ndt-server 
	linux-vdso.so.1 =>  (0x00007ffc67440000)
	libpthread.so.0 => /lib64/libpthread.so.0 (0x000000361e000000)
	libc.so.6 => /lib64/libc.so.6 (0x000000361d800000)
	/lib64/ld-linux-x86-64.so.2 (0x00005609ec882000)
