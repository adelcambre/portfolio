---
layout: post
title:  "Add-ons design process"
date:   2013-11-22 23:15:42
categories: UI
thumbnail: images/add-ons/thumb-add-ons.jpg
creation-date: 2013-10-22 23:15:42
short-description: The user interface to add third party software to customer's apps.
---
# Add-ons design process
### Engine Yard
 
## The goal

In 2012, Engine Yard was planning to launch a new feature which gives customers the ability to add third-party software to their applications.

The development of the API for this feature was already underway when I first joined the Add-ons team. I came in to help create a clear user interface for customers to activate add-ons for their applications.

## The Challenge
_Add-ons were complicated._

The API for add-ons had already been defined, and it didn't allow for "one-click activation". Since third party services are widely varied in their functionality, different add-ons had different requirements. 

Most add-ons had somewhere between 2-4 required steps to get set up. Some needed complex application code changes before they could integrate. A handful of uncomplicated add-ons only could be added in one click, but for most that was not the case.

I wanted to create an interface with a familiar flow for setting up these disparate add-ons.

## The plan

My plan was to address add-on activation in these three steps (counter-clockwise from the upper left.)

**Step 1.** Browse all the available add-ons.

**Step 2.** View details and pricing information on a specific add-on.

**Step 3.** Put that add-on in your application. Sometimes this would mean a few additional steps. Sometimes only one.

![Add-ons step 1](/images/add-ons/addons-1.jpg)
    <h2>Step 1: Browsing add-ons</h2>
    We were launching this feature with about ten add-ons (with the hope of adding many more in the future)

    <b>Research</b>

    To better understand user expectations, I looked at other add-ons registries in the same space (Heroku, Cloudbees, Rackspace) - and also at how other online marketplaces (like iTunes and the Google Chrome Store) display their offerings.

    <b>My conclusions</b>

    The add-ons needed to be easily scannable and searchable. I created a grid of small tiles, each with one add-on. The search and category filters are on the left menu. 

		The name and the logo of each of the add-ons would be useful for instant recognition and search-ability. A short description would be helpful for someone who didn't immediately recognize an add-on.
  </div><div class="aside-img">{image 6}
    <i>Early progress making the index page.</i>
  </div>
</div>
<div class="clear">
  <div class="aside">
		<b>Completion status</b>

    On the homepage, I needed a way for users to differentiate between an unused and in-use add-ons.
		
		I sketched the tiles and their possible states: Available, partially activated (incomplete), and fully activated.

    Activated add-ons have a diagonal banner in the upper right.
  	</div><div class="aside-img">{image 15}
    </div>
</div>
<div class="clear">
  <div class="aside">
    <b>Refinement</b>

    The logo of each add-on was added.

		The two calls-to-action "Enable" and "Details" were replaced with just one: "Details."
    
		<i>When an add-on is fully setup, the pink "enabled" flag is in the upper right corner, and the "Details" button becomes "Manage".</i>

		Category filters were made more clear in the left sidebar.
		  </div><div class="aside-img">{image 8}
  </div>
</div>
<div class="clear">
  <div class="aside">
    <h2>Step 2: View Details</h2>
    Clicking on an add-on from our marketplace would reveal more details about the service and it's pricing. A user could proceed to set it up from this view.

    At first, I considered using a lightbox, but decided against it because some add-ons had lengthy pricing details and complex integration instructions.

    Initially, I experimented with simply a "Setup" button to take users to the step(s) after Sign up.
  </div><div class="aside-img">{image 16}<i>Initial layout for the details page.</i>
  </div>
</div>
<div class="clear">
  <div class="aside"><h2>Step 3: Add-on activation</h2>
    <b>First attempt</b>

		On the Setup page (sketched here) there was a link back to the details page in the upper right.

    Because of the numerous steps on this page we decided to break the setup into separate pages.
    </div><div class="aside-img">{image 17}
  </div>
</div>

<div class="clear">
  <div class="aside"><b>Showing the steps</b>

    We wanted users to see what further steps needed to be taken, and indicate how far along they are in the process. To do this, I made a blue bar that describes the four setup steps:

    <b>Sign up.</b> Add-on details and sign up button.

    <b>Activate.</b> Select which application to use it on.

    <b>Update code.</b> Make configuration file changes in the application's code.

    <b>Deploy.</b> Deploy application.

    The white pointer at the bottom indicates which step the customer is on.
    </div><div class="aside-img">
    {image 13}
  </div>
</div>

<div class="clear">
  <div class="aside">
    The "Activate, Update Code, and Deploy" steps are semi-transparent until the required "Sign Up" is complete. The customer can still see the instructions and content on these pages, but there is a message at the top that says "you first need to sign up".

		<b>Activate</b>

		The Activate step lets customers choose which environment will use the add-on.
  </div><div class="aside-img">
{image 12}
  </div>
</div>
<div class="clear">
  <div class="aside">
    <i>When an environment is chosen, it is listed underneath.</i>
  </div><div class="aside-img">
	{image 11}
  </div>
</div>
<div class="clear">
  <div class="aside">
		<b>Update code</b>

		This step contains instructions for customers to edit their application code.
  </div><div class="aside-img">
{image 9}
  </div>
</div>
<div class="clear">
  <div class="aside">
		<b>Deploy</b>

		The final step is to re-deploy the environment. This step provides a link to the page in the app where customers do their deployments.
  </div><div class="aside-img">
{image 10}
  </div>
</div>
<div class="clear">
  <div class="aside">
		<h2>Next steps</h2>

		We launched the Add-ons and started looking at which were most popular and other usage patterns, like whether users deploy the same add-on on different environments or across many of their apps.

		I learned that customers were getting confused on steps that kicked them off to the third party site for sign up or activations. In these cases, the flow back to our app wasn't always clear. This often resulted in users having multiple windows open, each on a different setup step.
  </div>
</div>
<div class="clear">
  <div class="aside">
		Currently I am exploring different ways to improve that interaction. I'm leaning toward a separation of the "add-on details" and the "setup" page, putting the setup steps all on one page.
  </div><div class="aside-img">
{image 18}
  </div>
</div>
