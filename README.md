# Data-Integration-Log-bookmarklet
Sort Data Integration drop down to be in order alphabetically 


## How to Create the bookmarklet

#### Google Chrome, Microsoft Edge, Brave or any Chromium Browser
1a. You can right-click your bookmarks bar, then click "Add page...". Alternatively, you can go to your Bookmarks manager, then right-click and click "Add new bookmark":

#### Firefox Browser 
1b. Either in your bookmarks bar, or in the Bookmarks sidebar (CTRL + B), you can right-click, then click "Add Bookmark...":
   
2. Set a name for this bookmarklet. I named mine "Data Integration Log Dropdown Organize"

3. In the URL field, copy and paste the code below:

```
javascript: (() => {
function sortSelectOptions(selectId) { var select = document.getElementById(selectId); var options = Array.prototype.slice.call(select.options, 0); options.sort(function(a, b) { if (a.text.toLowerCase() < b.text.toLowerCase()) return -1; if (a.text.toLowerCase() > b.text.toLowerCase()) return 1; return 0; }); select.innerHTML = ""; for (var i = 0; i < options.length; i++) { select.appendChild(options[i]); }} sortSelectOptions("diId");
})();
```
4. Click Save

## How to use the bookmarklet

1. Go to your Blackboard Learn instance
2. Click on *Admin* then go to *Logs* under *Tools and Utilities*
3. Right click on SIS Logs
4. Click open in a new tab or open in a new window
5. In the new window or tab, click on the bookmarklet you created
6. Your drop down should now appear in alphabetical order. (See the image below)

#### Image Example of what the bookmarklet does

![A screenshot of the dropdown menu from the data integration page displaying before and after. The left side of the image displays before using the bookmarklet, the right shows after using it.](https://i.ibb.co/h8sK3d7/2024-05-03-12-46-56.png)
