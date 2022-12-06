# VLESS over TCP with TLS + 回落 & 分流 to WebSocket（进阶配置）


This is a superset of the simplest configuration, using the powerful fallback and distribution features of VLESS to realize the perfect coexistence of port 443 VLESS over TCP with TLS and any WSS

This configuration is for reference. You can replace VLESS on WS with any other protocol such as VMess, and set more PATHs and protocol coexistence.

After deployment, you can connect to the server through VLESS over TCP with TLS and any WebSocket with TLS at the same time, the latter of which can be through CDN

According to the actual measurement, the performance of VLESS fallback shunt WS is stronger than that of Nginx reverse generation WS. The traditional VMess + WSS solution can be completely migrated without loss of compatibility.


这里是 [最简配置](<../VLESS-TCP-TLS%20(minimal%20by%20rprx)>) 的超集，利用 VLESS 强大的回落分流特性，实现了 443 端口 VLESS over TCP with TLS 和任意 WSS 的完美共存

该配置供参考，你可以将 WS 上的 VLESS 换成 VMess 等其它任何协议，以及设置更多 PATH、协议共存，都可以做到

部署后，你可以同时通过 VLESS over TCP with TLS 和任意 WebSocket with TLS 方式连接到服务器，其中后者都可以通过 CDN

经实测，VLESS 回落分流 WS 比 Nginx 反代 WS 性能更强，传统的 VMess + WSS 方案完全可以迁移过来，且不失兼容
