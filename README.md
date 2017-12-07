# Suffolk Libraries intranet themes

This is a child of the [Genesis Framework](https://my.studiopress.com/themes/genesis/), based on the [Genesis Sample Theme](https://github.com/copyblogger/genesis-sample/).


## How it works

Intranet is a child of the [Genesis Framework theme](https://www.studiopress.com/).

It loads no Genesis styles; instead, it styles the parent theme's HTML. We also add functions to the child theme's `functions.php`, mainly to dequeue plugin styles and scripts, but also to add a few features, such as page excerpts.


## Workflow

1. Make changes to a local working branch
2. Merge into the `candidate` branch
3. Push the `candidate` branch
4. If needs external review, FTP to test site and get approval. If not revert branch.
5. Merge into `master`
6. Push `master`
7. FTP to live site


## Dependencies

### Themes

- Genesis Framework (parent theme)

### Plugins

- [Redux framework](https://reduxframework.com/)
    - [WPO365-login](https://wordpress.org/plugins/wpo365-login/) (for O365 authentication; WPO365-login's admin pages depend on the Redux Framework)
- [CC Child Pages](https://en-gb.wordpress.org/plugins/cc-child-pages/) (generates lists of child/sibling pages with excerpts)
- [Genesis Simple Edits](https://en-gb.wordpress.org/plugins/genesis-simple-edits/) (to edit footer text)
- [Genesis Simple Hooks](https://en-gb.wordpress.org/plugins/genesis-simple-hooks/) (to change WP hooks)
- [Widgets on Pages](https://en-gb.wordpress.org/plugins/widgets-on-pages/) (to add any widgets to pages, mostly navigation menus for lists of forms, for examples)
- [Relevanssi](https://en-gb.wordpress.org/plugins/relevanssi/) (for improved search)
- [Custom Sidebars](https://en-gb.wordpress.org/plugins/custom-sidebars/) (to alter sidebars according to the page you're on)

## User accounts

When users visit the site the WPO365-login plugin will redirect them to Office 365. If it's their first visit they'll be asked to allow the intranet to use their account details to login.

Assuming users allow this, they'll be redirected to the site and the plugin will create a WordPress user account in the background. All accounts are granted Subscriber permissions by default, just enough to view the site.

Whenever users visit the site in the future the plugin will check whether they're logged into O365, or whether they still have an active login token. If they're not, they'll be prompted to login again.

### Changing permissions

To change a user from, say, a Subscriber to an Administrator you'll need to uncheck the `WordPress Admin > WPO365-login > User management > User cannot change email` box first.
