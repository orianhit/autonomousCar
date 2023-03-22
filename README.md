# Lane detection and object intersection

## presentation
- Project summary is in `Project_Summary-תקציר הפרויקט.docx` under the root of this project
- Project display video: `https://www.youtube.com/watch?v=dMfKbLgRf4o`
- Presentation file is `פרוייקט סופי רכב אוטונומי אינטיליגנטי.pptx` under the root of this project
- Demo video on `https://youtu.be/8pshQXj9T8k` 

##in order to use the project
1. run `pip install -r requirements.txt`
2. change `VIDEOS_LOCATION` parameter in main.py to the desired video or image dir (should be under data dir)
3. select which view you want to see by simply commenting out the unwanted videos
   1. resize / canny / canny cropped / all lines / avg lines / final with object detection 
4. run the program `python main.py`
5. you will see opened windows with the views you asked for


## hyperparams
there are many hyperparams, some to keep in mind
1. RESIZE_TO -> resizing will require noticing region_of_interest function
2. changing crop in `image_manipulation.py` for other camera locations
3. slope in function `average_slope_intercept` under `lines.py`, should be changed for semi horizontal roads / more straight ones (highways)
4. function `extract_cnts` under `lanes_and_objects.py` may be change to detect more/less objects
