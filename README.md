# hagezi-mihomo-rule-sets
Converted hagezi blocklists to mrs format for mihomo.
Choose the right versions for you here: [Hagezi README](https://github.com/hagezi/dns-blocklists/blob/main/README.md)

You can view the files [here](https://github.com/awesfdawe/hagezi-mihomo-rule-sets/tree/main/hagezi)
## Example (pro + tif)
```yaml
rule-providers:
  hagezi-pro:
    type: http
    behavior: domain
    format: mrs
    url: https://raw.githubusercontent.com/awesfdawe/hagezi-mihomo-rule-sets/main/hagezi/pro.mrs
    interval: 86400
  hagezi-tif:
    type: http
    behavior: domain
    format: mrs
    url: https://raw.githubusercontent.com/awesfdawe/hagezi-mihomo-rule-sets/main/hagezi/tif.mrs
    interval: 86400

rules:
  - RULE-SET,hagezi-pro,REJECT
  - RULE-SET,hagezi-tif,REJECT
  - MATCH,DIRECT
```
## JSDeliver Example (pro + tif)
```yaml
rule-providers:
  hagezi-pro:
    type: http
    behavior: domain
    format: mrs
    url: https://cdn.jsdelivr.net/gh/awesfdawe/hagezi-mihomo-rule-sets@main/hagezi/pro.mrs
    interval: 86400
  hagezi-tif:
    type: http
    behavior: domain
    format: mrs
    url: https://cdn.jsdelivr.net/gh/awesfdawe/hagezi-mihomo-rule-sets@main/hagezi/tif.mrs
    interval: 86400

rules:
  - RULE-SET,hagezi-pro,REJECT
  - RULE-SET,hagezi-tif,REJECT
  - MATCH,DIRECT
```
