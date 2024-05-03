# Data-Integration-Log-bookmarklet
Sort Data Integration drop down to be in order alphabetically 


## Instructions

### Google Chrome, Microsoft Edge, Brave or any Chromium Browser
1a. You can right-click your bookmarks bar, then click "Add page...". Alternatively, you can go to your Bookmarks manager, then right-click and click "Add new bookmark":

### Firefox Browser 
1b. Either in your bookmarks bar, or in the Bookmarks sidebar (CTRL + B), you can right-click, then click "Add Bookmark...":
   
2. Set a name for this bookmarklet. I named mine "Data Integration Log Dropdown Organize"

3. In the URL field, copy and paste the code below:

```
javascript: (() => {
function sortSelectOptions(selectId) { var select = document.getElementById(selectId); var options = Array.prototype.slice.call(select.options, 0); options.sort(function(a, b) { if (a.text.toLowerCase() < b.text.toLowerCase()) return -1; if (a.text.toLowerCase() > b.text.toLowerCase()) return 1; return 0; }); select.innerHTML = ""; for (var i = 0; i < options.length; i++) { select.appendChild(options[i]); }} sortSelectOptions("diId");
})();
```
