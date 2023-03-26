# Lane detection and object intersection

## presentation
- Project summary is in `Project_Summary-תקציר הפרויקט.docx` under the root of this project
- Project Document (explaining the tech, the need and the usage) in `autonomousCarDocFile.docx` 
[//]: # (todo: record new version with actual explanation)
- WIP -> Project display video: `https://www.youtube.com/watch?v=dMfKbLgRf4o`
- Presentation file is `פרוייקט סופי רכב אוטונומי אינטיליגנטי.pptx` under the root of this project
- Demo video on `https://youtu.be/8pshQXj9T8k` 

## in order to use the project
1. Run `pip install -r requirements.txt`.
2. Change `VIDEOS_LOCATION` parameter in main.py to the desired video or image directory (should be under <project-root>/data directory).
3. Select which view you want to see by simply commenting out the wanted views:
   1. Resize / Canny / Canny cropped / All lines / Avg lines / Final with object detection.
4. Run the program using the command `python main.py`.
5. Windows will pop-out with the views you asked for.


## Hyper-parameters
there are many hyperparams, some to keep in mind
1.	VIDEOS_LOCATION -> the desired video or image directory
2.	RESIZE_TO -> resizing input image (noticing `region_of_interest` function which may need to be change also)
3.	Rectangle variable under `image_manipulation.py` will change ROI in frame for lane detection task (for different camera locations)
4.	Slope threshold in function `average_slope_intercept` under `lines.py`, will remove any lines with lower slop (change for semi horizontal roads / more straight ones (highways) )
5.	Under function `extract_cnts` on `lanes_and_objects.py` there are many params, which should be changed to detect more/less objects (depends on the road conditions)
