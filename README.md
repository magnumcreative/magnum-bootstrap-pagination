Bootstrap Pagination
===========================

This is a simple function that replaces the default WP style pagination with <a href="http://getbootstrap.com/components/#pagination">Bootstrap 3 pagination</a> styling in your theme templates. The below instrutions are reflecting the use of <a href="http://roots.io/starter-theme/">Roots.io Starter</a> theme. You may have to adjust things slightly differently in your theme.

<h3>Requirements</h3>
<ul>
  <li>Bootstrap 3 (and css)</li>
  <li>WP Theme</li>
</ul>

<h3>Instructions</h3>
<ul>
  <li>Install plugin</li>
  <li>Edit your theme template with the below changes.</li>
</ul>

<h3>Theme changes</h3>
Replace any instance of pagination found in your WP templates with the function *page_navi();*.
```
<?php if ($wp_query->max_num_pages > 1) : ?>
  <nav class="post-nav">
    <ul class="pager">
      <li class="previous"><?php next_posts_link(__('&larr; Older posts', 'roots')); ?></li>
      <li class="next"><?php previous_posts_link(__('Newer posts &rarr;', 'roots')); ?></li>
    </ul>
  </nav>
<?php endif; ?>
```
With the below
```
<?php if ($wp_query->max_num_pages > 1) : ?>
  <?php
    // custom function to output Bootstrap pagination, found in custom.php
    page_navi();
  ?>
<?php endif; ?>
```
