# gitlab-ci-templates

## A collection of `.gitlab-ci.yml` templates and includes for Security Products

This is Security Products collection of [`.gitlab-ci.yml`][ci-docs] file templates,
to be used in conjunction with [GitLab CI][gl-ci].

For more information about how `.gitlab-ci.yml` files work, and how to use them,
please read the [documentation on GitLab CI][ci-docs]. Please keep in mind that
these templates might need editing to suit your setup, and should be considered
guideline.

[ci-docs]: https://docs.gitlab.com/ee/ci/
[gl-ci]: https://about.gitlab.com/gitlab-ci/


To make the runner run, add the following tag: `security`.

Use `include:remote` via the `include` keyword to pull a template from a public URL (see GitLab docs: https://docs.gitlab.com/ee/ci/yaml/#include):

```yaml
include:
  - remote: "https://gitlab.com/yobasystems/gitlab-ci-templates/raw/master/container_scanning_all_arch.yml"
```

All nested includes are executed without context as a public user, so only another remote, public project, or built-in template is allowed.
