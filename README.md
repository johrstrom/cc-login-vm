# CloudyCluster Login VM

Configure and setup a CloudyCluster login VM. This initializes some
Open OnDemand directories, sets up some developers, the right rails
intializers and a message of the day.

## Configuration

This role primarily uses the `configure` and `developer` tags.

```yaml
# a list of developers to create and add to OOD
developers: []
files_to_move: []

# if you want to use ERB in your message of the day
erb_motd_initializer: false

# your message of the day content. Note that you'll have
# to also configure this location in /etc/ood/config/apps/dashboard/env
# for the dashboard to read it.
motd:
  content: "# Welcome to Cloudy Cluster Open OnDemand"
  dest: "/etc/ood/config/MOTD.md"
```
