## Byte Size and Time Duration Parsers

This fork of CDAP Wrangler adds support for parsing byte size and time duration units. These features make it easier to handle data columns representing file sizes or time intervals.

### Byte Size Support

The ByteSize parser automatically recognizes and converts various byte units:
- Bytes (B, b)
- Kilobytes (KB, kb)
- Megabytes (MB, mb)
- Gigabytes (GB, gb)
- Terabytes (TB, tb)
- Petabytes (PB, pb)

Example usage in directives:

### Time Duration Support

The TimeDuration parser automatically recognizes and converts various time units:
- Milliseconds (ms)
- Seconds (s)
- Minutes (m)
- Hours (h)
- Days (d)

Example usage in directives:

### Aggregate-Stats Directive

A new directive called `aggregate-stats` demonstrates the usage of these new parsers. This directive aggregates byte size and time duration values across multiple rows.

Syntax:

Parameters:
- `size-column`: Source column containing byte size values
- `time-column`: Source column containing time duration values
- `output-size-column`: Target column for aggregated byte size (in MB)
- `output-time-column`: Target column for aggregated time duration (in seconds)
- `type`: Optional parameter, either "total" (default) or "average"

Example:

This will calculate the total size in megabytes and total time in seconds.
