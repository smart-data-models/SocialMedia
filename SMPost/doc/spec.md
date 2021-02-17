Entity: SMPost  
==============





- No required properties  






  "id": "urn:ngsi-ld:SMPost:123",
  "type": "SMPost",
  "hasPostURL": "http://twt.com/121",
  "postCreatedAt": "2020-12-24T12:00:00Z",
  "postId": "21098319",
  "hasLanguage": "en",
  "platform": "Twitter",
  "hasText": "This is a tweet",
  "hasImage": "https://twt.com/image.png",
  "hasVideo": "https://twt.com/video.mp4",
  "hasPrivacy": "public",
  "location": {
    "type": "Point",
	"coordinates": 
	 [
	  40.3,
	  25.5
	 ]
	},
  "hasHashtag": "[#sample,#tag]",
  "hasThumbnail": "https://twt.com/thumb.png",
  "likes": 762,
  "createdBy": "urn:ngsi-ld:SMUser:123",
  "hasReferencedLocation": "urn:ngsi-ld:RefLocation:00",
  "hasMentions": "urn:ngsi-ld:SMUser:154",
  "isAnalyzedBy": "urn:ngsi-ld:Analysis:X",
  "belongsToCollection": "urn:ngsi-ld:SMCollection:001"
}
```  






  "id": "urn:ngsi-ld:SMPost:123",
  "type": "SMPost",
  "hasPostURL": {
    "type": "Property",
    "value": "http://twt.com/121"
  },
  "postCreatedAt": {
    "type": "Property",
    "value": {
			"@type": "DateTime",
			"@value": "2020-12-24T12:00:00Z"
			 }		
  },
  "postId": {
    "type": "Property",
    "value": "21098319"
  },
  "hasLanguage": {
    "type": "Property",
    "value": "en"
  },
  "platform": {
    "type": "Property",
    "value": "Twitter"
  },
  "hasText": {
    "type": "Property",
    "value": "This is a tweet"
  },
  "hasImage": {
    "type": "Property",
    "value": "https://twt.com/image.png"
  },
  "hasVideo": {
    "type": "Property",
    "value": "https://twt.com/video.mp4"
  },
  "hasPrivacy": {
    "type": "Property",
    "value": "public"
  },
  "location": {
    "type": "GeoProperty",
	"value": {
	 "type": "Point",
	 "coordinates": 
	 [
	  40.3,
	  25.5
	 ]
	}
  },
  "hasHashtag": {
    "type": "Property",
    "value": "[#sample,#tag]"
  },
  "hasThumbnail": {
    "type": "Property",
    "value": "https://twt.com/thumb.png"
  },
  "likes": {
    "type": "Property",
    "value": 762
  },
  "createdBy": {
   "type": "Relationship",
   "object": "urn:ngsi-ld:SMUser:123"
   },
   "hasReferencedLocation": {
   "type": "Relationship",
   "object": "urn:ngsi-ld:RefLocation:00"
   },
   "hasMentions": {
   "type": "Relationship",
   "object": "urn:ngsi-ld:SMUser:154"
   },
   "isAnalyzedBy": {
   "type": "Relationship",
   "object": "urn:ngsi-ld:Analysis:X"
   },
   "belongsToCollection": {
   "type": "Relationship",
   "object": "urn:ngsi-ld:SMCollection:001"
   },
  "@context": [
    "https://schema.lab.fiware.org/ld/context"
  ]
}
```  