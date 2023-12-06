
route

```yaml
  routes:
    - kind: Rule
      match: Host(`host`) && PathPrefix(`/api`)
      middlewares:
        - name: stripprefix-api
      services:
        - name: service-name
          port: 80
```
