---
title: Conditions for large files
intro: '{{ site.data.variables.product.product_name }} limits the size of files allowed in repositories, and will block a push to a repository if the files are larger than the maximum file limit.'
redirect_from:
  - /articles/conditions-for-large-files
versions:
  free-pro-team: '*'
  enterprise-server: '*'
---

{{ site.data.reusables.large_files.use_lfs_tip }}

### Warning for files larger than {{ site.data.variables.large_files.warning_size }}

If you attempt to add or update a file that is larger than {{ site.data.variables.large_files.warning_size }}, you will receive a warning from Git. The changes will still successfully push to your repository, but you can consider removing the commit to minimize performance impact. For more information, see "[Removing files from a repository's history](/github/managing-large-files/removing-files-from-a-repositorys-history)."

### Blocked pushes for large files

{% if currentVersion != "free-pro-team@latest" %}By default, {% endif %}{{ site.data.variables.product.product_name }} blocks pushes that exceed {{ site.data.variables.large_files.max_github_size }}. {% if currentVersion != "free-pro-team@latest" %}However, a site administrator can configure a different limit for your {{ site.data.variables.product.prodname_ghe_server }} instance. For more information, see "[Setting Git push limits](/enterprise/{{ currentVersion }}/admin/guides/installation/setting-git-push-limits)".{% endif %}