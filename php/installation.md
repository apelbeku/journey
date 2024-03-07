# Installation & Web Servers

Before we can write any `PHP` we need to have the local development environment setup for it.

We talking about a web server you could refer to:

- Hardware
    - Web server on the hardware is just computer that stores the web server software source code and some other stuff
- Software
- Hardware & Software

A web server can process incoming request using different protocols typically `HTTP` protocol which is the protocol used by the browser to view the web pages. A web server can host either a single or multiple websites on the same server using the same resource this is done by something called virtual hosts where the single web server is able to allocate and share a resource across multiple websites.

**_Simple diagram how the client and server communicate:_**

![How client and server communicate](./img/how-the-client-and-server-communicate.png "How client and server communicate")

## Ways To Install PHP In OS?

- `PHP` installed in OS
    - Manual installation
    - Manual `DB` installation
    - Manual configuration
- `XAMPP`/`MAPP`/`WAMP`
    - All in one solution
    - Contains web server
    - Contains database
    - Preconfigured
- `Virtual Machine`/`Docker`
    - Better alternative (covered in separated video)

## XAMPP Drawback

- No multiple versions of `PHP`
- No multiple versions of `MySQL`
- Not for production (due to it security)
- Difficult to maintain multiple projects
- Works on my machine (but not in server)
