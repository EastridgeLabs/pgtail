pgtail
======

Pronounced "pig tail" this python shell script will execute the tail shell command (with the -f, follow option) on your Postgresql database logs. The output is then piped through a database specific filter showing only the log entries and sql statements for that speciific database instead of all of them.

Developer: Eric Goodman

Requirements: Python 2.6+, Postgresql 7+ and a Linux or Mac OS shell

Configuration:

          1) Edit postgresql.conf
          2) Set the "log_statement" parameter value to 'all' (include single quotes).
          3) Restart the postgres server service

Usage:
<p>
          pgtail &lt;postgresql_log_path&gt; [&lt;database_name&gt;]
</p>

Examples:<br />
<p>
          pgtail /var/lib/pgsql9/data/pg_log/postgresql-Wed.log invoicedb<br />
          pgtail /var/lib/pgsql9/data/pg_log/postgresql-Wed.log (shows all log entries)<br />
</p>

<script type="text/javascript"><!--

  var _gaq = _gaq || [];
  _gaq.push(['_setAccount', 'UA-36685065-1']);
  _gaq.push(['_trackPageview']);

  (function() {
    var ga = document.createElement('script'); ga.type = 'text/javascript'; ga.async = true;
    ga.src = ('https:' == document.location.protocol ? 'https://ssl' : 'http://www') + '.google-analytics.com/ga.js';
    var s = document.getElementsByTagName('script')[0]; s.parentNode.insertBefore(ga, s);
  })();

--></script>