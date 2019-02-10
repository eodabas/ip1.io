# ip1.io: Simple Wildcard DNS for any IP Address

(This service is a fork of nip.io service by xp-dev.com)

IP1.IO allows you to map any IP Address in the following DNS wildcard entries:

- **10.0.0.1.ip1.io** maps to **10.0.0.1**
- **10-0-0-1.ip1.io** maps to **10.0.0.1**
- **10.0.0.1.app.ip1.io** maps to **10.0.0.1**
- **10-0-0-1.app.ip1.io** maps to **10.0.0.1**
- **app.10.0.0.1.ip1.io** maps to **10.0.0.1**
- **app.10-0-0-1.ip1.io** maps to **10.0.0.1**
- **app.10.0.0.1.customer1.ip1.io** maps to **10.0.0.1**
- **app.10-0-0-1.customer2.ip1.io** maps to **10.0.0.1**
- **customer1.app.10.0.0.1.ip1.io** maps to **10.0.0.1**
- **customer2.app.10.0.0.1.ip1.io** maps to **10.0.0.1**
- **otherapp.10.0.0.1.ip1.io** maps to **10.0.0.1**

and also:

- **anythinghere.ip1.io** maps to **127.0.0.1**
- **app.anythinghere.ip1.io** maps to **127.0.0.1**

Basically IP1.IO maps `<anything>.<IP Address>.<anything>.ip1.io to` the corresponding `<IP Address>`, even `127.0.0.1.ip1.io` maps to `127.0.0.1`

This service is powered by [PowerDNS](http://www.powerdns.com/) with a simple, custom [PipeBackend](http://doc.powerdns.com/pipebackend-dynamic-resolution.html). 

The custom PipeBackend is a single script written in Python and the source can be found on XP-Dev.com.
