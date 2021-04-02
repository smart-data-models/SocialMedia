Entidad: SMRefLocation  
======================







- `id`  

<details><summary><strong>full yaml details</strong></summary>    

SMRefLocation:    
  description: 'This entity contains a harmonised description of a generic SM Reference Location (SMRefLocation) made for the Social Media domain.'    
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
    locationName:    
      description: 'Name of the referenced location.'    
      type: Property    
      x-ngsi:    
        model: ' https://schema.org/Text'    
        units: 'No unit'    
    locationReferencedBy:    
      description: 'The ID of the post that references this location.'    
      format: uri    
      type: Relationship    
    type:    
      description: 'NGSI-LD Entity Type. It must be equal to SMRefLocation.'    
      enum:    
        - SMRefLocation    
      type: Property    
  required:    
    - id    
    - type    
    - locationName    
    - location    
  type: object    
```  
</details>    





  "id": "urn:ngsi-ld:RefLocation:00",
  "type": "SMRefLocation",
  "locationName": "Thessaloniki",
  "location": {
    "type": "Point",
	"coordinates": 
	 [
	  40.3,
	  25.5
	 ]
	},
  "locationReferencedBy": "urn:ngsi-ld:SMPost:123"
}  
```  






  "id": "urn:ngsi-ld:RefLocation:00",
  "type": "SMRefLocation",
  "locationName": {
    "type": "Property",
    "value": "Thessaloniki"
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
  "locationReferencedBy": {
   "type": "Relationship",
   "object": "urn:ngsi-ld:SMPost:123"
   },
  "@context": [
    "https://schema.lab.fiware.org/ld/context"
  ]
}  
```  