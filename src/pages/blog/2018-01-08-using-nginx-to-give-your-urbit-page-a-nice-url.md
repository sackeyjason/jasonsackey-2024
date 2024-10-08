---
title: "Using nginx to give your Urbit page a nice URL"
date: "2018-01-08"
categories: 
  - "address"
  - "cloud"
  - "network"
  - "operating-system"
  - "urbit"
  - "user"
  - "web"
tags: 
  - "nginx"
  - "server"
layout: "./_layout.astro"
---

Here's the newest component of my little media empire, a chat room:

chat.operatingspace.net (dead link removed)

It runs on Urbit, which is a fascinating, complex project which I'll sum up here as: a decentralised, programmable social network. This blog post is a tutorial for something I just learned how to do: set up nginx to give a nice URL to a page on my Urbit ship.

## Prerequisites

Details for getting here are beyond the scope of this post, but here are some helpful links:

- We have some cloud hosting (I use a 2048 MB server on [Vultr](https://www.vultr.com/?ref=7303314))
- We have a domain name (I use [Hover](https://hover.com/oZJOHHEz)) pointing to our server
- We've got an Urbit ship running on our server (see: [Install Urbit](https://urbit.org/docs/using/install/))
- We've got an [nginx](http://nginx.org/) server running there too
- The Urbit ship is [serving a web page](https://urbit.org/docs/using/web/)

(Those first two links are affiliate links.)

So we've got two servers, nginx and Urbit, running. We can see our urbit's web interface by going to `http://$ourdomain.net:8080`. We can get to the page of interest by appending `/pagename` or `/page/path` to that url.

E.g. [operatingspace.net:8080/chat/](http://operatingspace.net:8080/chat/)

Goal: get rid of the ':8080' there, and use 'chat' as a subdomain instead of a path.

## Procedure

We need nginx to be listening on port 80, the standard web port (so there's no need for any port number to be used in our url).

Edit the nginx config file, which is at `/etc/nginx/nginx.conf`.

Inside the http block, add a server block like this:

```
http {
  # (There'll be some stuff already here. Ignore it.)

  # (add this:)
  server {
    listen  80;
    server_name  nice-subdomain.your-domain.net;

    location = / {
      proxy_pass  http://localhost:8080/your-page;
    }

    location / {
      proxy_pass  http://localhost:8080;
    }
  }
}
```

Substitute 'nice-subdomain' with your preferred name, and substitute 'your-domain' and 'your-page' with the appropriate names according to your setup.

Save the file and reload nginx with our new config:

`$ service nginx reload`

**That should be all.** Getting here was a lot of trial and error for me, so I hope this post saves someone all that trouble. I am informed that a future Urbit update will make this all quite unnecessary, but some of us like to be early-adopters :)

If following these steps hasn't worked:

- Try [troubleshooting nginx](https://blog.serverdensity.com/troubleshoot-nginx/)
- Ensure your firewall isn't redirecting connections in an unwanted way -- [see the answer here](https://serverfault.com/questions/670575/failed-to-connect-to-127-0-0-1-port-80) (I had that issue on my server)

If I've missed something, please let me know so I can fix this post (while it's not yet obsolete). Feel free to [contact me](http://blog.operatingspace.net/contact/) -- pop into the [op-space chat room!](http://chat.operatingspace.net)

## Bonus: secure the connection with SSL

For maximal coolness, ensure a secure connection between client and server. You can get a free, automatically-updating certificate, and enable https on your page, with [Let's Encrypt](https://letsencrypt.org/getting-started/). The process is very streamlined with [Certbot](https://certbot.eff.org/).
