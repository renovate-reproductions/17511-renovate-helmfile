# 17511-renovate-helmfile

Renovate reproduction

Escaped helm templates are wrongly replaced, so yaml parsing fails

```yaml
namespace: {{`"{{request.object.metadata.name}}"`}}
```

is replaced to

```yaml
namespace: "`}}
```

see https://github.com/renovatebot/renovate/issues/17511
