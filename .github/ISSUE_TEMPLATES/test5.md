name: "Car Delete Form"
description: Request form for deletion of car in a existing repo
title: "[Car Delete Form]"
labels: ["form", "request", "delete"]
body: 
  - type: markdown
    attributes: 
      value: |
        **⚠️ Warning: This form deletes an car from an existing repository. Please follow the instructions carefully before submitting the issue.**
        Once submitted by an **admin** of repo, an issue cannot be undone. Please note the integration itself (Component in Boomi Platform) will not be deleted. 
  - type: input
    id: car
    attributes:
      label: Car Name
      description: Provide the name for your car. No spaces
      placeholder: car_name
    validations:
      required: true # doesn't work in private repos
  - type: input
    id: repository
    attributes: 
      label: Repository Name
      description: Name of the repository to delete car. No spaces.
      placeholder: repo_name
    validations:
      required: true
  - type: input
    id: year
    attributes: 
      label: Model Year 
      description: Provide the model year to delete car. No spaces.
      placeholder: year_number
    validations:
      required: true
  - type: input
    id: color
    attributes: 
      label: Car Colour 
      description: Provide the color  to delete car. No spaces.
      placeholder: color_name
    validations:
      required: true
  - type: markdown
    attributes: 
      value: |
       Once issue is submitted successfully, deletion of this car will be accomplished via a PR. After creating the issue the user will need to review, approve, and merge the PR before car will be deleted. 
