## The Octokit API for releases

octokit has a way to automate releases under the `repos` branch. 

[more details here](https://octokit.github.io/rest.js/v18#repos-create-release)

Github Actions requires single quotes to test for return values. This has to be explicit and with single quotes only.

Then we can create a release with a unique name, which is VERSION plus the tag name using the following code:

```
      await github.repos.createRelease({
              owner,
              repo,
              tag_name,
              name: "Version " + tag_name
            });
```

The big challenge is to have an appropriate token. 


The biggest nuisance of GitHub Actions plus Octokit is that the API returns a strange 404 code that does not help at all. 

How about two [links.md]?