# Realm Swift Releases

This repository contains releases of the Realm Swift precompiled binaries for specific Xcode versions.

## Overview

Realm Swift is a mobile database that runs directly inside phones, tablets or wearables. This repository maintains version history and framework files for different Xcode versions.

## Adding New Release

1. Go to the official release of the desired version in the Swift Realm repository:
[official Realm Swift repository](https://github.com/realm/realm-swift)
2. Download `Realm.xcframework` and `RealmSwift.xcframework` from the assets section.
3. Generate checksums for the frameworks:
```bash
swift package compute-checksum releases/xcodeX.X.X/realmX.X.X/Realm.xcframework.zip
swift package compute-checksum releases/xcodeX.X.X/realmX.X.X/RealmSwift.xcframework.zip
```
4. Create a new release in this repository and attach the archives in the assets:
5. Copy the asset links and generated checksums to the PayseraRealm package in your project.
```swift
.binaryTarget(
    name: "Realm",
    url: "https://gitlab.paysera.net/beka.demuradze/swiftrealmreleases/-/raw/master/releases/xcodeX.X.X/realmX.X.X/Realm.xcframework.zip",
    checksum: "generated_checksum"
),
.binaryTarget(
    name: "RealmSwift",
    url: "https://gitlab.paysera.net/beka.demuradze/swiftrealmreleases/-/raw/master/releases/xcodeX.X.X/realmX.X.X/RealmSwift.xcframework.zip",
    checksum: "generated_checksum"
)
```

## Version History

Releases are marked according to the official Realm Swift version numbers.

## Contributing

To download the newest relases of the realm precompiled binaries pleas echeck the official Realm repository for Swift [official Realm Swift repository](https://github.com/realm/realm-swift).

## Note

This repository contains only precompiled binaries and does not include any realisation logic