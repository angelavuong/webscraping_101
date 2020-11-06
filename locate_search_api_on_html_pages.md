# Guide: Locate search API on HTML pages

Simple guide to locate search API used to populate HTML pages

Resource: [http://www.gregreda.com/2015/02/15/web-scraping-finding-the-api/](http://www.gregreda.com/2015/02/15/web-scraping-finding-the-api/)

1. First, open the inspector tool for the browser you will be using.

2. Search for the URL you want to locate the relevant API.

    In our example, we use Cisco DevNet's Code Exchange for Ansible:

    ```
    https://developer.cisco.com/codeexchange/explore/#search=Ansible&page=1
    ```

    ![Image 1](https://github.com/angelavuong/webscraping_101/blob/master/images/webscraping-1.png)

3. Filter your dev inspector to Network and sort the requests by XHR.

    ![Image 2](https://github.com/angelavuong/webscraping_101/blob/master/images/webscraping-2.png)

4. Go through each requests and you can use the Preview tab to see the responses.

5. Once you found the API you were searching for, you can go to the Header tab and search for the ```request URL``` of the API you need.

    ![Image 3](https://github.com/angelavuong/webscraping_101/blob/master/images/webscraping-3.png)

    In our example, my request URL is:
    ```
    https://devnet.cisco.com/v1/metadata/catalogs/search?fastMode=true&type=Code&pageSize=12&pageNum=1&keyPrefix=Ansible&extended=true
    ```

    You can then verify the API response simply by searching the URL in your browser:

    ![Image 4](https://github.com/angelavuong/webscraping_101/blob/master/images/webscraping-4.png)
