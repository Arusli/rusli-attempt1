START INSTRUCTIONS:
I recommend loading the folder into VS Code, and opening the index.html file with VS Code's 'live server' extension. As the instructions stated, I fetched the json data from the local file. For this reason, this app will only work if opened with a server (the fetch request will have an error if you open index.html in the browser directly). 

OVERVIEW: 
I completed the goal as stated in the test instructions, which was to make a functional lock-history section, populated with the data loaded in from the json file.

DESIGN DECISIONS:
- Added a 'SHOW LESS' option, in addtion to 'SHOW MORE'.
- Seemed the json was in chronological order, I reversed the array to show history from most recent to earliest.
- Wrote a timestamp formatting function to convert time to match sample page. This would not be able to account for different time zones, would need to be built out or use an external package to do this on a live site.

ADDITIONAL NOTES:
When I removed the 'zepto' script reference, as instructed, I noticed that it broke the other two external js scripts. It seems perhaps those scripts relied on that initial zepto script. Those scripts provided the collapsing functions/animations in the Q&A section of the page. The instructions said to maintain all collapsing/expanding functionality, but I don't see how I could avoid this problem, since we were also instructed to remove the zepto script. So I replaced the collapse/expand function of the Q&A section with vanilla javascript, and removed all 3 external script tags, as they no longer were functioning.

I used the Shadow DOM for my web component, and I noticed that the Euclid Font would not load in Chrome, although it worked in Safari. I worked around this by pre-loading that font in the <head> tag of the html doc.

In the sample page (test-1_page.html), I noticed there were many lines of code dedicated to creating SVG lock icons, but it seemed the stylesheets hid them from the page. I included the SVG's in my code as well, just in case. But like I said, they do not appear on the page.

I noticed that the unstyled html loads onto the page a split second before the styles take effect. I'd guess this has to do with the fact that the web component script is being called before the link tags, as well as the link tags not being inside the <head> tag. I think I'd need to get more familiar with web components to understand how to fix this.

To conclude, I found it pretty straightforward to implement the functionality and manipulate the data. My main difficulty was my lack of knowledge on the interplay of external styling/scripts within a web component. Honestly, I'd never built a web component before. I'd hope to learn more about this in the future.

-andrew rusli

