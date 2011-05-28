---
layout: post
title: Mongo Mapper - Spelling Matters
categories: development mongodb Ruby
---
## Mongo Mapper: Spelling Matters

Added [Mongo Mapper](http://github.com/jnunemaker/mongomapper/) to my test Sinatra app today, and kept getting a gem not found error. All the examples that came up in my various Google searches had:

require ‘mongomapper’

After a reinstall of the gem and a few curse words, I tried a little experiement:

require ‘mongo_mapper’

That did the trick.
