---
title: "How to connect Github Pages to Custom Domain"
pubDate: 'Jan 15 2023'
description: ""
tags: ["Domain","Github Pages","namecheap","tutorial","Tips"]
heroImage: "https://images.unsplash.com/photo-1618401471353-b98afee0b2eb?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1488&q=80"
# images is optional, but needed for showing Twitter Card
images: []
categories:
comment: true
draft: false
---

## Intro

This is showing how to link Github Pages to a Custom Domain, I am using namecheap here. Others, e.g. GoDaddy… can apply the same method.

## Steps

1. Buy a domain
2. In Github repository Settings, then Click Page, add the domain you purchased to the ‘Custom domain box’ (no ‘www’)
3. Enforce HTTPS (Github) (Optional)
4. Go Dashboard (make sure NAMESERVERS of the domain is set to Basic DNS)
5. Click ‘Mange’ button of the domain name you choose
6. Click Advanced DNS
7. For the HOST RECORDS, Add new records
    - Type = CNAME * 1
        - Host = www
        - Value = username.github.io
        - TTL = Automatic
    - Type = A Records(@) * 4
        - Host = @
        - Value = 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153
        - TTL = Automatic

    Values might have changed since the time of writing. Check [offical docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site#configuring-an-apex-domain) for the most up-to-date values.

8. Remove old Records
9. Done. Visit to the domain and be patient!
