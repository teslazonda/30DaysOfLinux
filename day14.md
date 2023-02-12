# Day 14: Understanding Locale Management

## LPIC-1 Objective 107.3
<br></br>

## Notes

View current locale: `locale`

View current locale details for single variable: `locale -ck <LC_VARIABLE>`

View all locale `locale -a`

If on a systemd system: `localectl status`

Configuration file: `/etc/locale.conf` or`/etc/default/locale`

### Defining Character Sets

* ASCII - only 128 English characters

* Unicode - over 143,000 characters. UTF (Unicode Transformation Format)
* ISO/IEC 8859:  8-bit encodings

#### Managing Your Locale

Change the user locale: `export <LC_VARIABLE>=<setting>.<CHARACTER-SET>`

`export LC_ALL=hi_IN.UTF-8` - changes locale to hindi.
