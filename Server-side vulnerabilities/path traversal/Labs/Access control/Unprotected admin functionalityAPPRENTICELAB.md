

![](../../../../attachments/Pasted%20image%2020261105191031.png)


```
https://0a5f00e303cf590c82f0bf710095004d.web-security-academy.net/robots.txt
```


Now we know what too look for 
## What `robots.txt` means (short)

`robots.txt` is **not an acronym** — it means a plain-text file for **robots/web crawlers**. It sits at a site’s root and tells bots **which pages they may or may not crawl**.

- **Location:** `https://example.com/robots.txt`
- **Purpose:** guide search-engine crawlers
- **Important:** it’s a **voluntary convention**, not security — bad bots can ignore it

### Sample

```txt
# robots.txt for https://example.com

User-agent: *
Disallow: /admin/
Disallow: /private/
Allow: /public/

Sitemap: https://example.com/sitemap.xml
```

### What the sample means

| Directive | Meaning |
|---|---|
| `User-agent: *` | Applies to all crawlers |
| `Disallow: /admin/` | Don’t crawl `/admin/` |
| `Disallow: /private/` | Don’t crawl `/private/` |
| `Allow: /public/` | `/public/` is allowed |
| `Sitemap: ...` | Points bots to the sitemap |

**In one line:** `robots.txt` is a simple text file that politely tells web crawlers what they can and cannot crawl.


![](../../../../attachments/Pasted%20image%2020261105191244.png)


![](../../../../attachments/Pasted%20image%2020261105192226.png)




![](../../../../attachments/Pasted%20image%2020261105192258.png)








