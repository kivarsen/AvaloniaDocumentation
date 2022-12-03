# Release Process

* Create a branch named `release/0.10.2` for example. This branch should be level with the `master` commit that the release will be based on.
* Update the version number in the file `SharedVersion.props` i.e. `<Version>0.10.2</Version>`.
* Push the release branch.

If this is the first release of a major version change, i.e. `0.9.0` or `0.10.0` or the point at which breaking changes will start to be merged to `master` then before continuing we need to create a `stable/0.10.x` branch. This should be level with `master` at the same point that the `release/0.10.2`branched off from `master`

The git tree should now look like this:

![](<../../.gitbook/assets/image (4).png>)

* Now login at `dev.azure.com` to access the azure pipelines. Wait for the CI to finish the build.
* The package for `0.10.2` should now be on the `avalonia-all` nuget feed. You should run a due diligence test on this build to ensure you are happy with the release and the packages work.

{% hint style="danger" %}
Don't assume the Nuget packages will work just because master was working. In the past some technical changes i.e. Strong Naming broke nuget packages.
{% endhint %}

* Now click on "Releases" and select "Avalonia (master / release)" pipeline as shown below.

![](<../../.gitbook/assets/image (1).png>)

* On the release for your release branch `release/0.10.2` click on the badge for "Nuget Release"

![](<../../.gitbook/assets/image (11).png>)

![](<../../.gitbook/assets/image (17) (1) (1).png>)

* Then click on `Deploy`.

![](<../../.gitbook/assets/image (16).png>)

{% hint style="info" %}
At this point the packages will deploy to Nuget, it can take between 10 and 20 minutes for them to be indexed and publicly available. [https://www.nuget.org/packages/Avalonia/](https://www.nuget.org/packages/Avalonia/)
{% endhint %}

* Make a release on Github releases, this will set a tag named: `0.10.2` for you. You can add release notes here.
* Update the dotnet templates and visual studio plugin templates
* Announce on gitter, twitter, etc

{% hint style="info" %}
Now that the release is done, it is important to understand the process for maintaining the stable branch. Please see [Maintaining stable branch guide](maintaining-stable-branch-pr-merge-process.md)
{% endhint %}
