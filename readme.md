# Report

## Three components of my solution

I started with the NGINX, GUNICORN configuration of the previous exercise of WINC (deployment)

* Github Actions:
With Github Actions you can make a workflow that automatically test and deploy your code to the VPS.
You have Marketplace where you can find tools to improve your workflow.

* DigitalOcean:
In the beginning I had the problem to make a account, because I don't have a creditcard. But after that was fixed, I make a droplet, that is Linux-based virtual machine (VM) and get started. It was a good experience for me, because you have to learn using linux and bash commands and so I am not "afraid" of CLI anymore! Removing files/directories etc.

* SSH keys:
I have create a SSH key on the VPS server for authentication between Github and VPS. I use this key for Github Actions. And was also stored in Secrets settings in Github account for safety reasons.

## Problems

* The connection to Github and VPS/DigitalOcean was a big problem. In earlier exercise (deployment) I have tried with SSH key to push to a repository on Github. But somehow I didn't work. So with this in my mind I went searching on google and on marketplace, where I find a student named appleboy. And with his github actions I managed to copy repository via scp to VPS and execute remote commands. So big thanks to him!!

* A little and stupid problem was that I sometimes directed to the wrong directory. But error show me that.

* A big issue for me was that I was extemely insecure about this module. So many times I have to do a step back and make a new plan. Also I have done some own exercise with Github Actions via youtube and the course CI/CD from codedamn.

Maybe for other students:
<https://codedamn.com/learn/github-actions-ci-cd/intro/introduction.OKhdTPUb09-B9bIzGM0Nl>

* Indentation Yaml problem:
When I tried multiple times to use indentation of 2 spaces in VSCode, I had a big problem. First VSCode formatted automatically to 4, settings.json changed and tabs into spaces. In VSCode 2 spaces. But there goes something wrong when pushing my code to github. My code on laptop was different than on Github. I don't know why exactly. Online yaml validator/linter tried and copy past and same problem. And yml workflow fails, through syntax error. So I decided to edit yml file directly in Github account en use git pull in VSCode. Now the code works with indentation of 2.

[![Run tests and deploy application to VPS](https://github.com/JEBesteman/CD-assignment/actions/workflows/workflow.yml/badge.svg?branch=main)](https://github.com/JEBesteman/CD-assignment/actions/workflows/workflow.yml)
