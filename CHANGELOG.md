# Dokken Changelog

# 2.2.0
- Initial support for clusters / inter-suite name resolution
- Dokken now creates a user-defined network named "dokken" and
  connects containers to it. This allows us to take advantage of the
  built in DNS server that in Docker 1.10 and later.

  driver:
    hostname: www.computers.biz

# 2.1.10
- Adding boot2docker detection

# 2.1.9
- Various fixes around remote docker host usage

# 2.1.8
- Using user specified image_prefix in instance_name

# 2.1.7
- bumping version. must have accidentally pushed a 2.1.6

# 2.1.6
- PR #107 - pass write_timeout to runner exec
- PR #110 - (fix issue #109) - Add retry feature

# 2.1.5
- Fixing (again) latest/current logic (thanks @tas50)

# 2.1.4
- Fixing up current/stable/latest nomenclature to match Chef release pipeline

# 2.1.3
- Merged a bunch of PRs
- #85 - mount default boot2docker shared folder in Windows
- #93 - fix bundler path issue, should fix issue #92
- #97 - readme: systemd requires specific mount

## 2.1.2
- Making a CHANGELOG.md
- Updated gem spec to depend on test-kitchen ~> 1.5

## 2.1.1 
- Fixed busser (serverspec, etc) test data uploading

## 2.0.0
- Uses chef/chef (instead of someara/chef)

- Bind mounts data instead of uploading through kitchen-cache container when
  talking to a local Docker host. (most use cases)  

- Renders a Dockefile and builds dokken/kitchen-cache when taling to a
  remote Docker host. (DOCKER_HOST =~ /^tcp:/)

## 1.0.0
- First stable release. 
- Relied on someara/chef and someara/kitchen-cache from the
  Docker hub.