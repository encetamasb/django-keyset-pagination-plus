# Release notes.

* 0.9.9: Gracefully handle a `page=<valid json but invalid key string>`. For instance, this could be `page=2`, which users could enter thinking they are clever.

* 0.9.8: Correctly handle a page=1 input that comes from a view. This will be a string, which should be supported since we handle an integer of 1.

* 0.9.6: Better handling of empty lists and missing ordering on querysets.

* 0.9.5: Ensure the fixes from both 0.9.4 and 0.9.3 are in the same release.

* 0.9.4: Support ordering keys that follow lookups. Using these is at your own risk: You must ensure that you are using .select_related(), or it will trigger another database fetch for each lookup. This should only apply to the first/last instances, others will not be calculated.

* 0.9.3: Fix an issue where we have an empty object_list, but still think we have a previous page.

* 0.9.2: Fix issues with pagination boundaries when there are more than two ordering keys, and objects cross over a boundary that can only be discriminated by the last sort key.

* 0.9.1: Prevent errors when no objects in queryset.

* 0.9.0: Stop supporting page index and total item count.

* 0.8.5: Don't fail to render on empty result set.

* 0.8.4: Allow installing in Python 2.

* 0.8.1: Add description to pypi page.

* 0.8.0: First release.
