---
title: "GitLab"
date: 2018-06-08T13:14:11-07:00
draft: false
weight: 100
---

<img class="screenshot" src="/imgs/modules/gitlab.png" width="640" height="390" alt="gitlab screenshot" />

Displays information about your projects hosted on GitLab:

#### Open Approval Requests

All open merge requests that are requesting your approval.

#### Open Merge Requests

All open merge requests created by you.

## Configuration

```yaml
gitlab:
  apiKey: "3276d7155dd9ee27b8b14f8743a408a9"
  enabled: true
  position:
    top: 2
    left: 3
    height: 2
    width: 2
  refreshInterval: 300
  projects:
    tasks: "gitlab-org/release"
    gitlab-ce: "gitlab-org"
  username: "wtfutil"
```

{{% attributes %}}
  {{< attributes/apikey name="GitLab" link="https://docs.gitlab.com/ce/user/profile/personal_access_tokens.html" >}}
  {{< attributes/border >}}
  {{< attributes/custom name="domain" desc="_Optional_. Your GitLab corporate domain." value="A valid URI." >}}
  {{< attributes/enabled >}}
  {{< attributes/focusChar >}}
  {{< attributes/position >}}

  <tr>
    <td>`projects`</td>
    <td>
      A list of key/value pairs each describing a GitLab project to fetch data for. 
      <br />
      <br />
      <span class="caption">Key:</span> The name of the project. <br />
      <span class="caption">Value:</span> The namespace of the project.
    </td>
    <td></td>
  </tr>

  {{< attributes/refreshInterval >}}
  {{< attributes/username name="GitLab" desc="Used to figure out which requests require your approval." >}}
{{% /attributes %}}

{{% keyboard %}}
  {{< keyboard/foreSlash >}}

  {{< keyboard/spacer >}}

  {{< keyboard/h desc="Show the previous git repository" >}}
  {{< keyboard/l desc="Show the next git repository" >}}
  {{< keyboard/r >}}

  {{< keyboard/spacer >}}

  {{< keyboard/arrowBack desc="Show the previous git repository" >}}
  {{< keyboard/arrowFore desc="Show the next git repository" >}}
{{% /keyboard %}}

{{% sourcePath module="gitlab" %}}