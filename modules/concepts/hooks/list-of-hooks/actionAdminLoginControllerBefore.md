---
menuTitle: actionAdminLoginControllerBefore
Title: actionAdminLoginControllerBefore
hidden: true
hookTitle: Perform actions before admin login controller initialization
files:
  - controllers/admin/AdminLoginController.php
locations:
  - back office
type: action
hookAliases:
---

# Hook actionAdminLoginControllerBefore

## Information

{{% notice tip %}}
**Perform actions before admin login controller initialization:** 

This hook is launched before the initialization of the login controller
{{% /notice %}}

Hook locations: 
  - back office

Hook type: action

Located in: 
  - [https://github.com/PrestaShop/PrestaShop/blob/8.0.x/controllers/admin/AdminLoginController.php](controllers/admin/AdminLoginController.php)

## Call of the Hook in the origin file

```php
Hook::exec(
            'actionAdminLoginControllerBefore',
            [
                'controller' => $this,
            ]
        )
```