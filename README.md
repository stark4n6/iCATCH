
# iCATCH![iCatch](https://github.com/user-attachments/assets/38d5845a-e9d0-4bf7-9ce2-7b924dbac34e)

The iOS Cache Analysis for Tracking Coordinates History (iCatch) is a utility to process the iOS Cache.sqlite database and create a timelined KML map for use in Google Earth.


This utility allows you to export GPS data from the iOS Cache.SQLite database, generate CSV and KMZ files, and log details for analysis.

A processing log, csv file containing records of processed files (within time/date filter considerations), and KMZ file are output to a new directory at the user-selected location.

    
    *************
    All times are processed and output in Coordinated Universal Time (UTC-0)
    Due to their size, multiple KMZ files may be generated and are limited to 10,000 records each.
    *************
    


## Requirements

#### This tool is intended to be run using Python. A Windows executable with the latest updates be distributed from time to time.
Requirements - To install the required Python libraries, use the command: pip install -r requirements.txt
## Usage
To open GUI, from the CLI run 

    py iCatch_v1.X.pyw

1.	Input case information.
2.	Select path of Cache.sqlite database which is found at: private/var/mobile/Library/Caches/com.apple.routined/Cache.sqlite
3.	Select desired color for pin and accuracy ring.
4.	Select radius filter to limit the maximum radius of horizontal accuracy.
5.	Select Date/Time filter options. This option is enabled by default. 
a.	It is highly recommended to use this option as the database contains tens of thousands of points, and can have thousands of points in a short timeframe.

Date triage function will quickly display the dates which are stored within the database, along with the number of records for those dates.

### Google Earth Pro Usage:
•	The KMZ file should be used with Google Earth Pro desktop version. The file is loaded into temporary places. Each point has two items: the "Pin" and the horizontal accuracy overlay. Only the pin is loaded automatically to save system resources.

•	The timeline slider should be adjusted to a smaller timeframe before loading (full-checking) the loaded KMZ folder. This will ensure that not all (up to) 10,000 points and overlays are loaded at once.

•	To adjust the visible timeframe, use the slider points on the timeline bar, as well as the settings option.

•	All records are processed in UTC-0 and the settings options will allow for timezone display adjustments.

## Acknowledgements
For more informaiton about the Cache.sqlite database, including speed artifacts, check ou the amazing work by Scott Koenig at: https://theforensicscooter.com/2021/09/22/iphone-device-speeds-in-cache-sqlite-zrtcllocationmo/
