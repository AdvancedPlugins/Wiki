# Permissions

## `battlepass.use`

Give access to all default commands (/bp)

## `battlepass.admin`

Gives access to all admin commands (/bpa)

## Pass permission

Set the premium pass permission in the premium.yml as follows. Make sure to remove the `#` to enable the required-permission configuration.

**Example:**

```yaml
name: 'Premium :)'
default-points-required: 100
required-permission: 'battlepass.premium'
```

It will disable `/bpa set pass` command and will give premium pass to all players with `battlepass.premium` permission
