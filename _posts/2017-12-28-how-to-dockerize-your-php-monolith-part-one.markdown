---
layout: post
title:  "How to dockerize your old PHP monolith - part one"
img: posts/how-to-dockerize-php-monolith.png
categories: php, docker
---

This post does not pretend to be your definitive guide to docker, it’s just my own experience.
What about environments?
Local environment: a virtual machine with software installed manually.
PHP 5.5, MariaDb 5.5, Sphinx and Redis. Each dev had it own personalization in virtual machine.

Production environment: same software as local env, same minor versions, but different bugfixes. Big differences between configs.

### Changes in code
Is your code prepared to support multiple environments? If answer is no, here is a possible solution for you.
1. Choose a way to manage your environment variables: [DotEnv](https://symfony.com/doc/current/components/dotenv.html) with plane php or [Symfony Config](https://symfony.com/doc/current/components/config.html).
2. In my case I chose DotEnv. Create a .env.* file for each environment, example: .env.dev, .env.pre, .env.prod
3. 

### Useful links

* [Using DotEnv (.env) in your Symfony project](http://www.oliveradria.com/dotenv-symfony-project/)
