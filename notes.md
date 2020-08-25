## Notes

### Enable deno vs code extension for windows?.

Create .vscode for extension settings. Need to look into this more as some thing still are not working correctly.

```
{
    "deno.enable": true,
    "[typescript]": {
        "editor.defaultFormatter": "denoland.vscode-deno",
      },
      "[typescriptreact]": {
        "editor.defaultFormatter": "denoland.vscode-deno",
      },
}
```

### Use Drake to allow permissions (example)

```
import { desc, run, task, sh } from 'https://deno.land/x/drake@v1.2.6/mod.ts';

desc("Minimal Drake task");
task("hello", [], async function() {
  await sh('deno run --allow-env main.ts')
});

run()
```

### Create and set directory to store dependencies

mkdir deno_dir
set DENO_DIR ./deno_dir


### Deno runtime API

https://doc.deno.land/builtin/stable