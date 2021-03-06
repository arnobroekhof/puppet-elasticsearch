puppet-elasticsearch
===============

Description
-----------

A Puppet report handler for sending notifications to Elasticsearch.

Requirements
------------

* `tire`
* `puppet`
* `yajl-ruby`

Installation & Usage
--------------------

1.  Install the `tinder` gem on your Puppet master

        $ sudo gem install tire
        $ sudo gem install yajl-ruby 

2.  Install puppet-elsticsearch as a module in your Puppet master's module
path.

3.  Update the `server` and `port` variables in the
    `/etc/puppet/elasticsearch.yaml` with your Elasticserver, for example
    `http://127.0.0.1`, `9200`. An example file is included.

4.  Enable pluginsync and reports on your master and clients in `puppet.conf`

        [master]
        report = true
        reports = elasticsearch
        pluginsync = true
        [agent]
        report = true
        pluginsync = true

5.  Run the Puppet client and sync the report as a plugin

Author
------

Arno Broekhof <arnobroekhof@gmail.com>

License
-------

    Author:: Arno Broekhof (arnobroekhof@gmail.com)
    Copyright:: Copyright (c) 2013 Arno Broekhof
    License:: Apache License, Version 2.0

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.

TODO
----
make the elasticsearch.yaml work
