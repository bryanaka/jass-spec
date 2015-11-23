Item - Episode
================================================================================

This is an attempt to unify both the RSS 2.0 spec and extra data that the
iTunes Podcast spec uses as well in their Podcast Feeds.

RSS 2.0 Spec - http://cyber.law.harvard.edu/rss/rss.html
iTunes Podcast Spec - http://www.apple.com/itunes/podcasts/specs.html

There are six main categories of attributes defined on the channel resource:

- Required Attributes (based on RSS)
- Required Attributes (based on iTunes)
- Recommended Attributes (based on RSS)
- Recommended Attributes (based on iTunes)
- Optional Attributes (based on RSS)
- Optional Attributes (based on iTunes)

Required Attributes - RSS
--------------------------------------------------------------------------------

### title

### link

### description


Required Attributes - iTunes
--------------------------------------------------------------------------------

### explict


Recommended Attributes - RSS
--------------------------------------------------------------------------------
### sourceUrl

Recommended Attributes - iTunes
--------------------------------------------------------------------------------


Optional Attributes - RSS
--------------------------------------------------------------------------------


Optional Attributes - iTunes
--------------------------------------------------------------------------------


Relations
--------------------------------------------------------------------------------

{
  "data": {
    "type": "podcastItem",
    "id": Integer or UUID,
    "attributes": {
      // Required - RSS Attributes
      title - String
      link  - String - Full URL
      description - String

      // Optional - Recommended - RSS Attributes
      category - Array of Strings
      enclosure - how do we type this?
        url - String - Full URL
        length - Integer in bytes
        type
      guid - String
      pubDate - Date - RFC 2822 - When this was published

      // Optional - RSS Attributes

      // Required - iTunes Defined - not RSS Attributes

      // Optional - Recommended - iTunes Defined - not RSS Attributes

      // Optional - iTunes Defined - not RSS Attributes


      // relations
      comments
    }
  }
}


author
comments
source
itunes:author
itunes:subtitle
itunes:summary
itunes:image
enclosure - url - length - type
guid
pubDate - RFC 2822
itunes:duration
itunes:block
itunes:explicit
itunes:isClosedCaptioned
itunes:order
