# spacexlaunchdata
Try deno with space x launch data

## initial project setup steps
### setup settings.json
{
    "deno.enable": true,
    "deno.alwaysShowStatus": true,
    "deno.autoFmtOnSave": true,
    "editor.hover.enabled": true
}
### setup tsconfig.json
{
    "compilerOptions": {
        "allowJs": true,
        "esModuleInterop": true,
        "lib": [
            "esnext"
        ],
        "module": "esnext",
        "moduleResolution": "deno",
        "baseUrl": ".",
        "paths": {
            "http://*": [
                ".../deno/deps/http/*"
            ],
            "https://*": [
                ".../deno/deps/https/*"
            ],
        },
        "plugins": [
            {
                "name": "typescript-deno-plugin",
                "enable": true, // default is `true`
                "importmap": "import_map.json"
            }
        ],
        "noEmit": true,
        "pretty": true,
        "resolveJsonModule": true,
        "target": "esnext"
    },
    "include": [
        "./**/*.ts"
    ]
}
### setup $DENO_DIR
set $DENO_DIR=deno_dir
### Run npm install --save-dev typescript-deno-plugin typescript

