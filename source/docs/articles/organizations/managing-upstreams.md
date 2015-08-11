---
title: Managing Upstreams
description: Detailed information on how to merge updates to core, extensions, and themes running on Pantheon.
category:
  - managing
keywords: upstream, update upstream, apply updates, apply update, update core, update plugin, update module, update theme, update distribution, distribution, branch, deploy update, deploy updates, update, updates
---
Upstream maintainers bear the responsibility of updating Drupal and WordPress core for their users each time the project releases a new version. Upstreams that are not kept up-to-date with core security updates of either framework will be removed from the platform.
## Merging Core Releases
1. Create an update branch:

 ```bash
 git checkout -b update
 ```
2. Pull down changes from the applicable core:

 **WordPress**
 ```bash
 git pull git://github.com/pantheon-systems/wordpress.git master
 ```

 **Drupal 6**

 ```bash
 git pull git://github.com/pantheon-systems/drops-6.git master
 ```

 **Drupal 7**

 ```bash
 git pull git://github.com/pantheon-systems/drops-7.git master
 ```

3. Commit and push:

 ```nohighlight
 git commit -m “Update to Drupal 7.33. http://link-to-release-notes”
 git push origin update
 ```

## Adding or Updating Custom Code

Follow your organization’s process for managing Git repositories. Do not merge into the branch Pantheon is programmed to pull updates from, without testing first.

## Testing Your Updates

Using the testing site created when you submitted your distribution, test your updates for new installs and upgrades.

## Update Release Branching Strategy

We encourage you to use a continuous integration server, like Jenkins, Travis-CI, or Circle-CI, to automate this process.

1. Merge upstream updates into an update branch.
2. Pull the remote repository into the local clone of your testing site.
3. Checkout the updates branch.
4. Push the updates branch to Pantheon.
5. Create a Multidev environment for the branch.
6. Wipe the database and files from the update branch.
7. Run acceptance tests for a new-site installation use case.
8. Merge the code into dev.
9. Wipe the Dev environment’s database and files.
10. Test the code update installation process, and existing code update case.
11. Copy content from Live and deploy code to Test.
12. Test the code against test content for the existing site update case.
13. Deploy the code to Live.
14. Test your code against a live testing site (distribution demo site - pro plan?), ensuring that modules work in an environment with more than one application container.

## Deploy Updates to Downstream Sites

1. Prepare release notes.
2. Merge your pull request into the branch, providing a descriptive commit message. The message can follow the pattern: “Upstream release version, release notes http://link-to-release-notes”.

After you have merged an update, all sites that use the distribution will be given the option to apply updates on their Site Dashboard at  Dev > Code. It typically takes up to an hour for the update to be detected. Use your browser’s hard refresh if the updates do not appear after the first hour (`cmd+shift+R` on OSX, `shift+f5` on Windows).
