All Women's Big Bash League match data in CSV format
====================================================

The background
--------------

As an experiment, after being asked by a user of the site, I started
converting the YAML data provided on the site into a CSV format. That
initial version was heavily influenced by the format used by the baseball
project Retrosheet. I wasn't sure of the usefulness of my CSV format, but
nothing better was suggested so I persisted with it. Later Ashwin Raman
(https://twitter.com/AshwinRaman_) send me a detailed example of a format
he felt might work and, liking what I saw, I started to produce data in
a slightly modified version of that initial example.

This particular zip folder contains the CSV data for...
  All Women's Big Bash League matches
...for which we have data.

How you can help
----------------

Providing feedback on the data would be the most helpful. Tell me what you
like and what you don't. Is there anything that is in the JSON data that
you'd like to be included in the CSV? Could something be included in a better
format? General views and comments help, as well as incredibly detailed
feedback. All information is of use to me at this stage. I can only improve
the data if people tell me what does works and what doesn't. I'd like to make
the data as useful as possible but I need your help to do it. Also, which of
the 2 CSV formats do you prefer, this one or the original? Ideally I'd like
to settle on a single CSV format so what should be kept from each?

Finally, any feedback as to the licence the data should be released under
would be greatly appreciated. Licensing is a strange little world and I'd
like to choose the "right" licence. My basic criteria may be that:

  * the data should be free,
  * corrections are encouraged/required to be reported to the project,
  * derivative works are allowed,
  * you can't just take data and sell it.

Feedback, pointers, comments, etc on licensing are welcome.

The format of the data
----------------------

Full documentation of this CSV format can be found at:
  https://cricsheet.org/format/csv_ashwin/
but the following is a brief summary of the details...

This format consists of 2 files per match, although you can get all of
the ball-by-ball data from just one of the files. The files for a match
are named <id>.csv (for the ball-by-ball data), and <id>_info.csv (for
the match info), where <id> is the Cricinfo id for the match. The
ball-by-ball file contains one row per delivery in the match, while the
match info file contains match information such as dates the match was
played, the outcome, and lists of the players involved in the match.

The match info file format
--------------------------

The info section contains the information on the actual match, such as
when and where it was played, any event it was part of, the type of
match etc. The fields included in the info section will each appear as
one or more rows in the data. Some of the fields are required, whereas
some are optional. If a field has multiple values, such as team, then
each value will appear on a row of it's own.

The ball-by-ball file format
----------------------------

The first row of each ball-by-ball CSV file contains the headers for the
file, with each subsequent row providing details on a single delivery.
The headers in the file are:

  * match_id
  * season
  * start_date
  * venue
  * innings
  * ball
  * batting_team
  * bowling_team
  * striker
  * non_striker
  * bowler
  * runs_off_bat
  * extras
  * wides
  * noballs
  * byes
  * legbyes
  * penalty
  * wicket_type
  * player_dismissed
  * other_wicket_type
  * other_player_dismissed

Most of the fields above should, hopefully, be self-explanatory, but some may
benefit from clarification...

"innings" contains the number of the innings within the match. If a match is
one that would normally have 2 innings, such as a T20 or ODI, then any innings
of more than 2 can be regarded as a super over.

"ball" is a combination of the over and delivery. For example, "0.3" represents
the 3rd ball of the 1st over.

"wides", "noballs", "byes", "legbyes", and "penalty" contain the total of each
particular type of extras, or are blank if not relevant to the delivery.

If a wicket occurred on a delivery then "wicket_type" will contain the method
of dismissal, while "player_dismissed" will indicate who was dismissed. There
is also the, admittedly remote, possibility that a second dismissal can be
recorded on the delivery (such as when a player retires on the same delivery
as another dismissal occurs). In this case "other_wicket_type" will record
the reason, while "other_player_dismissed" will show who was dismissed.

Matches included in this archive
--------------------------------

2020-11-29 - club - WBB - female - 1226963 - Melbourne Stars vs Sydney Thunder
2020-11-26 - club - WBB - female - 1226962 - Sydney Thunder vs Brisbane Heat
2020-11-25 - club - WBB - female - 1226961 - Perth Scorchers vs Melbourne Stars
2020-11-22 - club - WBB - female - 1226957 - Hobart Hurricanes vs Sydney Thunder
2020-11-22 - club - WBB - female - 1226958 - Adelaide Strikers vs Perth Scorchers
2020-11-22 - club - WBB - female - 1226959 - Melbourne Stars vs Sydney Sixers
2020-11-22 - club - WBB - female - 1226960 - Brisbane Heat vs Melbourne Renegades
2020-11-21 - club - WBB - female - 1226953 - Melbourne Stars vs Brisbane Heat
2020-11-21 - club - WBB - female - 1226954 - Adelaide Strikers vs Sydney Thunder
2020-11-21 - club - WBB - female - 1226955 - Hobart Hurricanes vs Perth Scorchers
2020-11-21 - club - WBB - female - 1226956 - Sydney Sixers vs Melbourne Renegades
2020-11-18 - club - WBB - female - 1226949 - Perth Scorchers vs Brisbane Heat
2020-11-18 - club - WBB - female - 1226950 - Adelaide Strikers vs Melbourne Renegades
2020-11-18 - club - WBB - female - 1226951 - Melbourne Stars vs Hobart Hurricanes
2020-11-18 - club - WBB - female - 1226952 - Sydney Sixers vs Sydney Thunder
2020-11-17 - club - WBB - female - 1226945 - Adelaide Strikers vs Hobart Hurricanes
2020-11-17 - club - WBB - female - 1226946 - Sydney Sixers vs Brisbane Heat
2020-11-17 - club - WBB - female - 1226947 - Melbourne Stars vs Perth Scorchers
2020-11-17 - club - WBB - female - 1226948 - Melbourne Renegades vs Sydney Thunder
2020-11-15 - club - WBB - female - 1226941 - Adelaide Strikers vs Sydney Sixers
2020-11-15 - club - WBB - female - 1226942 - Hobart Hurricanes vs Brisbane Heat
2020-11-15 - club - WBB - female - 1226943 - Perth Scorchers vs Sydney Thunder
2020-11-15 - club - WBB - female - 1226944 - Melbourne Stars vs Melbourne Renegades
2020-11-14 - club - WBB - female - 1226937 - Melbourne Renegades vs Perth Scorchers
2020-11-14 - club - WBB - female - 1226938 - Brisbane Heat vs Adelaide Strikers
2020-11-14 - club - WBB - female - 1226939 - Sydney Sixers vs Hobart Hurricanes
2020-11-14 - club - WBB - female - 1226940 - Sydney Thunder vs Melbourne Stars
2020-11-11 - club - WBB - female - 1226935 - Sydney Sixers vs Perth Scorchers
2020-11-11 - club - WBB - female - 1226936 - Sydney Thunder vs Brisbane Heat
2020-11-10 - club - WBB - female - 1226933 - Adelaide Strikers vs Melbourne Stars
2020-11-10 - club - WBB - female - 1226934 - Hobart Hurricanes vs Melbourne Renegades
2020-11-08 - club - WBB - female - 1226929 - Sydney Thunder vs Hobart Hurricanes
2020-11-08 - club - WBB - female - 1226930 - Adelaide Strikers vs Melbourne Renegades
2020-11-08 - club - WBB - female - 1226931 - Melbourne Stars vs Brisbane Heat
2020-11-08 - club - WBB - female - 1226932 - Perth Scorchers vs Sydney Sixers
2020-11-07 - club - WBB - female - 1226926 - Melbourne Renegades vs Sydney Thunder
2020-11-07 - club - WBB - female - 1226927 - Sydney Sixers vs Hobart Hurricanes
2020-11-07 - club - WBB - female - 1226928 - Perth Scorchers vs Melbourne Stars
2020-11-04 - club - WBB - female - 1226923 - Sydney Thunder vs Perth Scorchers
2020-11-04 - club - WBB - female - 1226924 - Sydney Sixers vs Brisbane Heat
2020-11-03 - club - WBB - female - 1226921 - Melbourne Renegades vs Hobart Hurricanes
2020-11-03 - club - WBB - female - 1226922 - Adelaide Strikers vs Melbourne Stars
2020-11-01 - club - WBB - female - 1226917 - Adelaide Strikers vs Perth Scorchers
2020-11-01 - club - WBB - female - 1226918 - Sydney Thunder vs Brisbane Heat
2020-11-01 - club - WBB - female - 1226919 - Melbourne Renegades vs Sydney Sixers
2020-11-01 - club - WBB - female - 1226920 - Hobart Hurricanes vs Melbourne Stars
2020-10-31 - club - WBB - female - 1226913 - Sydney Thunder vs Adelaide Strikers
2020-10-31 - club - WBB - female - 1226914 - Melbourne Renegades vs Perth Scorchers
2020-10-31 - club - WBB - female - 1226915 - Brisbane Heat vs Hobart Hurricanes
2020-10-26 - club - WBB - female - 1226909 - Sydney Thunder vs Melbourne Stars
2020-10-26 - club - WBB - female - 1226912 - Adelaide Strikers vs Sydney Sixers
2020-10-25 - club - WBB - female - 1226905 - Melbourne Stars vs Melbourne Renegades
2020-10-25 - club - WBB - female - 1226906 - Hobart Hurricanes vs Adelaide Strikers
2020-10-25 - club - WBB - female - 1226908 - Perth Scorchers vs Brisbane Heat
2019-12-08 - club - WBB - female - 1188440 - Adelaide Strikers vs Brisbane Heat
2019-12-07 - club - WBB - female - 1188438 - Adelaide Strikers vs Perth Scorchers
2019-12-07 - club - WBB - female - 1188439 - Brisbane Heat vs Melbourne Renegades
2019-12-01 - club - WBB - female - 1188434 - Melbourne Renegades vs Sydney Thunder
2019-12-01 - club - WBB - female - 1188435 - Sydney Sixers vs Adelaide Strikers
2019-12-01 - club - WBB - female - 1188436 - Perth Scorchers vs Hobart Hurricanes
2019-12-01 - club - WBB - female - 1188437 - Melbourne Stars vs Brisbane Heat
2019-11-30 - club - WBB - female - 1188431 - Melbourne Stars vs Melbourne Renegades
2019-11-30 - club - WBB - female - 1188432 - Sydney Sixers vs Adelaide Strikers
2019-11-30 - club - WBB - female - 1188433 - Perth Scorchers vs Hobart Hurricanes
2019-11-27 - club - WBB - female - 1188429 - Brisbane Heat vs Melbourne Renegades
2019-11-27 - club - WBB - female - 1188430 - Sydney Thunder vs Melbourne Stars
2019-11-24 - club - WBB - female - 1188427 - Adelaide Strikers vs Sydney Thunder
2019-11-24 - club - WBB - female - 1188428 - Perth Scorchers vs Sydney Sixers
2019-11-23 - club - WBB - female - 1188424 - Hobart Hurricanes vs Adelaide Strikers
2019-11-23 - club - WBB - female - 1188425 - Melbourne Renegades vs Melbourne Stars
2019-11-22 - club - WBB - female - 1188423 - Hobart Hurricanes vs Brisbane Heat
2019-11-20 - club - WBB - female - 1188419 - Melbourne Stars vs Perth Scorchers
2019-11-17 - club - WBB - female - 1188417 - Brisbane Heat vs Perth Scorchers
2019-11-17 - club - WBB - female - 1188418 - Sydney Sixers vs Melbourne Renegades
2019-11-16 - club - WBB - female - 1188415 - Sydney Thunder vs Brisbane Heat
2019-11-16 - club - WBB - female - 1188416 - Melbourne Stars vs Adelaide Strikers
2019-11-15 - club - WBB - female - 1188414 - Sydney Thunder vs Sydney Sixers
2019-11-13 - club - WBB - female - 1188412 - Hobart Hurricanes vs Sydney Sixers
2019-11-13 - club - WBB - female - 1188413 - Melbourne Stars vs Brisbane Heat
2019-11-12 - club - WBB - female - 1188411 - Perth Scorchers vs Sydney Thunder
2019-11-10 - club - WBB - female - 1188408 - Adelaide Strikers vs Melbourne Stars
2019-11-10 - club - WBB - female - 1188409 - Perth Scorchers vs Sydney Thunder
2019-11-10 - club - WBB - female - 1188410 - Melbourne Renegades vs Hobart Hurricanes
2019-11-09 - club - WBB - female - 1188405 - Melbourne Renegades vs Hobart Hurricanes
2019-11-09 - club - WBB - female - 1188406 - Adelaide Strikers vs Perth Scorchers
2019-11-09 - club - WBB - female - 1188407 - Sydney Sixers vs Brisbane Heat
2019-11-03 - club - WBB - female - 1188403 - Hobart Hurricanes vs Sydney Thunder
2019-11-03 - club - WBB - female - 1188404 - Brisbane Heat vs Adelaide Strikers
2019-11-02 - club - WBB - female - 1188398 - Melbourne Renegades vs Sydney Sixers
2019-11-02 - club - WBB - female - 1188399 - Perth Scorchers vs Melbourne Stars
2019-11-02 - club - WBB - female - 1188401 - Brisbane Heat vs Adelaide Strikers
2019-11-01 - club - WBB - female - 1188397 - Perth Scorchers vs Melbourne Renegades
2019-10-27 - club - WBB - female - 1188394 - Adelaide Strikers vs Perth Scorchers
2019-10-27 - club - WBB - female - 1188395 - Sydney Thunder vs Melbourne Stars
2019-10-27 - club - WBB - female - 1188396 - Brisbane Heat vs Hobart Hurricanes
2019-10-26 - club - WBB - female - 1188390 - Adelaide Strikers vs Hobart Hurricanes
2019-10-26 - club - WBB - female - 1188391 - Sydney Sixers vs Melbourne Stars
2019-10-26 - club - WBB - female - 1188392 - Brisbane Heat vs Perth Scorchers
2019-10-26 - club - WBB - female - 1188393 - Sydney Thunder vs Melbourne Renegades
2019-10-23 - club - WBB - female - 1188389 - Melbourne Renegades vs Perth Scorchers
2019-10-20 - club - WBB - female - 1188386 - Adelaide Strikers vs Melbourne Renegades
2019-10-20 - club - WBB - female - 1188387 - Melbourne Stars vs Hobart Hurricanes
2019-10-20 - club - WBB - female - 1188388 - Sydney Thunder vs Brisbane Heat
2019-10-19 - club - WBB - female - 1188383 - Adelaide Strikers vs Melbourne Renegades
2019-10-19 - club - WBB - female - 1188384 - Melbourne Stars vs Hobart Hurricanes
2019-10-19 - club - WBB - female - 1188385 - Sydney Sixers vs Brisbane Heat
2019-10-18 - club - WBB - female - 1188382 - Sydney Sixers vs Sydney Thunder
2019-01-26 - club - WBB - female - 1152783 - Sydney Sixers vs Brisbane Heat
2019-01-19 - club - WBB - female - 1152781 - Sydney Thunder vs Brisbane Heat
2019-01-19 - club - WBB - female - 1152782 - Sydney Sixers vs Melbourne Renegades
2019-01-14 - club - WBB - female - 1152780 - Melbourne Stars vs Sydney Sixers
2019-01-13 - club - WBB - female - 1152778 - Perth Scorchers vs Adelaide Strikers
2019-01-13 - club - WBB - female - 1152779 - Melbourne Renegades vs Sydney Sixers
2019-01-12 - club - WBB - female - 1152775 - Adelaide Strikers vs Perth Scorchers
2019-01-12 - club - WBB - female - 1152776 - Melbourne Renegades vs Hobart Hurricanes
2019-01-12 - club - WBB - female - 1152777 - Brisbane Heat vs Sydney Thunder
2019-01-10 - club - WBB - female - 1152774 - Brisbane Heat vs Melbourne Stars
2019-01-09 - club - WBB - female - 1152773 - Adelaide Strikers vs Hobart Hurricanes
2019-01-08 - club - WBB - female - 1152771 - Sydney Thunder vs Melbourne Renegades
2019-01-08 - club - WBB - female - 1152772 - Adelaide Strikers vs Hobart Hurricanes
2019-01-06 - club - WBB - female - 1152769 - Sydney Thunder vs Melbourne Stars
2019-01-06 - club - WBB - female - 1152770 - Brisbane Heat vs Melbourne Renegades
2019-01-05 - club - WBB - female - 1152766 - Sydney Thunder vs Melbourne Stars
2019-01-05 - club - WBB - female - 1152767 - Brisbane Heat vs Adelaide Strikers
2019-01-03 - club - WBB - female - 1152765 - Melbourne Renegades vs Hobart Hurricanes
2019-01-02 - club - WBB - female - 1152764 - Sydney Thunder vs Sydney Sixers
2019-01-01 - club - WBB - female - 1152763 - Melbourne Stars vs Melbourne Renegades
2018-12-31 - club - WBB - female - 1152758 - Hobart Hurricanes vs Brisbane Heat
2018-12-31 - club - WBB - female - 1152762 - Adelaide Strikers vs Sydney Sixers
2018-12-30 - club - WBB - female - 1152760 - Perth Scorchers vs Sydney Thunder
2018-12-30 - club - WBB - female - 1152761 - Hobart Hurricanes vs Brisbane Heat
2018-12-29 - club - WBB - female - 1152757 - Perth Scorchers vs Sydney Thunder
2018-12-29 - club - WBB - female - 1152759 - Melbourne Renegades vs Melbourne Stars
2018-12-28 - club - WBB - female - 1152756 - Sydney Sixers vs Adelaide Strikers
2018-12-27 - club - WBB - female - 1152755 - Sydney Sixers vs Melbourne Renegades
2018-12-26 - club - WBB - female - 1152754 - Perth Scorchers vs Brisbane Heat
2018-12-24 - club - WBB - female - 1152753 - Sydney Thunder vs Hobart Hurricanes
2018-12-23 - club - WBB - female - 1152750 - Adelaide Strikers vs Melbourne Stars
2018-12-23 - club - WBB - female - 1152751 - Sydney Sixers vs Brisbane Heat
2018-12-23 - club - WBB - female - 1152752 - Perth Scorchers vs Melbourne Renegades
2018-12-22 - club - WBB - female - 1152748 - Sydney Sixers vs Brisbane Heat
2018-12-22 - club - WBB - female - 1152749 - Perth Scorchers vs Melbourne Renegades
2018-12-21 - club - WBB - female - 1152746 - Sydney Thunder vs Hobart Hurricanes
2018-12-21 - club - WBB - female - 1152747 - Melbourne Stars vs Adelaide Strikers
2018-12-19 - club - WBB - female - 1152745 - Brisbane Heat vs Melbourne Stars
2018-12-18 - club - WBB - female - 1152744 - Hobart Hurricanes vs Perth Scorchers
2018-12-16 - club - WBB - female - 1152740 - Melbourne Stars vs Perth Scorchers
2018-12-16 - club - WBB - female - 1152741 - Sydney Thunder vs Adelaide Strikers
2018-12-16 - club - WBB - female - 1152742 - Sydney Sixers vs Hobart Hurricanes
2018-12-16 - club - WBB - female - 1152743 - Melbourne Renegades vs Brisbane Heat
2018-12-15 - club - WBB - female - 1152737 - Melbourne Stars vs Perth Scorchers
2018-12-15 - club - WBB - female - 1152738 - Adelaide Strikers vs Sydney Thunder
2018-12-15 - club - WBB - female - 1152739 - Hobart Hurricanes vs Sydney Sixers
2018-12-09 - club - WBB - female - 1152734 - Hobart Hurricanes vs Melbourne Stars
2018-12-09 - club - WBB - female - 1152735 - Adelaide Strikers vs Melbourne Renegades
2018-12-09 - club - WBB - female - 1152736 - Sydney Thunder vs Brisbane Heat
2018-12-08 - club - WBB - female - 1152730 - Hobart Hurricanes vs Melbourne Stars
2018-12-08 - club - WBB - female - 1152731 - Melbourne Renegades vs Adelaide Strikers
2018-12-08 - club - WBB - female - 1152732 - Brisbane Heat vs Perth Scorchers
2018-12-08 - club - WBB - female - 1152733 - Sydney Sixers vs Sydney Thunder
2018-12-07 - club - WBB - female - 1152729 - Sydney Sixers vs Perth Scorchers
2018-12-02 - club - WBB - female - 1152727 - Adelaide Strikers vs Brisbane Heat
2018-12-02 - club - WBB - female - 1152728 - Melbourne Renegades vs Sydney Thunder
2018-12-01 - club - WBB - female - 1152725 - Perth Scorchers vs Hobart Hurricanes
2018-12-01 - club - WBB - female - 1152726 - Sydney Sixers vs Melbourne Stars
2018-02-04 - club - WBB - female - 1118530 - Perth Scorchers vs Sydney Sixers
2018-02-02 - club - WBB - female - 1118529 - Sydney Sixers vs Adelaide Strikers
2018-02-01 - club - WBB - female - 1118528 - Perth Scorchers vs Sydney Thunder
2018-01-28 - club - WBB - female - 1118524 - Hobart Hurricanes vs Melbourne Stars
2018-01-28 - club - WBB - female - 1118525 - Melbourne Renegades vs Perth Scorchers
2018-01-28 - club - WBB - female - 1118526 - Adelaide Strikers vs Sydney Sixers
2018-01-28 - club - WBB - female - 1118527 - Sydney Thunder vs Brisbane Heat
2018-01-27 - club - WBB - female - 1118520 - Hobart Hurricanes vs Melbourne Stars
2018-01-27 - club - WBB - female - 1118521 - Adelaide Strikers vs Sydney Sixers
2018-01-27 - club - WBB - female - 1118522 - Perth Scorchers vs Melbourne Renegades
2018-01-27 - club - WBB - female - 1118523 - Sydney Thunder vs Brisbane Heat
2018-01-24 - club - WBB - female - 1118519 - Melbourne Renegades vs Sydney Thunder
2018-01-21 - club - WBB - female - 1118516 - Hobart Hurricanes vs Perth Scorchers
2018-01-21 - club - WBB - female - 1118517 - Melbourne Stars vs Sydney Sixers
2018-01-19 - club - WBB - female - 1118512 - Sydney Sixers vs Brisbane Heat
2018-01-15 - club - WBB - female - 1118510 - Hobart Hurricanes vs Melbourne Renegades
2018-01-14 - club - WBB - female - 1118509 - Adelaide Strikers vs Perth Scorchers
2018-01-13 - club - WBB - female - 1118505 - Perth Scorchers vs Adelaide Strikers
2018-01-13 - club - WBB - female - 1118506 - Sydney Sixers vs Sydney Thunder
2018-01-13 - club - WBB - female - 1118507 - Brisbane Heat vs Melbourne Stars
2018-01-12 - club - WBB - female - 1118504 - Melbourne Stars vs Brisbane Heat
2018-01-09 - club - WBB - female - 1118503 - Melbourne Stars vs Adelaide Strikers
2018-01-08 - club - WBB - female - 1118501 - Brisbane Heat vs Hobart Hurricanes
2018-01-08 - club - WBB - female - 1118502 - Sydney Thunder vs Perth Scorchers
2018-01-07 - club - WBB - female - 1118499 - Hobart Hurricanes vs Brisbane Heat
2018-01-06 - club - WBB - female - 1118498 - Melbourne Renegades vs Melbourne Stars
2018-01-05 - club - WBB - female - 1118497 - Adelaide Strikers vs Melbourne Stars
2018-01-02 - club - WBB - female - 1118495 - Sydney Sixers vs Melbourne Renegades
2017-12-31 - club - WBB - female - 1118493 - Hobart Hurricanes vs Sydney Thunder
2017-12-31 - club - WBB - female - 1118494 - Adelaide Strikers vs Brisbane Heat
2017-12-30 - club - WBB - female - 1118491 - Sydney Sixers vs Perth Scorchers
2017-12-29 - club - WBB - female - 1118490 - Adelaide Strikers vs Brisbane Heat
2017-12-27 - club - WBB - female - 1118489 - Melbourne Stars vs Perth Scorchers
2017-12-26 - club - WBB - female - 1118488 - Melbourne Stars vs Perth Scorchers
2017-12-23 - club - WBB - female - 1118487 - Brisbane Heat vs Melbourne Renegades
2017-12-22 - club - WBB - female - 1118485 - Melbourne Renegades vs Brisbane Heat
2017-12-17 - club - WBB - female - 1118483 - Sydney Sixers vs Hobart Hurricanes
2017-12-17 - club - WBB - female - 1118484 - Melbourne Renegades vs Adelaide Strikers
2017-12-16 - club - WBB - female - 1118482 - Adelaide Strikers vs Melbourne Renegades
2017-12-15 - club - WBB - female - 1118480 - Perth Scorchers vs Brisbane Heat
2017-12-12 - club - WBB - female - 1118478 - Sydney Sixers vs Perth Scorchers
2017-12-12 - club - WBB - female - 1118479 - Melbourne Stars vs Sydney Thunder
2017-12-10 - club - WBB - female - 1118475 - Perth Scorchers vs Brisbane Heat
2017-12-10 - club - WBB - female - 1118477 - Sydney Thunder vs Sydney Sixers
2017-12-09 - club - WBB - female - 1118472 - Sydney Thunder vs Melbourne Renegades
2017-12-09 - club - WBB - female - 1118473 - Adelaide Strikers vs Hobart Hurricanes
2017-12-09 - club - WBB - female - 1118474 - Sydney Sixers vs Melbourne Stars
2017-01-28 - club - WBB - female - 1064720 - Sydney Sixers vs Perth Scorchers
2017-01-25 - club - WBB - female - 1064719 - Sydney Sixers vs Hobart Hurricanes
2017-01-24 - club - WBB - female - 1064718 - Brisbane Heat vs Perth Scorchers
2017-01-21 - club - WBB - female - 1064716 - Sydney Sixers vs Melbourne Renegades
2017-01-21 - club - WBB - female - 1064717 - Melbourne Stars vs Hobart Hurricanes
2017-01-20 - club - WBB - female - 1064710 - Adelaide Strikers vs Brisbane Heat
2017-01-20 - club - WBB - female - 1064711 - Perth Scorchers vs Sydney Thunder
2017-01-20 - club - WBB - female - 1064712 - Sydney Sixers vs Melbourne Renegades
2017-01-20 - club - WBB - female - 1064713 - Hobart Hurricanes vs Melbourne Stars
2017-01-16 - club - WBB - female - 1064709 - Sydney Thunder vs Hobart Hurricanes
2017-01-15 - club - WBB - female - 1064707 - Perth Scorchers vs Melbourne Stars
2017-01-14 - club - WBB - female - 1064704 - Adelaide Strikers vs Perth Scorchers
2017-01-14 - club - WBB - female - 1064705 - Melbourne Renegades vs Brisbane Heat
2017-01-14 - club - WBB - female - 1064706 - Sydney Sixers vs Sydney Thunder
2017-01-13 - club - WBB - female - 1064702 - Melbourne Stars vs Adelaide Strikers
2017-01-13 - club - WBB - female - 1064703 - Sydney Sixers vs Hobart Hurricanes
2017-01-10 - club - WBB - female - 1064697 - Adelaide Strikers vs Melbourne Stars
2017-01-09 - club - WBB - female - 1064700 - Brisbane Heat vs Hobart Hurricanes
2017-01-09 - club - WBB - female - 1064701 - Perth Scorchers vs Sydney Sixers
2017-01-08 - club - WBB - female - 1064698 - Brisbane Heat vs Hobart Hurricanes
2017-01-07 - club - WBB - female - 1064696 - Melbourne Stars vs Melbourne Renegades
2017-01-05 - club - WBB - female - 1064695 - Hobart Hurricanes vs Sydney Thunder
2017-01-04 - club - WBB - female - 1023715 - Perth Scorchers vs Melbourne Renegades
2017-01-03 - club - WBB - female - 1023711 - Adelaide Strikers vs Sydney Sixers
2017-01-02 - club - WBB - female - 1023707 - Sydney Sixers vs Adelaide Strikers
2017-01-02 - club - WBB - female - 1023709 - Sydney Thunder vs Brisbane Heat
2017-01-01 - club - WBB - female - 1023705 - Melbourne Stars vs Melbourne Renegades
2016-12-31 - club - WBB - female - 1023703 - Adelaide Strikers vs Perth Scorchers
2016-12-29 - club - WBB - female - 1023701 - Hobart Hurricanes vs Sydney Sixers
2016-12-28 - club - WBB - female - 1023697 - Sydney Sixers vs Sydney Thunder
2016-12-27 - club - WBB - female - 1023693 - Brisbane Heat vs Melbourne Stars
2016-12-26 - club - WBB - female - 1023687 - Melbourne Stars vs Brisbane Heat
2016-12-18 - club - WBB - female - 1023679 - Hobart Hurricanes vs Melbourne Renegades
2016-12-18 - club - WBB - female - 1023681 - Sydney Sixers vs Melbourne Stars
2016-12-17 - club - WBB - female - 1023671 - Hobart Hurricanes vs Melbourne Renegades
2016-12-17 - club - WBB - female - 1023673 - Sydney Sixers vs Melbourne Stars
2016-12-17 - club - WBB - female - 1023675 - Sydney Thunder vs Adelaide Strikers
2016-12-17 - club - WBB - female - 1023677 - Brisbane Heat vs Perth Scorchers
2016-12-13 - club - WBB - female - 1023667 - Melbourne Stars vs Sydney Thunder
2016-12-11 - club - WBB - female - 1023659 - Adelaide Strikers vs Melbourne Renegades
2016-12-11 - club - WBB - female - 1023661 - Perth Scorchers vs Hobart Hurricanes
2016-12-10 - club - WBB - female - 1023655 - Adelaide Strikers vs Melbourne Renegades
2016-01-22 - club - WBB - female - 896549 - Hobart Hurricanes vs Sydney Sixers
2016-01-21 - club - WBB - female - 896547 - Sydney Thunder vs Perth Scorchers
2016-01-17 - club - WBB - female - 896545 - Melbourne Renegades vs Perth Scorchers
2016-01-15 - club - WBB - female - 896527 - Sydney Sixers vs Hobart Hurricanes
2015-12-31 - club - WBB - female - 896493 - Adelaide Strikers vs Perth Scorchers
2015-12-27 - club - WBB - female - 896487 - Melbourne Stars vs Perth Scorchers
2015-12-26 - club - WBB - female - 896485 - Melbourne Stars vs Perth Scorchers
2015-12-19 - club - WBB - female - 896467 - Adelaide Strikers vs Brisbane Heat
2015-12-19 - club - WBB - female - 896471 - Sydney Sixers vs Melbourne Stars
2015-12-18 - club - WBB - female - 896463 - Sydney Sixers vs Melbourne Stars

Consolidated data
-----------------

You may notice that there is an extra CSV file in this archive, called
"all_matches.csv". This file, as the name suggests, contains all of the
ball-by-ball data for matches from the archive in a single CSV. Hopefully
it will make use of the data easier in some cases.

Further information
-------------------

You can find all of our currently available data at https://cricsheet.org/

You can contact me via the following methods:
  Email  : stephen@cricsheet.org
  Twitter: @cricsheet
