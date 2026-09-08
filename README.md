# WP Statuses

> **This is a maintained fork of [imath/wp-statuses](https://github.com/imath/wp-statuses)**, which was archived by its original author on 2024-11-17. All credit for the original design and implementation belongs to [imath](https://github.com/imath); this fork exists to continue maintenance for Content Pilot's projects. The code remains GPL-2.0+ licensed.

A WordPress plugin that eases custom post status integration, surfacing registered custom statuses in the block editor sidebar, the classic editor metabox, and the posts list quick-edit dropdown.

## Usage

Register a custom status with `register_post_status()` and the extra WP Statuses arguments (`post_type`, `dashicon`, `show_in_metabox_dropdown`, `show_in_inline_dropdown`, `labels`), and it becomes selectable in the editor UI. See `inc/core/functions.php` for the API (`wp_statuses_get_supported_post_types()`, `wp_statuses_is_post_type_supported()`, etc.).

## Development

The block editor sidebar is built from `src/sidebar/sidebar.js` into `js/sidebar.js` with Parcel:

```bash
npm install
npm run build   # or `npm start` to watch
```

The remaining scripts in `js/` are minified with Grunt (`npx grunt shrink`).
