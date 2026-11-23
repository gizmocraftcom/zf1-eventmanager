# Changelog

## 2.0.0

Fork of `diablomedia/zendframework1-eventmanager`, published as `gizmocraft/zendframework1-eventmanager`.

### Breaking changes

- Requires PHP `>=8.5`. Tested on PHP 8.5 and 8.6.
- Package renamed from `diablomedia/zendframework1-eventmanager` to `gizmocraft/zendframework1-eventmanager`. It now requires `gizmocraft/zendframework1-exception` and `gizmocraft/zendframework1-stdlib` `^2.0.0`.
- No public API changes. The only library change is `Zend_EventManager_Filter_FilterIterator` referencing `SplPriorityQueue::EXTR_BOTH` and `SplPriorityQueue::EXTR_DATA` instead of `self::`, which behaves the same and satisfies PHPStan.

### Other changes

- Dev dependencies upgraded (PHPUnit 13, PHPStan 2.3, php-cs-fixer 3.95, GrumPHP 2.27). Dropped `composer-require-checker`, which has no release for PHP 8.6.
- Tests migrated to PHPUnit 13 attributes. The test asset `MockAggregate` uses `spl_object_id()` instead of `spl_object_hash()`, which is deprecated in PHP 8.6. CI runs PHP 8.5 and 8.6.
