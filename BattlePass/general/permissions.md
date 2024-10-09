# Permissions

## `battlepass.use`

Give access to all default commands (/bp)

## `battlepass.block`

Blocks player from completing quests (requires `enable-ban-permission` enabled in `settings.yml`)

## `battlepass.admin`

Gives access to all admin commands (/bpa)

## Pass permission

Set the premium pass permission in the premium.yml as follows. Make sure to remove the # to enable the required-permission configuration.

```yaml
name: 'Premium :)'
default-points-required: 100
#required-permission: 'battlepass.premium'
```
