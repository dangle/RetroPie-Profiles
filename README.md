RetroPie-save-profiles 💾
======================
### RetroPie plugin to select which profile to use for save files and save states

This is a [RetroPie][] plugin that adds an entry to the `RetroPie` "system" in
EmulationStation. It provides a UI for logging in to your RetroPie via a login
server on your mobile device.

Specifically, this plugin is responsible for setting the `savefile_directory` and
`savestate_directory` values in the `retroarch.cfg` file. This way, you can have
different "profiles" of saves for when different people are using RetroPie.

I wrote this because my brother is always coming over to my house and wants to be
able to resume his game saves from home and vice versa. When using this plugin in
combination with [`sshfs`][sshfs] we share save files and ROMs over the cloud ☁️


Installation
------------

Clone the repo, or extract a tarball of `master` branch to your RetroPie:

``` bash
```


Login Servers
-------------

The "login server" is the URL in which you will visit on your mobile device when
the login dialog is open in RetroPie to change users. The URL is specified in
the `retroarch.cfg` file under the `save_profiles_login_server` config key.
The plugin will prompt you for the login server URL if the key is not already set:

A login server can have literally any logic implemented for the login mechanism.
It is recommended to use the `RetroPie-save-profiles-server` helper to implement
your own server.

Here's a list of known login server implementations:

 - [Facebook Login][fb] - Login using your Facebook profile

<sub>Send a pull request to add yours to the list!</sub>


License
-------

(The MIT License)

Copyright (c) 2016 Nathan Rajlich &lt;n@n8.io&gt;

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
'Software'), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

[RetroPie]: https://retropie.org.uk/
[sshfs]: https://github.com/libfuse/sshfs
[fb]: https://github.com/TooTallNate/RetroPie-profiles-facebook-login
