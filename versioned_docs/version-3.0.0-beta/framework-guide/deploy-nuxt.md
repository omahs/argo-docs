---
id: deploy-nuxt
title: How to Deploy a Nuxt.js Site with Spheron
sidebar_label: Deploy Nuxt.js App
slug: /framework-guide/deploy-nuxt
---

This guide will show you how to deploy a Nuxt.js project and get your domain up.

[Nuxt.js](https://nuxtjs.org/) is a free and open source JavaScript library based on Vue.js, Node.js, Webpack and Babel.js. Nuxt is inspired by Next.js, which is a framework of similar purpose, based on React.js. The framework is advertised as a "Meta-framework for universal [applications"](https://en.wikipedia.org/wiki/Nuxt.js).

## Follow these steps to deploy your Nuxt.js app on Spheron.

### Step 1: Put Your Nuxt.js Project Code in a Git Repo

While this feature is not new to developers, the magic of Spheron is that every push to any branch in your GitHub, GitLab, or Bitbucket repo triggers a new build and deployment of your project.

### Step 2: Update Your Nuxt.js Project for Deploying on Decentralised Storage

Decentralized Storage needs a different configuration for the dapp to work without any issues. The only issue you will face after deploying on decentralized Storage is the routing issue. The decentralized Storage works in a hash-based system, so you need to change your routing module from **BrowserRouter** (e.g., `domain.com/testing`) to **HashRouter** (e.g., `domain.com/#/testing`)

Once you change all the instances of browser routing to hash routing, you can now deploy your project via Spheron on any Protocol.

### Step 3: Deploy using the Spheron Platform UI.

You can **create a new Spheron project using the platform UI**. First, visit [Spheron Protocol](https://aqua.spheron.network/) in your browser.

<img src={require('@site/static/img/3.0.0/doca-git.png').default} /> <br/><br/>

Choose your preferred Git provider from the options as seen above and authorize Spheron to access the repo you want to deploy.

In the next screen, select your Nuxt.js repo from the list.

<img src={require('@site/static/img/3.0.0/guide-ss-6.png').default} /> <br/><br/>

Choose your preferred protocol where you want to deploy your static build. As of now, we support Arweave, Skynet, Filecoin & Pinata. You can choose any one protocol from all 4 of them.

<img src={require('@site/static/img/3.0.0/doca-proto.png').default} /> <br/><br/>

The third screen asks for details about where to create the project and how to build it. All the settings are already pre-filled based on the suggested framework. Learn more about each build setting. Check out [here](https://docs.spheron.network/deployments/get-started#configuring-the-deployment).

1. Choose the **branch** to deploy from the dropdown and provide the **root directory** if you have a monorepo-like app structure.

1. Set the **install command** to `yarn install`

1. Set the **build command** to `yarn generate`

1. Set the **publish directory** to `dist`

1. You can add some **environment variables** before the build.

1. You can change the **node engine** of your deployment as well.

1. Click **Deploy**

<img src={require('@site/static/img/3.0.0/nuxt-build.png').default} /> <br/><br/>

## That's All!

Now that you've deployed your Nuxt.js project on Spheron, you have all the benefits of Spheron — including a custom deployment environment, continuous deployment whenever you push to your repo, and much more — as well as the benefits of Nuxt.js like Preview Mode, Static site rendering.

After deploying, your new Nuxt.js project will automatically be assigned a **.spheron.app** suffixed domain. You can then add a [Custom Domain](https://docs.spheron.network/domain-and-https/centralized-domain/attach-domain) on your choice.

We're so excited to see what you build with Nuxt.js on Spheron!
