```
$ pnpm build

> rolldown-react-bootstrap-bug@1.0.0 build /home/user/rolldown-react-bootstrap-bug
> rolldown index.jsx --minify --file bundle.js


thread '<unnamed>' (1139236) panicked at crates/rolldown/src/module_finalizers/mod.rs:104:7:
canonical name not found for SymbolRef { owner: 34, symbol: SymbolId(4294967292) }, original_name: "import_prop_types" in module "node_modules/.pnpm/react-bootstrap@2.10.10_@types+react@19.2.7_react-dom@19.2.3_react@19.2.3__react@19.2.3/node_modules/react-bootstrap/esm/CloseButton.js" when finalizing module "node_modules/.pnpm/react-bootstrap@2.10.10_@types+react@19.2.7_react-dom@19.2.3_react@19.2.3__react@19.2.3/node_modules/react-bootstrap/esm/CloseButton.js" in chunk ""
note: run with `RUST_BACKTRACE=1` environment variable to display a backtrace

 ERROR  Panic in async function                                                                                                                                                             

  

 ELIFECYCLE  Command failed with exit code 1.
```

The error goes away if you either remove the --minify option or downgrade to rolldown@1.0.0-beta.54