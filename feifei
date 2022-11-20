proxies:
  - name: "菲菲"
    type: hysteria
    server: sharehy1.giize.com
    port: 2022
    auth_str: sharehy1
    alpn:
      - h3  
    protocol: udp          
    up: 12          
    down: 62       
    
proxy-groups:
  - name: PROXY 
    type: select
    proxies:
      - 菲菲
      
      
rules:
  - DOMAIN-SUFFIX,bilibili.com,DIRECT,tcp
  - DOMAIN,google.com,PROXY
  - DOMAIN-KEYWORD,baidu,DIRECT
  - IP-CIDR,127.0.0.0/8,DIRECT
  - SRC-IP-CIDR,192.168.0.0/16,DIRECT
  - DST-PORT,3389/445,DIRECT
  - GEOSITE,category-ads-all,REJECT
  - GEOSITE,icloud@cn,DIRECT
  - GEOSITE,apple@cn,DIRECT
  - GEOSITE,apple-cn,DIRECT
  - GEOSITE,microsoft@cn,DIRECT
  - GEOSITE,geolocation-cn,DIRECT
  - GEOSITE,geolocation-!cn,PROXY
  - GEOIP,private,DIRECT,no-resolve
  - GEOIP,cn,DIRECT

  - MATCH,PROXY
