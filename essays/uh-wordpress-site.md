---
layout: essay
type: essay
published: true
title: Setting up a UH WordPress Site
date: 2012-10-09
labels:
  - UH ITS
  - WordPress
---

The <a href="http://www.hawaii.edu/its/">University of Hawaii Information and Technology Services</a> (ITS) department provides hosting services to faculty and staff.  This has many advantages, including:
<ul>
	<li>No cost to you for hardware.</li>
	<li>No cost to you for backups, network, UPS, and OS administration.</li>
	<li>Energy savings, due to: (1) virtualization (because at ITS, multiple sites run on a single server); (2) reduced A/C (because shared, co-located servers at ITS require much less A/C ); and (3) green computing (unlike ITS, most departments run old, energy hogging, A/C demanding servers).   With electricity costs accounting for almost 25% of tuition, energy savings maybe the most compelling reason to switch.  But I digress.</li>
</ul>

Thus, for most departments and organizations on campus, it no longer makes economic or administrative sense to buy hardware and software just to run your website.  In hope of lowering the barrier to adoption, I am providing a few tips on my experiences developing three hosted websites (<a href="http://manoa.hawaii.edu/sustainability">http://manoa.hawaii.edu/sustainability</a>,  <a href="http://www.hawaii.edu/sustainability">http://www.hawaii.edu/sustainability</a>, and <a href="http://csdl.ics.hawaii.edu/">http://csdl.ics.hawaii.edu</a>) over the past couple of weeks.

<strong>Step 1:  Choose your hosting option.  </strong>At the time of writing, ITS basically offers three alternatives, a "managed" WordPress site (where they install and update the WordPress installation), a "self-hosted" environment (where they provide the database backend services and you must install/update WordPress yourself), or a virtual machine environment (so you can do whatever you want).  The easiest option and the one that probably works best for most people is the "managed" site. If you want to install custom plugins, then you will need the self-hosted WordPress option.   The downside of self-hosting is that you have to do your own updates when new versions of WordPress and your plugins are released. This happens regularly---every few weeks, so there is some maintenance overhead you incur for going with the self-hosted option.

ITS also supports Drupal, and you could use the virtual machine services to go with something like Plone, but (at the time of writing) I think WordPress has the best combination of power and ease-of-use.

The remainder of these steps assume you are choosing the self-hosted WordPress option.

<strong>Step 2:  Request your site.</strong>  Go to the <a href="http://www.hawaii.edu/infotech/webservice/apply.php">ITS application page</a> to apply.  Fill it out as best you can, and you can answer "not applicable--want to install WordPress" for many of the questions.   ITS will respond within a day or two with an email indicating the name of your new domain along with FTP instructions and database information.  Don't freak out by the contents of this email, it will all make sense soon and some of it you don't actually need to know.

<strong>Step 3:  Download WordPress.</strong>  Go to the <a href="http://wordpress.org/download/">WordPress download page</a> and get the latest release.  While you are there, sign up to receive notifications of future releases.

<strong>Step 4: Configure wp-config.php.</strong> The <a href="http://codex.wordpress.org/Installing_WordPress">WordPress installation guide</a> explains the next step, which is to create a file called wp-config.php from the sample template and edit the variable values inside. The ITS email shows that they have already created the database for you, so you just have to set the variables for the database user, password, and table name.   Also, you have to provide the "secret key" definitions using the <a href="https://api.wordpress.org/secret-key/1.1/salt/">WordPress salt generator</a>.

<strong>Step 6: Copy the WordPress files to the directory provided by ITS.</strong>  Once you have created and edited your wp-config.php file, use a secure FTP client to transmit the WordPress files over to the directory specified in the ITS email.  For a Mac, I recommend the <a href="http://panic.com/transmit/">Transmit FTP client</a>. Once you've done that, reply to the ITS email to tell them that the site is ready to be enabled.  Also, I recommend that you specify in the email that you want the .htaccess file to be write-enabled for your WordPress system (so that WordPress can add rewrite rules to .htaccess to change the format of posting URLs).

<strong>Step 7: Run the install script.</strong>  Once ITS has emailed you back that the site is ready, return to the WordPress instructions and retrieve the URL to run the install script. That takes about 10 seconds and your site is now live and available for development.

<strong>Step 8:  Install the One Click Child Theme plugin.</strong>  The vast majority of website  development in WordPress occurs by choosing a pre-existing theme and then customizing it in either simple or complicated ways.   If you simply activate and customize one of the existing themes provided in the WordPress release, then you will create a headache for yourself in the future, because installing a future release of WordPress (and/or your chosen theme) will wipe out some/all of your customizations.   The solution, as is recommended in countless WordPress postings, is to never customize an existing theme directly.  Instead, you should create what is called a "Child Theme" of the existing theme, which inherits all the features of the parent theme but allows you to store your customizations in your own (child) theme definition, rather than in the parent theme definition.   That way, when you install an update, your customizations will survive.  Fortunately, WordPress has a plugin called the <a href="http://wordpress.org/extend/plugins/one-click-child-theme/">One Click Child Theme</a>, which enables you to create child themes in, well, one click.  So, install this plugin, then when you've decided on the theme you want to use, make sure to create and customize a newly created child of your chosen theme.

<strong>Step 9: Install and activate the <a href="http://wordpress.org/plugins/wordfence/">WordFence</a> plugin</strong>.  Due to recent (April, 2013) attacks on WordPress sites, it is very important to protect your site by installing some sort of security protection. An easy way to significantly improve the security of your site is to install the <a href="http://wordpress.org/plugins/wordfence/">WordFence</a> plugin.  In addition, be sure to create strong passwords for administrative users.

<strong>Step 10:  Miscellaneous Site Setup.</strong>  Having developed three sites in a row, there are a few things I have done repeatedly. Here's the action and the menu selections to get to the appropriate admin page:
<ul>
	<li>Remove/change tagline (Settings, General)</li>
	<li>To change front page to a static page (Settings, Reading)</li>
	<li>To remove the ability to comment on future pages and posts (Settings, Discussion).</li>
	<li>To remove the ability to comment on current pages and posts (Display all posts/pages, select "Quick Edit", then deselect "Comments enabled".)</li>
	<li>To make permalinks look better (Settings, Permalinks).</li>
	<li>To remove sidebar from interior pages (Edit page, select "One Column, No Sidebar rather then "Default Template")</li>
	<li>To provide your full name on postings (Users, Your Profile)</li>
	<li>To make a post "sticky" (Click on "edit" by visibility, select "Sticky")</li>
	<li>Create a custom menu (Appearance, Menus)</li>
</ul>
<strong>Step 12: Fix the footer (or whatever else you find lacking in your parent theme).</strong>  One of the common desires of those using the otherwise excellent WordPress default themes (twentyten, twentyeleven, etc.)  is to eliminate or replace the annoying "Proudly powered by WordPress" in the footer.   Once you have created a child theme, this is incredibly simple.  Just find the footer.php file in the parent theme, copy that file into the folder defining your child theme, and edit it to your heart's content.  WordPress will use your footer.php file (or any other file) in your child theme directory instead of the parent's.

<strong>Step 13: Just FYI, here are a few plugins I've found useful:</strong>
<ul>
	<li><a href="http://wordpress.org/extend/plugins/easy-columns/">easy-columns</a></li>
	<li><a href="http://wordpress.org/extend/plugins/iframe/">iframe</a></li>
	<li><a href="http://wordpress.org/extend/plugins/printfriendly/">printfriendly</a></li>
	<li><a href="http://wordpress.org/extend/plugins/unattach/">unattach</a></li>
	<li><a href="http://wordpress.org/extend/plugins/advanced-excerpt/">advanced-excerpt</a></li>
	<li><a href="http://wordpress.org/extend/plugins/children-excerpt-shortcode-plugin/">children-excerpt-shortcode</a></li>
	<li><a href="http://wordpress.org/extend/plugins/list-category-posts/">list-category-posts</a></li>
	<li><a href="http://wordpress.org/extend/plugins/ultimate-tag-cloud-widget/">ultimate-tag-cloud-widget</a></li>
	<li><a href="http://wordpress.org/extend/plugins/wp-gallery-custom-links/">wp-gallery-custom-links</a></li>
</ul>

And that's just after the first couple of weeks of using WordPress.  That's the thing that's cool about the ecosystem: for whatever you want to do, try googling "wordpress plugin &lt;what you want to do&gt;".  Someone probably already had the itch and scratched it.

<strong>Notes from my first updating experience:</strong>  I just tried to update to WordPress 3.5 on one of the sites.  The process went relatively smoothly, except that after the update I discovered that the wp-content directory no longer had the correct write permissions.   This appears to be because I used a GUI FTP client and simply dragged all of the WordPress files and subdirectories over at one time, which resulted in the client deleting the directories and recreating them.  In future, to avoid this problem, do the update in batches, such that you don't drag the wp-content directory over itself (that way the FTP client does not delete and recreate that directory).

Here are the <a href="http://codex.wordpress.org/Updating_WordPress">instructions on updating WordPress</a>.