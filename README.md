<img src="https://raw.githubusercontent.com/Mazeorz/Clash.Tray/master/icon/Clash.Tray.png" height="100" width="100"> <h2>Format Akun Openclash</h2>
# Format Akun TROJAN
<pre>
1. Trojan GFW (SNI)
- name: Trojan GFW (SNI)
  type: trojan
  server: SERVER.COM
  port: 443
  password: PASSWORD
  udp: true
  sni: BUGSNI.COM
  skip-cert-verify: true

2. Trojan WS (SNI)
- name: Trojan WS (SNI)
  server: SERVER.COM
  port: 443
  type: trojan
  password: PASSWORD
  skip-cert-verify: true
  sni: BUGSNI.COM
  network: ws
  ws-opts:
    path: /PATH
    headers:
      Host: BUGSNI.COM
  udp: true

3. Trojan GO/WS (CDN)
- name: Trojan GO/WS (CDN)
  server: IPCDN/BUGCDN.COM
  port: 443
  type: trojan
  password: PASSWORD
  network: ws
  sni: SERVER.COM
  skip-cert-verify: true
  udp: true
  ws-opts:
    path: /PATH
    headers:
        Host: SERVER.COM

4. Trojan XTLS (SNI)
- name: Trojan XTLS (SNI)
  server: SERVER.COM
  port: 443
  type: trojan
  password: PASSWORD
  flow: xtls-rprx-direct
  skip-cert-verify: true
  sni: BUGSNI.COM
  udp: true

5. Trojan gRPC (SNI)
- name: Trojan gRPC (SNI)
  type: trojan
  server: SERVER.COM
  port: 443
  password: PASSWORD
  udp: true
  sni: BUGSNI.COM
  skip-cert-verify: true
  network: grpc
  grpc-opts:
    grpc-service-name: NAMAGRPC
</pre>
# Format Akun VMESS
<pre>
1. Vmess WS (SNI)
- name: Vmess WS (SNI)
  type: vmess
  server: SERVER.COM
  port: 443
  uuid: UUID
  alterId: 0
  cipher: auto
  udp: true
  tls: true
  skip-cert-verify: true
  servername: BUGSNI.COM
  network: ws
  ws-opts:
    path: /PATH
    headers:
      Host: BUGSNI.COM

2. Vmess WS (CDN)
- name: Vmess WS (CDN)
  type: vmess
  server: IPCDN/BUGCDN.COM
  port: 443
  uuid: UUID
  alterId: 0
  cipher: auto
  udp: true
  tls: true
  skip-cert-verify: true
  servername: SERVER.COM
  network: ws
  ws-opts:
    path: /PATH
    headers:
      Host: SERVER.COM

3. Vmess WS (CDN) Non TLS
- name: Vmess WS (CDN) Non TLS
  type: vmess
  server: IPCDN/BUGCDN.COM
  port: 80
  uuid: UUID
  alterId: 0
  cipher: auto
  udp: true
  tls: false
  skip-cert-verify: false
  servername: SERVER.COM
  network: ws
  ws-opts:
    path: /PATH
    headers:
      Host: SERVER.COM

4. Vmess gRPC (SNI)
- name: Vmess gRPC (SNI)
  server: SERVER.COM
  port: 443
  type: vmess
  uuid: UUID
  alterId: 0
  cipher: auto
  network: grpc
  tls: true
  servername: BUGSNI.COM
  skip-cert-verify: true
  grpc-opts:
    grpc-service-name: NAMAGRPC
</pre>
# Format Akun VLESS
<pre>
1. Vless WS (SNI)
- name: Vless WS (SNI)
  server: SERVER.COM
  port: 443
  type: vless
  uuid: UUID
  cipher: auto
  tls: true
  skip-cert-verify: true
  servername: BUGSNI.COM
  network: ws
  ws-opts:
    path: /PATH
    headers:
      Host: BUGSNI.COM

2. Vless WS (CDN)
- name: Vless WS (CDN)
  server: IPCDN/BUGCDN.COM
  port: 443
  type: vless
  uuid: UUID
  cipher: auto
  tls: true
  skip-cert-verify: true
  servername: SERVER.COM
  network: ws
  ws-opts:
    path: /PATH
    headers:
      Host: SERVER.COM

3. Vless WS (CDN) Non TLS
- name: Vless WS (CDN) Non TLS
  server: IPCDN/BUGCDN.COM
  port: 80
  type: vless
  uuid: 81f1f510-3ca7-4734-8956-0f4fce670af5
  cipher: auto
  tls: false
  skip-cert-verify: false
  servername: SERVER.COM
  network: ws
  ws-opts:
    path: /PATH
    headers:
      Host: SERVER.COM
  udp: true

4. Vless XTLS (SNI)
- name: Vless XTLS (SNI)
  server: SERVER.COM
  port: 443
  type: vless
  uuid: UUID
  cipher: auto
  tls: true
  flow: xtls-rprx-direct
  skip-cert-verify: true
  servername: BUGSNI.COM

5. Vless gRPC (SNI)
- name: Vless gRPC (SNI)
  server: SERVER.COM
  port: 443
  type: vless
  uuid: UUID
  cipher: auto
  tls: true
  skip-cert-verify: true
  servername: BUGSNI.COM
  network: grpc
  grpc-opts:
  grpc-mode: gun
  grpc-service-name: NAMAGRPC
  udp: true
</pre>
# Format Akun SOCKS5
<pre>
1. Socks5 (SNI)
- name: Socks5 (SNI)
  type: socks5
  server: SERVER.COM
  port: 443
  username: USERNAME
  password: PASSWORD
  tls: true
  skip-cert-verify: true
  udp: true
  sni: BUGSNI.COM
</pre>
# Format Akun SHADOWSOCKS
<pre>
1. Shadowsocks Tanpa Plugin
- name: Shadowsocks Tanpa Plugin
  type: ss
  server: SERVER.COM
  port: 34963
  cipher: chacha20-ietf-poly1305
  password: PASSWORD
  udp: true
  
2. Shadowsocks Plugin Obfs
- name: Shadowsocks Plugin Obfs
  type: ss
  server: SERVER.COM
  port: 32033
  cipher: chacha20-ietf-poly1305
  password: PASSWORD
  plugin: obfs
  plugin-opts:
    mode: tls
    host: BUGSNI.COM
</pre>
# Format Akun SHADOWSOCKSR
<pre>
1. ShadowsocksR (SNI)
- name: ShadowsocksR (SNI)
  server: SERVER.COM
  port: 1235
  type: ssr
  cipher: AES-256-CTR
  password: PASSWORD
  protocol: origin
  obfs: tls1.2_ticket_auth
  protocol-param: "#"
  obfs-param: BUGSNI.COM
  udp: true
</pre>
# Format Akun SNELL
<pre>
1. Snell V3 (Support UDP)
- name: Snell V3
  type: snell
  server: SERVER.COM
  port: 33223
  psk: PASSWORD
  version: 3
  udp: true
  obfs-opts:
    mode: tls
    host: BUGSNI.COM
</pre>
