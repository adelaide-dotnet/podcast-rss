# ADNUG Podcast

Adelaide .NET User Group monthly meeting podcast RSS feed

This repository contains the source for the RSS feed for the recordings of ADNUG monthly meetings.

The RSS feed is automatically published to an Azure Website (Azure monitors this repo for changes).

The public URL for the Podcast is [https://feeds.feedburner.com/adnug](https://feeds.feedburner.com/adnug), which is a wrapper over [https://raw.githubusercontent.com/adelaide-dotnet/podcast-rss/master/PodcastFeed.xml](https://raw.githubusercontent.com/adelaide-dotnet/podcast-rss/master/PodcastFeed.xml)

## Script for episode introduction

> Hello and welcome to the ADNUG Podcast - the podcast for the Adelaide .NET User Group.
> I'm your host, &lt;your name&gt;.
>
> This is the recording from our &lt;month, year&gt; meeting.
> &lt;presentation title&gt;, with &lt;presenter name&gt;
>
> And now over to the presentation!

## Technical notes for Audacity

1. Use noise reduction effect (select a quiet bit to analyze and then apply that to the whole recording)
2. Export as MP3
3. Encoding - choose 'VBR' smallest size
4. Audacity Metadata
    Field|Value
    ---|----
    Artist Name|Adelaide .NET User Group
    Track Title|Topic title
    Year|year
    Genre|Podcast

5. Upload to [https://archive.org/upload/](https://archive.org/upload/), with the following metadata
    Field|Value
    --|---
    Page Title |Topic title
    Description|Topic overview
    Creator | Adelaide .NET User Group
    Date | Date of recording
    License | Attribution-Noncommercial-No Derivative Works 3.0
6. If two presentations, then save them as separate files
7. Edit the [PodcastFeed.xml](PodcastFeed.xml) file to add the new episode. You can edit it manually, or use a tool like [RSS Builder](https://chocolatey.org/packages/rss-builder). Just review the changes it makes as sometimes it deletes things we want to keep.
8. Push changes to master if you have access. Otherwise, create a pull request from your fork

## Extracting audio from video recording

```bash
ffmpeg -i "Meeting Recording.mp4" -vn -acodec copy output-audio.aac
```

## Images

Need to be 1400x1400 pixels (up to 3000x3000).

## Validation

- [https://podba.se/validate/?url=https://adnug.azurewebsites.net/PodcastFeed.xml](https://podba.se/validate/?url=https://adnug.azurewebsites.net/PodcastFeed.xml)

## References

* [Apple Podcast RSS Technical Specification](https://help.apple.com/itc/podcasts_connect/#/itcb54353390)
