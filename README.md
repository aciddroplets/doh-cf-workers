# doh-cf-workers
A very minimalist DNS-over-HTTPS proxy on Cloudflare Workers that randomly pick a server using the OISD list. I don't think there's actually any point for someone to use this, for starters you're probably better off just picking one of the servers since the subtle behavior differences between the servers might make debugging harder. For a blocked domain, DNSWarden, ControlD, and RethinkDNS return a null address with one hour, one minute, and 5 minutes TTL respectively, while AhaDNS responds with REFUSED.

I also can't get the Deploy button to work specifically for a branch, and since I don't think this warrant its own repo, I'll just leave it here as a proof of concept. Note that the workflow works too, so if you manually run the workflow from the Action tab after using the Deploy button on the main branch, and then pick this branch, you'll get a separate Workers instance that uses the random OISD logic.
