---
title: IAS3 Perl Use Cases
author: Victoria M Brasseur
---

# IAS3 Perl Use Cases

Probably will be of use for implementations in other languages.

In no particular order (yet) and requiring details:

* Create Item
* Add file to Item
* Update metadata for Item
* Update metadata for Item using _ (underscore) in metadata field name.
* Setting metadata for Item using files
* Updating metadata for Item using files
* Add file to Item and update metadata
    * `x-archive-ignore-preexisting-bucket` set to `1`
* Update a file on Item
* Update a file on Item but keep the prior version
    * `x-archive-keep-old-version` set to `1`
* Add or Update a file on an Item but disable derives
    * `x-archive-queue-derive` set to `0`
* Delete file from Item
* Delete a file and all its derivatives from Item
    * `x-archive-cascade-delete` set to `1`
* Create Item while uploading one or more files
    * PUT `x-amz-auto-make-bucket` with a value of `1`
* Authenticating on IAS3
* Authorizing on IAS3 (see 'Authenticating on IAS3'; just acknowledging they're different A's)
* Downloading all files in an Item
* Downloading a single file in an Item
* Downloading all files in a Collection

The following use cases are based on [jjjake/internetarchive](https://github.com/jjjake/internetarchive)
* Data mining Items
* Searching Internet Archive Items
