# ADNUG Podcast
Adelaide .NET User Group monthly meeting podcast RSS feed

This repository contains source for the RSS feed for the recordings of ADNUG monthly meetings.

The RSS feed is automatically published to an Azure Website (Azure monitors this repo for changes).

The public URL for the Podcast is https://feeds.feedburner.com/adnug

## Technical notes for Audacity

1. Use noise reduction effect (select a quiet bit to analyze and then apply that to the whole recording)
2. Export as MP3
3. Encoding - choose VBR smallest size
4. Audacity Metadata

Field|Value
---|----
Artist Name|Adelaide .NET User Group
Track Title|Topic title
Year|year
Genre|Podcast

5. Upload to https://archive.org/upload/, with the following metadata

Field|Value
--|---
Page Title	|Topic title
Description|Topic overview
Creator | Adelaide .NET User Group
Date | Date of recording
License	| Attribution-Noncommercial-No Derivative Works 3.0

5. If two presentations, then save as separate files
6. Edit the [PodcastFeed.xml](PodcastFeed.xml) file to add the new episode. You can edit it manually, or use a tool like [RSS Builder](https://chocolatey.org/packages/rss-builder). Just review the changes it makes as sometimes it deletes things we want to keep.
8. Push changes to master if you have access, otherwise create a pull request from your fork
