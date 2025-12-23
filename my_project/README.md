Reproduce 


pixi run dg dev -> in my_project ->  works

pixi run dg utils refresh-defs-state -> throws error

terminal output:
➜ pixi run dg utils refresh-defs-state
DAGSTER_HOME is not set, which means defs state for VERSIONED_STATE_STORAGE components cannot be stored in a persistent location. 
You can resolve this warning by exporting the environment variable. For example, you can run the following command in your shell or include it in your shell configuration file:
        export DAGSTER_HOME="~/dagster_home"


Traceback (most recent call last):
  File "/Users/milicevica23/git/example-dg-utils/my_project/.pixi/envs/default/bin/dg", line 10, in <module>
    sys.exit(main())
  File "/Users/milicevica23/git/example-dg-utils/my_project/.pixi/envs/default/lib/python3.10/site-packages/dagster_dg_cli/cli/__init__.py", line 76, in main
    cli(auto_envvar_prefix=ENV_PREFIX)
  File "/Users/milicevica23/git/example-dg-utils/my_project/.pixi/envs/default/lib/python3.10/site-packages/click/core.py", line 1485, in __call__
    return self.main(*args, **kwargs)
  File "/Users/milicevica23/git/example-dg-utils/my_project/.pixi/envs/default/lib/python3.10/site-packages/click/core.py", line 1406, in main
    rv = self.invoke(ctx)
  File "/Users/milicevica23/git/example-dg-utils/my_project/.pixi/envs/default/lib/python3.10/site-packages/click/core.py", line 1873, in invoke
    return _process_result(sub_ctx.command.invoke(sub_ctx))
  File "/Users/milicevica23/git/example-dg-utils/my_project/.pixi/envs/default/lib/python3.10/site-packages/click/core.py", line 1873, in invoke
    return _process_result(sub_ctx.command.invoke(sub_ctx))
  File "/Users/milicevica23/git/example-dg-utils/my_project/.pixi/envs/default/lib/python3.10/site-packages/click/core.py", line 1269, in invoke
    return ctx.invoke(self.callback, **ctx.params)
  File "/Users/milicevica23/git/example-dg-utils/my_project/.pixi/envs/default/lib/python3.10/site-packages/click/core.py", line 824, in invoke
    return callback(*args, **kwargs)
  File "/Users/milicevica23/git/example-dg-utils/my_project/.pixi/envs/default/lib/python3.10/site-packages/dagster_dg_core/utils/telemetry.py", line 108, in wrap
    result = f(*args, **kwargs)
  File "/Users/milicevica23/git/example-dg-utils/my_project/.pixi/envs/default/lib/python3.10/site-packages/dagster_dg_cli/cli/utils.py", line 551, in refresh_defs_state
    asyncio.run(
  File "/Users/milicevica23/git/example-dg-utils/my_project/.pixi/envs/default/lib/python3.10/asyncio/runners.py", line 44, in run
    return loop.run_until_complete(main)
  File "/Users/milicevica23/git/example-dg-utils/my_project/.pixi/envs/default/lib/python3.10/asyncio/base_events.py", line 649, in run_until_complete
    return future.result()
  File "/Users/milicevica23/git/example-dg-utils/my_project/.pixi/envs/default/lib/python3.10/site-packages/dagster_dg_cli/cli/utils.py", line 450, in _refresh_defs_state_with_live_display
    refresh_task, statuses = get_updated_defs_state_info_task_and_statuses(
  File "/Users/milicevica23/git/example-dg-utils/my_project/.pixi/envs/default/lib/python3.10/site-packages/dagster_dg_cli/cli/defs_state.py", line 143, in get_updated_defs_state_info_task_and_statuses
    component_tree = ComponentTree.for_project(project_path)
  File "/Users/milicevica23/git/example-dg-utils/my_project/.pixi/envs/default/lib/python3.10/site-packages/dagster/components/core/component_tree.py", line 158, in for_project
    defs_module = importlib.import_module(defs_module_name)
  File "/Users/milicevica23/git/example-dg-utils/my_project/.pixi/envs/default/lib/python3.10/importlib/__init__.py", line 126, in import_module
    return _bootstrap._gcd_import(name[level:], package, level)
  File "<frozen importlib._bootstrap>", line 1050, in _gcd_import
  File "<frozen importlib._bootstrap>", line 1027, in _find_and_load
  File "<frozen importlib._bootstrap>", line 992, in _find_and_load_unlocked
  File "<frozen importlib._bootstrap>", line 241, in _call_with_frames_removed
  File "<frozen importlib._bootstrap>", line 1050, in _gcd_import
  File "<frozen importlib._bootstrap>", line 1027, in _find_and_load
  File "<frozen importlib._bootstrap>", line 1004, in _find_and_load_unlocked
ModuleNotFoundError: No module named 'my_project'