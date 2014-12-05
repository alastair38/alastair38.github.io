##Advanced Custom Fields - Collegiate.ly##

**ACF** can be assigned to pages as well as post-types, so values such as a contact details etc can be input directly on the main page editor outwith. As this information is independent of any loops, a separate **includes** file could be used to generate these snippets across the site without hardcoding the field output into the page templates. Any change in contact methods (eg additional social network links) could be added with one code change.

**Includes** would similarly be employed for other code reused across pages; this could range from staff and course info to featured slideshow code (utilising  a common departmental taxonomy value, you could loop through a series of featured images eg using **owl carousel**)

###Common Taxonomies###

The application of a common taxonomy (and therefore shared taxonomy values) across post-types allows for pages to operate at a hierarchical - and somewhat static - level and tangibly separate from **custom-post-types**. Yet, this shared taxonomy enables on-demand cross-referencing between pages, child pages and CPTs

###Templating###

Using a page-based hierarchy means that a minimal number of templates could be use to layout both departmental and related child pages. 

Some simple **conditionals** could also be used for swapping out content for departments which (for example) don't run any events or perhaps do not deal with postgraduate admissions. This could streamline further the number of templates used depending on the site requirements.

###Search###

Use [WP Advanced Search][1] to build out sophisticated search options. **WPAS** takes numerous fields as part of the arguments for the search object, including post_type, taxonomy, author, date and meta_key. This should enable not only filtering by CPT, category and tag (or other custom taxonomies) but also **advanced custom fields** using the meta_key field. 

A single search page could be used, with an initial checkbox option to restrict to specific CPTs. Alternatively, separate search pages could be utilised for each CPT.

The search format can be any of the following: 'select', 'multi-select', 'checkbox', 'radio', 'text', 'hidden'

**Possible Issues**: search by **author** may have to be defined by user IDs, if it does not default to authors only. No obvious option for restricting users by role.


  [1]: http://wpadvancedsearch.com/