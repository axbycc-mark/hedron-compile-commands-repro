```
bazel run @hedron_compile_commands//:refresh_all
Starting local Bazel server and connecting to it...
WARNING: --enable_bzlmod is set, but no MODULE.bazel file was found at the workspace root. Bazel will create an empty MODULE.bazel file. Please consider migrating your external dependencies from WORKSPACE to MODULE.bazel. For more details, please refer to https://github.com/bazelbuild/bazel/issues/18958.
INFO: Analyzed target @@hedron_compile_commands//:refresh_all (72 packages loaded, 333 targets configured).
INFO: Found 1 target...
Target @@hedron_compile_commands//:refresh_all up-to-date:
  bazel-bin/external/hedron_compile_commands/refresh_all.zip
  bazel-bin/external/hedron_compile_commands/refresh_all.exe
  bazel-bin/external/hedron_compile_commands/refresh_all.check_python_version.py
  bazel-bin/external/hedron_compile_commands/refresh_all.py
INFO: Elapsed time: 7.082s, Critical Path: 0.04s
INFO: 1 process: 1 internal.
INFO: Build completed successfully, 1 total action
INFO: Running command line: bazel-bin/external/hedron_compile_commands/refresh_all.exe
>>> Analyzing commands used in @//...
Traceback (most recent call last):
  File "C:\Users\marki\AppData\Local\Temp\Bazel.runfiles_fuolzcoy\runfiles\hedron_compile_commands\refresh_all.check_python_version.py", line 15, in <module>
    refresh_all.main()
  File "C:\Users\marki\AppData\Local\Temp\Bazel.runfiles_fuolzcoy\runfiles\hedron_compile_commands\refresh_all.py", line 1421, in main
    compile_command_entries.extend(_get_commands(target, flags))
  File "C:\Users\marki\AppData\Local\Temp\Bazel.runfiles_fuolzcoy\runfiles\hedron_compile_commands\refresh_all.py", line 1283, in _get_commands
    yield from _convert_compile_commands(parsed_aquery_output)
  File "C:\Users\marki\AppData\Local\Temp\Bazel.runfiles_fuolzcoy\runfiles\hedron_compile_commands\refresh_all.py", line 1163, in _convert_compile_commands
    for source_files, header_files, compile_command_args in outputs:
  File "D:\Python310\lib\concurrent\futures\_base.py", line 621, in result_iterator
    yield _result_or_cancel(fs.pop())
  File "D:\Python310\lib\concurrent\futures\_base.py", line 319, in _result_or_cancel
    return fut.result(timeout)
  File "D:\Python310\lib\concurrent\futures\_base.py", line 451, in result
    return self.__get_result()
  File "D:\Python310\lib\concurrent\futures\_base.py", line 403, in __get_result
    raise self._exception
  File "D:\Python310\lib\concurrent\futures\thread.py", line 58, in run
    result = self.fn(*self.args, **self.kwargs)
  File "C:\Users\marki\AppData\Local\Temp\Bazel.runfiles_fuolzcoy\runfiles\hedron_compile_commands\refresh_all.py", line 1127, in _get_cpp_command_for_files
    source_files, header_files = _get_files(compile_action)
  File "C:\Users\marki\AppData\Local\Temp\Bazel.runfiles_fuolzcoy\runfiles\hedron_compile_commands\refresh_all.py", line 678, in _get_files
    header_files = _get_headers(compile_action, source_file)
  File "C:\Users\marki\AppData\Local\Temp\Bazel.runfiles_fuolzcoy\runfiles\hedron_compile_commands\refresh_all.py", line 596, in _get_headers
    headers, should_cache = _get_headers_gcc(compile_action.arguments, source_path, compile_action.actionKey)
  File "C:\Users\marki\AppData\Local\Temp\Bazel.runfiles_fuolzcoy\runfiles\hedron_compile_commands\refresh_all.py", line 302, in _get_headers_gcc
    headers = _parse_headers_from_makefile_deps(header_search_process.stdout)
  File "C:\Users\marki\AppData\Local\Temp\Bazel.runfiles_fuolzcoy\runfiles\hedron_compile_commands\refresh_all.py", line 176, in _parse_headers_from_makefile_deps
    assert target.endswith(('.o', '.obj')), "Something went wrong in makefile parsing to get headers. The target should be an object file. Output:\n" + d_file_content
AssertionError: Something went wrong in makefile parsing to get headers. The target should be an object file. Output:
nvcc fatal   : Cannot find compiler 'cl.exe' in PATH
```
