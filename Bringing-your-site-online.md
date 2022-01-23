# Bringing your site Online

## WireFrames

- low fidelity sketch of a digital interface.
- communicate how a designer intends to lay out the product.
- __emphasize usability__ over aesthetics.
- allow developers to __provide feedback__ on the design.
- are like _blueprints_.
- omit implementation details.
- are created before mockups in the design process.
- developers _breakdown_ wireframes __into__ a __development plan__.

### Creating Wireframes

[The Definitive Guide: How To Make Your First Wireframe](https://careerfoundry.com/en/blog/ux-design/how-to-create-your-first-wireframe/)

[WireFrame Design and Prototypes](https://xd.adobe.com/ideas/process/wireframing/wireframe-design-definition/)

#### 2 Types

1. Handwritten Wireframes

2. Digital Wireframes
- [Figma](https://www.figma.com/file/pcf4aWYtACBViBI0U2OGJk/Untitled?node-id=0%3A1)
- [wireframe](https://wireframe.cc/)


---

## From Design to Website

- think __grid__ (underlying structure as grids).
- think __visual hierarchy__ which inform the user experience.
  - locate the _focal points_ (main, header, nav-bar, footer, etc.)
- think __visual continuity__ or visual cohesion.
  - can be achieved through _color_, _type_ and through adding _similar sections_ to our site.
  - we keep this in mind as we build our css.
- web design workflow:
  - gather your content(images, text, video files).
  - make design decisions
    - we decide what colors to use.
    - choose between images.
    - edit text and choose typography.
  - add a style guide (this informs our html and css).

Process:

- Take _one section_ at a time.
- Allow HTML and CSS to inform your layout.
- look for _similarities_ and _differences_ as you begin to choose HTML tags and CSS selectors.
- apply and build your _style guide_.
- be open to change.

---

## Web Hosting

Hosting Provider

- business that maintains all the resources needed to host applications.
- storage area and where we post the content of the website.

### Types of Hosting

1. Website Builders

   - build website without manually writing code (ie. [wix](https://www.wix.com/mystunningwebsites/illustration?utm_source=affiliate&utm_medium=paid_referral&utm_campaign=af_29@realinfopoint.com/&experiment_id=cake_98491926^108), [squarespace](https://www.squarespace.com))
   - include different kinds of **CMS** or _Content Management Systems_.

2. Shared Web Hosting

   - you share a server with other people.
   - cheaper

3. Dedicated Web Hosting

   - server only for you.
   - more expensive.

4. Cloud Hosting

   - **cloud** is a vast network of data centers and different computing resources made available to consumers.
   - lots of services, highly distributed in nature.
   - best-suited when you want to run different parts of your application on different types of machine.

   - Types:

     - Infrastructure as a Service (IaaS)
       - get _raw_ infrastructure resources.
       - gives you _access to servers, storage, networks_ but you have to maintain them.
       > You manage: Application, Data, Runtime, Middleware, OS
       > Provider manage: Virtualization, Servers, Storage, Network

     - Platform as a Service (PaaS)
       - the _provider manages the infrastructure_ while _you deploy functions_.
       > You manage: Functions, Data
       > Provider manage: Runtime, Middleware, OS, Virtualization, Servers, Storage, Network

     - Function as a Service (FaaS)

---

### Terms in Hosting

Disk Space

- total size of all the files that make up your site. (all HTML, CSS, images and scripts)

Bandwidth

- the amount of data the hosting company will send to your site's visitors.
  > ie. 10 visitors == bandwidth is 10 times of your disk space.

Backups

- check whether the hosting company performs backups on your site and how often.

Email accounts

- most hosting companies provide email servers.
- check the size of mailbox allowed and the number of mailboxes you can use

Server-side languages and databases

- if you are using CMS, it will likely use a server-side programming language and a database (such as _PHP with a MySQL database_ or _ASP.Net with a SQL Server database_)

FTP (File Transfer Protocol) & Third Party Tools

- to transfer code and images across the internet from your local computer to the web server hosting your site.
- faster at transmitting files.
- web hosting often provides FTP details to enter in the FTP program to connect to the server.
- this will be an address (such as `ftp://mydomain.com`), a `username` and a `password`.
  
  - Popular FTP Applications:
    - [FileZilla](filezilla-project.org) for Windows, Mac, Linux
    - [FireFTP](fireftp.mozdev.org) for Windows, Mac, Linux
    - [CuteFTP](cuteftp.com) for Windows, Mac
    - [SmartFTP](smartftp.com) for Windows
    - [Transmit](panic.com/transmit) for Mac
  - Popular third party tools:
    - for BLOGS: [wordpress](wordpress.com), [tumblr](tumblr.com), [posterous](posterous.com)
    - for E-Commerce: [shopify](shopify.com)[bigcartel](bigcartel.com), [goMagento](go.magento.com)
    - for E-mail Newsletter: [campaign monitor](campaignmonitor.com), [mailchimp](mailchimp.com)
    - for Social Networking Sharing Buttons: [addthis](addthis.com), [addtoany](addtoany.com)


### What (Web Hosting) to choose? (recommended)

1. [GitHub Pages](https://pages.github.com/)

   - best-suited for static applications
   - for simple html and css files.
   - for compiled version of react applications.
   - for personal portfolio.

2. [Heroku](https://www.heroku.com/)

   - good for more complex full-stack apps.
   - for node.js server or SQL database.

3. [Digital Ocean](https://www.digitalocean.com/)

   - Full control over cloud resources.
   - have a lot of resources on how to get started.


---

## Domain Name

- is used to translate _IP Addresses_ (coded-numbers) into _names_ for humans to remember.
- serves as a bridge the communication gap between humans and computers.
- are registered and can be used for a website and/or email account.
- are what users type in the browsers to access websites.
- also known as **web addresses**

### How does it work?

1. `Domain name` 
    -(type into)-> 
2. `Web browser` (translated by `DNS` into `IP Address`) 
    -(if not pulled from cache, goes to..)-> 
3. `Resolver Server` or `ISP` 
    -(if still cannot find, goes to..)-> 
4. `root server`
    -(sends the query to..)->
5. `TLD server`
    -(goes back to...)->
6. `Resolver Server`
    -(then goes to..)->
7. `Name Server`
    -(will return the IP address for the requested hostname back to)->
8. `Web browser`
    -(will be stored in memory of the browser as **cache**)

Domain Name System (DNS)

- translates domain names to IP addresses so browsers can load internet resources.

Resolver Server

- is the computer that responds to a recursive request from a client and takes the time to track down the DNS record.
- **caching** is a data persistence process that helps short-circuit the necessary requests by serving the requested resource record earlier in the DNS lookup.

Internet Service Provider (ISP)

- provides access to the internet.

Root Server

- at top level in the hierarchy of the domain name searcher or internet search
- there are 13 root servers throughout the world and operated by different organizations.
- does not exactly know the domain but it directs the resolver server where to find it.

Top Level Domain Server (TLDs)

- it hosts the last portion of a hostname (ie. `com` from example.com)
- stores the address information for the top level domains.

Name Server

- responsible for knowing everything about the domain including the IP address.
- final authority that will send back to the computer with the site

### Domain Name examples

Parts of domain name
> https://www.codecademy.com
> `https://`: Protocol
> `www.`: Sub-domain
> `codecademy`: Second-level Domain
> `.com`: Top-level Domain

- `.com`, `.org`, `.edu`, `.net`, `.biz`, `.info`
- for country codes: `.ph` for Philippines, `.cn` for China, `.fr` for France, `.us` for United States etc.

### Building a Website through Domain and Web Hosting

1. Get a Domain name. [Namecheap](https://www.namecheap.com)
   - our domain will point to our website that is hosted on a server.
2. Get Web Hosting for your website.
3. Post content of the website to the web host or service provider.
   - website will be stored to web servers.
