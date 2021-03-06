---
layout: "cloudstack"
page_title: "CloudStack: cloudstack_ssh_keypair"
sidebar_current: "docs-cloudstack-resource-ssh-keypair"
description: |-
  Creates or registers an SSH key pair.
---

# cloudstack\_ssh\_keypair

Creates or registers an SSH key pair.

## Example Usage

```
resource "cloudstack_ssh_keypair" "default" {
  name = "myKey"
}
```

## Argument Reference

The following arguments are supported:

* `name` - (Required) The name of the SSH key pair. This is a unique value
    within a CloudStack account. Changing this forces a new resource to be
    created.

* `public_key` - (Optional) The path to a public key that will be uploaded
    the remote machine. If this is omitted, CloudStack will generate a new
    key pair. Changing this forces a new resource to be created.

## Attributes Reference

The following attributes are exported:

* `id` - The key pair ID.
* `fingerprint` - The fingerprint of the public key specified or created.
* `private_key` - The private key generated by CloudStack. Only available
    if CloudStack generated the key pair.
