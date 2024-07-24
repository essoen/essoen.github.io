# essoen.github.io
My personal website, served on [svorstol.com](https://www.svorstol.com/)

Built with [Hugo](https://gohugo.io/), using the fantastic [Bear-theme](https://github.com/janraasch/hugo-bearblog) from [Bearblog](https://bearblog.dev). Served through Github Pages. There's an admin panel on `/admin` if browser is all you have and you _must_ write.

## Local setup
Install Hugo, and get submodules for the theme.

`git submodule update --init --recursive`

and later `git submodule update --recursive --remote` to update.


## Usage
New post: `hugo new blog/<year>/date-postname.md`, or just add files. 
Additional content in `static`-folder, and can be used in posts like `![alt](/subfolder/filename.extension)`

Serve locally with `hugo serve`, build with `hugo`

