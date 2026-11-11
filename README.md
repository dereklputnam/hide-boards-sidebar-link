# Hide Boards Sidebar Link

A Discourse theme component that hides the **Boards** link in the sidebar.

It does one thing: a single CSS rule hides any sidebar link whose URL ends in `/boards` (for example `https://example.com/boards` or `https://example.com/community/boards`). No settings, no JavaScript.

For more information, see the [Discourse Boards topic on Meta](https://meta.discourse.org/t/discourse-boards/411414).

## Installation

1. In the admin panel, go to **Appearance → Themes and components**.
2. Click **Install → From a git repository** and enter `https://github.com/dereklputnam/hide-boards-sidebar-link`.
3. Add the component to your active theme.

## How it works

See [`stylesheets/app/sidebar.scss`](stylesheets/app/sidebar.scss):

```scss
.sidebar-section-link-wrapper:has(.sidebar-section-link[href$="/boards"]) {
  display: none;
}
```

This only hides the link. The Boards page itself is still reachable by URL.

## License

See [LICENSE](LICENSE).
