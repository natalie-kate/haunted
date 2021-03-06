# Testing

## Contents 
   - [Automated Testing](#automated-testing)
      * [HTML validation](#w3c-markup-validator)
      * [CSS validation](#w3c-css-validator)
      * [Lighthouse testing](#lighthouse-in-devtools)
   - [Testing User Stories](#testing-user-stories)
   - [Manual testing](#manual-testing)
   - [Bugs](#bugs)
      * [Found and Fixed](#found-and-fixed)
      * [Existing](#existing)


## Automated Testing

The W3C Markup Validator and W3C CSS Validator were used to validate every page of the project to ensure there were no 
syntax errors in the project.

-   ## [W3C Markup Validator](https://jigsaw.w3.org/css-validator/#validate_by_input) 

    ### Initial testing
    - index.html

    ![Initial index html test](assets/testing/testing-images/initial-html-test.png)

    From this I removed the aria label from the badges, reformatted my comment and removed figcaption from my 
    picture. Changed the figcaption to paragraph, but did not like either so just made it an img element with a 
    paragraph below for the attribute.

    - evidence.html

    ![Initial evidence html test](assets/testing/testing-images/initial-html-test2.png)

    I had missed a bracket in the media attribute of a few source elements so I added them in.
    
    ![Initial evidence html test](assets/testing/testing-images/initial-html-test3.png)
    
    I had put paragraph elements in my iframes to give a message with a link to the video in the event that
    the video would't load. This isn't allowed so I put the paragraph below the iframe and encased them both
    in a div. Styled with media queries to be responsive.
    Near the end of the project I re-ran it through and I had to remove loading, width and height attributes from 
    the source elements. 
    
    - contact.html

    ![Initial contact html test](assets/testing/testing-images/initial-html-test4.png)
    
    ### Final testing (for those that needed fixed)
    - index.html

    ![Final html text](assets/testing/testing-images/final-html-test.png)

    - evidence.html

    ![Final html text](assets/testing/testing-images/final-html-test2.png)


-   ## [W3C CSS Validator](https://jigsaw.w3.org/css-validator/#validate_by_input) 
    
    ### Initial testing

    ![Initial css test](assets/testing/testing-images/initial-css-test2.png)

    Had wrote display:relative instead of position: relative for an image.
    Had also put a comma instead of a semi-colon at the end of text-decoration: none.

    ![Initial css test](assets/testing/testing-images/initial-css-test.png)

    Ran again near end of project and I hadn't put px in some of the font-size styles.

    ### Final testing

    ![Final css test](assets/testing/testing-images/final-css-test.png)

-   ## [Lighthouse](https://chrome.google.com/webstore/detail/lighthouse/blipmdconlkpinefehnmjammfjpmpbjk?hl=en) in devtools
    
    ### Initial scores 

    #### Landing page

    + Initial lighthouse score for landing page on desktop was Performance 77, Accessible 92, Best Practices 87 and SEO 91
    
    + Initial mobile

    ![Initial landing page scores for mobile](assets/testing/testing-images/landing-page-mobile-initial.png)

    #### Evidence Page

    + Initial desktop

    ![Initial evidence page scores for desktop](assets/testing/testing-images/evidence-desktop-initial.png)

    + Initial mobile

    ![Initial evidence page scores for mobile](assets/testing/testing-images/evidence-mobile-initial.png)

    #### Contact Page

    + Desktop and mobile initial and final values didn't change much so I have just included the final test results

    ### Actions taken

    From these scores I added in meta description, keywords and author. rel:noopener to my extenal links and changed 
    an h2 to an h5. I had used in the h2 in my fact-box where I should have used the h5 and styled the font-size. I 
    also had skipped h3 so I changed the h4's to h3's. Went over all my buttons and links ensuring I had aria labels 
    and images had alt text, darkened the badge colour to increase contrast. Due to these changes the rest of my 
    tests had 100% accessibility, Best Practices and SEO so just had to focus on performance.
    
    Lighthouse didn't like that the images didn't have explicit width and height attributes so added them in.
    Removed scripts from both evidence and index pages as seemed to be a major rendor blocking resource. Helped
    fractionally but then had to add them back in when I realised I needed them for the bootstrap dropdown 
    toggled menu to work.

    Images were still an issue, found an article that mentioned using the loading attribute, so added with a 
    value of lazy to all my images and iframes. That helped immensely.
    First contentful paint still slow, mostly this seems to be down to the external CDN's such as bootstrap 
    and font awesome. Did highlight that one of my image files was still quite large so resized image 15, along with
    both my main landing page image and header image for mobile screens. 

    ### Final test 

    #### Landing page

    + Final Desktop (see report [here](assets/testing/testing-reports/landing-page-desktop.pdf))

    ![Final landing page scores for desktop](assets/testing/testing-images/landing-page-desktop.png)

    + Final mobile (see report [here](assets/testing/testing-reports/landing-page-mobile.pdf))

    ![Final landing page scores for mobile](assets/testing/testing-images/landing-page-mobile.png)

    #### Evidence page

    + Final desktop (see report [here](assets/testing/testing-reports/evidence-desktop.pdf))

    ![Final evidence page scores for desktop](assets/testing/testing-images/evidence-desktop.png)

    + Final mobile (see report [here](assets/testing/testing-reports/evidence-mobile.pdf))

    ![Final evidence page scores for mobile](assets/testing/testing-images/evidence-mobile.png)

    #### Contact Page

    + Final Desktop (see report [here](assets/testing/testing-reports/contact-desktop.pdf))

    ![Contact page scores for desktop](assets/testing/testing-images/contact-desktop.png)

    + Final Mobile (see report [here](assets/testing/testing-reports/contact-mobile.pdf))

    ![Contact page scores for mobile](assets/testing/testing-images/contact-mobile.png)

## Testing User Stories 

- ### First Time Visitor 

 1. As a first time visitor, I want to easily understand the main purpose of the site. 
   <span style="color: grey;">The content overlay has a ghost icon that links to ghost stories, slogan of "Do you
    believe in Ghosts", and directly below is an About paragraph with the first sentence 
    explaining the purpose of the site.</span>

    ![Image showing landing page](assets/testing/testing-images/mobile2.png)
    
 2. As a first time visitor, I want to be able to easily navigate throughout the site to find content.<br>
   <span style="color: grey;">The nav menu is at the top of all pages with drop down menus to find and jump to the section of 
   interest. The brand name is also a link back to home.

    ![Image showing navbar](assets/testing/testing-images/nav.png)  ![Image showing dropdown menu](assets/testing/testing-images/menu.png)

    In addition a "back to top" link is present in the footer meaning the user doesn't have to scroll back up to 
    the top, which is especially important for the mobile site.</span>

    ![Image showing back to top link](assets/testing/testing-images/social.png)

3. As a first time visitor, I expect to see an attractive, visually appealing site.
    <span style="color: grey;">Used blocks of colour as the background colours for section headings to break up the page,
    and highlight a new section. Information is presented in different formats and hover effects draw attention to links 
    and call to action buttons. The same colours were consistently used across the site for predictability and simplicity 
    and doesn't look too busy which can be off putting.</span>

    ![Image showing section heading and fact box](assets/testing/testing-images/information-formats.png)
    ![Image showing text and table content](assets/testing/testing-images/information-formats2.png)

4. As a first time visitor, I expect an accessible site.
   <span style="color: grey;">Aria labels, screen reader only text and alternative text have been used throughout the site. 
   Styled the outline of keyboard focus making it more obvious as to where they are on the page and colour ties in with the 
   other colours on the screen. All colour contrast scores were a pass in chrome dev tools and accessibility score was 100%.
   As the buttons have an animation hover effect added in code in the case of user prefers reduced motion to turn the animation 
   off but to change colour instead so they still see clickable elements. </span>

   ![Image showing keyboard focus style](assets/testing/testing-images/keyboard-focus.png)

5. As a first time visitor, I expect the site to look good on any device I choose to use.
   <span style="color: grey;">Designed with mobile first in mind, using bootstrap and media queries to ensure that on all screen 
   sizes that the site looks good with no escaping contents or horizontal scrolling and that the hero and header images are positioned 
   correctly as these are what people see first upon loading so they have to be perfect. As mobile users can't see hover effect on 
   buttons, gave them a border colour to make it clearer that they are clickable.</span>

   ![Image showing mobile landing page with style button](assets/testing/testing-images/mobile2.png) 
   ![Image showing mobile evidence page](assets/testing/testing-images/mobile1.png) 
   ![Image showing mobile contact page](assets/testing/testing-images/mobile3.png)

   ![Image showing tablet landing page](assets/testing/testing-images/tablet1.png) 
   ![Image showing tablet evidence page](assets/testing/testing-images/tablet2.png) 
   ![Image showing tablet contact page](assets/testing/testing-images/tablet3.png)

   ![Image showing desktop landing page](assets/testing/testing-images/desktop1.png) 
   ![Image showing desktop evidence page](assets/testing/testing-images/desktop2.png) 
   ![Image showing desktop contact page](assets/testing/testing-images/desktop3.png)


- ### Returning Visitor Goals

1. As a returning visitor, I want to easily identify new content.
   <span style="color: grey;">Bright badges have been used to highlight in the nav which page contains new 
   content, in the dropdown menu the section also has a badge and when you are taken to this section the new content
    itself is highlighted with the badge.</span>

    ![Image showing new content badges](assets/testing/testing-images/menu.png)

2. As a returning visitor, I want to see social media links so that I can follow on my chosen platforms.
    <span style="color: grey;">At the bottom of each page is the social platform icons with links to the pages. Only 
    takes you to the social media platform itself as accounts for this website don't exist in real life.</span>

    ![Image showing social media links](assets/testing/testing-images/social.png)

3. As a returning visitor, I want to see recommended resources to learn more.
    <span style="color: grey;">This is one of the main nav menu items and therefore easy to find and navigate to.</span>

    ![Image showing further resources section](assets/testing/testing-images/resources.png)
    
4. As a returning visitor, I want to be able to contact the owner with comments or questions.
    <span style="color: grey;">The contact page is one of the main nav items so is easy to find and navigate to. The 
    form has a text box to enter comments and/or questions. The form will not submit unless the personal (required) details
    are completed. There is also a feedback modal so that the user knows that their form has been submitted successfully.</span>

    ![Image showing comments box](assets/testing/testing-images/text-box.png)
    ![Image showing form prompts](assets/testing/testing-images/prompt.png)
    ![Image showing modal for successful form submit](assets/testing/testing-images/modal.png)


- ### Frequent Visitor Goals

1. As a frequent visitor, I want to easily identify new content.
    <span style="color: grey;">Bright badges have been used to highlight in the nav which page contains new 
   content, in the dropdown menu the section also has a badge and when you are taken to this section the new content
    itself is highlighted with the badge. </span>

    ![Image showing new content badge on he new content](assets/testing/testing-images/badge.png)

2. As a frequent visitor, I want to sign up to the mailing list so that i'm informed of new content or features.
    <span style="color: grey;">Contact is one of the main nav items so its easy to find and navigate to and there is a 
    checkbox to select to be added to the mailing list.</span>

    ![Image showing checkbox to sign up to mailing list](assets/testing/testing-images/mailing-list.png)

3. As a frequent visitor, I want to send stories, pictures or videos to be added to the page. 
    <span style="color: grey;">Contact is one of the main nav items so it is easy to find and navigate to. There is a 
    text box to add a story and a file upload input for pictures and videos. There is also a call to action button in the 
    landing page container to "Tell us your true stories", and two in the evidence page to "Share your experiences" and 
    "Share your photos and pictures"</span>

    ![Image showing call to action button on landing page](assets/testing/testing-images/landing-button.png)
    ![Image showing call to action button in true story section](assets/testing/testing-images/true-story-button.png)
    ![Image showing call to action button in media evidence section](assets/testing/testing-images/media-evidence-button.png)

## Manual Testing

-   The website was viewed with browsers: Internet explorer, Google chrome, Safari, Microsoft Edge, Firefox
    and Opera. Viewed all three pages on each and checked the following:
    * Haunted brand takes user back to landing page from the other two pages.
    * Nav links work from all three pages to all links.
        + <span style="color: grey;">Theory nav item was missing from both the evidence and contact pages. Amended.</span>
        + <span style="color: grey;">Found that the link to resource section from contact page was wrong. Amended.</span>
    * Clicking the font awesome ghost takes user to True stories section.
    * Clicking "Tell us your true Stories", "Share your experiences" and "Share your picture and videos" buttons take user to contact page.
    * The reference links open in a new page, to the correct resource.
        + <span style="color: grey;">Reference 2 and 4 were to the same website, this is correct but no need for different numbers so all 
        the numbers changed to reflect this.</span>
    * The two pictures that required an attribute had links that opened in a new page to the correct places.
    * Social links in footer all open in a new page and work from all three pages.
       + <span style="color: grey;">When trying to open with internet explorer, kept opening with Microsoft Edge instead, apparently they no 
       longer work with Internet explorer. Ensured it wasn't my link by trying to visit the page separately and it did the same.</span>
    * Back to top link in footer works in all three pages.
    * Hover effects on Brand, ghost icon, social icons and all links and buttons.
        + <span style="color: grey;">Hover change of colour on resource page picture attribute and "back to top" link not working, amended.</span>
    * "Show me more awesome stories" button works.
    * All embedded videos play with controls and not automatically.
    * Video links incase of embedded video not loading, open in a new page and are correct.
        + <span style="color: grey;">Internet explorer issue same as social links.</span>
    * Resource links all open in a new page and are correct.
        <span style="color: grey;">Internet explorer issue same as social links for the youtube resources, the others opened fine.</span>
    * Form will not submit without all three required personal details being completed. Checkboxes work, can only check one, can type in text area,
      "Choose file" input opens computer files and allows user to add files. On successful form submission, modal appears and can be closed by both
      close buttons.
        + <span style="color: grey;">Form legend not centred on Internet Explorer or Firefox, added the bootstrap class text-center. This did
          not fix it. Tried putting a surronding div around the legeng to target it, it put the legend into the fieldset set box. Gave the legend 
          another class to target with text-align: center, this did not work either.</span>
-   Friends, family and slack peer review used. Devices and browsers were iphone 11: Safari (x3), iphone XS Max: Safari,
    iphone 6: Chrome, iphone XR: safari, iphone 11 Pro: Safari, iphone 10: Safari, Samsung S20 FE: Chrome, Samsung S10, Sony Xperia I3: Chrome,
    Samsung tab 7, Huawei tablet and HP chromebook.
    + <span style="color: grey;"> One comment was to increase spacing after picture section and video heading which I did.</span>
    + <span style="color: grey;"> Another found that the burger icon wasn't working. This was when I had removed the javascript to try
    and improve performance score before realising I needed the javascript for the collapsible menu. Thankfully it was only out for 
    10 minutes </span>
-   Chrome devtools used to test responsiveness throughout the development process see bugs found [below](#bugs). Viewed all pages on all of the 
    available devices at the end of the project to ensure everything still looked good.
-   Viewed physically on Macbook air 13", Dell 21" HD screen, iphone 11, Dell 17" laptop and Pixel 4XL phone to ensure that after all 
    issues found and resolved that there was nothing else appearing   

## Bugs

   ### Found and Fixed 

   In addition to the issues found in manual testing, I also found the below.

   - Header image on bigger screens looked a bit thin, so added a media query for over 1400 screens 
    to make background image min-height: 40vh .
   - Toggle menu dropdown was going behind header text so added z-index: 1. Dropdown menu was moving
    the content below down which didn't look nice so changed position to absolute which I found by playing
    with devtools.
    Also in mobile it was taking up a lot of real estate so decreased font-size and line-height.
   - Found one of the new badges on the True Stories was going into the second line between screen sizes
    980 to 1030 so changed font size from 75% to 55% for the h3's only.
   - Iphone 5 footer content not contained, reduced size of icons and font-weight of span. Media query
    wrote to increase again on bigger screens.
   - Footer was still escaping for galaxy fold so added in a media query for screens less than 350px.
   - On ipad Pro there was a gap below hero image on landing page and About header. Changed positioning 
    of background image that was in media query from top to bottom. This resurfaced as I was rechecking before
    submission, changed media query for image for >1000px and changed back for >1200px with a new query.
   - Hero image and header image looking pixelated where the xsmall version is being used. Have changed back 
     to small will change again if I find a solution as will effect my performance scores. Solution: Added 
     in media query for screens smaller than 450px (majority of mobiles) to use the xsmall versions of the
     main images. Looks pixelated on devtools but fine on phones themselves- Amendment took back out again 
     hadn't refreshed on phone and was pixelated still. Similarly the small version is looking pixelated on 
     screens above 1000px so have changed to original image at this point. 
   - Testing on mobile when realised that the read more button wasn't working. After two and a half hours of
    going back the stack overflow example and playing about in code pen, realised I had put the input and 
    label in its own div so that i could apply bootstrap classes to it for positioning. So after playing 
    about with it put the input and label along with the hidden stories in one big div and applied the 
    bootstrap col class directly to the label. 
  - On mobile after clicking the "Show me more awesome stories" button, there should be another button to share 
    your experiences. Realised this was not appearing on mobile as wasn't included within the hidden-stories row
    div. Moved the closing tag.
  - Realised that on some of the mobile devices, start of the about section couldn't be seen upon loading, 
    therefore the landing page container was taking up too much room. Changed it to 75vh but realised that it was 
    the content that was causing it to take up too much room. So for screen sizes less that 350px reduced size of 
    fonts of h1, h2, icon, margin-top of slogan container and removed the call to action button. As there are numerous 
    ways to go to contact page felt that this was justifiable.

   ### Existing

   - Table legend not centred on Internet explorer and Firefox.