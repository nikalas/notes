Rails
=====

Tips and tricks in Ruby on Rails.

Dump activerecord table to file from rails console
-------------------------------

`$ rails console

> f = File.new("filename.xxx", "w")
> f << JSON.pretty_generate((TableName.all).as_json)
> f.close
> exit
