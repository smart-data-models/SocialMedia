Entity: SMCollection  
====================







- `id`  

<details><summary><strong>full yaml details</strong></summary>    

SMCollection:    
  description: 'This entity contains a harmonised description of a generic SMCollection made for the Social Media domain. This entity is primarily associated with the process of collection of Social Media posts (primarily Twitter).'    
  properties:    
    address:    
      description: 'The mailing address'    
      properties:    
        addressCountry:    
          description: 'Property. The country. For example, Spain. Model:''https://schema.org/addressCountry'''    
          type: string    
        addressLocality:    
          description: 'Property. The locality in which the street address is, and which is in the region. Model:''https://schema.org/addressLocality'''    
          type: string    
        addressRegion:    
          description: 'Property. The region in which the locality is, and which is in the country. Model:''https://schema.org/addressRegion'''    
          type: string    
        areaServed:    
          description: 'Property. The geographic area where a service or offered item is provided. Model:''https://schema.org/areaServed'''    
          type: string    
        postOfficeBoxNumber:    
          description: 'Property. The post office box number for PO box addresses. For example, Spain. Model:''https://schema.org/postOfficeBoxNumber'''    
          type: string    
        postalCode:    
          description: 'Property. The postal code. For example, Spain. Model:''https://schema.org/https://schema.org/postalCode'''    
          type: string    
        streetAddress:    
          description: 'Property. The street address. Model:''https://schema.org/streetAddress'''    
          type: string    
      type: Property    
      x-ngsi:    
        model: https://schema.org/address    
    areaServed:    
      description: 'The geographic area where a service or offered item is provided'    
      type: Property    
      x-ngsi:    
        model: https://schema.org/Text    
    description:    
      description: 'General description of the SMCollection.'    
      type: Property    
      x-ngsi:    
        model: ' https://schema.org/Text'    
        units: 'No unit'    
    hasPosts:    
      description: 'The IDs of the SMPost that belong in this SMCollection.'    
      items:    
        format: uri    
        type: string    
      type: Relationship    
      x-ngsi:    
        model: ' https://schema.org/Text'    
        units: 'No unit'    
    isAnalyzedBy:    
      description: 'The ID of the SMAnalysis that analyzes this SMCollection.'    
      format: uri    
      type: Relationship    
      x-ngsi:    
        model: ' https://schema.org/Text'    
        units: 'No unit'    
    location:    
      $id: https://geojson.org/schema/Point.json    
      $schema: "http://json-schema.org/draft-07/schema#"    
      properties:    
        bbox:    
          items:    
            type: number    
          minItems: 4    
          type: array    
        coordinates:    
          items:    
            type: number    
          minItems: 2    
          type: array    
        type:    
          enum:    
            - Point    
          type: string    
      required:    
        - type    
        - coordinates    
      title: 'GeoJSON Point'    
      type: object    
    type:    
      description: 'NGSI-LD Entity Type. It must be equal to SMCollection.'    
      enum:    
        - SMCollection    
      type: Property    
  required:    
    - id    
    - type    
  type: object    
```  
</details>    





  "id": "urn:ngsi-ld:SMCollection:001",
  "type": "SMCollection",
  "description": "this is a collection of posts",
  "location": {
    "type": "Point",
    "coordinates": 
	 [
	  40.3,
	  25.5
	 ]
	},
  "hasPosts": ["urn:ngsi-ld:SMPost:125","urn:ngsi-ld:SMPost:124"],
  "isAnalyzedBy": "urn:ngsi-ld:Analysis:331"
}
```  






  "id": "urn:ngsi-ld:SMCollection:001",
  "type": "SMCollection",
  "description": {
    "type": "Property",
    "value": "this is a collection of posts"
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
  "hasPosts": [
  {
   "type": "Relationship",
   "object": "urn:ngsi-ld:SMPost:125",
   "datasetId": "urn:ngsi-ld:Dataset:01"
  },
  {
   "type": "Relationship",
   "object": "urn:ngsi-ld:SMPost:124",
   "datasetId": "urn:ngsi-ld:Dataset:camera:01"
  }
  ],
   "isAnalyzedBy": {
   "type": "Relationship",
   "object": "urn:ngsi-ld:Analysis:331"
   },
  "@context": [
    "https://schema.lab.fiware.org/ld/context"
  ]
}
```  