# sample-ios-project-cocoapods-renovate-demo

## Note
* Created [private pods repo](https://github.com/asoneji/test-pods-repo) in a private github repo.
* Created sample pod [TestMeLib](https://github.com/asoneji/TestMe) in a private github repo.

## Demo Private Repo Renovate Issue Using Cocoapods
Sample project with automated dependency updates for Cocoapods using Renovatebot.
1. Created sample repo [sample-ios-project-cocoapods-renovate-demo](https://github.com/asoneji/sample-ios-project-cocoapods-renovate-demo)
2. Create a sample XCode Project [sample-ios-project](https://github.com/asoneji/sample-ios-project-cocoapods-renovate-demo/tree/master/sample-ios-project)
3. Did `pod init` and added a pod dependency
   * Added Source:
     * `source 'https://github.com/asoneji/test-pods-repo.git'` **//NOTE: This is a private repo**
     * `source 'https://github.com/CocoaPods/Specs.git'`
   * Added Dependency:
     * `pod 'Analytics', '3.8.1'`
     * `pod 'TestMeLib', '0.1.0'`
4. Connect Renovate using [renovate](https://github.com/marketplace/renovate) to the repo [sample-ios-project-cocoapods-renovate-demo](https://github.com/asoneji/sample-ios-project-cocoapods-renovate-demo). In our case we use [renovate-on-prem](https://github.com/whitesource/renovate-on-prem).
5. Renovate created a [pr](https://github.com/asoneji/sample-ios-project-cocoapods-renovate-demo/pull/1) with renovate config and in the dependency lookup warning gives an error
   * `Failed to look up dependency TestMeLib`
   * [Renovate Job](https://app.renovatebot.com/dashboard#github/asoneji/sample-ios-project-cocoapods-renovate-demo/193041246)

