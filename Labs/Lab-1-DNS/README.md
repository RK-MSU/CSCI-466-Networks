# Lab 1 - DNS

## ipconfig/ifconfig

**Empty DNS cache in your host**:

```bash
sudo systemd-resolve --flush-caches
--- or
sudo resolvectl flush-caches
```

**Check Stats**:

```bash
sudo systemd-resolve --statistics
```

<details>
<summary>
  systemd-resolve --statistics
</summary>
DNSSEC supported by current servers: no

Transactions             
Current Transactions: 0  
  Total Transactions: 758
                         
Cache                    
  Current Cache Size: 0  
          Cache Hits: 506
        Cache Misses: 287
                         
DNSSEC Verdicts          
              Secure: 0  
            Insecure: 0  
               Bogus: 0  
       Indeterminate: 0  
</details>
