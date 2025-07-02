- When generating production files, view the Gerbers
	- Select the board outline and press on "Home" to view full screen
	- Go through the layers trying to find errors. Sometimes overlay two related layers to check things are done properly
	- Use Isolate to set 1 layers as the top, and can select another to view (eg. Solder paste and Solder mask)


- When Gerbers are done, and ready to close off the project (no more changes), remeber to "Save to Server" and put the Version # in the comments (eg. V1.1)


- When all the files are completed, create the following files:
	- Put Gerbers folder in the Project Outputs/Version
	- Copy Project Outputs/Version to Google Drive in Work in Technical Work/02 - Electronic Work
	- Keep only latest version of the files (delete old)
	- Create zip folder of the gerber folder
	- Add Zip folder of the Altium Backup
		- Altium Backup:
			- Create a folder with the main project files as a backup
			- BomDoc, OutJob, PcbDoc, SchDoc, PrjPcb, Stucture, Variants