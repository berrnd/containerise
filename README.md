# Containerise @berrnd Fork

-----
-----

> This is a fork of [Containerise](https://github.com/kintesh/containerise) (based on the v3.9.0 release) which adds an option to exclude certain containers.
> 
> The (signed) .xpi file for manual installation can be found in the [release assets](https://github.com/berrnd/containerise/releases/latest).
>
> If you also use [Temporary Containers](https://github.com/stoically/temporary-containers), here is a compatible fork: <https://github.com/berrnd/temporary-containers>
>
> _Dev note: Node v16 is needed for building._

-----
-----

Original README:

|![](https://raw.githubusercontent.com/kintesh/containerise/master/static/screenshots/1.png)  |  ![](https://raw.githubusercontent.com/kintesh/containerise/master/static/screenshots/2.png)  |  ![](https://raw.githubusercontent.com/kintesh/containerise/master/static/screenshots/3.png)  |  ![](https://raw.githubusercontent.com/kintesh/containerise/master/static/screenshots/4.png)|
| --- | --- | --- | --- |
|Select your container and add a domain to always open all visits in the chosen container. | Add many domains as you wish. | Special `No Container` option to break out of a container. | Simple CSV based mapping of a domain to a container by name for easy backup and bulk editing. |

# Usage

## Basic mapping

`amazon.co.uk, Shopping` will open all amazon.co.uk (not subdomains) links in Shopping container.

## Glob
`!*.amazon.co.uk, Shopping`  will be treated as `*.amazon.co.uk` glob pattern. (suitable to subdomains)

## Regex

`@.+\.amazon\.co\.uk$, Shopping` will be treat as `.+\.amazon\.co\.uk$` regex. (suitable to subdomains and complex paths)



# Development

## Available Scripts
In the project directory, you can run:

#### `npm ci`
Installs required dependencies. 

#### `npm run webpack`
Starts webpack with `--watch` option and outputs to `./build` directory.
 
#### `npm run build`
Builds the extension for production use.<br>

#### `npm run test`
Runs test specs using jest.
Use `test:watch` to watch for edits and re-run the tests.

#### `npm run lint`
Lint using eslint.

#### `npm run web-ext`
Runs web-ext process to debug the extension on Firefox. See [web-ext docs](https://github.com/mozilla/web-ext) <br/>
To live reload the extension, start this process in a new tab after starting `npm run webpack` process.
