# CloudFront Exclude China IPs

在某些情况下使用 CloudFront CDN 需要剔除中国 IP 地址段。

获取最新的中国 IP 地址段：
```bash
wget https://raw.githubusercontent.com/17mon/china_ip_list/master/china_ip_list.txt
```

在 Amazon 给出 [CloudFront CDN 地址段列表](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/LocationsOfEdgeServers.html) 中获取最新的所有 IP 地址，例如：
```
{"CLOUDFRONT_GLOBAL_IP_LIST": ["120.52.22.96/27", "205.251.249.0/24", "180.163.57.128/26", "204.246.168.0/22", "111.13.171.128/26", "18.160.0.0/15", "205.251.252.0/23", "54.192.0.0/16", "204.246.173.0/24", "54.230.200.0/21", "120.253.240.192/26", "116.129.226.128/26", "130.176.0.0/17", "108.156.0.0/14" ...
```

用上面的地址替换 `main.py` 中已有的地址。

运行 `main.py`，剔除中国 IP 地址段后的地址段储存在 `filtered_ip_list.txt`。