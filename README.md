# Sitebuilder page template

This project includes a template to be used as a starting point to develop a Sitebuilder page or site design.

## Getting started

You could use a number of editors to edit the files and run a local server, but we recommend installing [Visual Studio Code](https://code.visualstudio.com/) - you can install the zip version and it should work on Warwick's Windows 7 Managed Desktop.

Once you've got Visual Studio Code running, you'll need to install the "Live Server" extension:

* Click the extensions button in the bar on the far left, or go to `View` > `Extensions` in the menu
* Search for "Live Server" and click "Install", then "Restart" when prompted

When you have this project open, you should see a `Go Live` button in the status bar at the bottom:

[[https://github.com/ritwickdey/vscode-live-server/raw/master/images/Screenshot/vscode-live-server-statusbar-3.jpg]]

This button should open a web browser with the template in it. The page will automatically reload when you make changes to the template.

## {less}

ID7 is built using `.less` files instead of `.css` files - this lets you use things like variables and nesting in your CSS rules, and you can even use variables from ID7 that make a lot more sense than just typing numbers in and hoping they don't change.

The `page.less` and `site.less` files in this project include the ID7 {less} scripts at the top. This means you can do things like:

    /* CSS rules that only apply when the screen is "sm" or bigger (i.e. not mobile) */
    @media (min-width: @screen-sm-min) {
      .my-div {
        background: @id7-brand-red;
      }
    }

The template includes a script that automatically converts your `.less` files to `.css` files. When you upload a `.less` file to Sitebuilder, the same thing happens, and you can include it in your web page as a `.css` file - if you upload `page.less` you can add `<link href="page.css" rel="stylesheet">` and it will just work. You shouldn't include the `less.min.js` script like in this project, that's for development only.