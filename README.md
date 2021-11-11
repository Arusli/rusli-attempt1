Andrew Rusli, front-end test README.

START INSTRUCTIONS:
As the instructions stated, I fetched the json data from the local file. For this reason, this app will only work if opened with a server (the fetch request will break if you try to open index.html in the browser directly). I recommend loading the folder into VS Code, and opening with VS Code's 'live server' extension.

OVERVIEW: 
I completed the goal as stated in the test instructions, which was to make the lock-history section functional with the data loaded in from the json file.

NOTES:
When I removed the 'zepto' script reference, as instructed, I noticed that it broke the other two external js scripts. It seems perhaps those scripts relied on that initial zepto script. Those scripts provided the collapsing functions/animations in the Q&A section of the page. The instructions said we were not to lose any collapsing/expanding functionality, but I don't see how I could avoid this, since we were also instructed to remove the zepto script. So I replaced the collapse/expand function of the Q&A section with vanilla javascript, and removed all 3 external script tags, as they no longer were functioning.

I decided to use the Shadow DOM in my component. Although this was not explicitly instructed, I assumed that because we were working with a web component that this was desirable.

As a result of using the Shadow DOM, I did notice that some (but not all) of the linked stylesheets stopped working. So my final page does not have all the same stylings as the sample html page. I wish I knew how to fix this, but couldn't find much literature on it, so I left it. I'd be interested to learn more about this should I continue to work on web components.


