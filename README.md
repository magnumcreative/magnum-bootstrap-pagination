magnum-bootstrap-pagination
===========================

Changes WP default pagination to Bootstrap 3 style


<h3>Theme changes</h3>
Replace WP pagination with
```
<?php if ($wp_query->max_num_pages > 1) : ?>
  <?php
    // custom function to output Bootstrap pagination, found in custom.php
    page_navi();
  ?>
<?php endif; ?>
```
