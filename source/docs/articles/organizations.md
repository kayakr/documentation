---
title: Organizations
description: Detailed information on Pantheon organization types and the features available to them.
category:
- managing
keywords: pantheon, pantheon for agencies, org, organization, org dashboard, change management
---
Organizations on Pantheon bring together users, sites, custom upstreams, unified support, and Multidev to provide administrators with the tools needed to effectively manage a large number of websites. Several service levels are as types of organizations on our platform. Please see your organization dashboard or contact your sales representative to determine which type you are. Partners who signed up for "Pantheon for Agencies" via our self-service form are "Ally Partners." Ally Partners do not qualify for custom upstreams or free sites. Take a moment to read about all of the awesome we have available for your organization.

## The Organization Dashboard
Access the Organization Dashboard from the User Dashboard in the Organizations tab, between the site name and service level in an org-associated Site Dashboard, or in the **My Sites & Account** list by using the keyboard shortcut, "s". To perform the URL hack, type `dashboard.pantheon.io/org` and your browser will likely autocomplete the URL for your org dashboard. My fastest is a quick tap of the `s` key, followed by a move of the mouse to click on my org.

## Multidev

All Partner organizations have Multidev available on every site. Click on **Multidev** in your Site Dashboard to get going. Sites have a maximum of ten Multidev environments and unlimited git branches, from which Multidev environments can be created on-demand. Learn how to [use Multidev](/source/docs/articles/sites/multidev).

## Change Management

Organizational roles propagate to sites within. All organization members can create sites, but only admins and site owners can delete them. Enable only Team Members and Administrators to deploy code to the Test and Live environments, and restrict the Developer role from doing so. [Learn More](/docs/articles/organizations/change-management).

## Upstreams

Upstreams are Git forks of Pantheon's versions of Drupal and WordPress, owned and managed by organizations. They are available for all members of the organization to select when starting a new site. Reseller partners customers deliver SAAS products built with Drupal or WordPress, automatically creating a new site for each of their clients. Learn all about [custom upstreams](/docs/articles/organizations/running-a-custom-upstream).

### Organization UUID
Every user, organization, product and site is assigned a UUID which is internal to Pantheon. The organization UUID is found within the URL for the organization Dashboard and resembles the following:
```
de305d54-75b4-431b-adb2-eb6b9e546014
```
You can also use [Terminus](https://github.com/pantheon-systems/cli) to find the UUID of your organizations:

```
$ terminus organizations list
```


## More Resources

- [Pantheon for Agencies](/docs/articles/organizations/pantheon-for-agencies)
- [Pantheon for Agencies FAQ](/docs/articles/organizations/pantheon-for-agencies-faq)
