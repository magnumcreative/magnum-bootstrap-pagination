magnum-bootstrap-pagination
===========================

Changes WP default pagination to Bootstrap 3 style


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
