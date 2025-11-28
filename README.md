Go to the "releases" section to the right and download the first .zip file then extract onto your computer. Inside you will find the .exe and working directory where you can put your on-board footage.

Welcome to Andrew's Formula Apex Grapher! This is v1 so if you have any question dm me on discord: invisiblecrumb

This program generates a speed graph of a Formula Apex car by using Tesseract OCR on on-board footage. 

Since this is v1, users of this program must be careful to type the full names of files and follow the naming conventions below. However, users who who simply input cropped video (most users) will have the naming of files done automatically by the program.

(i made this at 3 am lol)

---------------------------------IN THIS DOCUMENT---------------------------------:

- Requirements
- How it Works
- How to use
- Notes
- Example use cases
- Future updates

---------------------------------REQUIREMENTS---------------------------------:

- Formula Apex on-board video cropped to speedometer with OCR-B font enabled. 

- The higher resolution the better, 1080p is known to work in my own testing. 

- The tool will not read the default formula apex font effectively. Roblox font must be changed either via Bloxstrap for windows or Appleblox for mac. I am working on training an OCR model that can read the default font. This will be in later versions of the tool.

- An example video has been placed in the 'cropped videos' folder for reference.

- A .txt file of raw data has been given if you want to try graphing it

---------------------------------HOW IT WORKS---------------------------------:

The program:

	1. Converts video into an image sequence
	
	2. Reads the speed measurement on each image 

	3. Saves each measurement to a .txt file

	4. Generates a speed graph.

---------------------------------HOW TO USE ---------------------------------

1. Place your cropped video in the cropped videos folder (if not reading from .txt file)

2. Launch the tool

3. Enter the video's fps

4. Enter the video's name including the file type extension. e.g. Germany.mp4

*5. If you do not want to generate a new image sequence (e.g. you already have one generated, from another software or this one), enter 'y'. If you need to generate a new sequence, enter 'n'

**6. If you already have a .txt file with your data, enter the file name. If not, generate data by entering 'n'

---------------------------------NOTES---------------------------------

* Make sure your image sequence is in a folder named: "frames_out_" + [video name] 
e.g. frames_out_Germany.mp4 

** Make sure your .txt file is named: [video name] + raw data (.txt files do not need their own folder)
e.g. Germany.mp4 raw data

If you use this tool in one go from start to finish, all naming conventions are already taken care for you and you do not have to worry about the above notes.

Sometimes the OCR model may misread values. e.g. '0', '839'. You will be able to easily spot any outliers on the graph. If you get outliers, you may simply open the generated raw data file and delete these values. After you have done this, you can skip straight to graphing, no need to extract data again.

---------------------------------EXAMPLE USAGE---------------------------------: 

- video -> graph (most use cases):
	Enter video fps: 60
	Enter video name (including file type!): Germany.mp4
	Skip video conversion? ('frames_out folder already generated?)(y/n): n
	Skip OCR reading + data extraction? ([insert existing file name.txt]/n): n

- image sequence -> graph (use if image sequence previously generated):
	Enter video fps: 60
	Enter video name (including file type!): Germany.mp4
	Skip video conversion? ('frames_out folder already generated?)(y/n): y
	Skip OCR reading + data extraction? ([insert existing file name.txt]/n): n

- .txt -> graph (use if data previously generated)
	Enter video fps: 60
	Enter video name (including file type!): Germany.mp4
	Skip video conversion? ('frames_out folder already generated?)(y/n): y
	Skip OCR reading + data extraction? ([insert existing file name.txt]/n): Germany.mp4 raw data.txt

---------------------------------Future updates---------------------------------:

- Train OCR model for default font
- better organized and intuitive naming/filing conventions
- Ability to represent 2 datasets in 1 graph for easy comparison between drivers
- Faster reading of images
