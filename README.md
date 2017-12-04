# Suffolk Libraries intranet themes

This is a child of the [Genesis Framework](https://my.studiopress.com/themes/genesis/), based on the [Genesis Sample Theme](https://github.com/copyblogger/genesis-sample/).


## How it works

Intranet is a child of the [Genesis Framework theme](https://www.google.co.uk/url?sa=t&rct=j&q=&esrc=s&source=web&cd=1&cad=rja&uact=8&ved=0ahUKEwijr82Rh_DXAhViIsAKHaIfCRQQFgg5MAA&url=https%3A%2F%2Fmy.studiopress.com%2Fthemes%2Fgenesis%2F&usg=AOvVaw1O73haj2e_YcJ4E-C1OudE). It loads no Genesis styles; instead, it styles the parent theme's CSS.


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

- Redux framework
    - WPO365-login (for O365 authentication)
- Genesis Featured Page Advanced (for outputting page lists in sidebars)
- Shortcodes Ultimate (for layout and other shortcode options)
- Genesis Simple Edits (to edit footer text)
- Genesis Simple Hooks (to change WP hooks)
- Widgets on Pages (to add any widgets to pages, good for front page menu, for example)
