# Overview

* Grid with number and letter coordinates
* Button on the grid that brings in the next picture
* Each time the button is pressed the other pictures are also randomly positioned

# Tech stuff

## Provisioning

### Terraform?
  * Build out s3 buckets
  * Build out API gateway
  * Deploy lambda scripts


## Frontend

* React frontend
  * CSS grid?
  * How are the images within the grid placed?
    * CSS background?
    * Image tag?
    * CSS-in-JS?
  * Gets a list of all the objects in the box
  * {
      (obj1.1, obj1.2, obj1.3, obj1.4)
      (obj2.1, obj2.2, obj2.3, obj2.4)
      (...)
      (...)
  }
    

### Backend:

  * API gateway
  * Lamdba scripts (python)
  * /current_image
    * If no manifest file exists, then write one
      * Object ID of file
      * Listed in order of display
    * If a manifest file exists then read it
      * return the grid references and the paths
  * /new_image
    * Moves new image from one folder to another folder
    * Resizes image as well (https://docs.wand-py.org/en/0.6.10/)
    * randomises the grid references for the 
