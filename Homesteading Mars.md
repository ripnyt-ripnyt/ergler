# Homesteading Mars
Created 2022 02 07 21:59

---

You've started with [Port](https://urbit.org/getting-started) and joined a few groups, made a few friends, and no longer want to leave your Urbit locked in your laptop. Here's how you can access it 24/7, from wherever you may be via any web browser. There's a whole constellation of options available to choose from, but how do you choose?

In this article we'll go over three styles of hosting from easiest to most difficult. 3rd party hosting, self managed cloud hosting, and self hosted.

Given that Urbit's portability makes it more like a nomad than a settler, the choice of where to host your running ship is fluid and can change whenever needed. Much like homesteading the western expanses of the United States: any new immigrant will face key decisions on where to settle. Your Urbit [Ship](https://urbit.org/getting-started) can be operated on any and there's a simple process for migrating. As long as you own your keys and have your Pier, you can easily move the ship between operating locations without missing a single message from the network. Eventually each Pilot will find their Homestead.

If Urbit is a personal server, why consider using 3rd party services or letting someone else operate your ship? Let's face it, providing reliable service at the level of a data center is difficult for any individual to do. Running an accessible from anywhere ship at home means that you'd need to setup a webserver with all the security precautions that it requires. By using a data center or cloud environment with a virtual server you get to ride on a service with extremely high uptime without the hassle of dealing with backup power supplies, secure environments, and adverse weather events.

First, an explainer on the portability of your Urbit [Ship](https://urbit.org/getting-started). When you first boot your ship a set of folders is started, and it's become a unique-to-you set of files. Your digital presence on Mars is contained in this folder which is known as a [Pier](https://urbit.org/docs/glossary/pier). It's continually updated when your ship is running and online with all its neighbors, messages and running apps. Since this is a continually changing set of files it's generally advised to stay away from backing it up. Booting an outdated backup will corrupt the state of your ship on the Urbit network and requires [Breaching](https://urbit.org/using/id/guide-to-resets) to recover. Breaching is the ship announcing to the world that it has broken continuity of it's log and every other ship should forget the old version of it and start fresh like a phoenix reborn. Time travel or parallel operation is not allowed on Mars.

With that warning out of the way, you'll need to know the basics of safely moving a pier without breaching. It's the same process no matter where it's going or coming from

1. Stop the running Ship
2. Move the Pier to new Host
3. Start the Ship

Once the ship is running on it's new host it's important to delete the now outdated folders on the original host and the compressed folders. Removing outdated Piers is a great way to reduce the potential of double booting by mistake later on.

## Paid Hosting Services
These services are where most [Star](https://urbit.org/docs/glossary/star) owners are going to do their best to learn and provide the most professional level of services. For a nominal fee they will use their expertise to offer you boutique services with high availability and a hands-off experience for the owner. Often, these are the easiest and most economical options however they require sharing your Ship's keys with the service provider.

- [UrbitHost](https://urbithost.com/)
- [3rd Earth](https://third.earth/)
- [Escape Pod Store](https://escapepod.store)

## Guided Command Line Installs in the Cloud
If you value complete control over your files over convenience and are willing to dive into using the command line with a guide there are plenty of options for you. Here's a list of the guides I've come across and have had varying levels of success using. Urbit and the community around it is rapidly changing and evolving; if you have trouble with some of these guides be sure to reach out their respective authors. As with all open-source software exercise due diligence and caution before running commands in the command line interface.

### Urbit For Normies: Installing Urbit on a Cloud Host
(Sep 24, 2021) - The Remilia Collective put this together for their DAO and it's very thorough with pictures. 

- [Urbit For Normies: Installing Urbit on a Cloud Host](https://blog.remilia.org/urbit-cloud-host/)

### Urbit User's Manual: Cloud Hosting
From Tlon, this is a barebones but clear instruction set on how to setup Urbit to a Droplet on Digital Ocean. 

- [Urbit User's Manual: Cloud Hosting](https://urbit.org/using/running/hosting)

### Urbit, Nginx and Letsencrypt
(Sep 26, 2020) - A guide from Networked Subject, a long standing community group full of useful technical guidance for Pilots.

- [Urbit, Nginx and Letsencrypt](https://subject.network/posts/urbit-nginx-letsencrypt/)

and a follow-up:

- [Easy Urbit TLS with Caddy](https://subject.network/posts/caddyserver-urbit-tls/)

### Urbit In The Cloud
(Jun 6, 2020) - This is an older guide with additional details on nginx. 

- [Urbit In The Cloud](https://zalberico.com/essay/2020/06/06/urbit-on-the-cloud.html)

### Home Urbit
This is an interesting project which aims to provide a whole suite of software to make running your personal server as easy as possible with a lot of features that are available to typical cloud hosted ships. It will run on best on a raspberry pi with attached SSD similar to the Argon package from ~botter-nidul's guide. This project is in alpha and has known issues.

- [~Home-Urbit](https://github.com/OdysLam/home-urbit)

As a bonus: 

- [Free Cloud Host with Oracle](https://subject.network/posts/free-cloud-oracle/)

## Homelab
Urbit's overlay OS architecture means that it can run anywhere a \*nix operating system can run. You'll find Pilots operating Urbit Ships anywhere from a raspberry pi to a cloud based Virtual Private Server with any of the cloud computing services offered today. Some individuals that love personal computing may even have their own server rack in a home lab setup. They would have the capability to host many planets for family and friends, each in their own Virtual Machine running on a chunk of commercial server equipment. A Pilot who chooses to go this route will have ultimate flexibility in configuration and compute resource management at the cost of electricity, static IP registration, and maintenance. This level of personal server hosting requires adept Linux and general networking knowledge to implement properly. Pilots going this route simply need to know where to grab the binaries, or what apt command to issue the terminal. Here it is:

### x86
- [Getting Started CLI Guide](https://urbit.org/getting-started/cli)

- [Urbit v1.8 GitHub](https://github.com/urbit/urbit/releases/tag/urbit-v1.8)

### ARM
Raspberry Pi binaries were built by ~botter-nidnul of ~dasfeb and Dasfeb Industries. Raspberry Pi's need to be slightly modified with a fast SSD in order to be performant, here's a guide:

- [Smol Guide](https://docs.google.com/document/d/10lnkkbm_YVA5GRmK7xEkuiFu0llLKF-eBQPH7mqnOyg/edit)

For all ARM beyond Raspberry Pi:

- [Urbit on ARM](https://botter-nidnul.github.io/)

If you're interested in low power computing, you would want to join the smol computing group currently hosted by Dalten Collective.

~naltyc-wornes-dozzod-dalten/big-urbit-smol-computer

### Urbit on Umbrel
Umbrel has recently added the Urbit app to their app store thanks to ~sitful-hatred and ~mopfel-winrux, 
- [Urbit Apps for Umbrel](https://subject.network/posts/urbit-apps-umbrel/). 
 
This is a great fit for someone that also wants to run their personal bitcoin node. As an added benefit it comes with a bitcoin provider app for your Bitcoin wallet on within your ship. It's recommended to add the Urbit app after the Bitcoin node fully synchronizes for the best experience. As an added benefit, Umbrel comes with Tailscale for remote VPN access to your ship and other self sovereign focused apps.

### Urbit on ...Nock CPU?
Urbit is full of deep thinkers and engineers. There is even an effort to build a CPU which runs Nock directly. Perhaps we'll see this when Urbit is in everyone's home.

## Where will *your* ship's Pier be hosted?
Now that you've learned basics of Pier movement and explored the current options for hosting, where will you host your ship? It's a personal decision with tradeoffs between convenience, sovereignty, and cost. At the end of the day, they all work for hosting your Ship and no one else on the network will know where yours is. You may continue piloting with Port and trade restricted access for sovereignty and low cost. You can trust your 3rd party Urbit Host to manage it all for you for a monthly fee but share your key with them. You can also pay for a virtual cloud server that takes some setup and a recurring fee. Most current Urbit pilots believe that more and more users will end up with a 3rd party Urbit host, and that's alright. It offers a nice blend of convenience at a low cost if you’re willing to share your keys.

With the rapid expansion of the Urbit community more and more options and improved services will be available. We can't wait to see how the network grows.

Join the dcSpark group on mars to learn about how we're bringing Web2 and Urbit together.

~havbex/dcspark
