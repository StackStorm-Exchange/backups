# Change Log

## v2.0.0

* Drop Python 2.7 support

## v1.0.5

* Forced release to included hotfix for `backups.full_backup`

## v1.0.4

* Added mongodb_host option to backup remote MongoDB database. Defaults to '127.0.0.1'

## v1.0.3

* Fixed issues with join task not being executed when items fail.

  Contributed by Bradley Bishop (Encore Technologies)

## v1.0.2

* Fixed issue that if backups failed or timeed out then the old backups were not cleaned
  up causing disks to fill.

  Contributed by Bradley Bishop (Encore Technologies)

## v1.0.1

* Added backup.timeout key value look up for backup_timeout param
* Fixed issue with full_backup workflow that if only 1 of the methods failed
  it would still exit successful.

  Contributed by Bradley Bishop (Encore Technologies)

## v1.0.0

* Migrated from Mistral -> Orquesta (Feature)

  Contributed by Nick Maludy (@nmaludy Encore Technologies)

* Added compression-in-place instead of dumping to a file/directory then running gzip.
  This reduces the required disk space to execute backups, because we don't have to store
  the intermediate uncompress data. (Feature)

  Contributed by Nick Maludy (@nmaludy Encore Technologies)

* Added `--quiet` to the `mongodump` command, so that progress bars don't litter the `stdout`
  of the action execution. (Bugfix)

  Contributed by Nick Maludy (@nmaludy Encore Technologies)

## v0.1.2

Added `backup_timeout` parameter to all actions to control the timeout of the long-running
backup commands within the workflows (`mongodump`, `pg_dump`, `tar`, etc).

## v0.1.1

Added pack icon. No code changes.

## v0.1.0

Initial Revision
