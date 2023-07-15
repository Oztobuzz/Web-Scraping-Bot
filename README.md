
<h3 align="center">WEB SCRAPING BOT</h3>
  <p align="center">
    A dynamic/static web scraping bot using Selenium 3 and Beautiful Soup 4
  </p>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

I build this mini-project as I need a tool to scrape web data for my own use. I hope this simple tool can help you guys with your bigger project. 

<p align="right">(<a href="#readme-top">back to top</a>)</p>



### Built With

* <a href= "https://www.selenium.dev/"><img src= "https://camo.githubusercontent.com/74ed64243ba05754329bc527cd4240ebd1c087a1/68747470733a2f2f73656c656e69756d2e6465762f696d616765732f73656c656e69756d5f6c6f676f5f7371756172655f677265656e2e706e67" width="200"  />
* <a href= "https://www.python.org/"><img src= "https://miro.medium.com/v2/resize:fit:1400/1*m0H6-tUbW6grMlezlb52yw.png" width="200"  />
* <a href= "https://www.crummy.com/software/BeautifulSoup/bs4/doc/"><img src= "https://www.jeveuxetredatascientist.fr/wp-content/uploads/2022/06/BeautifulSoup-1080x428.jpg" width="200"  />

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- GETTING STARTED -->
## Getting Started

In order to be able to run the code, you will have to install some **separate libraries**, those libraries will be listed below in installation

I also give flow of the code and an example of how to modify your code to extract information from **raw html**

### Installation

1. [Chrome Driver](https://chromedriver.chromium.org/) compatible to your Chrome version (or your preferred browser driver) (Remember your .exe path, we will use it)
2. [Selenium](https://pypi.org/project/selenium/) (different versions will have different syntax, in my project I use Selenium 4)
   ```sh
   pip install -U selenium
   ```
3. [Beautiful Soup 4](https://www.crummy.com/software/BeautifulSoup/bs4/doc/)
   ```sh
   pip install beautifulsoup4
   ```
4. Download this repository .ipynb file and run

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- USAGE EXAMPLES -->
## Usage
- Pass website link at website
- Pass your path of _ChromeDriver.exe_ into path
  ```python
  website = 'your website'
  path = 'path to your chromedriver.exe file'
  ```
- **OPTIONAL:** there is one optional module that helps us to auto-scrolling the website, I set it as an **infinite scroll** because 
 https://hcmut.edu.vn/danh-sach-tin-tuc requires scrolling to fetch new data (just stop by interrupting the cell)
 - Extract information from website:
    1. Check for **html structure** of your desired website
    2. Check for the _tag_ and _class_ of your interested fields. 
    3. Put it in the 
    ```python    
    soup.findall('yourtag', class_ = 'yourclass') (#this will return a list)
    ```
    4. Loop through the list (use find to get an element)
 - There are **2 ways** to save data: 
    1. Save all data to **csv file**
    2. Save to **separate txt files** ( _Remember to first create a folder to contain all the txt files_ )
 - Further **modification** to your need

### Example
  This is my scraped **website's HMTL structure**
  
  ![exampleHTML](https://user-images.githubusercontent.com/77455949/236163720-e2c0c4dd-8642-4a2a-9dd6-4a2c56bac6dd.png)
  
  In order to get the **header content** out:
  ```python
  headers = soup.find_all('h3', class_ = 'heading')
headerContent = []
for header in headers:
    headerContent.append(header.find('p').text.lower())
print(headerContent) 
  ```
  
  **Result:**
  
  ```sh
  '555 bộ bàn ghế học tập được trường đh bách khoa trao tặng cho ubnd huyện châu thành'
  ```



<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.



<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE.txt` for more information.

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- CONTACT -->
## Contact

**Oanh Tran - oanh.tranotsc1123@hcmut.edu.vn**

Project Link: [https://github.com/Oztobuzz/Web-Scraping-Bot](https://github.com/Oztobuzz/Web-Scraping-Bot) 

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

* [Web Scraping to CSV | Multiple Pages Scraping with BeautifulSoup](https://www.youtube.com/watch?v=MH3641s3Roc&t=1480s)
* [Web Scraping with Python - Beautiful Soup Crash Course](https://www.youtube.com/watch?v=XVv6mJpFOb0&t=3420s)
* [Automate with Python – Full Course for Beginners](https://www.youtube.com/watch?v=PXMJ6FS7llk&t=4989s)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

