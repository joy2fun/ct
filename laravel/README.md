
route

```yaml
ingressRoute:
  additionalRoutes:
    - kind: Rule
      match: Host(`host`) && PathPrefix(`/api`)
      middlewares:
        - name: stripprefix-api
      services:
        - name: service-name
          port: 80
```

service ports

```yaml
service:
  additionalPorts:
    - port: 81
      targetPort: 81
      protocol: TCP
      name: backend
```
