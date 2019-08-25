# git-map

Git plugin for slicing through time and collecting command results.

## Usage

```
git-map: Slice through time, collecting results of command on file
git-map [<option>...] <file-to-slice-through> <command-to-run> [<command-arg>...]

Options:
  (--format|-f) <format-string>     git log format string with placeholder `{}` for
                                    command output
```

```
# Example for tracking change of certain metric (in a notebook) over time
git map -f "%cI,{}" ./metric.ipynb ./calculate-metric wer

2019-06-23T10:18:58+05:30,1.994184
2019-06-21T17:47:12+05:30,2.101576
2019-06-16T02:23:35+05:30,2.101576
2019-06-16T00:36:17+05:30,2.101576
2019-06-12T14:46:01+05:30,1.322993
2019-06-11T10:56:55+05:30,1.322993
2019-06-09T03:50:57+05:30,1.322993
2019-06-09T03:21:23+05:30,1.322993
2019-06-08T17:02:33+05:30,1.322993
2019-06-08T15:58:33+05:30,1.322993
2019-06-06T16:59:03+05:30,1.322993
2019-06-06T01:30:52+05:30,1.322993
2019-06-05T16:40:26+05:30,1.870438
2019-06-05T16:38:45+05:30,1.870438
2019-06-03T20:46:41+05:30,1.870438
2019-06-01T01:12:45+05:30,1.891144
2019-05-29T15:25:44+05:30,2.064451
2019-05-26T00:48:57+05:30,2.064451
2019-05-23T18:04:18+05:30,2.223523
2019-05-23T13:59:59+05:30,2.223523
...
```
