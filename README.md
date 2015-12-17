BeEF Cookbook
=============
Install and configures [BeFF](http://beefproject.com)

[![Cookbook Version](https://img.shields.io/cookbook/v/beef.svg)](https://community.opscode.com/cookbooks/beef) [![Build Status](https://secure.travis-ci.org/sliim-cookbooks/beef.png)](http://travis-ci.org/sliim-cookbooks/beef)

Requirements
------------
#### Platforms
The following platforms and versions are tested and supported using Opscode's test-kitchen.
- Debian wheezy
- Debian jessie

Attributes
----------
#### beef::default
|               Key        |  Type  |                 Description                                                      |
| ------------------------ | ------ | -------------------------------------------------------------------------------- |
| `[beef][packages]`       | Array  | Additional packages to install (default: [git, libsqlite3-dev, build-essential]) |
| `[beef][user]`           | String | BeEF user (default: beef)                                                        |
| `[beef][group]`          | String | BeEF group (default: beef)                                                       |
| `[beef][path]`           | String | BeEF installation path (default: /opt/beef)                                      |
| `[beef][git_repository]` | String | BeEF repository url (default: https://github.com/beefproject/beef.git)           |
| `[beef][git_reference]`  | String | BeEF repository reference (default: beef-0.4.6.1)                                |
| `[beef][ruby_bin_dir]`   | String | Ruby bin directory (default: /opt/chef/embedded/bin)                             |

#### beef::config
The `[beef][config][beef]` namespace is a Hash containing the BeEF configuration.
Default configuration is set from [beef-0.4.6.1](https://github.com/beefproject/beef/blob/beef-0.4.6.1/config.yaml)

Usage
-----
#### beef::default
Just include `beef` in your node's `run_list`:

```json
{
  "name":"my_node",
  "run_list": [
    "recipe[beef]"
  ]
}
```

#### Running tests

- First, install dependencies:  
`bundle install`

- Run Checkstyle and ChefSpec:  
`bundle exec rake`

- Run Kitchen tests:  
`bundle exec rake kitchen`  

Contributing
------------

1. Fork the repository on Github
2. Create a named feature branch (like `add_component_x`)
3. Write your change
4. Write tests for your change (if applicable)
5. Run the tests, ensuring they all pass
6. Submit a Pull Request using Github

License and Authors
-------------------
Authors: Sliim <sliim@mailoo.org> 

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.

