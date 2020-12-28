# Selenium Images Scraper for Rawpixel Website
This project scrape images from [rawpixel website](https://www.rawpixel.com/) that are on public domain.

## Prerequisites
* Install Chrome [Web Browser](https://www.google.com/chrome/).
* Install Chrome [WebDriver](https://sites.google.com/a/chromium.org/chromedriver/downloads), just ensure version compatibility with you Chrome Web Browser version.
* Install `Python 3.7`.

## Requirements
* The `requirements.txt` file contain `Selenium` and `tqdm` libraries.
* Install Requirements with `pip install -r requirements.txt`, it's good to install dependencies in Python virtual environment.

## Getting started
To start using this project you need to have account or create one in [rawpixel website](https://www.rawpixel.com/).

1. Open Chrome Web Browser in debugger mode.
    1. navigate to where your Chrome Web Browser application (`chrome.exe`) is installed in your filesystem, and copy the path where it's installed.
    2. Add the path to system environment variable `i.e PATH` "make sure to not include `chrome.exe` in the path".
    3. Create new directory fro where to launch the browser. it's added to avoid conflict with your already installed Chrome Web Browser.
    4. Open command prompt, and enter this command:
        ```
            chrome.exe -remote-debugging-port=9014 --user-data-dir="C:\Selenium\Chrome_Test_Profile"
        ```
        the port number is any four number of your choice. the command will launch Chrome Web Browser window in debugging mode.
    5. In the opened window (tab) navigate to [rawpixel website](https://www.rawpixel.com/) and login with your account informations.
    <br>**NOTE:** This feature run on >= 63 version of chrome web browser only.

2. Next, you need to run `get_session_cookies.py` Python script. to save your session cookies as `cookies.pkl` file.

## Running the tests
3. Finally, you need to run `img_scraper_rawpixel.py` Python script, to downlowd images in in your specified directory. Here is the command to run:

    ```
    python img_scraper_rawpixel.py \ 
        --browser_path="C:\Program Files (x86)\WebDriver\chromedriver.exe" \
        --output_dir="C:\ENP\Projects\GAN\Scripts\Download_img" \
        --url="https://www.rawpixel.com/board/574376/les-roses-pierre-joseph-redoute-free-cc0-roses-illustrations?sort=curated&mode=shop&page=1"
    ```
### Command Arguments:
* `--browser_path` absolute path to where you saved Chrome WebDriver `chromedriver.exe`.
* `--output_dir` where to put downloded images.
* `--url` URL of public domain images collection in [rawpixel website](https://www.rawpixel.com/) (e.g: https://www.rawpixel.com/board/574376/les-roses-pierre-joseph-redoute-free-cc0-roses-illustrations?sort=curated&mode=shop&page=1)

## Authors
Khalil Meftah.

## License
This Project is under MIT-License.













































