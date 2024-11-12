# Digits UI

<img src="doc/landing.png">

<i>Digits is website that allows users to:</i>

- Register an account.
- Create and manage a set of contacts.
- Add a set of timestamped notes regarding their interactions with each contact.

## Set Up
<font color="red"><i>Assuming you have a Postgres account and log in already</i></font>

First, you will need to download a copy of "Digits". Since it is a private repository, you must gain access from the author.

Second, you will need to download npm with:

<img src="doc/npminstall.png">

Third, open a terminal window in VSCode an run the command <font color="turquoise"> createdb digits </font>

Fourth, copy the <font color="turquoise">sample.env</font> file to a new file called <font color="turquoise">.env</font>.

Fifth, edit the <font color="turquoise">.env</font> file to set the <font color="turquoise">DATABASE_URL</font> to <font color="turquoise">postgresql://<username>:<password>@localhost:5432/digits?schema=public</font>.

Sixth, migrate the database by running the command <font color="turquoise">npx prisma migrate dev</font>. This will create the tables in the digits database.

Seventh, seed the database by running the command <font color="turquoise">npx prisma db seed</font>. This will populate the tables with some sample data.

Eigth, start the website by using the command <font color="turquoise">npm run dev</font>

If it all goes correctly your Ferminal should say something like below:
<img src="doc/npmrundev.png">

You can view the website at https://localhost:3000. You are able to register with a new account or log in just use one of the credentials in the <font color="turquoise">settings.development.json</font> file.

## User Interface Walkthrough
### Landing Page
Going on the website for the first time, the landing page will provide some insight as to the capabilities of what <font color="turquoise">Digits</font> can do:

<img src="doc/landing.png">

&nbsp;

### Register
Assuming you wanted to create your own account, you would click on the <font color="turquoise">Login</font> button at the top right where you would then select <font color="turquoise">Sign up</font> to create a new account.

<img src="doc/signup.png">

&nbsp;

### Sign In
To sign in you would click on the <font color="turquoise">Login</font> button at the top right where you would then select <font color="turquoise">Sign in</font> where you would then put in your information. (As mentioned previously, you may also just use one of the credentials in the <font color="turquoise">settings.development.json</font> file.)

<img src="doc/signin.png">

&nbsp;

### User Home Page
After you have logged in, the system will take you to the homepage which looks very similar to the landing page. However, the NavBar contains links to "Add Contact" and "List Contacts".

<img src="doc/UserHP.png">

&nbsp;

### Add Contacts
Clicking on "Add Contacts" allows for the user to create a new contact to put into the database and associate it with their user.

<img src="doc/addcontact.png">
&nbsp;

### List Contacts
Clicking on the "List Contacts" will list all of the contacts which are associated with the user.

#### Timestamped Note
As you can see there is also a section where you can add a note to the contact where you could write things such as last time you saw them or things to remember them by. I just put some random examples as you can see in the image where it has the date I wrote it and just some random phrases I put in as an example.

<img src="doc/ListContacts.png">

 
&nbsp;

### Edit Contacts
If you notice in the previous picture there is a blue <font color="turquoise">Edit</font> button in the bottom left hand corner of the individual contacts. When you click that it brings you to the page below where you can see it has the information already put in but allows you to change it.

<img src="doc/editcontact.png">

&nbsp;

### Admin Mode
If you were to sign into <font color="turquoise">Admin</font> you will be given another option within your NavBar called "Admin" (login can be found in the setting file). You will get access to all Contacts associated with all of the users as well as the user in which it belongs to underneath the bio of each contact.

<img src="doc/admin.png">