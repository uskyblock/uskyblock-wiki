![uSkyblock-Revived](http://i.imgur.com/JbSV18m.png)

# Versioning Scheme
We follow a versioning scheme that is somewhat ever changing.

We have a Travis CI setup to automatically compile and publish jar-files back to GitHub when a tag is detected on a push.

Since Travis CI (as opposed to a Jenkins CI) doesn't host the release-artefacts, we have to make "releases", even for development-snapshots, used for testing.

This influences our versioning-scheme.

Scheme: `{major}.{minor}[-HF{hotfixnumber}[a-z]]`

We use the `major` version to indicate backward compatibility breaking changes. I.e. as long as we do not require an offline conversion or import from previous versions, the major version number will be `2`.

The `minor` version number indicates major feature-releases. I.e. `v2.2` introduced a lot of features, most notable the dynamic challenges/ranks support.

A `HF` release is a smaller increment based on a minor-release (i.e. one feature added).
The sub-identifier on HF-releases (a, b, c, ...) indicates bug-fixes to the features introduced in the first HF.

*Example* 
```
v2.2-HF11b
```
This release is based on the `v2.2` release, and is the 11th *hotfix* (aka *feature addition or bugfix*). It's also the 2nd iteration of that particular feature-release (we've found bugs or improvements 2 times to the `HF11` release).

I hope this makes sense.

# Releasing
Since we have a Travis CI configured, all that is required to make a release is:

1. Commit (and push) your changes to GitHub.
2. Identify the right release-name (run `git tag` to get a clue).
3. Tag the last commit (`git tag v2.2-HF13b`) and push the tag to GitHub (`git push --tags`).

Travis will now take over, and 3-5 minutes later, a new release will be available under the https://github.com/rlf/uSkyBlock/releases

Once the release has been tested (see [[Test Cases]]) it can be published to Bukkit (Dutchy1001) and Spigot (R4zorax).