# Automated-ERA5-Land-Daily-Statistic-Data-Downloads-and-Conversion-to-GeoTIFF-with-Python

Overview:
Automates the process of downloading ERA5-Land daily statistical data, such as 2m temperature, and converting it into GeoTIFF format using Python. 
The script handles data extraction, conversion, and visualization, making it easy to work with geospatial datasets for climate analysis and mapping.

Features:
- Automatically download ERA5-Land data (e.g., 2m temperature, precipitation, etc.) using Python.
- Convert the downloaded NetCDF data to GeoTIFF format.
- Plot all GeoTIFF files together in a single grid.
- Save the layout as a PNG image.

Requirements:
- Python 3.x
- 'xarray' for handling NetCDF data.
- `rasterio' for writing GeoTIFF files.
- 'matplotlib' for plotting the GeoTIFFs.
- 'os', 'glob', and 'datetime' for file management.

Steps:
To use the Copernicus Climate Data Store (CDS) API for downloading ERA5-Land data, you need to create a .cdsapirc file for authentication. This file stores your CDS API credentials securely.

Steps to Create .cdsapirc File
  Obtain API Key:
    First, register on the Copernicus Climate Data Store if you don't have an account already.
    After registration, log in to the CDS and go to the "API key" section in your profile settings.
    Copy the CDS API Key (it will look like this: cdsapi.key=<your_api_key>).
    
Create .cdsapirc File:
  Open Notepad (or any text editor).
  Paste the following content into the file:
  makefile
  Copy
  Edit
  url: https://cds.climate.copernicus.eu/api/v2
  key: <your_username>:<your_api_key>
  Replace <your_username> with your CDS username and <your_api_key> with the API key you copied from the CDS website.
  
Save the .cdsapirc File:
  Save the file as .cdsapirc (including the dot at the beginning of the filename).
  Save the file in your home directory:
  On Windows, save it in C:/Users/YourUsername/ (replace YourUsername with your actual username).
  On Linux/Mac, save it in ~/.cdsapirc.

Verify Configuration:
  To ensure the .cdsapirc file is set up correctly, you can try to run a simple test using the CDS API client in Python.

Steps to Download ERA5 Data:
  This project includes a script to download ERA5-Land daily statistics. The script downloads 2m temperature data (e.g., minimum temperature) for a specified time period, converts it to GeoTIFF format, and saves the output.

Steps to Convert NetCDF Data to GeoTIFF
  Once the data is downloaded, you can convert it into GeoTIFF format. The following script uses xarray to load the NetCDF file and rasterio to convert the data.

Steps to Visualize the GeoTIFF Files:
  After converting the data into GeoTIFF files, the next step is to visualize them. Use the following script to load and plot the GeoTIFF files in a grid layout.

Conclusion:
This project automates the process of downloading, converting, and visualizing ERA5-Land data in GeoTIFF format. You can customize the script to adjust the variables and time period to fit your needs.
