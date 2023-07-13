# Video Start
When the video starts playing.

Google automatically tracks this for YouTube videos that have JS API support enabled. For videos that aren't on YouTube and/or don't support JS API, this event must fire.

*Special note:* This event does not apply to videos inside iFrames. Please see [iFrame messages](/events/standard/iframe_post_message.md) for instructions.
## Sample JS
``` javascript
window.dataLayer = window.dataLayer || [];
dataLayer.push({ eventModel: null });  // Clear the previous eventModel object.
dataLayer.push({
  event: "video_progress",
  eventModel: {
    video_current_time: "video_current_time",
    video_duration: "video_duration",
    video_percent: "video_percent",
    video_provider: "video_provider",
    video_title: "video_title",
    video_url: "video_url",
    visible: "visible"
  }
});
```
## Parameter Definitions

|Field|Type|Required?|Description|Example|
| --- | --- | --- | --- | --- |
|video_current_time|string|required|The timestamp of the video in HH:MM:SS.|`00:00:01`|
|video_duration|string|required|The total length of the video in HH:MM:SS.|`00:06:00`|
|video_percent|string|required|The proportion of the video watched.|`0%`|
|video_provider|string|required|The platform hosting the video.|`vimeo`|
|video_title|string|required|The title of the video.|`F1 races rock`|
|video_url|string|required|The address of the video.|`https://example.com`|
|visible|boolean|required|Was the video visible while playing?|`true`|
