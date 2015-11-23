Channel - Podcast
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
** String **

### link
** URL **

### description
** String **


Required Attributes - iTunes
--------------------------------------------------------------------------------

### explict
** Boolean **

Recommended Attributes - RSS
--------------------------------------------------------------------------------

### language
** String ** - RFC 1766

### lastBuildDate
** Date ** - RFC 2822
Last updated at

### ttl
** Integer **

minutes of how long it can be cached

Recommended Attributes - iTunes
--------------------------------------------------------------------------------

### subtitle
** String **

Optional Attributes - RSS
--------------------------------------------------------------------------------

### copyright
** String **

### generator
** String **
What generated this feed

### docs
** URL **
Docs to reading the format


Optional Attributes - iTunes
--------------------------------------------------------------------------------
### summary
** String **

### complete
** Boolean **

### newFeedURL
** URL **

### block
** Boolean **

Relations
--------------------------------------------------------------------------------
### author - Has One - Person
### owner  - Has One - Person
### managingEditor - Has One - Person

### webMaster - Has One - Person
### image - has one - Image

### editors - Has Many - Person
### hosts   - Has Many - Person
### guests  - Has Many - Person
### contributors - Has Many - Person

other resources?
bookmarks on podcast?
Show notes?
categories - has many (nesting?)


```json
{
  "data": {
    "type": "podcast",
    "id": 1,
    "attributes": {
      "title": "Example Podcast",
      "link":  "https://example-podcast.com/podcasts",
      "description": "Description for the Example Podcast",
      "language": "en-us",
      "lastBuildDate": "Sun, 15 Jun 2014 19:00:00 GMT",
      "ttl": 1440,
      "pubDate": "Sat, 14 Jun 2014 12:00:00 GMT",
      "copyright": "",
      "generator": "",
      "docs": "",
      "explicit": false,
      "subtitle": "",
      "complete": false,
      "newFeedURL": "",
      "block": false
    },
    "relationships": {
      "author": {
        "links": {
          "self": "",
          "related": ""
        },
        "data": { "type": "person", "id": 2 }
      },
      "owner":{
        "links": {
          "self": "",
          "related": ""
        },
        "data": { "type": "person", "id": 3 }
      },
      "managingEditors": {
        "links": {
          "self": "",
          "related": ""
        },
        "data": { "type": "person", "id": 4 }
      },
    }
  }
}
```
