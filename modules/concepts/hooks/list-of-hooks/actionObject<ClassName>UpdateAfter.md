---
Title: actionObject<ClassName>UpdateAfter
hidden: true
hookTitle: 
files:
    -
        url: 'https://github.com/PrestaShop/PrestaShop/blob/8.0.x/classes/ObjectModel.php'
        file: classes/ObjectModel.php
locations:
    - 'back office'
    - 'front office'
type: action
hookAliases: 
array_return: false
check_exceptions: false
chain: false
origin: core
description: ''

---

{{% hookDescriptor %}}

## Call of the Hook in the origin file

```php
Hook::exec('actionObject' . $this->getFullyQualifiedName() . 'UpdateAfter', ['object' => $this]);
```

## Example implementation

In this example, we dump the product object after the changes have been saved: 

First you need to hook your module during installation.
```php
public function install()
{
    return parent::install() 
        && $this->registerHook('actionObjectProductUpdateAfter')
        ;
}
```

Then you need to add the function that is called when the hook is triggered.
```php
public function hookActionObjectProductUpdateAfter($params)
{
    dump($params['object']);
}
```
