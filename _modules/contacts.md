---
layout: module
title: Contacts Module

category: core-module

module_name: Contacts
module_path: contacts
module_creator: dotProject
module_devs: web2project
module_version: 3.3
module_source: https://github.com/web2project/web2project
module_download: http://github.com/web2project/web2project/archive/master.zip
---

## Module Overview

The contacts module is a place to store information about users and additional contacts. When you add a new user to the database they are automatically added to the contacts page, however not all contacts need to be registered users.

You can access the data in this module by clicking on the contacts link in the main navigation. You can also access contacts from the add/edit project, add/edit task, resources, and other places throughout the dynamic application.

### Contacts List View (Contacts Index)

<a href="/assets/docs/contacts/index.png"><img src="/assets/docs/contacts/thumb-index.png" /></a>

The contacts list view is the default page for the contacts tab.

From this page you can:

1.	Search for contacts using a search field.
1.	Download a CSV of specific or entire list.
1.	View contact name, company, phone, email and location
1.	Email the contact
1.	Edit the contact
1.	Send an instant message and more

### Contacts Add/Edit (Contacts addedit)

<a href="/assets/docs/contacts/addedit.png"><img src="/assets/docs/contacts/thumb-addedit.png" /></a>

Sometimes you may want to add a contact to the system rather than make the contact an actual user.  The add/edit contacts page allows you to enter user data without having to create a login.

From this page you can keep detailed records about a person such as:

* Their name
* Job Title
* Company
* Department
* Address
* Country
* Phone numbers
* Emails (2X)
* Web Address
* Instant Messenger(s)
* General Notes


### Contacts Confirming Email (Contacts email confirm)

<a href="/assets/docs/contacts/email_confirm.png"><img src="/assets/docs/contacts/thumb-email_confirm.png" /></a>

Starting on web2Project the Contacts Confirming Email lets you notify you contacts to complete their contacts for you. <br />
Imagine you only have the Name and Email of a contact and you'd like to have the rest of his information, then simply edit the contact record and set the Waiting Update checkbox on the top right and submit.<br />
This will issue an email to your contact like the one seen on the image, with an URL for your contact.<br />
This URL will lead your contact to his contact record form and he will be able to edit and add the missing information for you.

### Import Contacts from LDAP Active Directory

Create a service Account, the account only needs to be a member of the domain users group in active directory in order to search ldap.

Go to Import Contacts from LDAP Directory
These are my setting, you would replace them to match your environment.

Server: 10.10.10.10
Protocol: Version 3
Bind Name: CN=project,CN=Users,DC=peanutbutter,DC=com
Bind Password: (password for the user account used in Bind Name above)
Base DN: OU=111,OU=Cary,OU=WRUsers,DC=peanutbutter,DC=com
Filter: (objectclass=Person)

Bind Name: must contain the full path to the user account you will be using to search ldap
For the "Base DN" be sure to use OU for an organizational unit and CN for a Container, CN would be used if your users were in the default "User" folder created when you install Active Directory. As an example if I wanted to import from that directory you would use this.
Base DN: CN=Users,DC=wrinternal01,DC=com
If I want to import the contacts from and organizational unit you created you would use this as an example.
Base DN: OU=MYUsers,DC=wrinternal01,DC=com
If you have multiple OU's which contain users you will need to modify the Base DN and import each one separately, if you know of a better way please tack it on to this post.