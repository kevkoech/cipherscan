CipherScan
==========
A very simple way to find out which SSL ciphersuites are supported by a target.

Run: ./CipherScan.sh www.google.com:443
And watch.

The newer your version of openssl, the better results you'll get. Older versions
of OpenSSL don't support TLS1.2 ciphers, elliptic curves, etc... Build Your Own!

Options
-------
Enable benchmarking by setting DOBENCHMARK to 1 at the top of the script.

Use '-v' to get more stuff to read.

Use '-a' to force openssl to test every single cipher it know.


Example
-------

```
$ ./CiphersScan.sh google.com:443
prio  ciphersuite                  protocol  pfs_keysize
1     ECDHE-RSA-AES128-GCM-SHA256  TLSv1.2   ECDH,P-256,256bits
2     ECDHE-RSA-RC4-SHA            TLSv1.2   ECDH,P-256,256bits
3     ECDHE-RSA-AES128-SHA         TLSv1.2   ECDH,P-256,256bits
4     AES128-GCM-SHA256            TLSv1.2
5     RC4-SHA                      TLSv1.2
6     RC4-MD5                      TLSv1.2
7     ECDHE-RSA-AES256-GCM-SHA384  TLSv1.2   ECDH,P-256,256bits
8     ECDHE-RSA-AES256-SHA384      TLSv1.2   ECDH,P-256,256bits
9     ECDHE-RSA-AES256-SHA         TLSv1.2   ECDH,P-256,256bits
10    AES256-GCM-SHA384            TLSv1.2
11    AES256-SHA256                TLSv1.2
12    AES256-SHA                   TLSv1.2
13    ECDHE-RSA-DES-CBC3-SHA       TLSv1.2   ECDH,P-256,256bits
14    DES-CBC3-SHA                 TLSv1.2
15    ECDHE-RSA-AES128-SHA256      TLSv1.2   ECDH,P-256,256bits
16    AES128-SHA256                TLSv1.2
17    AES128-SHA                   TLSv1.2
18    (NONE)
```
