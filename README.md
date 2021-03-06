go-notify
=====================

[![go-notify](https://godoc.org/github.com/TheCreeper/go-notify?status.png)](http://godoc.org/github.com/TheCreeper/go-notify)

Package notify provides an implementation of the [Freedesktop Notifications Specification](https://developer.gnome.org/notification-spec/) using the DBus API.

## Example

```
package main

import (
	"log"

	"github.com/TheCreeper/go-notify"
)

func main() {

	ntf, err := notify.NewNotification("Test Notification", "This is a test notification")
	if err != nil {

		log.Fatal(err)
	}

	if _, err := ntf.Send(); err != nil {

		log.Fatal(err)
	}
}
```