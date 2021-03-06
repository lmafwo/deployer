<!-- DO NOT EDIT THIS FILE! -->
<!-- Instead edit recipe/laravel.php -->
<!-- Then run bin/docgen -->

# laravel

[Source](/recipe/laravel.php)



* Require
  * [`recipe/common.php`](/docs/recipe/common.md)
* Config
  * [`shared_dirs`](#shared_dirs)
  * [`shared_files`](#shared_files)
  * [`writable_dirs`](#writable_dirs)
  * [`log_files`](#log_files)
  * [`laravel_version`](#laravel_version)
* Tasks
  * [`artisan:up`](#artisanup) — Disable maintenance mode
  * [`artisan:down`](#artisandown) — Enable maintenance mode
  * [`artisan:migrate`](#artisanmigrate) — Execute artisan migrate
  * [`artisan:migrate:fresh`](#artisanmigratefresh) — Execute artisan migrate:fresh
  * [`artisan:migrate:rollback`](#artisanmigraterollback) — Execute artisan migrate:rollback
  * [`artisan:migrate:status`](#artisanmigratestatus) — Execute artisan migrate:status
  * [`artisan:db:seed`](#artisandbseed) — Execute artisan db:seed
  * [`artisan:cache:clear`](#artisancacheclear) — Execute artisan cache:clear
  * [`artisan:config:clear`](#artisanconfigclear) — Execute artisan config:clear
  * [`artisan:config:cache`](#artisanconfigcache) — Execute artisan config:cache
  * [`artisan:route:cache`](#artisanroutecache) — Execute artisan route:cache
  * [`artisan:view:clear`](#artisanviewclear) — Execute artisan view:clear
  * [`artisan:view:cache`](#artisanviewcache) — Execute artisan view:cache
  * [`artisan:optimize`](#artisanoptimize) — Execute artisan optimize
  * [`artisan:optimize:clear`](#artisanoptimizeclear) — Execute artisan optimize:clear
  * [`artisan:queue:restart`](#artisanqueuerestart) — Execute artisan queue:restart
  * [`artisan:storage:link`](#artisanstoragelink) — Execute artisan storage:link
  * [`artisan:horizon:assets`](#artisanhorizonassets) — Execute artisan horizon:assets
  * [`artisan:horizon:publish`](#artisanhorizonpublish) — Execute artisan horizon:publish
  * [`artisan:horizon:terminate`](#artisanhorizonterminate) — Execute artisan horizon:terminate
  * [`artisan:telescope:clear`](#artisantelescopeclear) — Execute artisan telescope:clear
  * [`artisan:telescope:prune`](#artisantelescopeprune) — Execute artisan telescope:prune
  * [`artisan:telescope:publish`](#artisantelescopepublish) — Execute artisan telescope:publish
  * [`artisan:nova:publish`](#artisannovapublish) — Execute artisan nova:publish
  * [`artisan:event:clear`](#artisaneventclear) — Execute artisan event:clear
  * [`artisan:event:cache`](#artisaneventcache) — Execute artisan event:cache
  * [`deploy:public_disk`](#deploypublic_disk) — Make symlink for public disk
  * [`deploy`](#deploy) — Deploy your project

## Config
### shared_dirs
[Source](/recipe/laravel.php#L8)

* Overrides [`shared_dirs`](/docs/recipe/common.md#shared_dirs) from `recipe/common.php`



### shared_files
[Source](/recipe/laravel.php#L9)

* Overrides [`shared_files`](/docs/recipe/common.md#shared_files) from `recipe/common.php`



### writable_dirs
[Source](/recipe/laravel.php#L10)

* Overrides [`writable_dirs`](/docs/recipe/deploy/writable.md#writable_dirs) from `recipe/deploy/writable.php`



### log_files
[Source](/recipe/laravel.php#L21)



### laravel_version
[Source](/recipe/laravel.php#L22)




## Tasks
### artisan:up
[Source](/recipe/laravel.php#L81)



### artisan:down
[Source](/recipe/laravel.php#L84)



### artisan:migrate
[Source](/recipe/laravel.php#L87)



### artisan:migrate:fresh
[Source](/recipe/laravel.php#L90)



### artisan:migrate:rollback
[Source](/recipe/laravel.php#L93)



### artisan:migrate:status
[Source](/recipe/laravel.php#L96)



### artisan:db:seed
[Source](/recipe/laravel.php#L99)



### artisan:cache:clear
[Source](/recipe/laravel.php#L102)



### artisan:config:clear
[Source](/recipe/laravel.php#L105)



### artisan:config:cache
[Source](/recipe/laravel.php#L108)



### artisan:route:cache
[Source](/recipe/laravel.php#L111)



### artisan:view:clear
[Source](/recipe/laravel.php#L114)



### artisan:view:cache
[Source](/recipe/laravel.php#L117)



### artisan:optimize
[Source](/recipe/laravel.php#L120)



### artisan:optimize:clear
[Source](/recipe/laravel.php#L123)



### artisan:queue:restart
[Source](/recipe/laravel.php#L126)



### artisan:storage:link
[Source](/recipe/laravel.php#L129)



### artisan:horizon:assets
[Source](/recipe/laravel.php#L132)



### artisan:horizon:publish
[Source](/recipe/laravel.php#L135)



### artisan:horizon:terminate
[Source](/recipe/laravel.php#L138)



### artisan:telescope:clear
[Source](/recipe/laravel.php#L141)



### artisan:telescope:prune
[Source](/recipe/laravel.php#L144)



### artisan:telescope:publish
[Source](/recipe/laravel.php#L147)



### artisan:nova:publish
[Source](/recipe/laravel.php#L150)



### artisan:event:clear
[Source](/recipe/laravel.php#L153)



### artisan:event:cache
[Source](/recipe/laravel.php#L156)



### deploy:public_disk
[Source](/recipe/laravel.php#L167)

Task deploy:public_disk support the public disk.
To run this task automatically, please add below line to your deploy.php file

    before('deploy:symlink', 'deploy:public_disk');

[Laravel filesystem configuration](https://laravel.com/docs/5.2/filesystem#configuration)

### deploy
[Source](/recipe/laravel.php#L182)

Main deploy task.

This task is group task which contains next tasks:
* [`deploy:prepare`](/docs/recipe/common.md#deployprepare)
* [`deploy:vendors`](/docs/recipe/deploy/vendors.md#deployvendors)
* [`artisan:storage:link`](/docs/recipe/laravel.md#artisanstoragelink)
* [`artisan:view:cache`](/docs/recipe/laravel.md#artisanviewcache)
* [`artisan:config:cache`](/docs/recipe/laravel.md#artisanconfigcache)
* [`deploy:publish`](/docs/recipe/common.md#deploypublish)


