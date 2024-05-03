# Google Cloud Vision API Documentation 

## Badges
![Status](https://img.shields.io/badge/status-active-brightgreen)
![API Version](https://img.shields.io/badge/version-v1-blue) 
![GitHub last commit](https://img.shields.io/github/last-commit/AlfredoJMacias/MachineLearning_Documentation)
![GitHub issues](https://img.shields.io/github/issues/AlfredoJMacias/MachineLearning_Documentation)

<!--![Technology Banner](https://images.pexels.com/photos/577585/pexels-photo-577585.jpeg) <!-- Banner image sourced from Pexels -->
<div style="overflow:hidden; height:200px; position:relative;">
  <img src="https://images.pexels.com/photos/577585/pexels-photo-577585.jpeg" alt="Technology Banner" style="position:absolute; bottom:0;">
</div>


## Overview 🌐

The Google Cloud Vision API provides an advanced, powerful solution for integrating vision-related capabilities into applications. This API allows developers to perform tasks such as image labeling, face detection, landmark identification, optical character recognition (OCR), and the detection and tagging of explicit content, enhancing applications' understanding of images in various contexts.

## Authentication 🔑

**Authentication Type:** OAuth 2.0

**Usage:** To ensure secure access, the API uses the OAuth 2.0 authentication protocol. Access tokens must be obtained and included in the HTTP Authorization header as a Bearer token during API requests.

## API Endpoints 🚀

### Label Detection

- **Endpoint:** `POST /v1/images:annotate`
  
- **Description:** This endpoint detects and categorizes various elements within an image, including general categories, specific attributes, commercial logos, and notable landmarks.
  
- **Headers Required:**
  - **Authorization:** `string` - Bearer token
  - **Content-Type:** `string` - Application/json
    
- **Request Body Structure:**
  ```json
  {
    "requests": [
      {
        "image": {
          "source": {
            "imageUri": "https://example.com/photo.jpg"
          }
        },
        "features": [
          {
            "type": "LABEL_DETECTION",
            "maxResults": 10
          }
        ]
      }
    ]
  }


- **Response Structure:**
  ```json
  {
    "responses": [
      {
        "labelAnnotations": [
          {"description": "outdoor", "score": 0.99},
          {"description": "nature", "score": 0.98}
        ]
      }
    ]
  }


## Common Use Cases

- **Image Labeling**: Use the API to detect broad sets of categories within an image, such as tags, attributes, logos, and landmarks.
- **Face Detection**: Identify human faces within images along with their key attributes.
- **Landmark Detection**: Recognize well-known landmarks in images.
- **Optical Character Recognition (OCR)**: Convert images of typed or handwritten text into machine-encoded text.
- **Explicit Content Tagging**: Detect explicit content within images to help filter inappropriate content.

## 🔑 Authentication

Type: OAuth 2.0  
In Use: Access tokens are required and must be included in the Authorization header as a Bearer token.

## 📜 Conclusion

This document provides comprehensive details about the Google Cloud Vision API. This API allows developers to integrate advanced vision detection features within applications. Key functionalities include image labeling, face and landmark detection, optical character recognition (OCR), and tagging of explicit content. This guide includes information on how to authenticate, make requests, and handle responses.
