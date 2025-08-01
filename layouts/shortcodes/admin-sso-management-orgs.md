{{ $product_link := "[Docker Hub](https://hub.docker.com)" }}
{{ $sso_navigation := "Select **My Hub**, your organization, and then **Settings**." }}

{{ if eq (.Get "product") "admin" }}
  {{ $product_link = "[Docker Home](https://app.docker.com) and select your organization. Note that when an organization is part of a company, you must select the company and configure SSO for that organization at the company level. Each organization can have its own SSO configuration and domain, but it must be configured at the company level." }}
  {{ $sso_navigation = "Select **Admin Console**, then **SSO and SCIM**." }}
{{ end }}

### Connect an organization

1. Sign in to {{ $product_link }}.
2. {{ $sso_navigation }}
3. In the SSO connections table, select the **Action** icon and then **Edit connection**.
4. Select **Next** to navigate to the section where connected organizations are listed.
5. In the **Organizations** drop-down, select the organization to add to the connection.
6. Select **Next** to confirm or change the default organization and team provisioning.
7. Review the **Connection Summary** and select **Update connection**.

### Remove an organization

1. Sign in to {{ $product_link }}.
2. {{ $sso_navigation }}
3. In the SSO connections table, select the **Action** icon and then **Edit connection**.
4. Select **Next** to navigate to the section where connected organizations are listed.
5. In the **Organizations** drop-down, select **Remove** to remove the connection.
6. Select **Next** to confirm or change the default organization and team provisioning.
7. Review the **Connection Summary** and select **Update connection**.
