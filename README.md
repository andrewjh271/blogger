# Blogger App

This was a tutorial from [Jumpstart Lab](http://tutorials.jumpstartlab.com/projects/blogger.html), and was completed as part of the Odin Project Curriculum. View the live app [here](https://vast-escarpment-91025.herokuapp.com/).

### Thoughts

Mostly some good review of basic Rails concepts. I also learned about the `paperclip` and `sorcery` gems. This was my first time using the Rails scaffold generator. The only real issue I ran into was `flash` not working with the new `form_with`. (I was using Rails 6 compared to the tutorial's Rails 4, which uses the now deprecated `form_for`.) Form submits are remote by default with `form_for`, which doesn't work with `flash`. Setting `local: true` fixed the problem.

I wasn't particuarly happy with the final functionality of authentication, but I've hardcoded more natural functionality in previous projects, and don't expect to be using the `sorcery` gem in the future.

I was unable to figure out how to push my `sqlite3` development database into the `postgresql` production database. I expect I will use `postgresql` for development going forward.

###### A note on node_modules

In an effort to remove much of the bloated and unused `node_modules` folder, I deleted  `"@rails/actioncable": "^6.0.0"`, `"@rails/webpacker": "4.3.0"` and `"turbolinks": "^5.2.0"` from the list of `"dependencies"` and `"webpack-dev-server": "^3.11.0"`from the list of `"devDependencies"` in `package.json`, then ran `$ yarn install` again. I explain more about this process in the README of my [re-former project](https://github.com/andrewjh271/re-former).

