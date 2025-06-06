## unplanned

BACKWARDS INCOMPATIBILITIES:
* Update golangci-lint support to expect golangci-lint/v2.
  [[GH-3710]](https://github.com/fatih/vim-go/pull/3710)

IMPROVEMENTS:

BUG FIXES:
* Fix delay when listing breakpoints when stepping in Neovim.
  [[GH-3714]](https://github.com/fatih/vim-go/pull/3714)

## v1.29 - (April 18, 2025)

BACKWARDS INCOMPATIBILITIES:
* Drop support for [guru](https://docs.google.com/document/d/1_Y9xCEMj5S-7rv2ooHpZNH15JgRT5iM742gJkw5LtmQ/edit?pli=1&tab=t.0#heading=h.ojv16z1d1gas).
  [[GH-3650]](https://github.com/fatih/vim-go/pull/3650)
  [[GH-3654]](https://github.com/fatih/vim-go/pull/3654)
* Drop support for `keyify`.
  [[GH-3665]](https://github.com/fatih/vim-go/pull/3665)

IMPROVEMENTS:
* Change the group that godebugStracktrace is default linked to.
  [[GH-3483]](https://github.com/fatih/vim-go/pull/3483)
* Add `:GoCoverageOverlay`.
  [[GH-3485]](https://github.com/fatih/vim-go/pull/3485)
* Add `:GoTestFile`.
  [[GH-3486]](https://github.com/fatih/vim-go/pull/3486)
  [[GH-3487]](https://github.com/fatih/vim-go/pull/3487)
* Add `(go-fill-struct)` mapping.
  [[GH-3502]](https://github.com/fatih/vim-go/pull/3502)
  [[GH-3503]](https://github.com/fatih/vim-go/pull/3503)
* Output an error message when `g:go_fillstruct_mode` and `g:go_gopls_enabled`
  conflict.
  [[GH-3504]](https://github.com/fatih/vim-go/pull/3504)
* Add `:GoExtract` command and related mapping.
  [[GH-3506]](https://github.com/fatih/vim-go/pull/3506)
  [[GH-3617]](https://github.com/fatih/vim-go/pull/3617)
  [[GH-3626]](https://github.com/fatih/vim-go/pull/3626)
* Halt the debugger after a connection is establish with `:GoDebugConnect`.
  [[GH-3514]](https://github.com/fatih/vim-go/pull/3514)
  [[GH-3520]](https://github.com/fatih/vim-go/pull/3520)
  [[GH-3570]](https://github.com/fatih/vim-go/pull/3570)
* Clarify `:GoImpl` usage message.
  [[GH-3522]](https://github.com/fatih/vim-go/pull/3522)
* Add commands and mappings related to godoc to the godoc preview window.
  [[GH-3527]](https://github.com/fatih/vim-go/pull/3527)
  [[GH-3532]](https://github.com/fatih/vim-go/pull/3532)
  [[GH-3559]](https://github.com/fatih/vim-go/pull/3559)
* Link goPredefinedIdentifiers to Constant instead of goBoolean by default.
  [[GH-3528]](https://github.com/fatih/vim-go/pull/3528)
* Add `gD` mapping for `:GoDefType`.
  [[GH-3531]](https://github.com/fatih/vim-go/pull/3531)
* Use Vim's native tag stack when possible.
  [[GH-3548]](https://github.com/fatih/vim-go/pull/3548)
  [[GH-3554]](https://github.com/fatih/vim-go/pull/3554)
  [[GH-3556]](https://github.com/fatih/vim-go/pull/3556)
  [[GH-3557]](https://github.com/fatih/vim-go/pull/3557)
  [[GH-3558]](https://github.com/fatih/vim-go/pull/3558)
* Update codeAction response handling to work with gopls v0.12.0.
  [[GH-3555]](https://github.com/fatih/vim-go/pull/3555)
* Drop support for Vim 8.0.
  [[GH-3538]](https://github.com/fatih/vim-go/pull/3538)
* Set gopls clientInfo field.
  [[GH-3567]](https://github.com/fatih/vim-go/pull/3567)
* Add support for the Go 1.21's new builtin functions.
  [[GH-3578]](https://github.com/fatih/vim-go/pull/3578)
* Add syntax support for the toolchain directive in go.mod.
  [[GH-3633]](https://github.com/fatih/vim-go/pull/3633)
* Add fuzz snippet.
  [[GH-3636]](https://github.com/fatih/vim-go/pull/3636)
* Update gopls code action handling.
  [[GH-3695]](https://github.com/fatih/vim-go/pull/3695)
* Remove installation of `gorename`.
  [[GH-3697]](https://github.com/fatih/vim-go/pull/3697)
* Add support for `gopls rename`.
  [[GH-3698]](https://github.com/fatih/vim-go/pull/3698)
* Use a double border around doc popup.
  [[GH-3705]](https://github.com/fatih/vim-go/pull/3705)


BUG FIXES:
* Update [impl](https://github.com/josharian/impl) source path after its default branch was changed from master to main.
  [[GH-3477]](https://github.com/fatih/vim-go/pull/3477)
* Update `:GoMetaLinter` help.
  [[GH-3534]](https://github.com/fatih/vim-go/pull/3534)
* Update syntax file for empty const, var, and import lists.
  [[GH-3577]](https://github.com/fatih/vim-go/pull/3577)
  [[GH-3579]](https://github.com/fatih/vim-go/pull/3579)
* Fix sameids highlighting when id is preceded with multi-byte characters.
  [[GH-3587]](https://github.com/fatih/vim-go/pull/3587)
* Avoid creating an anonymous snippet when selected completion lacks
  placeholders.
  [[GH-3603]](https://github.com/fatih/vim-go/pull/3603)
* Fix sameids highlighting when identifier immediately precedes newline.
  [[GH-3606]](https://github.com/fatih/vim-go/pull/3606)
* Fix Python escape sequence in UltiSnips/go.snippets.
  [[GH-3614]](https://github.com/fatih/vim-go/pull/3614)
* Do not attempt to use gopls for documentation when gopls is disabled.
  [[GH-3610]](https://github.com/fatih/vim-go/pull/3610)
* Fix spelling of go#util#EchoWarning in a few calls.
  [[GH-3613]](https://github.com/fatih/vim-go/pull/3613)
* Improve matching of package comments.
  [[GH-3637]](https://github.com/fatih/vim-go/pull/3637)
* Fix editing of lines with multibyte characters.
  [[GH-3644]](https://github.com/fatih/vim-go/pull/3644)
* Swallow delve errors when trying to place a breakpoint at an invalid location.
  [[GH-3652]](https://github.com/fatih/vim-go/pull/3652)
* Fix parsing of gopls error message to determine debug port.
  [[GH-3672]](https://github.com/fatih/vim-go/pull/3672)
* Handle unexpected code action commands from `gopls`.
  [[GH-3678]](https://github.com/fatih/vim-go/pull/3678)
* Fix substitution paths in debug stacktrace window.
  [[GH-3675]](https://github.com/fatih/vim-go/pull/3675)
* Fix handling of gopls restarts.
  [[GH-3685]](https://github.com/fatih/vim-go/pull/3685)
* Fix :GoDocBrowser's handling of arguments.
  [[GH-3703]](https://github.com/fatih/vim-go/pull/3703)

## v1.28 - (December 17, 2022)

BUG FIXES:
* Remove diagnostic message used during development.
  [[GH-3476]](https://github.com/fatih/vim-go/pull/3476)

## v1.27 - (December 17, 2022)

BACKWARDS INCOMPATIBILITIES:

IMPROVEMENTS:
* Update documentation for installing tools.
  [[GH-3413]](https://github.com/fatih/vim-go/pull/3413)
* Show diagnostics via go#tool#DescribeBalloon().
  [[GH-3415]](https://github.com/fatih/vim-go/pull/3415)
  [[GH-3417]](https://github.com/fatih/vim-go/pull/3417)
* Allow version of individual tools to be installed with `:GoUpdateBinaries`
  and `:GoInstallBinaries` to be overridden by users.
  [[GH-3435]](https://github.com/fatih/vim-go/pull/3435)
  [[GH-3436]](https://github.com/fatih/vim-go/pull/3436)
* Highlight numeric formats introduced in Go 1.13.
  [[GH-3440]](https://github.com/fatih/vim-go/pull/3440)

BUG FIXES:
* Fix quoting of arguments when shell is set to pwsh on Windows.
  [[GH-3422]](https://github.com/fatih/vim-go/pull/3422)
* Use -mod=mod instead of -mod=readonly when installing tools.
  [[GH-3449]](https://github.com/fatih/vim-go/pull/3449)
* Remove support for /* */ comments in go.mod files.
  [[GH-3460]](https://github.com/fatih/vim-go/pull/3460)
* Fix go.work syntax support.
  [[GH-3461]](https://github.com/fatih/vim-go/pull/3461)
* Split the buffer without considering the current buffer when a mapping to
  split and jump to definition is used.
  [[GH-3462]](https://github.com/fatih/vim-go/pull/3462)
* Fix hilighting of package references via `:GoSameIds`.
  [[GH-3469]](https://github.com/fatih/vim-go/pull/3469)

## v1.26 - (April 23, 2022)

BACKWARDS INCOMPATIBILITIES:

IMPROVEMENTS:
* Add mapping for formatting, `(go-fmt)`.
  [[GH-3209]](https://github.com/fatih/vim-go/pull/3209)
* Add `tr` snippet for `"testing.T".Run`.
  [[GH-3210]](https://github.com/fatih/vim-go/pull/3210)
  [[GH-3220]](https://github.com/fatih/vim-go/pull/3220)
* Use `go env GOBIN` to determine `GOBIN`'s value.
  [[GH-3207]](https://github.com/fatih/vim-go/pull/3207)
* List register in the debugger.
  [[GH-3221]](https://github.com/fatih/vim-go/pull/3221)
* Install the latest release of tools that seem to be using tags to do releases
  instead of installing from their master/main branch.
  [[GH-3227]](https://github.com/fatih/vim-go/pull/3227)
* Expose error message when `gopls` cannot be found and
  `g:go_echo_command_info` is set.
  [[GH-3244]](https://github.com/fatih/vim-go/pull/3244)
* Install all tools in module aware mode in preparation for Go 1.17 release.
  [[GH-3226]](https://github.com/fatih/vim-go/pull/3226)
* Add `g:go_doc_balloon` to allow godoc to be displayed in hover balloons.
  [[GH-3252]](https://github.com/fatih/vim-go/pull/3252)
* Default to using `revive` in place of `golint`.
  [[GH-3248]](https://github.com/fatih/vim-go/pull/3248)
  [[GH-3401]](https://github.com/fatih/vim-go/pull/3401)
* Teach `:GoDebugPrint` to show function call return values.
  [[GH-3256]](https://github.com/fatih/vim-go/pull/3256)
* Do not enable keyify unless in GOPATH.
  [[GH-3095]](https://github.com/fatih/vim-go/pull/3095)
* Show LSP messages to users.
  [[GH-3058]](https://github.com/fatih/vim-go/pull/3058)
* Check omnifunc's value before executing actions on CompletedDone event.
  [[GH-3274]](https://github.com/fatih/vim-go/pull/3274)
* Highlight new form of build constraints.
  [[GH-3292]](https://github.com/fatih/vim-go/pull/3292)
* Teach `:GoDiagnostics` to handle package pattern arguments.
  [[GH-3297]](https://github.com/fatih/vim-go/pull/3297)
* Add `g:go_debug_subsitute_paths` to support debugging applications when the
  source is hosted in a local location that is different from where the binary
  was compiled.
  [[GH-3301]](https://github.com/fatih/vim-go/pull/3301)
* Wrap text in the fzf preview window by default.
  [[GH-3310]](https://github.com/fatih/vim-go/pull/3310)
* Wait for up to five seconds when opening a connection to a remote debugger.
  [[GH-3312]](https://github.com/fatih/vim-go/pull/3312)
* Install tools with `go install` instead of `go get`.
  [[GH-3317]](https://github.com/fatih/vim-go/pull/3317)
  [[GH-3370]](https://github.com/fatih/vim-go/pull/3370)
* Update `:GoPlay` to use `go.dev/play` instead of `play.golang.org`.
  [[GH-3331]](https://github.com/fatih/vim-go/pull/3331)
  [[GH-3348]](https://github.com/fatih/vim-go/pull/3348)
* Recurse local variables more deeply when debugging.
  [[GH-3344]](https://github.com/fatih/vim-go/pull/3344)
* Add syntax elements for `any` and `comparable` types.
  [[GH-3351]](https://github.com/fatih/vim-go/pull/3351)
* Add syntax support for go.work files.
  [[GH-3375]](https://github.com/fatih/vim-go/pull/3375)
* Show the current goroutine at the top of the list of goroutines when debugging.
  [[GH-3379]](https://github.com/fatih/vim-go/pull/3379)
* Add `:GoModReload` and autocmd events to reload go.mod when it changes on
  disk and is open in a buffer.
  [[GH-3387]](https://github.com/fatih/vim-go/pull/3387)
  [[GH-3391]](https://github.com/fatih/vim-go/pull/3391)
* Add syntax support for generics.
  [[GH-3397]](https://github.com/fatih/vim-go/pull/3397)
* Remove invalid numeric literal highlighting.
  [[GH-3404]](https://github.com/fatih/vim-go/pull/3404)

BUG FIXES:
* Handle terminating parenthesis on hexadecimal values.
  [[GH-3216]](https://github.com/fatih/vim-go/pull/3216)
* Fix applying text edits from gopls.
  [[GH-3231]](https://github.com/fatih/vim-go/pull/3231)
* Apply arguments to `:GoCoverageBrowser`.
  [[GH-3240]](https://github.com/fatih/vim-go/pull/3240)
* Fix `:GoFillStruct` when `g:go_fillstruct_mode` is `gopls`.
  [[GH-3279]](https://github.com/fatih/vim-go/pull/3279)
* Fix example in `g:go_metalinter_enabled` documentation.
  [[GH-3291]](https://github.com/fatih/vim-go/pull/3291)
* Fix changing directories in older Vims.
  [[GH-3299]](https://github.com/fatih/vim-go/pull/3299)
* Highlight the receive type when method declarations that omit the receiver
  identifier.
  [[GH-3306]](https://github.com/fatih/vim-go/pull/3306)
* Do not highlight misspellings in import paths.
  [[GH-3308]](https://github.com/fatih/vim-go/pull/3308)
  [[GH-3321]](https://github.com/fatih/vim-go/pull/3321)
* Handle shell quoting when execing.
  [[GH-3323]](https://github.com/fatih/vim-go/pull/3323)
* Do not automatically add directories from the module cache into the LSP
  workspace.
  [[GH-3343]](https://github.com/fatih/vim-go/pull/3343)
* Resolve symlinks in autocmd events.
  [[GH-3353]](https://github.com/fatih/vim-go/pull/3353)
* Fix `:GoRename` in Neovim so that it does not take 10 seconds to complete.
  [[GH-3386]](https://github.com/fatih/vim-go/pull/3386)
* Fix `:GoDebugConnect` argument handling.
  [[GH-3400]](https://github.com/fatih/vim-go/pull/3400)

## v1.25 - (April 18, 2021)

BACKWARDS INCOMPATIBILITIES:
* Remove g:go_autodetect_gopath.
  [[GH-3078]](https://github.com/fatih/vim-go/pull/3078)

IMPROVEMENTS:
* Clarify allowed values for `gopls` related configuration options.
  [[GH-3016]](https://github.com/fatih/vim-go/pull/3016)
  [[GH-3017]](https://github.com/fatih/vim-go/pull/3017)
* Add `g:go_fillstruct_mode` to allow `:GoFillStruct` to be satisfied by either
  `fillstruct` or by `gopls`.
  [[GH-3018]](https://github.com/fatih/vim-go/pull/3018)
* Add `:GoDebugTestFunc` to debug the test function surrounding the current
  cursor location.
  [[GH-3011]](https://github.com/fatih/vim-go/pull/3011)
* Implicitly add a workspace when a file from a module is opened.
  [[GH-3028]](https://github.com/fatih/vim-go/pull/3028)
* Add support for using static check as the gometalinter.
  [[GH-3036]](https://github.com/fatih/vim-go/pull/3036)
  [[GH-3133]](https://github.com/fatih/vim-go/pull/3133)
* Add `g:go_debug_mappings` to allow the debug key mappings to be customized.
  [[GH-3035]](https://github.com/fatih/vim-go/pull/3035)
  [[GH-3143]](https://github.com/fatih/vim-go/pull/3143)
* Use `gopls` as the default instead of `guru` to satisfy `:GoImplements`.
  [[GH-3034]](https://github.com/fatih/vim-go/pull/3034)
* Deprecate g:go_diagnostics_enabled` and add `g:go_diagnostics_level` to allow
  more finely grained control of the handling of diagnostics messages.
  [[GH-3050]](https://github.com/fatih/vim-go/pull/3050)
  [[GH-3052]](https://github.com/fatih/vim-go/pull/3052)
  [[GH-3119]](https://github.com/fatih/vim-go/pull/3119)
* Add support for allowing `g:go_gopls_local`  to specify different local
  imports values per workspace.
  [[GH-3053]](https://github.com/fatih/vim-go/pull/3053)
* Improve `:GoDecls` and `:GoDeclsDir` display.
  [[GH-3081]](https://github.com/fatih/vim-go/pull/3081)
* Preserve existing window layout when debugging and `g:go_debug_windows` is
  empty.
  [[GH-3068]](https://github.com/fatih/vim-go/pull/3068)
* Show identifier in fzf's preview window with `:GoDecls` and `:GoDeclsDir`.
  [[GH-3083]](https://github.com/fatih/vim-go/pull/3083)
* Use `gopls` for `:GoCallers`.
  [[GH-3088]](https://github.com/fatih/vim-go/pull/3088)
  [[GH-3090]](https://github.com/fatih/vim-go/pull/3090)
  [[GH-3141]](https://github.com/fatih/vim-go/pull/3141)
  [[GH-3142]](https://github.com/fatih/vim-go/pull/3142)
* Update denite integration to work with python3.9.
  [[GH-3097]](https://github.com/fatih/vim-go/pull/3097)
* Add syntax highlighting for go.sum files.
  [[GH-3102]](https://github.com/fatih/vim-go/pull/3102)
* Change the default from metalinter to staticcheck.
  [[GH-3126]](https://github.com/fatih/vim-go/pull/3126)
* Add `g:go_debug_preserve_layout` to prevent `:GoDebug` and friends from
  closing windows.
  [[GH-3125]](https://github.com/fatih/vim-go/pull/3125)
* Add support for `fillstruct`'s new `-tags` flag.
  [[GH-3156]](https://github.com/fatih/vim-go/pull/3156)
* Display map key and slice elements more usefully in the local vars window in
  debug mode.
  [[GH-3170]](https://github.com/fatih/vim-go/pull/3170)
* Add support for go.mod's `retract` directive.
  [[GH-3166]](https://github.com/fatih/vim-go/pull/3166)
* Do not execute disabled code actions.
  [[GH-3155]](https://github.com/fatih/vim-go/pull/3155)
* Add `:GoDebugConnect` to support connecting to an instance of delve started
  outside of vim-go.
  [[GH-3179]](https://github.com/fatih/vim-go/pull/3179)
* Use gopls to adjust imports and formatting by default.
  [[GH-2986]](https://github.com/fatih/vim-go/pull/2986)
* Set the filetype for .tmpl files to gohtmltmpl even if it's already been set.
  [[GH-3146]](https://github.com/fatih/vim-go/pull/3146)

BUG FIXES:
* Remove implications that terminal mode is only applied for Neovim.
  [[GH-3010]](https://github.com/fatih/vim-go/pull/3010)
* Correct documentation to clearly show the default value for
  `g:go_gopls_options`.
  [[GH-3019]](https://github.com/fatih/vim-go/pull/3019)
* Allow truthy values for `g:go_gopls_gofumpt`.
  [[GH-3017]](https://github.com/fatih/vim-go/pull/3017)
  [[GH-3022]](https://github.com/fatih/vim-go/pull/3022)
* Fix quickfix title for `:GoMetaLinter`.
  [[GH-3040]](https://github.com/fatih/vim-go/pull/3040)
* Change key mapping for (go-debug-halt) to F8 to resolve collision with key
  mapping for (go-debug-print).
  [[GH-3047]](https://github.com/fatih/vim-go/pull/3047)
* Handle gopls v0.5.2 addition of a prefix on the expected code actions names.
  [[GH-3077]](https://github.com/fatih/vim-go/pull/3077)
* Make sure all buffers' mappings are restored when debugging stops.
  [[GH-3048]](https://github.com/fatih/vim-go/pull/3048)
* Return early when `g:go_referrers_modes` is `gopls` and `gopls` is disabled.
  [[GH-3090]](https://github.com/fatih/vim-go/pull/3090)
* Handle yet another error format produced by golangci-lint.
  [[GH-3094]](https://github.com/fatih/vim-go/pull/3094)
* Handle additional ways that gopls can provide links for godoc.
  [[GH-3112]](https://github.com/fatih/vim-go/pull/3112)
* Remove implication that `g:go_def_reuse_buffer` only applies to split variant
  of jumping to a definition.
  [[GH-3128]](https://github.com/fatih/vim-go/pull/3128)
* Organize imports correctly when `gopls` formatting uses `gofumpt`.
  [[GH-3154]](https://github.com/fatih/vim-go/pull/3154)
* Rename all instances of an identifier when `g:go_rename_mode` is `gopls`.
  [[GH-3181]](https://github.com/fatih/vim-go/pull/3181)
  [[GH-3182]](https://github.com/fatih/vim-go/pull/3182)
* Terminate a case statement in the select snippet with a colon.
  [[GH-3185]](https://github.com/fatih/vim-go/pull/3185)
* Fix syntax highlighting in template files.
  [[GH-3188]](https://github.com/fatih/vim-go/pull/3188)
  [[GH-3189]](https://github.com/fatih/vim-go/pull/3189)

## v1.24 - (September 15, 2020)

IMPROVEMENTS:
* Clarify how `g:go_imports_autosave` and `g:go_fmt_autosave` interact.
  [[GH-2893]](https://github.com/fatih/vim-go/pull/2893)
* Document what the working directory will be for `:GoRun`.
  [[GH-2898]](https://github.com/fatih/vim-go/pull/2898)
* Add Ultisnip snippet for wrapping errors.
  [[GH-2883]](https://github.com/fatih/vim-go/pull/2883)
* Beautify the godoc pop up window border.
  [[GH-2900]](https://github.com/fatih/vim-go/pull/2900)
* Default `g:go_doc_url` to https://pkg.go.dev.
  [[GH-2884]](https://github.com/fatih/vim-go/pull/2884)
* Default `g:go_gopls_options` to `[-remote=auto]` to share gopls instances
  with other plugins and multiple instances of Vim.
  [[GH-2905]](https://github.com/fatih/vim-go/pull/2905)
* Use the module root as the working directory when renaming so that all
  references to the symbol will be renamed when in module aware mode and
  `g:go_rename_command` is set to `gopls`.
  [[GH-2917]](https://github.com/fatih/vim-go/pull/2917)
* Change `g:go_rename_command`'s default to `gopls`.
  [[GH-2922]](https://github.com/fatih/vim-go/pull/2922)
* Do not send unnecessary textDocument/didChange notifications to `gopls`.
  [[GH-2902]](https://github.com/fatih/vim-go/pull/2902)
  [[GH-2930]](https://github.com/fatih/vim-go/pull/2930)
* Stop the debugger when the process being debugged exits.
  [[GH-2921]](https://github.com/fatih/vim-go/pull/2921)
* Use the module package cache as a source of packages candidates when trying
  to complete package names.
  [[GH-2936]](https://github.com/fatih/vim-go/pull/2936)
  [[GH-2939]](https://github.com/fatih/vim-go/pull/2939)
* Allow interaction with Vim while waiting for a breakpoint to be hit while
  debugging.
  [[GH-2932]](https://github.com/fatih/vim-go/pull/2932)
* Refactor Vim signs used for debugging breakpoints to avoid id collision with
  other plugins.
  [[GH-2943]](https://github.com/fatih/vim-go/pull/2943)
* Refactor debugger's rpc response handling to be asynchronous so that Vim will
  be responsive while the program being debugged is executing.
  [[GH-2948]](https://github.com/fatih/vim-go/pull/2948)
  [[GH-2952]](https://github.com/fatih/vim-go/pull/2952)
* Warn when the debugger breaks in a file that has changed since debugging started.
  [[GH-2950]](https://github.com/fatih/vim-go/pull/2950)
* Enable `go-run` mappings that use the terminal to work with Vim in addition to Neovim.
  [[GH-2956]](https://github.com/fatih/vim-go/pull/2956)
* Use existing diagnostics for the file when the file hasn't changed and
  `g:go_metalinter_command` is `gopls`.
  [[GH-2960]](https://github.com/fatih/vim-go/pull/2960)
* Add a new option, `g:go_code_completion_icase`, to allow ignoring case when
  filtering completion results.
  [[GH-2961]](https://github.com/fatih/vim-go/pull/2961)
 * Make sure tools are not cross-compiled with `:GoInstallBinaries` and
   `:GoUpdateBinaries`.
   [[GH-2982]](https://github.com/fatih/vim-go/pull/2982)
   [[GH-2988]](https://github.com/fatih/vim-go/pull/2988)
* Add `:GoDebugHalt` to allow a program being debugged to be paused before it
  hits a breakpoint.
  [[GH-2983]](https://github.com/fatih/vim-go/pull/2983)
* Clear highlighting of the current line when after resuming when debugging.
  [[GH-2984]](https://github.com/fatih/vim-go/pull/2984)
* Add `:GoDebugAttach` to debug a running process.
  [[GH-2989]](https://github.com/fatih/vim-go/pull/2989)
* Add `g:go_term_reuse` option to allow the reuse of a terminal window.
  [[GH-2990]](https://github.com/fatih/vim-go/pull/2990)
* Add official support for using `gopls`' `gofumpt` workspace setting via
  `g:go_gopls_gofumpt`.
  [[GH-2994]](https://github.com/fatih/vim-go/pull/2994)
  [[GH-3005]](https://github.com/fatih/vim-go/pull/3005)
* Add support for using `gopls`' workspace settings that are otherwise not yet
  officially supported by vim-go.
  [[GH-2994]](https://github.com/fatih/vim-go/pull/2994)

BUG FIXES:
* Fix call to non-existent function in terminal mode edge case.
  [[GH-2895]](https://github.com/fatih/vim-go/pull/2895)
* Do not show errors when adding a text property for highlighting fails.
  [[GH-2892]](https://github.com/fatih/vim-go/pull/2892)
* Include `errcheck` in `g:go_metalinter_enabled`'s default.
  [[GH-2903]](https://github.com/fatih/vim-go/pull/2903)
* Fix display of completion selection information on command-line when
  `g:go_echo_go_info` is enabled.
  [[GH-2907]](https://github.com/fatih/vim-go/pull/2907)
* Prevent `:GoDebugBreakpoint` from causing delve to exit.
  [[GH-2908]](https://github.com/fatih/vim-go/pull/2908)
* Use the resolved directory name for `gopls`' working directory when `go.mod`
  is in a symlinked path.
  [[GH-2913]](https://github.com/fatih/vim-go/pull/2913)
* Fix buffer reuse with `:GoDef`.
  [[GH-2928]](https://github.com/fatih/vim-go/pull/2928)
* Handle breakpoints that are already set before calling `:GoDebugStart` or
  `:GoDebugTest` in some locales that cause the `sign place` output to vary.
  [[GH-2921]](https://github.com/fatih/vim-go/pull/2921)
* Handle diagnostic errors at the end of a .go file.
  [[GH-2942]](https://github.com/fatih/vim-go/pull/2942)
* Fix the `go-implements` mapping to use respect `g:go_implements_mode`.
  [[GH-2944]](https://github.com/fatih/vim-go/pull/2944)
* Handle null results from `gopls` when getting definitions or type definitions
  from virtual files.
  [[GH-2951]](https://github.com/fatih/vim-go/pull/2951)
* Fix warning when Neovim is older than v0.4.0.
  [[GH-2959]](https://github.com/fatih/vim-go/pull/2959)
* Correct documentation that referred to `g:go_imports_command` to refer to
  `g:go_imports_mode`  instead.
  [[GH-2969]](https://github.com/fatih/vim-go/pull/2969)
* Remove reference to gocode in error message when `g:go_info_mode` is set to
  an unsupported value.
  [[GH-2978]](https://github.com/fatih/vim-go/pull/2978)
* Make sure debugging commands are configured when debugging a second time
  within a single Vim session.
  [[GH-2985]](https://github.com/fatih/vim-go/pull/2985)
* Correct documentation in for `:GoModifyTags` when adding a specific tag
  value.
  [[GH-3001]](https://github.com/fatih/vim-go/pull/3001)
* Fix the path given to `gopls` when `let g:go_metalinter='gopls'` and
  `:GoMetaLinter` is called without any arguments.
  [[GH-2992]](https://github.com/fatih/vim-go/pull/2992)
* Do not override a user's configuration for `GoDebugBreakpoint` or
  `GoDebugCurrent` highlight groups.
  [[GH-2998]](https://github.com/fatih/vim-go/pull/2998)
* Apply `gopls` text edits correctly that insert solitary newlines.
  [[GH-3000]](https://github.com/fatih/vim-go/pull/3000)

## v1.23 - (May 16, 2020)

BACKWARDS INCOMPATIBILITIES:
* Remove support for gocode.
  [[GH-2686]](https://github.com/fatih/vim-go/pull/2686)
* Require at least Neovim >= 0.4.0
  [[GH-2853]](https://github.com/fatih/vim-go/pull/2853)
  [[GH-2856]](https://github.com/fatih/vim-go/pull/2856)
  [[GH-2863]](https://github.com/fatih/vim-go/pull/2863)

IMPROVEMENTS:
* Make signs for breakpoints configurable.
  [[GH-2676]](https://github.com/fatih/vim-go/pull/2676)
  [[GH-2690]](https://github.com/fatih/vim-go/pull/2690)
* Enable g:go_gopls_complete_unimported by default to stay aligned with gopls' defaults.
  [[GH-2695]](https://github.com/fatih/vim-go/pull/2695)
* Document mappings that were recently added.
  [[GH-2699]](https://github.com/fatih/vim-go/pull/2699)
* Handle null arrays better in gopls responses.
  [[GH-2703]](https://github.com/fatih/vim-go/pull/2703)
* Use `gopls` defaults by default when they're not otherwise specified in vim-go options.
  [[GH-2696]](https://github.com/fatih/vim-go/pull/2696)
* Add support for `gomodifytags --skip-unexported`
  [[GH-2660]](https://github.com/fatih/vim-go/pull/2660)
* Show problems that prevent golangci-lint from running linters.
  [[GH-2706]](https://github.com/fatih/vim-go/pull/2706)
  [[GH-2720]](https://github.com/fatih/vim-go/pull/2720)
* Support golangci-lint config file by not using `--disable-all` when
  `g:go_metalinter_enable` or `g:go_metalinter_autosave_enabled` is set to an
  empty array.
  [[GH-2655]](https://github.com/fatih/vim-go/pull/2655)
  [[GH-2715]](https://github.com/fatih/vim-go/pull/2715)
* Add support for Vim8 terminals.
  [[GH-2639]](https://github.com/fatih/vim-go/pull/2639)
  [[GH-2736]](https://github.com/fatih/vim-go/pull/2736)
* Replace `g:go_gopls_fuzzy_matching` with `g:go_gopls_matcher` in response to
  `gopls` deprecation of its `fuzzyMatching` option.
  [[GH-2728]](https://github.com/fatih/vim-go/pull/2728)
* Set statuses and progress messages consistently for code quality tools.
  [[GH-2727]](https://github.com/fatih/vim-go/pull/2727)
* Add a new supported value to `g:go_fmt_command` to format with `gopls`.
  [[GH-2729]](https://github.com/fatih/vim-go/pull/2729)
  [[GH-2752]](https://github.com/fatih/vim-go/pull/2752)
  [[GH-2852]](https://github.com/fatih/vim-go/pull/2852)
* Handle changes to `go test -v` output.
  [[GH-2743]](https://github.com/fatih/vim-go/pull/2743)
* Add `g:go_gopls_mod_tempfile` to configure `gopls`' `tempModfile`
  configuration.
  [[GH-2747]](https://github.com/fatih/vim-go/pull/2747)
* Add `g:go_gopls_options` to configure `gopls`' commandline options.
  [[GH-2747]](https://github.com/fatih/vim-go/pull/2747)
* Improve readability of gopls logs.
  [[GH-2773]](https://github.com/fatih/vim-go/pull/2773)
* Introduce `g:go_implements_mode` to allow `:GoImplements` to be satisfied
  with `gopls`.
  [[GH-2741]](https://github.com/fatih/vim-go/pull/2741)
  [[GH-2799]](https://github.com/fatih/vim-go/pull/2799)
* Introduce `g:go_imports_mode` to allow `:GoImports` to be satisfied with
  `gopls`.
  [[GH-2791]](https://github.com/fatih/vim-go/pull/2791)
  [[GH-2794]](https://github.com/fatih/vim-go/pull/2794)
  [[GH-2796]](https://github.com/fatih/vim-go/pull/2796)
  [[GH-2848]](https://github.com/fatih/vim-go/pull/2848)
* Send LSP synchronization messages to `gopls` when the file does not yet exist
  on disk as long as its directory exists.
  [[GH-2805]](https://github.com/fatih/vim-go/pull/2805)
* Run `gogetdoc` in the buffer's directory so that it will work regardless of
  the user's working directory in module-aware mode.
  [[GH-2804]](https://github.com/fatih/vim-go/pull/2804)
* Add `g:go_gopls_analyses` to support `gopls`' analyses options.
  [[GH-2820]](https://github.com/fatih/vim-go/pull/2820)
* Add `g:go_gopls_local` to support `gopls`' local option to control how third
  party imports are organized.
  [[GH-2821]](https://github.com/fatih/vim-go/pull/2821)
* Use gopls to get documentation and documentation links for identifiers under
  the cursor.
  [[GH-2822]](https://github.com/fatih/vim-go/pull/2822)
  [[GH-2839]](https://github.com/fatih/vim-go/pull/2839)
* Clarify documentation for terminal options.
  [[GH-2843]](https://github.com/fatih/vim-go/pull/2843)

BUG FIXES:
* Use the discovered full path for gopls when renaming.
  [[GH-2692]](https://github.com/fatih/vim-go/pull/2692)
* Execute commands correctly on windows when `'shell'` is not cmd.exe
  [[GH-2713]](https://github.com/fatih/vim-go/pull/2713)
  [[GH-2724]](https://github.com/fatih/vim-go/pull/2724)
* Always execute `errcheck` in the current package's directory.
  [[GH-2726]](https://github.com/fatih/vim-go/pull/2726)
* Fix errors when highlighting diagnostics after a `:GoImports`.
  [[GH-2746]](https://github.com/fatih/vim-go/pull/2746)
* Preserve errors from formatting when both formatting and metalinting happen
  on save.
  [[GH-2733]](https://github.com/fatih/vim-go/pull/2733)
  [[GH-2810]](https://github.com/fatih/vim-go/pull/2810)
* Preserve ordering of gopls messages in the log.
  [[GH-2753]](https://github.com/fatih/vim-go/pull/2753)
* Fix `:GoDef` on windows when `g:go_def_mode` is set to `gopls`.
  [[GH-2768]](https://github.com/fatih/vim-go/pull/2768)
* Handle null values from `gopls`.
  [[GH-2778]](https://github.com/fatih/vim-go/pull/2778)
* Preserve diagnostics highlights after formatting.
  [[GH-2779]](https://github.com/fatih/vim-go/pull/2779)
* Fix the decoding and encoding of multi-byte file paths received from and sent
  to `gopls`.
  [[GH-2784]](https://github.com/fatih/vim-go/pull/2784)
* Fix `:GoRun` so that it works as expected when the current working directory
  is neither in GOPATH nor within a module.
  [[GH-2782]](https://github.com/fatih/vim-go/pull/2782)
  [[GH-2818]](https://github.com/fatih/vim-go/pull/2818)
  [[GH-2842]](https://github.com/fatih/vim-go/pull/2842)
* Use absolute file paths for `:GoRun`'s arguments in terminal mode.
  [[GH-2844]](https://github.com/fatih/vim-go/pull/2844)
* Show the command executed by `:GoRun` when `g:go_debug` includes `'shell-commands'`.
  [[GH-2785]](https://github.com/fatih/vim-go/pull/2785)
  [[GH-2817]](https://github.com/fatih/vim-go/pull/2817)
* Clear the list for formatting errors when `g:go_fmt_command` is `gopls`.
  [[GH-2790]](https://github.com/fatih/vim-go/pull/2790)
* Handle text edits from gopls that are only line insertions.
  [[GH-2802]](https://github.com/fatih/vim-go/pull/2802)
  [[GH-2803]](https://github.com/fatih/vim-go/pull/2803)
* Add `g:go_imports_autosave` so that imports can be adjusted on save when
  `g:go_imports_mode` is set to `gopls`.
  [[GH-2800]](https://github.com/fatih/vim-go/pull/2800)
  [[GH-2858]](https://github.com/fatih/vim-go/pull/2858)
* Correct vim-go's help to correctly identify `g:go_referrer_mode`'s default.
  [[GH-2832]](https://github.com/fatih/vim-go/pull/2832)
* Clear the quickfix list when `:GoLint` succeeds.
  [[GH-2833]](https://github.com/fatih/vim-go/pull/2833)
* Respect arguments to `:GoDocBrowser`.
  [[GH-2822]](https://github.com/fatih/vim-go/pull/2822)
* Use the correct path to documentation for struct fields with `:GoDocBrowser`.
  [[GH-2822]](https://github.com/fatih/vim-go/pull/2822)
* Do not try parsing errors from terminal jobs when the working directory has
  been removed.
  [[GH-2824]](https://github.com/fatih/vim-go/pull/2824)
* Document that `g:go_jump_to_error` apples to running the metalinter on save,
  too.
  [[GH-2854]](https://github.com/fatih/vim-go/pull/2854)
* Ignore commented out import statements when executing `:GoImport`.
  [[GH-2862]](https://github.com/fatih/vim-go/pull/2862)
* Interpret file paths in `go vet` errors relative to the current buffer's
  directory.
  [[GH-2882]](https://github.com/fatih/vim-go/pull/2882)

## v1.22 - (January 30, 2020)

BACKWARDS INCOMPATIBILITIES:
* Drop support for Vim 7.4. The minimum required version of Vim is now 8.0.1453.
  [[GH-2495]](https://github.com/fatih/vim-go/pull/2495)
  [[GH-2497]](https://github.com/fatih/vim-go/pull/2497)
* Drop support for `gometalinter`
  [[GH-2494]](https://github.com/fatih/vim-go/pull/2494)

IMPROVEMENTS:
* Highlight the `go` keyword in go.mod files.
  [[GH-2473]](https://github.com/fatih/vim-go/pull/2473)
* Use echo functions consistently.
  [[GH-2458]](https://github.com/fatih/vim-go/pull/2458)
* Add support for managing goroutines in debugger.
  [[GH-2463]](https://github.com/fatih/vim-go/pull/2463)
  [[GH-2527]](https://github.com/fatih/vim-go/pull/2527)
* Document `g:go_doc_popup_window`.
  [[GH-2506]](https://github.com/fatih/vim-go/pull/2506)
* Make `g:go_doc_popup_window=1` work for Neovim, too.
  [[GH-2451]](https://github.com/fatih/vim-go/pull/2451)
  [[GH-2512]](https://github.com/fatih/vim-go/pull/2512)
* Handle errors jumping to a definition in a file open in another Vim process
  better.
  [[GH-2518]](https://github.com/fatih/vim-go/pull/2518)
* Improve the UX when the gopls binary is missing.
  [[GH-2522]](https://github.com/fatih/vim-go/pull/2522)
* Use gopls instead of guru for `:GoSameIds`.
  [[GH-2519]](https://github.com/fatih/vim-go/pull/2519)
* Use gopls instead of guru for `:GoReferrers`.
  [[GH-2535]](https://github.com/fatih/vim-go/pull/2535)
* Update documentation for `g:go_addtags_transform`.
  [[GH-2541]](https://github.com/fatih/vim-go/pull/2541)
* Install most helper tools in module aware mode.
  [[GH-2545]](https://github.com/fatih/vim-go/pull/2545)
* Add a new option, `g:go_referrers_mode` to allow the user to choose whether
  to use gopls or guru for finding references.
  [[GH-2566]](https://github.com/fatih/vim-go/pull/2566)
* Add options to control how gopls responds to completion requests.
  [[GH-2567]](https://github.com/fatih/vim-go/pull/2567)
  [[GH-2568]](https://github.com/fatih/vim-go/pull/2568)
* Add syntax highlighting for binary literals.
  [[GH-2557]](https://github.com/fatih/vim-go/pull/2557)
* Improve highlighting of invalid numeric literals.
  [[GH-2571]](https://github.com/fatih/vim-go/pull/2571)
  [[GH-2587]](https://github.com/fatih/vim-go/pull/2587)
  [[GH-2589]](https://github.com/fatih/vim-go/pull/2589)
  [[GH-2584]](https://github.com/fatih/vim-go/pull/2584)
  [[GH-2597]](https://github.com/fatih/vim-go/pull/2597)
  [[GH-2599]](https://github.com/fatih/vim-go/pull/2599)
* Add highlighting of sections reported by gopls diagnostics' errors
  and warnings.
  [[GH-2569]](https://github.com/fatih/vim-go/pull/2569)
  [[GH-2643]](https://github.com/fatih/vim-go/pull/2643)
* Make the highlighting of fzf decls configurable.
  [[GH-2572]](https://github.com/fatih/vim-go/pull/2572)
  [[GH-2579]](https://github.com/fatih/vim-go/pull/2579)
* Support renaming with gopls.
  [[GH-2577]](https://github.com/fatih/vim-go/pull/2577)
  [[GH-2618]](https://github.com/fatih/vim-go/pull/2618)
* Add an option, `g:go_gopls_enabled`, to allow gopls integration to be
  disabled.
  [[GH-2605]](https://github.com/fatih/vim-go/pull/2605)
  [[GH-2609]](https://github.com/fatih/vim-go/pull/2609)
  [[GH-2638]](https://github.com/fatih/vim-go/pull/2638)
  [[GH-2640]](https://github.com/fatih/vim-go/pull/2640)
* Add a buffer level option, `b:go_fmt_options`, to control formatting options
  per buffer.
  [[GH-2613]](https://github.com/fatih/vim-go/pull/2613)
* Use build tags when running `:GoVet`.
  [[GH-2615]](https://github.com/fatih/vim-go/pull/2615)
* Add new snippets for UltiSnips.
  [[GH-2623]](https://github.com/fatih/vim-go/pull/2623)
  [[GH-2627]](https://github.com/fatih/vim-go/pull/2627)
* Expand completions as snippets when `g:go_gopls_use_placeholders` is set.
  [[GH-2624]](https://github.com/fatih/vim-go/pull/2624)
* Add a new function, `:GoDiagnostics` and an associated mapping for seeing
  `gopls` diagnostics. Because of the performance implications on large
  projects, `g:go_diagnostics_enabled` controls whether all diagnostics are
  processed or only the diagnostics for the current buffer.
  [[GH-2612]](https://github.com/fatih/vim-go/pull/2612)
* Explain how to find and detect multiple copies of vim-go in the FAQ.
  [[GH-2632]](https://github.com/fatih/vim-go/pull/2632)
* Update the issue template to ask for the gopls version and
  `:GoReportGitHubIssue` to provide it.
  [[GH-2630]](https://github.com/fatih/vim-go/pull/2630)
* Use text properties when possible for some highlighting cases.
  [[GH-2652]](https://github.com/fatih/vim-go/pull/2652)
  [[GH-2662]](https://github.com/fatih/vim-go/pull/2662)
  [[GH-2663]](https://github.com/fatih/vim-go/pull/2663)
  [[GH-2672]](https://github.com/fatih/vim-go/pull/2672)
  [[GH-2678]](https://github.com/fatih/vim-go/pull/2678)


BUG FIXES:
* Fix removal of missing directories from gopls workspaces.
  [[GH-2507]](https://github.com/fatih/vim-go/pull/2507)
* Change to original window before trying to change directories when term job
  ends.
  [[GH-2508]](https://github.com/fatih/vim-go/pull/2508)
* Swallow errors when the hover info cannot be determined.
  [[GH-2515]](https://github.com/fatih/vim-go/pull/2515)
* Fix errors when trying to debug lsp and hover.
  [[GH-2516]](https://github.com/fatih/vim-go/pull/2516)
* Reset environment variables on Vim <= 8.0.1831 .
  [[GH-2523]](https://github.com/fatih/vim-go/pull/2523)
* Handle empty results from delve.
  [[GH-2526]](https://github.com/fatih/vim-go/pull/2526)
* Do not overwrite `updatetime` when `g:go_auto_sameids` or
  `g:go_auto_type_info` is set.
  [[GH-2529]](https://github.com/fatih/vim-go/pull/2529)
* Fix example for `g:go_debug_log_output` in docs.
  [[GH-2547]](https://github.com/fatih/vim-go/pull/2547)
* Use FileChangedShellPost instead of FileChangedShell so that reload messages
  are not hidden.
  [[GH-2549]](https://github.com/fatih/vim-go/pull/2549)
* Restore cwd after `:GoTest` when `g:go_term_enabled` is set.
  [[GH-2556]](https://github.com/fatih/vim-go/pull/2556)
* Expand struct variable correctly in the variables debug window.
  [[GH-2574]](https://github.com/fatih/vim-go/pull/2574)
* Show output from errcheck when there are failures other than problems it can
  report.
  [[GH-2667]](https://github.com/fatih/vim-go/pull/2667)

## v1.21 - (September 11, 2019)

BACKWARDS INCOMPATIBILITIES:
* `g:go_metalinter_disabled` has been removed.
  [[GH-2375]](https://github.com/fatih/vim-go/pull/2375)

IMPROVEMENTS:
* Add a new option, `g:go_code_completion_enabled`, to control whether omnifunc
  is set.
  [[GH-2229]](https://github.com/fatih/vim-go/pull/2229)
* Use build tags with golangci-lint.
  [[GH-2261]](https://github.com/fatih/vim-go/pull/2261)
* Allow debugging of packages outside of GOPATH without a go.mod file.
  [[GH-2269]](https://github.com/fatih/vim-go/pull/2269)
* Show which example failed when Example tests fail
  [[GH-2277]](https://github.com/fatih/vim-go/pull/2277)
* Show function signature and return types in preview window when autocompleting functions and methods.
  [[GH-2289]](https://github.com/fatih/vim-go/pull/2289)
* Improve the user experience when using null modules.
  [[GH-2300]](https://github.com/fatih/vim-go/pull/2300)
* Modify `:GoReportGitHubIssue` to include vim-go configuration values
  [[GH-2323]](https://github.com/fatih/vim-go/pull/2323)
* Respect `g:go_info_mode='gopls'` in go#complete#GetInfo.
  [[GH-2313]](https://github.com/fatih/vim-go/pull/2313)
* Allow `:GoLint`, `:GoErrCheck`, and `:GoDebug` to work in null modules.
  [[GH-2335]](https://github.com/fatih/vim-go/pull/2335)
* Change default value for `g:go_info_mode` and `g:go_def_mode` to `'gopls'`.
  [[GH-2329]](https://github.com/fatih/vim-go/pull/2329)
* Add a new option, `g:go_doc_popup_window` to optionally use a popup window
  for godoc in Vim 8.1.1513 and later.
  [[GH-2347]](https://github.com/fatih/vim-go/pull/2347)
* Add `:GoAddWorkspace` function to support multiple workspaces with gopls.
  [[GH-2356]](https://github.com/fatih/vim-go/pull/2356)
* Install gopls from its stable package.
  [[GH-2360]](https://github.com/fatih/vim-go/pull/2360)
* Disambiguate progress message when initializing gopls.
  [[GH-2369]](https://github.com/fatih/vim-go/pull/2369)
* Calculate LSP position correctly when on a line that contains multi-byte
  characters before the position.
  [[GH-2389]](https://github.com/fatih/vim-go/pull/2389)
* Calculate Vim position correctly from LSP text position.
  [[GH-2395]](https://github.com/fatih/vim-go/pull/2395)
* Use the statusline to display gopls initialization status messages and only
  echo the statuses when `g:go_echo_command_info` is set.
  [[GH-2422]](https://github.com/fatih/vim-go/pull/2422)
* Send configuration to gopls so that build tags will be considered and hover
  content won't have documentation.
  [[GH-2429]](https://github.com/fatih/vim-go/pull/2429)
* Add a new option, `g:go_term_close_on_exit`, to control whether jobs run in a
  terminal window will close the terminal window when the job exits.
  [[GH-2409]](https://github.com/fatih/vim-go/pull/2409)
* Allow `g:go_template_file` and `g:go_template_test_files` to reside outside
  of vim-go's template directory.
  [[GH-2434]](https://github.com/fatih/vim-go/pull/2434)
* Add a new command, `:GoLSPDebugBrowser`, to open a browser to gopls debugging
  view.
  [[GH-2436]](https://github.com/fatih/vim-go/pull/2436)
* Restart gopls automatically when it is updated via `:GoUpdateBinaries`.
  [[GH-2453]](https://github.com/fatih/vim-go/pull/2453)
* Reset `'more'` while installing binaries to avoid unnecessary more prompts.
  [[GH-2457]](https://github.com/fatih/vim-go/pull/2457)
* Highlight `%w` as a format specifier (for Go 1.13).
  [[GH-2433]](https://github.com/fatih/vim-go/pull/2433)
* Handle changes to Go 1.13's go vet output that gometalinter isn't expecting.
  [[GH-2475]](https://github.com/fatih/vim-go/pull/2475)
* Make `golangci-lint` the default value for `g:go_metalinter_command`.
  [[GH-2478]](https://github.com/fatih/vim-go/pull/2478)
* Parse compiler errors from Go 1.13 `go vet` correctly.
  [[GH-2485]](https://github.com/fatih/vim-go/pull/2485)

BUG FIXES:
* display info about function and function types whose parameters are
  `interface{}` without truncating the function signature.
  [[GH-2244]](https://github.com/fatih/vim-go/pull/2244)
* install tools that require GOPATH mode when in module mode.
  [[GH-2253]](https://github.com/fatih/vim-go/pull/2253)
* Detect GOPATH when starting `gopls`
  [[GH-2255]](https://github.com/fatih/vim-go/pull/2255)
* Handle `gopls` responses in the same window from which the respective request
  originated.
  [[GH-2266]](https://github.com/fatih/vim-go/pull/2266)
* Show completion matches from gocode.
  [[GH-2267]](https://github.com/fatih/vim-go/pull/2267)
* Show the completion preview window.
  [[GH-2268]](https://github.com/fatih/vim-go/pull/2268)
* Set the anchor for method documentation correctly.
  [[GH-2276]](https://github.com/fatih/vim-go/pull/2276)
* Respect the LSP information for determining where candidate matches start.
  [[GH-2291]](https://github.com/fatih/vim-go/pull/2291)
* Restore environment variables with backslashes correctly.
  [[GH-2292]](https://github.com/fatih/vim-go/pull/2292)
* Modify handling of gopls output for `:GoInfo` to ensure the value will be
  displayed.
  [[GH-2311]](https://github.com/fatih/vim-go/pull/2311)
* Run `:GoLint` successfully in null modules.
  [[GH-2318]](https://github.com/fatih/vim-go/pull/2318)
* Ensure actions on save work in new buffers that have not yet been persisted to disk.
  [[GH-2319]](https://github.com/fatih/vim-go/pull/2319)
* Restore population of information in `:GoReportGitHubIssue`.
  [[GH-2312]](https://github.com/fatih/vim-go/pull/2312)
* Do not jump back to the originating window when jumping to definitions with
  `g:go_def_mode='gopls'`.
  [[GH-2327]](https://github.com/fatih/vim-go/pull/2327)
* Fix getting information about a valid identifier for which gopls returns no
  information (e.g. calling `:GoInfo` on a package identifier).
  [[GH-2339]](https://github.com/fatih/vim-go/pull/2339)
* Fix tab completion of package names on the cmdline in null modules.
  [[GH-2342]](https://github.com/fatih/vim-go/pull/2342)
* Display identifier info correctly when the identifier has no godoc.
  [[GH-2373]](https://github.com/fatih/vim-go/pull/2373)
* Fix false positives when saving a buffer and `g:go_metalinter_command` is
  `golangci-lint`.
  [[GH-2367]](https://github.com/fatih/vim-go/pull/2367)
* Fix `:GoDebugRestart`.
  [[GH-2390]](https://github.com/fatih/vim-go/pull/2390)
* Do not execute tests twice in terminal mode.
  [[GH-2397]](https://github.com/fatih/vim-go/pull/2397)
* Do not open a new buffer in Neovim when there are compilation errors and
  terminal mode is enabled.
  [[GH-2401]](https://github.com/fatih/vim-go/pull/2401)
* Fix error due to typo in implementation of `:GoAddWorkspace`.
  [[GH-2415]](https://github.com/fatih/vim-go/pull/2401)
* Do not format the file automatically when `g:go_format_autosave` is set and
  the file being written is not the current file.
  [[GH-2442]](https://github.com/fatih/vim-go/pull/2442)
* Fix `go-debug-stepout` mapping.
  [[GH-2464]](https://github.com/fatih/vim-go/pull/2464)
* Handle paths with spaces correctly when executing jobs.
  [[GH-2472]](https://github.com/fatih/vim-go/pull/2472)
* Remove a space in the default value for `g:go_debug_log_output`, so that
  Delve will start on Windows.
  [[GH-2480]](https://github.com/fatih/vim-go/pull/2480)

## 1.20 - (April 22, 2019)

FEATURES:
* ***gopls support!***
  * use gopls for autocompletion by default in Vim8 and Neovim.
  * use gopls for `:GoDef` by setting `g:go_def_mode='gopls'`.
  * use gopls for `:GoInfo` by setting `g:go_info_mode='gopls'`.
* Add support for golangci-lint.
  * set `g:go_metalinter_command='golangci-lint'` to use golangci-lint instead
    of gometalinter.
* New `:GoDefType` command to jump to a type definition from an instance of the
  type.

BACKWARDS INCOMPATIBILITIES:
* `g:go_highlight_function_arguments` is renamed to `g:go_highlight_function_parameters`
  [[GH-2117]](https://github.com/fatih/vim-go/pull/2117)

IMPROVEMENTS:
* Disable `g:go_gocode_propose_source` by default.
  [[GH-2050]](https://github.com/fatih/vim-go/pull/2050)
* Don't spam users when Vim is run with vi compatibility.
  [[GH-2055]](https://github.com/fatih/vim-go/pull/2055)
* Add bang support to lint commands to allow them to be run without jumping to
  errors.
  [[GH-2056]](https://github.com/fatih/vim-go/pull/2056)
* Use `go doc` for `:GoDoc` instead of `godoc`.
  [[GH-2070]](https://github.com/fatih/vim-go/pull/2070)
* Detach from and shutdown dlv correctly.
  [[GH-2075]](https://github.com/fatih/vim-go/pull/2075)
* Do not require `'autowrite'` or `'autowriteall'` to be set when using
  autocompletion in module mode.
  [[GH-2091]](https://github.com/fatih/vim-go/pull/2091)
* Fix use of `g:go_metalinter_command` _and_ apply it even when autosaving.
  [[GH-2101]](https://github.com/fatih/vim-go/pull/2101)
* Report errors in quickfix when Delve fails to start (e.g. compiler errors).
  [[GH-2111]](https://github.com/fatih/vim-go/pull/2111)
* Support `'undo_ftplugin'`, make most autocmds buffer-local, and only do the
  bare minimum based on file names alone.
  [[GH-2108]](https://github.com/fatih/vim-go/pull/2108)
* Write a message when `:GoInfo` can't display any results when `g:go_info_mode='gocode'`.
  [[GH-2122]](https://github.com/fatih/vim-go/pull/2122)
* Highlight fields followed by an operator when `g:go_highlight_fields` is set.
  [[GH-1907]](https://github.com/fatih/vim-go/pull/1907)
* Skip autosave actions when the buffer is not a readable file.
  [[GH-2143]](https://github.com/fatih/vim-go/pull/2143)
* Run `godef` from the current buffer's directory to make sure it works with modules.
  [[GH-2150]](https://github.com/fatih/vim-go/pull/2150)
* Add a function, `go#tool#DescribeBalloon`, to show information in a balloon
  with `'balloonexpr'`. (Vim8 only).
  [[GH-1975]](https://github.com/fatih/vim-go/pull/1975)
* Add initial support for `gopls`.
  [[GH-2163]](https://github.com/fatih/vim-go/pull/2163).
* Add `:GoDefType` to jump to the type definition of the identifier under the
  cursor.
  [[GH-2165]](https://github.com/fatih/vim-go/pull/2165)
* Notify gopls about changes.
  [[GH-2171]](https://github.com/fatih/vim-go/pull/2171)
* Respect `g:go_jump_to_error` when running `gometalinter` automatically on
  save.  [[GH-2176]](https://github.com/fatih/vim-go/pull/2176)
* Use gopls for code completion by default in Vim8 and Neovim.
  [[GH-2172]](https://github.com/fatih/vim-go/pull/2172)
* Add support for golangci-lint.
  [[GH-2182]](https://github.com/fatih/vim-go/pull/2182)
* Show hover balloon using gopls instead of gocode.
  [[GH-2202]](https://github.com/fatih/vim-go/pull/2202)
* Add a new option, `g:go_debug_log_output`, to control logging with the
  debugger.
  [[GH-2203]](https://github.com/fatih/vim-go/pull/2203)
* Do not jump to quickfix or location list window when bang is used for async
  jobs or linting.
  [[GH-2205]](https://github.com/fatih/vim-go/pull/2205)
* Tab complete package names for commands from vendor directories and in
  modules.
  [[GH-2213]](https://github.com/fatih/vim-go/pull/2213)
* Add support for `gopls` to `g:go_info_mode`.
  [[GH-2224]](https://github.com/fatih/vim-go/pull/2224)

BUG FIXES:
* Fix opening of non-existent file from `:GoDeclsDir` when the current
  directory is not the directory containing the current buffer.
  [[GH-2048]](https://github.com/fatih/vim-go/pull/2048)
* Fix jumping to an identifier with godef from a modified buffer.
  [[GH-2054]](https://github.com/fatih/vim-go/pull/2054)
* Fix errors when `g:go_debug` contains `debugger-commands`.
  [[GH-2075]](https://github.com/fatih/vim-go/pull/2075)
* Fix errors from `:GoDebugStop` in Neovim.
  [[GH-2075]](https://github.com/fatih/vim-go/pull/2075)
* Fix `:GoSameIdsToggle`.
  [[GH-2086]](https://github.com/fatih/vim-go/pull/2086)
* Do not set fileencoding or fileformat options or populate from template when
  the buffer is not modifiable.
  [[GH-2097]](https://github.com/fatih/vim-go/pull/2097)
* Do not clear buffer-local autocmds of other buffers. 
  [[GH-2109]](https://github.com/fatih/vim-go/pull/2109)
* Highlight return parameter types when g:go_highlight_function_arguments is
  set.  [[GH-2116]](https://github.com/fatih/vim-go/pull/2116)
* Fix lockup in Neovim when trying to run `:GoDebugTest` when there are no
  tests.  [[GH-2125]](https://github.com/fatih/vim-go/pull/2125)
* Keep track of breakpoints correctly when buffer is edited after breakpoints
  are set.
  [[GH-2126]](https://github.com/fatih/vim-go/pull/2126)
* Fix race conditions in `:GoDebugStop`.
  [[GH-2127]](https://github.com/fatih/vim-go/pull/2127)
* Fix jumping to module or package using godef.
  [[GH-2141]](https://github.com/fatih/vim-go/pull/2141)
* Fix errors caused by redefining functions within functions.
  [[GH-2189]](https://github.com/fatih/vim-go/pull/2189)
* Highlight pre-release and metadata in versions in go.mod.
  [[GH-2192]](https://github.com/fatih/vim-go/pull/2192)
* Handle runtime panics from `:GoRun` when using Neovim's terminal.
  [[GH-2209]](https://github.com/fatih/vim-go/pull/2209)
* Fix adding tag option when a tag is added.
  [[GH-2227]](https://github.com/fatih/vim-go/pull/2227)

## 1.19 - (November 4, 2018)

FEATURES:

* **go.mod file support!** This is the first feature for upcoming Go modules
  support. The followings are added:
  * Syntax highlighting for the `go.mod` file. 
  * A new `gomod` filetype is set if a `go.mod` file has been opened and starts
    with the line `module `
  * New **:GoModFmt** command that formats the `go.mod` file
  * Auto format on save feature for `:GoModFmt`, enabled automatically. Can be
    toggled of with the setting `g:go_mod_fmt_autosave` or with the command:
    `GoModFmtAutoSaveToggle`
    [[GH-1931]](https://github.com/fatih/vim-go/pull/1931)

IMPROVEMENTS:
* Unify async job handling for Vim8 and Neovim.
  [[GH-1864]](https://github.com/fatih/vim-go/pull/1864)
* Document Vim and Neovim requirements in README.md and help file.
  [[GH-1889]](https://github.com/fatih/vim-go/pull/1889)
* Highlight `context.Context` when `g:go_highlight_extra_types` is set.
  [[GH-1903]](https://github.com/fatih/vim-go/pull/1903)
* Run gometalinter asynchronously in Neovim.
  [[GH-1901]](https://github.com/fatih/vim-go/pull/1901)
* Run gorename asynchronously in Vim8 and Neovim.
  [[GH-1894]](https://github.com/fatih/vim-go/pull/1894)
* Install keyify from its canonical import path.
  [[GH-1924]](https://github.com/fatih/vim-go/pull/1924)
* Update the tested version of Neovim to v0.3.1.
  [[GH-1923]](https://github.com/fatih/vim-go/pull/1923)
* Run autocompletion asynchronously in Vim8 and Neovim.
  [[GH-1926]](https://github.com/fatih/vim-go/pull/1926)
* Show statusline update when running `:GoInfo` with `g:go_info_mode='gocode'`.
  [[GH-1937]](https://github.com/fatih/vim-go/pull/1937)
* Do not update statusline when highlighting sameids or showing type info via
  an autocmd.
  [[GH-1937]](https://github.com/fatih/vim-go/pull/1937)
* Do not indent within a raw string literal.
  [[GH-1858]](https://github.com/fatih/vim-go/pull/1858)
* Highlight Go's predeclared function identifiers (the functions in `builtins`)
  using keyword groups and highlight them using the `Identifiers` group.
  [[GH-1939]](https://github.com/fatih/vim-go/pull/1939)
* Add a new FAQ entry to instruct users how to modify the vim-go highlight
  groups.
  [[GH-1939]](https://github.com/fatih/vim-go/pull/1939)
* Improve use of statusline and progress messages.
  [[GH-1948]](https://github.com/fatih/vim-go/pull/1948)
* Add `tt` snippet to create a table test boilerplate (see
  https://github.com/golang/go/wiki/TableDrivenTests for more information on
  how to use a table driven test).
  [[GH-1956]](https://github.com/fatih/vim-go/pull/1956)
* Add `<Plug>(go-decls)` and `<Plug>(go-decls-dir)` mappings.
  [[GH-1964]](https://github.com/fatih/vim-go/pull/1964)
* Handle go1.11 test output.
  [[GH-1978]](https://github.com/fatih/vim-go/pull/1978)
* Internal: install tools by their custom names
  [[GH-1984]](https://github.com/fatih/vim-go/pull/1984)
* Support the go-debugger features in Neovim.
  [[GH-2007]](https://github.com/fatih/vim-go/pull/2007)
* color the statusline for termguicolors and Neovim.
  [[GH-2014]](https://github.com/fatih/vim-go/pull/2014)
* add an option to disable highlighting of breakpoints and the current line
  when debugging.
  [[GH-2025]](https://github.com/fatih/vim-go/pull/2025)
* Update autocompletion to work with Go modules.
  [[GH-1988]](https://github.com/fatih/vim-go/pull/1988)
* Add an option to search $GOPATH/bin or $GOBIN _after_ $PATH.
  [[GH-2041]](https://github.com/fatih/vim-go/pull/2041)

BUG FIXES:
* Fix `:GoRun %` on Windows.
  [[GH-1900]](https://github.com/fatih/vim-go/pull/1900)
* Fix `go#complete#GetInfo()` to return a description of the identifier.
  [[GH-1905]](https://github.com/fatih/vim-go/pull/1905)
* Restore support for running tests in the Neovim terminal.
  [[GH-1895]](https://github.com/fatih/vim-go/pull/1895)
* Fix `:GoInfo` when `g:go_info_mode` is `gocode`
  [[GH-1915]](https://github.com/fatih/vim-go/pull/1915)
* Fix highlighting of pointer type in var blocks.
  [[GH-1794]](https://github.com/fatih/vim-go/pull/1794)
* Fix `:GoImport` when adding to an empty import block (i.e`import ()`)
  [[GH-1938]](https://github.com/fatih/vim-go/pull/1938)
* Run shell commands with shellcmdflag set to `-c`.
  [[GH-2006]](https://github.com/fatih/vim-go/pull/2006)
* Use the correct log output option for delve.
  [[GH-1992]](https://github.com/fatih/vim-go/pull/1992)
* Pass empty arguments correctly in async jobs on Windows.
  [[GH-2011]](https://github.com/fatih/vim-go/pull/2011)
* Don't close godoc scratch window when using arrow keys.
  [[GH-2021]](https://github.com/fatih/vim-go/pull/2021)

BACKWARDS INCOMPATIBILITIES:
* Bump minimum required version of Vim to 7.4.2009.
  [[GH-1899]](https://github.com/fatih/vim-go/pull/1899)
* Switch gocode to github.com/mdempsky/gocode. Several gocode options have been
  removed and a new one has been added.
  [[GH-1853]](https://github.com/fatih/vim-go/pull/1853)

## 1.18 - (July 18, 2018)

FEATURES:

* Add **:GoIfErr** command together with the `<Plug>(go-iferr)` plug key to
  create a custom mapping. This command generates an `if err != nil { return ...  }` 
  automatically which infer the type of return values and the numbers.
  For example:

  ```
  func doSomething() (string, error) {
      f, err := os.Open("file")
  }
  ```
 
  Becomes:

  ```
  func doSomething() (string, error) {
      f, err := os.Open("file")
      if err != nil {
          return "", err
      }
  }
  ```

* Two new text objects has been added: 
  * `ic` (inner comment) selects the content of the comment, excluding the start/end markers (i.e: `//`, `/*`)
  * `ac` (a comment) selects the content of the whole commment block, including markers
  To use this new feature, make sure you use use the latest version of
  [motion](https://github.com/fatih/motion). You can update the tool from Vim
  via `:GoUpdateBinaries`
  [[GH-1779]](https://github.com/fatih/vim-go/pull/1779)
* Add `:GoPointsTo` to show all variables to which the pointer under the cursor
  may point to.
  [[GH-1751]](https://github.com/fatih/vim-go/pull/1751)
* Add `:GoReportGitHubIssue` to initialize a new GitHub issue with as much data
  that our template requests as possible.
  [[GH-1738]](https://github.com/fatih/vim-go/pull/1738)

IMPROVEMENTS:

* Add build tags (with `g:go_build_tags`) to all commands that support it.
  [[GH-1705]](https://github.com/fatih/vim-go/pull/1705)
* Some command which operate on files (rather than Vim buffers) will now show a
  warning if there are unsaved buffers, similar to Vim's `:make`.
  [[GH-1754]](https://github.com/fatih/vim-go/pull/1754)
* Don't return an error from `:GoGuru` functions when the import path is
  unknown and scope is unneeded.
  [[GH-1826]](https://github.com/fatih/vim-go/pull/1826)
* Performance improvements for the `go.vim` syntax file.
  [[GH-1799]](https://github.com/fatih/vim-go/pull/1799)
* Allow `GoDebugBreakpoint` and `GoDebugCurrent` highlight groups to be
  overridden by user configuration.
  [[GH-1850]](https://github.com/vim-go/pull/1850)
* Strip trailing carriage returns from quickfix errors that are parsed
  manually. [[GH-1861]](https://github.com/fatih/vim-go/pull/1861).
* Cleanup title of terminal window.
  [[GH-1861]](https://github.com/fatih/vim-go/pull/1861).
* Add `:GoImpl` is able to complete interfaces by their full import path in
  addition to the current package name (i.e: `:GoImpl t *T github.com/BurntSushi/toml.Unmarshaller` 
  is now possible)
  [[GH-1884]](https://github.com/fatih/vim-go/pull/1884)

BUG FIXES:

* Update the correct window's location list after a long running async job
  completes, even when the user changes their window layout while the job is
  running.
  [[GH-1734]](https://github.com/fatih/vim-go/pull/1734)
* Apply debugger mappings only for Go buffers, and not all buffers.
  [[GH-1696]](https://github.com/fatih/vim-go/pull/1696)
* The `gohtmltmpl` filetype will now highlight `{{ .. }}` syntax HTML attributes
  and some other locations.
  [[GH-1790]](https://github.com/fatih/vim-go/pull/1790)
* Use the correct logging flag argument for delve.
  [[GH-1809]](https://github.com/fatih/vim-go/pull/1809)
* Fix gocode option string values that would cause gocode settings not to set
  correctly
  [[GH-1818]](https://github.com/fatih/vim-go/pull/1818)
* Fix Neovim handling of guru output.
  [[GH-1846]](https://github.com/fatih/vim-go/pull/1846)
* Execute commands correctly when they are in $GOBIN but not $PATH.
  [[GH-1866]](https://github.com/fatih/vim-go/pull/1866)
* Open files correctly with ctrlp.
  [[GH-1878]](https://github.com/fatih/vim-go/pull/1878)
* Fix checking guru binary path 
  [[GH-1886]](https://github.com/fatih/vim-go/pull/1886)
* Add build tags to `:GoDef` if only it's present 
  [[GH-1882]](https://github.com/fatih/vim-go/pull/1882)

## 1.17 - (March 27, 2018)

FEATURES:

* **Debugger support!** Add integrated support for the
  [`delve`](https://github.com/go-delve/delve) debugger. Use
  `:GoInstallBinaries` to install `dlv`, and see `:help go-debug` to get
  started.
  [[GH-1390]](https://github.com/fatih/vim-go/pull/1390)

IMPROVEMENTS:

* Add descriptions to neosnippet abbrevations.
  [[GH-1639]](https://github.com/fatih/vim-go/pull/1639)
* Show messages in the location list instead of the quickfix list when
  `gometalinter` is run automatically when saving a buffer. Whether the
  location list or quickfix list is used can be customized in the usual ways.
  [[GH-1652]](https://github.com/fatih/vim-go/pull/1652)
* Redraw the screen before executing blocking calls to gocode.
  [[GH-1671]](https://github.com/fatih/vim-go/pull/1671)
* Add `fe` -> `fmt.Errorf()` snippet for NeoSnippet and UltiSnippets.
  [[GH-1677]](https://github.com/fatih/vim-go/pull/1677)
* Use the async api when calling guru from neovim.
  [[GH-1678]](https://github.com/fatih/vim-go/pull/1678)
* Use the async api when calling gocode to get type info.
  [[GH-1697]](https://github.com/fatih/vim-go/pull/1697)
* Cache import path lookups to improve responsiveness.
  [[GH-1713]](https://github.com/fatih/vim-go/pull/1713)

BUG FIXES:

* Create quickfix list correctly when tests timeout.
  [[GH-1633]](https://github.com/fatih/vim-go/pull/1633)
* Apply `g:go_test_timeout` when running `:GoTestFunc`.
  [[GH-1631]](https://github.com/fatih/vim-go/pull/1631)
* The user's configured `g:go_doc_url` variable wasn't working correctly in the
  case when the "gogetdoc" command isn't installed.
  [[GH-1629]](https://github.com/fatih/vim-go/pull/1629)
* Highlight format specifiers with an index (e.g. `%[2]d`).
  [[GH-1634]](https://github.com/fatih/vim-go/pull/1634)
* Respect `g:go_test_show_name` change for `:GoTest` when it changes during a
  Vim session.
  [[GH-1641]](https://github.com/fatih/vim-go/pull/1641)
* Show `g:go_test_show_name` value for `:GoTest` failures if it's available.
  [[GH-1641]](https://github.com/fatih/vim-go/pull/1641)
* Make sure linter errors for the file being saved are shown in vim74 and nvim.
  [[GH-1640]](https://github.com/fatih/vim-go/pull/1640)
* Make sure only linter errors for the file being saved are shown in vim8.
  Previously, all linter errors for all files in the current file's directory
  were being shown.
  [[GH-1640]](https://github.com/fatih/vim-go/pull/1640)
* Make sure gometalinter is run on the given directories when arguments are
  given to :GoMetaLinter.
  [[GH-1640]](https://github.com/fatih/vim-go/pull/1640)
* Do not run disabled linters with `gometalinter`.
  [[GH-1648]](https://github.com/fatih/vim-go/pull/1648)
* Do not prompt user to press enter after when `gometalinter` is called in
  autosave mode.
  [[GH-1654]](https://github.com/fatih/vim-go/pull/1654)
* Fix potential race conditions when using vim8 jobs.
  [[GH-1656]](https://github.com/fatih/vim-go/pull/1656)
* Treat `'autowriteall'` the same as `'autowrite'` when determining whether to
  write a buffer before calling some commands.
  [[GH-1653]](https://github.com/fatih/vim-go/pull/1653)
* Show the file location of test errors when the message is empty or begins
  with a newline.
  [[GH-1664]](https://github.com/fatih/vim-go/pull/1664)
* Fix minisnip on Windows.
  [[GH-1698]](https://github.com/fatih/vim-go/pull/1698)
* Keep alternate filename when loading an autocreate template.
  [[GH-1675]](https://github.com/fatih/vim-go/pull/1675)
* Parse the column number in errors correctly in vim8 and neovim.
  [[GH-1716]](https://github.com/fatih/vim-go/pull/1716)
* Fix race conditions in the terminal handling for neovim.
  [[GH-1721]](https://github.com/fatih/vim-go/pull/1721)
* Put the user back in the original window regardless of the value of
  `splitright` after starting a neovim terminal window.
  [[GH-1725]](https://github.com/fatih/vim-go/pull/1725)

BACKWARDS INCOMPATIBILITIES:

* Highlighting function and method declarations/calls is fixed. To fix it we
  had to remove the meaning of the previous settings. The following setting is
  removed:

  * `go_highlight_methods`

  in favor of the following settings and changes:

  * `go_highlight_functions`: This highlights now all function and method
    declarations (whereas previously it would also highlight function and
    method calls, not anymore)
  * `go_highlight_function_calls`: This higlights now all all function and
    method calls.
  [[GH-1557]](https://github.com/fatih/vim-go/pull/1557)
* Rename g`g:go_metalinter_excludes` to `g:go_metalinter_disabled`.
  [[GH-1648]](https://github.com/fatih/vim-go/pull/1648)
* `:GoBuild` doesn't append the `-i` flag anymore due the recent Go 1.10
  changes that introduced a build cache.
  [[GH-1701]](https://github.com/fatih/vim-go/pull/1701)

## 1.16 - (December 29, 2017)

FEATURES:

* Add `g:go_doc_url` to change the `godoc` server from `godoc.org` to a custom
  private instance. Currently only `godoc -http` instances are supported.
  [[GH-1957]](https://github.com/fatih/vim-go/pull/1957).
* New setting `g:go_test_prepend_name` (off by default) to add the failing test
  name to the output of `:GoTest`
  [[GH-1578]](https://github.com/fatih/vim-go/pull/1578).
* Support [denite.vim](https://github.com/Shougo/denite.nvim) for `:GoDecls[Dir]`
  [[GH-1604]](https://github.com/fatih/vim-go/pull/1604).

IMPROVEMENTS:

* `:GoRename` is a bit smarter when automatically pre-filling values, and what
  gets pre-filled can be configured with `g:go_gorename_prefill` option.
  In addition `:GoRename <Tab>` now lists some common options.
  [[GH-1465]](https://github.com/fatih/vim-go/pull/1465).
* Add support for `g:go_build_tags` to the `:GoTest` family of functions.
  [[GH-1562]](https://github.com/fatih/vim-go/pull/1562).
* Pass `--tests` to gometalinter when autosaving and when a custom gometalinter
  command has not been set.
  [[GH-1563]](https://github.com/fatih/vim-go/pull/1563).
* Do not spam messages when command is run in a directory that does not exist.
  [[GH-1527]](https://github.com/fatih/vim-go/pull/1527).
* Run `syntax sync fromstart` after `:GoFmt`; this should make syntax
  highlighting break slightly less often after formatting code
  [[GH-1582]](https://github.com/fatih/vim-go/pull/1582).
* `:GoDescribe` doesn't require a scope anymore
  [[GH-1596]](https://github.com/fatih/vim-go/pull/1596).
* Add some standard snippets for
  [vim-minisnip](https://github.com/joereynolds/vim-minisnip)
  [[GH-1589]](https://github.com/fatih/vim-go/pull/1589).
* `g:go_snippet_engine` now defaults to `automatic` to use the first installed
  snippet engine it can find.
  [[GH-1589]](https://github.com/fatih/vim-go/pull/1589).
* Make sure temporary files created for `:GoFmt` end with `.go` suffix as this
  is required by some Go formatting tools
  [[GH-1601]](https://github.com/fatih/vim-go/pull/1601).

BUG FIXES:

* Fix compatibility with Vim version before 7.4.1546
  [[GH-1498]](https://github.com/fatih/vim-go/pull/1498).
* Don't resize godoc window if it's already visible
  [[GH-1488]](https://github.com/fatih/vim-go/pull/1488).
* `:GoTestCompile` produces a test binary again. The test binary will be
  written to a temporary directory to avoid polluting the user's working
  directory. [[GH-1519]](https://github.com/fatih/vim-go/pull/1519)
* Fix incorrect `:GoSameIdsToggle` behavior when there were match groups
  present, but none were goSameId.
  [[GH-1538]](https://github.com/fatih/vim-go/pull/1538)
* Fix `gpl` snippet for UltiSnips.
  [[GH-1535]](https://github.com/fatih/vim-go/pull/1535)
* Fix test output processing to correctly handle panics and log statements.
  [[GH-1513]](https://github.com/fatih/vim-go/pull/1513)
* `:GoImpl` tab-completion would sometimes stop working
  [[GH-1581]](https://github.com/fatih/vim-go/pull/1581).
* Add `g:go_highlight_function_arguments` to highlight function arguments.
  [[GH-1587]](https://github.com/fatih/vim-go/pull/1587).
* Fix installation of `gocode` on MS-Windows.
  [[GH-1606]](https://github.com/fatih/vim-go/pull/1606).
* Fix template creation for files in directories that don't exist yet.
  [[GH-1618]](https://github.com/fatih/vim-go/pull/1618).
* Fix behavior of terminal windows and resize terminal windows correctly for
  all valid `g:go_term_mode` values.
  [[GH-1611]](https://github.com/fatih/vim-go/pull/1611).

BACKWARDS INCOMPATIBILITIES:

* Display a warning for Vim versions older than 7.4.1689. Older versions may
  still work, but are not supported. You can use `let g:go_version_warning = 0`
  to disable the warning.
  [[GH-1524]](https://github.com/fatih/vim-go/pull/1524).
* `g:go_autodetect_gopath` is *disabled* by default, as support for `vendor` has
  been in Go for a while.<br>
  Also change the implementation for `g:go_autodetect_gopath`; instead of manually
  setting it before every command it will now be set with the `BufEnter` event,
  and reset with the `BufLeave` event. This means that `$GOPATH` will be
  changed for all commands run from Vim.
  [[GH-1461]](https://github.com/fatih/vim-go/pull/1461) and
  [[GH-1525]](https://github.com/fatih/vim-go/pull/1525).
* Update `:GoFillStruct` to check the current line (vs. the exact cursor
  position) for a struct literal to fill. To support this, fillstruct made
  [backwards imcompatible
  changes](https://github.com/davidrjenni/reftools/pull/8).
  [[GH-1607]](https://github.com/fatih/vim-go/pull/1607).

## 1.15 - (October 3, 2017)

FEATURES:

* Add `:GoFillStruct` to fill a struct with all fields; uses
  [`fillstruct`](https://github.com/davidrjenni/reftools/tree/master/cmd/fillstruct)
  [[GH-1443]](https://github.com/fatih/vim-go/pull/1443).

IMPROVEMENTS:

* `:GoAddTags` and `:GoRemoveTags` now continue to process if there are
  malformed individual struct tags (run `:GoUpdateBinaries` to update
  `gomodifiytags` binary) [[GH-1401]](https://github.com/fatih/vim-go/pull/1401)
* `:GoAddTags` and `:GoRemoveTags` now shows a location list if there are
  malformed struct tags (run `:GoUpdateBinaries` to update `gomodifiytags`
  binary) [[GH-1401]](https://github.com/fatih/vim-go/pull/1401)
* Add folding of the package-level comment (enabled by default) and/or any
  other comments (disabled by default) [[GH-1377]](https://github.com/fatih/vim-go/pull/1377).
  [[GH-1428]](https://github.com/fatih/vim-go/pull/1428).
* Allow using :GoImpl on the type and struct parts too. Makes it a wee bit
  easier to use [[GH-1386]](https://github.com/fatih/vim-go/pull/1386)
* `:GoDef` sets the path of new buffers as relative to the current directory
  when appropriate, instead of always using the full path [[GH-1277]](https://github.com/fatih/vim-go/pull/1277).
* Syntax highlighting for variable declarations and assignments (disabled by default)
  [[GH-1426]](https://github.com/fatih/vim-go/pull/1426) and
  [[GH-1458]](https://github.com/fatih/vim-go/pull/1458).
* Add support for `:GoDecls[Dir]` in [unite.vim](https://github.com/Shougo/unite.vim)
  [[GH-1391]](https://github.com/fatih/vim-go/pull/1391).
* Add support for [fzf.vim](https://github.com/junegunn/fzf.vim) in
  `GoDecls[Dir]`.
  [[GH-1437]](https://github.com/fatih/vim-go/pull/1437).
* Support relative imports for `:GoImpl` [[GH-1322]](https://github.com/fatih/vim-go/pull/1322).
* A new `g:go_list_type_commands` setting is added to individually set the list type for each command [[GH-1415]](https://github.com/fatih/vim-go/pull/1415). As en example:

        let g:go_list_type_commands = {"GoBuild": "quickfix", "GoTest": "locationlist"}
* Show unexpected errors better by expanding newlines and tabs
  [[GH-1456]](https://github.com/fatih/vim-go/pull/1456).
* `:GoInstallBinaries` and `:GoUpdateBinaries` can now install/update only the
  selected binaries (e.g. `:GoUpdateBinaries guru golint`)
  [[GH-1467]](https://github.com/fatih/vim-go/pull/1467).

BUG FIXES:

* `:GoFmt` now (again) uses `locationlist` to show formatting errors instead of
  `quickfix`. To change back to `locationlist` you can change it with the
  setting `let g:go_list_type_commands = { "GoFmt": locationlist" }` [[GH-1415]](https://github.com/fatih/vim-go/pull/1415)
* Include comments in import block when folding is enabled [[GH-1387]](https://github.com/fatih/vim-go/pull/1387)
* Fix opening definitions in tabs [[GH-1400]](https://github.com/fatih/vim-go/pull/1400)
* Fix accidentally closing quickfix window from other commands if :GoFmt or autosave format was called [[GH-1407]](https://github.com/fatih/vim-go/pull/1407)
* Fix entering into insert mode after for term mode in nvim [[GH-1411]](https://github.com/fatih/vim-go/pull/1411)
* When using :GoImpl on type foo struct{} it would work, but with:

        type foo struct{
        }

  or with a struct with fields, it would create the generated methods inside the
  struct [[GH-1386]](https://github.com/fatih/vim-go/pull/1386)
* `:GoImpl` output would include extra newline, and error would include
  trailing newline from shell command: `vim-go: invalid receiver: "} *}"<00>`.
  Fixed with [[GH-1386]](https://github.com/fatih/vim-go/pull/1386)
* Run `:GoMetaLinter` against the package of the open file [[GH-1414]](https://github.com/fatih/vim-go/pull/1414).
* The `g:go_doc_command` and `g:go_doc_options` to configure the command for
  `:GoDoc` were documented but never referenced [[GH-1420]](https://github.com/fatih/vim-go/pull/1420).
* `go#package#FromPath()` didn't work correctly [[GH-1435]](https://github.com/fatih/vim-go/pull/1435).
* Fix race condition for `guru` based commands [[GH-1439]](https://github.com/fatih/vim-go/pull/1439).
* The `gohtmltmpl` filetype now sources the `html` ftplugin, so that `matchit`,
  completion, and some other things work better.
  [[GH-1442]](https://github.com/fatih/vim-go/pull/1442)
* Fix `:GoBuild` shell escaping [[GH-1450]](https://github.com/fatih/vim-go/pull/1450).
* Ensure fmt list gets closed when title cannot be checked [[GH-1474]](https://github.com/fatih/vim-go/pull/1474).

BACKWARDS INCOMPATIBILITIES:

* `:GoMetaLinter` now runs against the package of the open file instead of the
  current working directory. This is so all commands behave the same relative
  to the current open buffer. [[GH-1414]](https://github.com/fatih/vim-go/pull/1414)

* `:GoImpl` now requires [`impl`](https://github.com/josharian/impl) version
  3fb19c2c or newer (released June 13, 2017); use `:GoUpdateBinaries` to make
  sure that you've got a recent version [[GH-1322]](https://github.com/fatih/vim-go/pull/1322)

## 1.14 - (August 6, 2017)

FEATURES:

* We now have folding support based on Go syntax. To enable it you have to set
  the following Vim setting: `set foldmethod=syntax`. Currently it folds blocks
  (`{ }`), `import`, `var`, and `const` blocks, and package-level comments.
  These can be individually disabled/enabled if desired. For more info please
  read the documentation for the `g:go_fold_enable` setting. [[GH-1339]](https://github.com/fatih/vim-go/pull/1339)
  [[GH-1377]](https://github.com/fatih/vim-go/pull/1377)
* `:GoFiles` accepts now an argument to change the type of files it can show.
  By default it shows`.go source files` but now it can be changed to show
  various kind of files. The full list can be seen via `go list --help` under
  the `// Source Files` section [[GH-1372]](https://github.com/fatih/vim-go/pull/1372) i.e:

```
:GoFiles CgoFiles        // shows .go sources files that import "C"
:GoFiles TestGoFiles     // shows _test.go files in package
:GoFiles IgnoredGoFiles  // shows .go sources ignored due to build constraints
etc..
```

IMPROVEMENTS

* Files created with `_test.go` extension have a new template with a ready to
  go test function. The template can be changed with the
  `g:go_template_test_file` setting. [[GH-1318]](https://github.com/fatih/vim-go/pull/1318)
* Improve performance for highly used operations by caching `go env` calls [[GH-1320]](https://github.com/fatih/vim-go/pull/1320)
* `:GoCoverage` can accept arguments now. i.e: `:GoCoverage -run TestFoo` [[GH-1326]](https://github.com/fatih/vim-go/pull/1326)
* `:GoDecls` and `:GoDeclsDir` shows a warning if [ctrlp.vim](https://github.com/ctrlpvim/ctrlp.vim) is not installed
* `:GoBuild` now compiles the package with the `-i` flag added. This means that subsequent calls are much more faster due caching of packages [[GH-1330]](https://github.com/fatih/vim-go/pull/1330)
* `:GoCoverage` echos now the progress if `g:go_echo_command_info` is enabled [[GH-1333]](https://github.com/fatih/vim-go/pull/1333)
* Add `g:go_doc_max_height` setting to control the maximum height of the window created by `:GoDoc` and `K` mapping [[GH-1335]](https://github.com/fatih/vim-go/pull/1335)
* The `af` text object is able to include the assignment variable for anonymous functions. Can be disabled with `g:go_textobj_include_variable = 0` [[GH-1345]](https://github.com/fatih/vim-go/pull/1345)
* Add `g:go_list_autoclose` setting to prevent closing the quickfix/location list after zero items [[GH-1361]](https://github.com/fatih/vim-go/pull/1361)
* Cursor is now adjusted and locked to the correct line when `goimports` is used for autosave [[GH-1367]](https://github.com/fatih/vim-go/pull/1367)
* Complement the path of command for different situations of Cygwin environment [[GH-1394]](https://github.com/fatih/vim-go/pull/1394)
* Show message when using :GoDef and opening a new buffer [[GH-1385]](https://github.com/fatih/vim-go/pull/1385)


BUG FIXES:

* Fix obtaining package's import path for the current directory. This fixes some issues we had if the user was using multiple GOPATH's [[GH-1321]](https://github.com/fatih/vim-go/pull/1321)
* Fix documentation for vim-go & syntastic integration for errcheck using [[GH-1323]](https://github.com/fatih/vim-go/pull/1323)
* Fix showing an output if a test has finished when `:GoTest` is called [[GH-1327]](https://github.com/fatih/vim-go/pull/1327)
* Fix warning when goimports doesn't support srcdir [[GH-1344]](https://github.com/fatih/vim-go/pull/1344)
* Fix broken code folding with go_highlight_types [[GH-1338]](https://github.com/fatih/vim-go/pull/1338)
* Fix blocking the ui when swapfile is enabled and `:GoFmt` is called (either manually or via autosave) [[GH-1362]](https://github.com/fatih/vim-go/pull/1362)
* Fix getting bin paths for binaries if GOPATH was not set and Go version =>1.7 was used [[GH-1363]](https://github.com/fatih/vim-go/pull/1363)
* Fix picking up the correct list type for showing `:GoFmt` errors [[GH-1365]](https://github.com/fatih/vim-go/pull/1365)
* Fix auto detecting of GOPATH for import paths with string 'src' (i.e: `GOPATH/src/github.com/foo/src/bar`) [[GH-1366]](https://github.com/fatih/vim-go/pull/1366)
* Fix showing an empty window if `gogetdoc` was not found [[GH-1379]](https://github.com/fatih/vim-go/pull/1379)
* Fix commands not being executed if paths would include spaces (binary name, GOPATH, file itself, etc..)  [[GH-1374]](https://github.com/fatih/vim-go/pull/1374)
* Fix showing correct message when editing a new file [[GH-1371]](https://github.com/fatih/vim-go/pull/1371)
* Fix filepaths in the quickfix list for :GoVet [[GH-1381]](https://github.com/fatih/vim-go/pull/1381)
* Run :GoLint against the package of the open file [[GH-1382]](https://github.com/fatih/vim-go/pull/1382)

BACKWARDS INCOMPATIBILITIES:

* `:GoFmt` now uses `quickfix` to show formatting errors instead of
  `locationlist`. To change back to `locationlist` you can change it with the
  setting `let g:go_list_type = "locationlist"` [[GH-1365]](https://github.com/fatih/vim-go/pull/1365)
* `:GoLint` now runs against the package of the open file instead of the
  current working directory. This is so all commands behave the same relative
  to the current open buffer. For more info check the [comment
  here](https://github.com/fatih/vim-go/issues/1375#issuecomment-317535953)
  [[GH-1382]](https://github.com/fatih/vim-go/pull/1382)

## 1.13 - (June 6, 2017)

FEATURES:

* New `:GoKeyify` command that turns unkeyed struct literals into keyed struct literals. [[GH-1258]](https://github.com/fatih/vim-go/pull/1258). i.e:

```
Example{"foo", "bar", "qux"}
```

will be converted to:

```
Example{
  foo: "foo",
  bar: "bar",
  qux: "qux",
}
```

Checkout the demo here: https://twitter.com/fatih/status/860410299714764802


* New `g:go_addtags_transform` setting to change the transform rule (snakecase, camelcase, etc..) for `:GoAddTags` command [[GH-1275]](https://github.com/fatih/vim-go/pull/1275)
* New snippet shortcut assigned to `ife` that expands to `if err := foo(); err != nil { ... }` [[GH-1268]](https://github.com/fatih/vim-go/pull/1268)

IMPROVEMENTS

* :GoMetaLinter can now exclude linters with the new `g:go_metalinter_excludes` option [[GH-1253]](https://github.com/fatih/vim-go/pull/1253)
* Override `<C-LeftMouse>` mapping so `:GoDef` is used by default (as we do the same for `CTRL-]`, `gd`, etc. [[GH-1264]](https://github.com/fatih/vim-go/pull/1264)
* add support for `go_list_type` setting in `:GoFmt` and `:GoImports` commands [[GH-1304]](https://github.com/fatih/vim-go/pull/1304)
* add support for `go_list_type` setting in `:GoMetaLinter` commands [[GH-1309]](https://github.com/fatih/vim-go/pull/1309)
* `go_fmt_options` can be now a dictionary to allow us to specifcy the
  options for multiple binaries [[GH-1308]](https://github.com/fatih/vim-go/pull/1308). i.e:

```
  let g:go_fmt_options = {
    \ 'gofmt': '-s',
    \ 'goimports': '-local mycompany.com',
    \ }
```
* If win-vim(x64) with Cygwin is used, `cygpath` is used for constructing the paths [[GH-1092]](https://github.com/fatih/vim-go/pull/1092)

BUG FIXES:

* job: fix race between channel close and job exit [[GH-1247]](https://github.com/fatih/vim-go/pull/1247)
* internal: fix system calls when using tcsh [[GH-1276]](https://github.com/fatih/vim-go/pull/1276)
* path: return the unmodified GOPATH if autodetect is disabled [[GH-1280]](https://github.com/fatih/vim-go/pull/1280)
* fix jumping to quickfix window when autom gometalinter on save was enabled [[GH-1293]](https://github.com/fatih/vim-go/pull/1293)
* fix highlighting for `interface` and `structs` words when `go_highlight_types` is enabled [[GH-1301]](https://github.com/fatih/vim-go/pull/1301)
* fix cwd for running `:GoRun` when used with neovim [[GH-1296]](https://github.com/fatih/vim-go/pull/1296)
* `:GoFmt` handles files that are symlinked into GOPATH better (note that this behaviour is discouraged, but we're trying our best to handle all edge case :)) [[GH-1310]](https://github.com/fatih/vim-go/pull/1310)
* `:GoTest` is able to parse error messages that include a colon `:` [[GH-1316]](https://github.com/fatih/vim-go/pull/1316)
* `:GoTestCompile` under the hood doesn't produces a test binary anymore. Sometimes a race condition would happen which would not delete the test binary. [[GH-1317]](https://github.com/fatih/vim-go/pull/1317)
* `:GoDef` jumps now to definition for build tags defined with `:GoBuildTags` (only guru) [[GH-1319]](https://github.com/fatih/vim-go/pull/1319)

BACKWARDS INCOMPATIBILITIES:

* `:GoLint` works on the whole directory instead of the current file. To use it for the current file give it as an argument, i.e `:GoLint foo.go` [[GH-1295]](https://github.com/fatih/vim-go/pull/1295)
* `go_snippet_case_type` is removed in favor of the new `go_addtags_transform` setting [[GH-1299]](https://github.com/fatih/vim-go/pull/1299)
* `go_imports_bin` is removed to avoid confusion as it would lead to race
  conditions when set to `gofmt` along with the usage of `go_fmt_command`
  [[GH-1212]](https://github.com/fatih/vim-go/pull/1212) [[GH-1308]](https://github.com/fatih/vim-go/pull/1308)
* commands such as `:GoTest` has been refactored for easy maintainability. If
  you use any custom script that was using the function `go#cmd#Test`, it
  should be renamed to `go#test#Test`

## 1.12 - (March 29, 2017)

FEATURES:

* New `:GoAddTags` and `:GoRemoveTags` command based on the tool
  [gomodifytags](https://github.com/fatih/gomodifytags). This fixes many old
  bugs that were due prior regexp based implementation. For the usage please
  read the docs and checkout the demo at:
  https://github.com/fatih/vim-go/pull/1204 [[GH-1204]](https://github.com/fatih/vim-go/pull/1204)
* Add new `errl` snippet that expands to [[GH-1185]](https://github.com/fatih/vim-go/pull/1185):

```
if err != nil {
  log.Fatal(err)
}
```
* New `:GoBuildTags` command to change build tags for tools such as `guru`,
  `gorename`, etc ... There is also a new setting called `g:go_build_tags`
  [[GH-1232]](https://github.com/fatih/vim-go/pull/1232)

IMPROVEMENTS:

* vim-go works now even if GOPATH is not set (starting with Go 1.8) [[GH-1248]](https://github.com/fatih/vim-go/pull/1248)
* Lowercase `<Leader>` in mappings examples for consistent documentation across the README [[GH-1192]](https://github.com/fatih/vim-go/pull/1192)
* All of files should be written in utf-8 if the file will be passed to external command. [[GH-1184]](https://github.com/fatih/vim-go/pull/1184)
* `:GoAddTags` is now able to add options to existing tags with the syntax
  `:GoAddTags key,option`, i.e: `:GoAddTags json,omitempty` [[GH-985]](https://github.com/fatih/vim-go/pull/985)
* Document 'noshowmode' requirement for echo_go_info [[GH-1197]](https://github.com/fatih/vim-go/pull/1197)
* Improve godoc view for vertical splits [[GH-1195]](https://github.com/fatih/vim-go/pull/1195)
* Set GOPATH for both possible go guru execution paths (sync and async) [[GH-1193]](https://github.com/fatih/vim-go/pull/1193)
* Improve docs for :GoDef usage [[GH-1242]](https://github.com/fatih/vim-go/pull/1242)
* Highlight trimming syntax for Go templates [[GH-1235]](https://github.com/fatih/vim-go/pull/1235)

BUG FIXES:

* Honor `g:go_echo_command_info` when dispatching builds in neovim [[GH-1176]](https://github.com/fatih/vim-go/pull/1176)
* Fix `:GoBuild` error in neovim due to invalid jobcontrol handler function
  signatures (`s:on_stdout`, `s:on_stderr`)[[GH-1176]](https://github.com/fatih/vim-go/pull/1176)
* Update statusline before and after `go#jobcontrol#Spawn` command is executed [[GH-1176]](https://github.com/fatih/vim-go/pull/1176)
* Correctly report the value of the 'g:go_guru_tags' variable [[GH-1177]](https://github.com/fatih/vim-go/pull/1177)
* Ensure no trailing `:` exist in GOPATH detection if initial GOPATH is not set [[GH-1194]](https://github.com/fatih/vim-go/pull/1194)
* Fix `:GoAddTags` to allow modifying existing comments [[GH-984]](https://github.com/fatih/vim-go/pull/984)
* Fix `:GoAddTags` to work with nested structs [[GH-990]](https://github.com/fatih/vim-go/pull/990)
* Fix `:GoAddTags` adding tags twice for existing tags [[GH-1064]](https://github.com/fatih/vim-go/pull/1064)
* Fix `:GoAddTags` not working for fields of types `interface{}` [[GH-1091]](https://github.com/fatih/vim-go/pull/1091)
* Fix `:GoAddTags` not working for fields with one line comments [[GH-1181]](https://github.com/fatih/vim-go/pull/1181)
* Fix `:GoAddTags` not working if any field comment would contain `{}` [[GH-1189]](https://github.com/fatih/vim-go/pull/1189)
* Respect go_fmt_options when running goimports [[GH-1211]](https://github.com/fatih/vim-go/pull/1211)
* Set the filename in the location-list when there is an error with :GoFmt [[GH-1199]](https://github.com/fatih/vim-go/pull/1199)
* Fix `:GoInstall` to accept additional arguments if async mode was enabled [[GH-1246]](https://github.com/fatih/vim-go/pull/1246)

BACKWARDS INCOMPATIBILITIES:

* The command `:GoGuruTags` is removed in favour of the new command
  `:GoBuildTags`. This command will be used now not just for `guru`, also for
  all new commands such as `gorename` [[GH-1232]](https://github.com/fatih/vim-go/pull/1232)
* The setting `g:go_guru_tags` is removed in favour of the new setting
  `g:go_build_tags` [[GH-1232]](https://github.com/fatih/vim-go/pull/1232)


## 1.11 - (January 9, 2017)

FEATURES:

* Travis test integration has been added. Now any file that is added as
  `<name>_test.vim` will be automatically tested in for every Pull Request
  (just like how we add tests to Go with `_test.go`). Going forward this will
  tremendously increase the stability and decrease the maintenance burden of
  vim-go. [[GH-1157]](https://github.com/fatih/vim-go/pull/1157)
* Add new `g:go_updatetime` setting to change the default updatetime (which was hardcoded previously) [[GH-1055]](https://github.com/fatih/vim-go/pull/1055)
* Add new `g:go_template_use_pkg` setting to enable to use cwd as package name instead of basic template file [[GH-1124]](https://github.com/fatih/vim-go/pull/1124)

IMPROVEMENTS:

* Add `statusline` support for `:GoMetaLinter` [[GH-1120]](https://github.com/fatih/vim-go/pull/1120)
* Quickfix and Location lists contain now a descriptive title (requires at least Vim `7.4.2200`)[[GH-1004]](https://github.com/fatih/vim-go/pull/1004)
* Check `go env GOPATH` as well for `:GoInstallBinaries` as Go has now a default path for GOPATH ("~/go")starting with 1.8 [[GH-1152]](https://github.com/fatih/vim-go/pull/1152)
* `:GoDocBrowser` now also works on import paths [[GH-1174]](https://github.com/fatih/vim-go/pull/1174)

BUG FIXES:

* Always use full path to detect packages to be shown in statusline [[GH-1121]](https://github.com/fatih/vim-go/pull/1121)
* Use `echom` to persist errors in case of multiple echos [[GH-1122]](https://github.com/fatih/vim-go/pull/1122)
* Fix a race condition where a quickfix window was not closed if a job has succeeded [[GH-1123]](https://github.com/fatih/vim-go/pull/1123)
* Do not expand coverage arguments for non job execution of `:GoCoverage` [[GH-1127]](https://github.com/fatih/vim-go/pull/1127)
* `:GoCoverage` doesn't mess up custom syntax anymore [[GH-1128]](https://github.com/fatih/vim-go/pull/1128)
* Disable autoformat for `asm` files as they might be non Go ASM format [[GH-1141]](https://github.com/fatih/vim-go/pull/1141)
* Fix indentation broken when using a action with a minus sign like `{{-` [[GH-1143]](https://github.com/fatih/vim-go/pull/1143)
* Fix breaking Neovim change of passing less arguments to callbacks [[GH-1145]](https://github.com/fatih/vim-go/pull/1145)
* Fix `guru` commands if custom build tags were set [[GH-1136]](https://github.com/fatih/vim-go/pull/1136)
* Fix referencing a non defined variable for async commands when bang (!) was used
* Fix `:GoDef` failing for a modified buffer if `hidden` was not set [[GH-1132]](https://github.com/fatih/vim-go/pull/1132)
* Fix `:GoDefStack` to allow popping from jump list when buffer is modified [[GH-1133]](https://github.com/fatih/vim-go/pull/1133)
* Improve internal defining of functions and referencing them for async operations [[GH-1155]](https://github.com/fatih/vim-go/pull/1155)
* Fix `:GoMetaLinter` failing if `go_metalinter_command` is set. [[GH-1160]](https://github.com/fatih/vim-go/pull/1160)
* Fix `:GoMetaLinter`'s `go_metalinter_deadline` setting for async mode [[GH-1146]](https://github.com/fatih/vim-go/pull/1146)

BACKWARDS INCOMPATIBILITIES:

* The following syntax options are now disabled by default. If you're using them be sure to set them in your .vimrc [[GH-1167]](https://github.com/fatih/vim-go/pull/1167)

```viml
g:go_highlight_array_whitespace_error
g:go_highlight_chan_whitespace_error
g:go_highlight_extra_types
g:go_highlight_space_tab_error
g:go_highlight_trailing_whitespace_error
```



## 1.10 (November 24, 2016)

FEATURES:

* **Vim 8.0 support!** This is the initial version to add Vim 8.0 based support to
  all basic commands (check out below for more information). With time we'll
  going to extend it to other commands. All the features are only enabled if
  you have at least Vim 8.0.0087. Backwards compatible with Vim 7.4.x.
  If you see any problems, please open an issue.

* We have now a [logo for vim-go](https://github.com/fatih/vim-go/blob/master/assets/vim-go.png)! Thanks to @egonelbre for his work on this.
* `:GoBuild`, `:GoTest`, `:GoTestCompile`, `:GoInstall` commands are now fully
  async. Async means it doesn't block your UI anymore. If the command finished
  it echoes the status. For a better experience use the statusline information
  (more info below)

* `:GoCoverage` and `:GoCoverageBrowser` commands are fully async.
* `:GoDef` is fully async if `guru` is used as command.
* `:GoRename` is fully async .

* `:GoMetaLinter` is fully asnyc. Also works with the current autosave linting
  feature. As a reminder, to enable auto linting on save either call
  `:GoMetaLinterAutoSaveToggle` (temporary) or add `let
  g:go_metalinter_autosave = 1` (persistent) to your virmc).

* All `guru` commands run asynchronously if Vim 8.0 is being used. Current
  Commands:
  * GoImplements
  * GoWhicherrs
  * GoCallees
  * GoDescribe
  * GoCallers
  * GoCallstack
  * GoFreevars
  * GoChannelPeers
  * GoReferrers

* `:GoSameIds` also runs asynchronously. This makes it useful especially for
  auto sameids mode. In this mode it constantly evaluates the identifier under the
  cursor whenever it's in hold position and then calls :GoSameIds. As a
  reminder, to enable auto info either call `:GoSameIdsAutoToggle`(temporary)
  or add `let g:go_auto_sameids = 1` (persistent) to your vimrc.

* `:GoInfo` is now non blocking and works in async mode if `guru` is used in
  `g:go_info_mode`. This makes it useful especially for autoinfo mode. In this
  mode it constantly evaluates the identifier under the cursor whenever it's in
  hold position and then calls :GoInfo. As a reminder, to enable auto info
  either call `:GoAutoTypeInfoToggle`(temporary) or add `let
  g:go_auto_type_info = 1` (persistent) to your vimrc. To use `guru` instead of
  `gocode` add following to your vimrc: `let g:go_info_mode = 'guru'`

  The `guru` is more accurate and reliabed due the usage of `guru` describe. It
  doesn't rely on `pkg/` folder like `gocode` does. However it's slower than
  `gocode` as there is no caching mechanism in `guru` yet.

* **New**: Statusline function: `go#statusline#Show()` which can be plugged into
  the statusline bar. Works only with vim 8.0. It shows all asynchronously
  called functions status real time.  Checkout it in action:
  https://twitter.com/fatih/status/800473735467847680. To enable it add the
  following to your `vimrc`. If you use lightline, airline, .. check out their
  respective documentation on how to add a custom function:

```viml
" go command status (requires vim-go)
set statusline+=%#goStatuslineColor#
set statusline+=%{go#statusline#Show()}
set statusline+=%*
```

IMPROVEMENTS:

* **:GoDocBrowser** is now capable to to understand the identifier under the cursor (just like :GoDoc)
* Function calls are now highlighted as well when `g:go_highlight_functions` is enabled [[GH-1048]](https://github.com/fatih/vim-go/pull/1048)
* Add completion support for un-imported packages. This allows to complete even
  if the package is not imported. By default it's disabled, enable by adding
  `let g:go_gocode_unimported_packages = 1` [[GH-1084]](https://github.com/fatih/vim-go/pull/1084)
* Tools that embeds GOROOT into their binaries do not work when people update
  their Go version and the GOROOT contains the vesion as part of their path
  (i.e: `/usr/local/Cellar/go/1.7.2/libexec`, [more
  info](https://blog.filippo.io/stale-goroot-and-gorebuild/)) . This is now
  fixed by introducing automatic GOROOT set/unset before each tool invoke.
  [[GH-954]](https://github.com/fatih/vim-go/pull/954)
* Added new setting `g:go_echo_go_info` to enable/disable printing identifier
  information when completion is done [[GH-1101]](https://github.com/fatih/vim-go/pull/1101)
* Added new `go_echo_command_info` setting is added, which is enabled by
  default.  It's just a switch for disabling messages of commands, such as
  `:GoBuild`, `:GoTest`, etc.. Useful to *disable* if `go#statusline#Show()` is
  being used in Statusline, to prevent to see duplicates notifications.
* goSameId highlighting is now linked to `Search`, which is much more clear as
  it changes according to the users colorscheme
* Add plug mapping `(go-lint)` for :GoLint [[GH-1089]](https://github.com/fatih/vim-go/pull/1089)


BUG FIXES:

* Change back nil and iota highlighting color to the old type [[GH-1049]](https://github.com/fatih/vim-go/pull/1049)
* Fix passing arguments to `:GoBuild` while using NeoVim [[GH-1062]](https://github.com/fatih/vim-go/pull/1062)
* Do not open a split if `:GoDef` is used on a modified file [[GH-1083]](https://github.com/fatih/vim-go/pull/1083)
* Highlight nested structs correctly [[GH-1075]](https://github.com/fatih/vim-go/pull/1075)
* Highlight builtin functions correctly if `g:go_highlight_functions` is enabled [[GH-1070]](https://github.com/fatih/vim-go/pull/1070)
* Fix `:GoSameIds` highlighting if a new buffer is opened in the same window [[GH-1067]](https://github.com/fatih/vim-go/pull/1067)
* Internal: add `abort` to all vim function to return in case of errors [[GH-1100]](https://github.com/fatih/vim-go/pull/1100)
* Fix `:GoCoverage` to be executed if working dir is not inside the test dir [[GH-1033]](https://github.com/fatih/vim-go/pull/1033)

BACKWARDS INCOMPATIBILITIES:

* remove vim-dispatch and vimproc.vim support. vim 8.0 has now the necessary
  API to invoke async jobs and timers. Going forward we should use those. Also
  this will remove the burden to maintain compatibility with those plugins.

* `go#jobcontrol#Statusline()` is removed in favor of the new, global and
  extensible `go#statusline#Show()`

## 1.9 (September 13, 2016)

IMPROVEMENTS:

* **guru** uses now the `-modified` flag, which allows us use guru on modified
  buffers as well. This affects all commands where `guru` is used. Such as
  `:GoDef`, `:GoReferrers`, etc.. [[GH-944]](https://github.com/fatih/vim-go/pull/944)
* **:GoDoc** uses now the `-modified` flag under the hood (for `gogetdoc), which allows us to get documentation for the identifier under the cursor ina modified buffer. [[GH-1014]](https://github.com/fatih/vim-go/pull/1014)
* Cleanup and improve documentation [[GH-987]](https://github.com/fatih/vim-go/pull/987)
* Add new `g:go_gocode_socket_type` setting to change the underlying socket type passed to `gocode`. Useful to fallback to `tcp` on cases such as Bash on Windows [[GH-1000]](https://github.com/fatih/vim-go/pull/1000)
* `:GoSameIds` is now automatically re-evaluated in cases of buffer reloads (such as `:GoRename`) [[GH-998]](https://github.com/fatih/vim-go/pull/998)
* Improve docs about `go_auto_sameids` [[GH-1017]](https://github.com/fatih/vim-go/pull/1017)
* Improve error message by printing the full path if an incompatible `goimports` is being used [[GH-1006]](https://github.com/fatih/vim-go/pull/1006)
* `iota` and `nil` are now highlighted correctly and are not treated as booleans [[GH-1030]](https://github.com/fatih/vim-go/pull/1030)

BUG FIXES:

* Fix system calls on Windows [[GH-988]](https://github.com/fatih/vim-go/pull/988)
* Fix :GoSameIds and :GoCoverage for light background and after changing color schemes [[GH-983]](https://github.com/fatih/vim-go/pull/983)
* Fix TagBar and `GoCallers` for Windows user [[GH-999]](https://github.com/fatih/vim-go/pull/999)
* Set updatetime for for `auto_sameids` feature as well [[GH-1016]](https://github.com/fatih/vim-go/pull/1016)
* Update docs about missing `go_highlight_generate_tags` setting [[GH-1023]](https://github.com/fatih/vim-go/pull/1023)
* Fix updating the jumplist if `:GoDef` is used [[GH-1029]](https://github.com/fatih/vim-go/pull/1029)
* Fix highlighting literal percent sign (`%%`) in strings [[GH-1011]](https://github.com/fatih/vim-go/pull/1011)
* Fix highlighting of nested fields [[GH-1007]](https://github.com/fatih/vim-go/pull/1007)
* Fix checking for `exepath` feature for the upcoming vim 8.0 release [[GH-1046]](https://github.com/fatih/vim-go/pull/1046)

BACKWARDS INCOMPATIBILITIES:

* Rename `GoMetalinterAutoSaveToggle` to `GoMetaLinterAutoSaveToggle` to make it compatible with the existing `:GoMetaLinter` command [[GH-1020]](https://github.com/fatih/vim-go/pull/1020)

## 1.8 (July 31, 2016)

FEATURES:
* New **`:GoAddTags`** command that adds field tags for the fields of a struct automatically based on the field names. Checkout the demo to see it in action: https://twitter.com/fatih/status/759822857773907968 [[GH-971]](https://github.com/fatih/vim-go/pull/971)
* The snippet expansion `json` is now much more smarter. It pre populates the placeholder according to the first word and it also applies `snake_case` or `camelCase` conversion. Together with `:GoAddTags` it gives `vim-go` users flexible ways of populating a field tag. Checkout the demo to see it in action: https://twitter.com/fatih/status/754477622042689536 [[GH-927]](https://github.com/fatih/vim-go/pull/927)
* New **`:GoSameIds`** command. When called highlights all same identifiers in the current file. Can be also enabled to highlight identifiers automatically (with `:GoSameIdsAutoToggle` or `g:go_auto_sameids`). Checkout the demo to see it in action: https://twitter.com/fatih/status/753673709278339072. [[GH-936]](https://github.com/fatih/vim-go/pull/936)
* New **`:GoWhicherrs`** command. It shows all possible values of the selected error variable. [[GH-948]](https://github.com/fatih/vim-go/pull/948)
* Add new `errp` snippet to expand an `if err != nil { panic() }` clause [[GH-926]](https://github.com/fatih/vim-go/pull/926)
* If you open a new buffer with a Go filename it get automatically populated based on the directory. If there are no Go files a simple main package is created, otherwise the file will include the package declaration line based on the package in the current directory. Checkout the demo to see it in action: https://twitter.com/fatih/status/748333086643994624. This is enabled by default. Can be disabled with `let g:go_template_autocreate = 0`. You can use your own template with `let g:go_template_file = "foo.go"` and putting the file under the `templates/` folder. [[GH-918]](https://github.com/fatih/vim-go/pull/918)
* Added new toggle commands to enable/disable feature that run for your
  automatic. For example if you have `let g:go_auto_type_info = 1` enabled, you
  can now easily enable/disable it on the fly. Support added with the following
  commands: `:GoAutoTypeInfoToggle`, `:GoFmtAutoSaveToggle`,
  `:GoAsmFmtAutoSaveToggle`, `:GoMetalinterAutoSaveToggle`,
  `:GoTemplateAutoCreateToggle` [[GH-945]](https://github.com/fatih/vim-go/pull/945)


IMPROVEMENTS:
* `:GoDoc` accepts arguments now which are passed directly to `godoc`. So usages like `:GoDoc flag` works again (it was changed in previous versions [[GH-894]](https://github.com/fatih/vim-go/pull/894)
* `:GoDef` works now for modified files as well [[GH-910]](https://github.com/fatih/vim-go/pull/910)
* Internal: pass filename to the `--srcdir` flag to enable upcoming `goimports` features [[GH-957]](https://github.com/fatih/vim-go/pull/957)
* Internal: fix indentations on all files to **2-spaces/no tabs**. This is now the default vim-go style across all VimL files [[GH-915]](https://github.com/fatih/vim-go/pull/915)
* Internal: autocmd settings can be now dynamically enabled/disabled [[GH-939]](https://github.com/fatih/vim-go/pull/939)
* Internal: automatically detect `GOPATH`  for :GoInstall [[GH-980]](https://github.com/fatih/vim-go/pull/980)
* Internal: shell executions uses now by default `sh` and then resets it back to the user preference. [[GH-967]](https://github.com/fatih/vim-go/pull/967)
* Syntax: improved syntax highglighting performance for methods, fields, structs and interface type declarations [[GH-917]](https://github.com/fatih/vim-go/pull/917)
* Syntax: moved `:GoCoverage` highlight definition into go's syntax file for more customizability [[GH-962]](https://github.com/fatih/vim-go/pull/962)


BUG FIXES:

* Escape `#` characters when opening URL's, as it's handled as alternative file in vim [[GH-895]](https://github.com/fatih/vim-go/pull/895)
* Fix typos in `doc/vim-go.txt` about usages of syntax highglightings [[GH-897]](https://github.com/fatih/vim-go/pull/897)
* Fix `:GoCoverage` not running for Neovim [[GH-899]](https://github.com/fatih/vim-go/pull/899)
* Fix `:GoFmt` not picking up `-srcdir` if the command was set to use `goimports` [[GH-904]](https://github.com/fatih/vim-go/pull/904)
* Fix `:GoTestCompile` to not leave behind artifacts if the cwd and the test files's directory do not match [[GH-909]](https://github.com/fatih/vim-go/pull/909)
* Fix `:GoDocBrowser` to not fail if godoc doesn't exist [[GH-920]](https://github.com/fatih/vim-go/pull/920)
* Fix `:GoFmt` to not change the permissions of saved file. Now original file permissions are restored [[GH-922]](https://github.com/fatih/vim-go/pull/922)

BACKWARDS INCOMPATIBILITIES:

* `g:go_highlight_structs` and `g:go_highlight_interface` are removed in favor of `g:go_highlight_types` [[GH-917]](https://github.com/fatih/vim-go/pull/917)


## 1.7.1 (June 7, 2016)

BUG FIXES:
* Fixed typo in `syntax/go.vim` file from `go:go_highlight_fields` to `g:go_highlight_fields`

## 1.7 (June 7, 2016)

FEATURES:

* New **`:GoImpl`** command that generates method stubs for implementing an interface. Checkout the [demo](https://twitter.com/fatih/status/729991365581545472) to see how it works. [[GH-846]](https://github.com/fatih/vim-go/pull/846)
* `godef` support is added back as an optional setting.  By default `:GoDef` still uses `guru`, but can be changed to `godef` by adding the option: `let g:go_def_mode = 'godef'` [[GH-888]](https://github.com/fatih/vim-go/pull/888)
* New `<C-w><C-]>` and `<C-w>]>` shortcuts to split current window and jumpt to the identifier under cursor. [[GH-838]](https://github.com/fatih/vim-go/pull/838)
* New syntax setting" `g:go_highlight_fields` that highlights struct field references [[GH-854]](https://github.com/fatih/vim-go/pull/854)

IMPROVEMENTS:

* Invoking `:GoRename` now reloads all files to reflect new changes automatically [[GH-855]](https://github.com/fatih/vim-go/pull/855)
* Calling `:GoTestCompile` does not create any temporary binary file anymore [[GH-879]](https://github.com/fatih/vim-go/pull/879)
* Enable passing the `-tags` flag to `:GoDef`. Now you can pass build tags to `:GoDef` via `:GoGuruTags` or `g:go_guru_tags`
* Internal refactoring to use custom `system()` function that wraps both the standard `system()` call and `vimproc`. Now all system calls will take advantage and will use `vimproc` if installed. [[GH-801]](https://github.com/fatih/vim-go/pull/801)
* Completion enables now `gocode`'s `autobuild` and `propose-builtins` flags automatically. With these settings packages will be automatically build to get the freshest completion candidates and builtin keywords will be showed as well. By defaults these settings are enabled. Settings can be disabled/enabled via `g:go_gocode_autobuild` and `g:go_gocode_propose_builtins`. [[GH-815]](https://github.com/fatih/vim-go/pull/815)
* Added new `http.HandlerFunc` snippets with `hf` and `hhf` shortcuts [[GH-816]](https://github.com/fatih/vim-go/pull/816)
* Added new `Example` and `Benchmark` snippets with `example` and `benchmark` shortcuts [[GH-836]](https://github.com/fatih/vim-go/pull/836)
* Search tool binaries first in `GOBIN` and then in `PATH` as most of vim-go users installs it to `GOBIN` mostly [[GH-823]](https://github.com/fatih/vim-go/pull/823)
* Improve `guru` based commands by providing automatically detected GOPATHS, such as `gb`, `godep` to be used if possible [[GH-861]](https://github.com/fatih/vim-go/pull/861)
* Add `<Plug>(go-imports)` mapping to make it assignable to other keys [[GH-878]](https://github.com/fatih/vim-go/pull/878)
* Increase compatibility with tcsh [[GH-869]](https://github.com/fatih/vim-go/pull/869)
* Improve `:GoInstallBinaries` for GOPATH's which don't have packages that work well with `go get -u`. We have a new `g:go_get_update` setting to disable it. By default it's enabled. [[GH-883]](https://github.com/fatih/vim-go/pull/883)



BUG FIXES:
* Fix `(go-freevars)` plug mapping to work as in visual mode instead of noncompatible normal mode [[GH-832]](https://github.com/fatih/vim-go/pull/832)
* Commands based on guru now shows a more meaningful error message instead of just showing the exit status (-1)
* Fix `:GoCoverage` accidentally enabling syntax highlighting for users who don't use syntax (i.e syntax off) [[GH-827]](https://github.com/fatih/vim-go/pull/827)
* Fix `:GoCoverage` colors to work for xterm as well [[GH-863]](https://github.com/fatih/vim-go/pull/863)
* Fix commenting out block of texts for Go templates (filetype gothtmltmpl) [[GH-813]](https://github.com/fatih/vim-go/pull/813)
* Fix `:GoImplements` failing because of an empty scope definition. Now we default to current package to make it usable.
* Fix `:GoPlay` posting to non HTTPS url. [[GH-847]](https://github.com/fatih/vim-go/pull/847)
* Fix escaping the filenames for lint and motion commands [[GH-862]](https://github.com/fatih/vim-go/pull/862)
* Fix escaping the filename to `:GoDef` completely for tcsh [[GH-868]](https://github.com/fatih/vim-go/pull/868)
* Fix showing SUCCESS for `go test` related commands if no test files are available [[GH-859]](https://github.com/fatih/vim-go/pull/859)



## 1.6 (April 25, 2016)

FEATURES:

* New `CHANGELOG.md` file (which you're reading now). This will make it easier
  for me to track changes and release versions
* **`:GoCoverage`** is now highlighting the current source file for
  covered/uncovered lines. If called again it runs the tests and updates the
  annotation. Use `:GoCoverageClear` to clear the coverage annotation.
  This is a pretty good addition to vim-go and I suggest to check out the gif
  that shows it in action: https://twitter.com/fatih/status/716722650383564800
  [[GH-786]](https://github.com/fatih/vim-go/pull/786)
* **`:GoCoverageToggle`** just like `:GoCoverage` but acts as a toggle. If run
  again it clears the annotation.
* **`:GoCoverageBrowser`** opens a new annotated HTML page. This is the old
  `:GoCoverage` behavior [[GH-786]](https://github.com/fatih/vim-go/pull/786)
* **`:GoDoc`** uses now [gogetdoc](https://github.com/zmb3/gogetdoc) to
  lookup and display the comment documentation for the identifier under the
  cursor. This is more superior as it support looking up dot imports, named
  imports and imports where package name and file name are different [[GH-782]](https://github.com/fatih/vim-go/pull/782)
* **`guru support`**: `oracle` is replaced by the new tool `guru`. `oracle.vim`
  is therefore renamed to `guru.vim`. I've also refactored the code to make it
  much more easier to maintain and add additional features in future (such as
  upcoming JSON decoding). vim-go is now fully compatible with `guru`. Please
  be sure you have installed `guru`. You can easily do it with
  `:GoInstallBinaries`.
* **`:GoDef`** uses now `guru definition` under the hood instead of `godef`.
  This fixes the following issues: 1. dot imports 2. vendor imports 3. folder
  != package name imports. The tool `godef` is also deprecated and not used
  anymore.
* **`:GoDef`** does have now history of the call stack. This means you can
  easily jump back to your last entry. This can be done with the new command
  `:GoDefPop` or the mapping `CTRL-t`. To see the stack and jump between entries
  you can use the new command `:GoDefStack`, which shows the list of all stack
  entries. To reset the stack list anytime you can call `:GoDefStackClear`
  [[GH-776]](https://github.com/fatih/vim-go/pull/776)

IMPROVEMENTS:

* **`:GoCoverage`** is executed asynchronously when used within Neovim [[GH-686]](https://github.com/fatih/vim-go/pull/686)
* **`:GoTestFunc`** supports now testable examples [[GH-794]](https://github.com/fatih/vim-go/pull/794)
* **`:GoDef`** can jump to existing buffers instead of opening a new window
  (split, vsplit or tab). By default it's disabled to not break the old
  behavior, can be enabled with `let g:go_def_reuse_buffer = 1`

BUG FIXES:

* Fix not showing documentation for dot, named and package/file name being different imports [[GH-332]](https://github.com/fatih/vim-go/pull/332)
* Term mode: fix closing location list if result is successful after a failed attempt [[GH-768]](https://github.com/fatih/vim-go/pull/768)
* Syntax: fix gotexttmpl identifier highlighting [[GH-778]](https://github.com/fatih/vim-go/pull/778)
* Doc: fix wrong wording for `go-run` mapping. It's for the whole main package,
  not for the current file

BACKWARDS INCOMPATIBILITIES:

* `:GoDef` doesn't accept any identifier as an argument. This is not suported
  via `guru definition` and also was not widely used either. Also with this, we
  significantly simplified the existing def.vim code
* `:GoOracleScope`  and `:GoOracleTags` are deprecated in favor of
  `:GoGuruScope` and `:GoGuruTags`. Also `g:go_oracle_scope` is renamed to
  `g:go_guru_scope`
* `g:go_guru_scope` accepts a variable in type of `list` instead of `string`.
  i.g: `let g:go_guru_scope = ["github.com/fatih/structs", "golang.org/x/tools/..."]`


## 1.5 (Mar 16, 2016)

FEATURES:
* Introducing code name "motion". A new whole way of moving
  around and navigating [[GH-765]](https://github.com/fatih/vim-go/pull/765). Checkout the following new changes:
  * A vim-go specific tool, called [motion](https://github.com/fatih/motion) is being developed which
    provides us the underlying foundation for the following and upcoming
    new features.
  * `]]` and `[[` motions can be used to jump between functions
  * `if` and `af` are improved and implement from scratch. It has now
    support for literal functions, comments of functions, better cursor
    position support and more stable.
  * New `:GoDecls` and `:GoDeclsDir` commands that are available if
    `ctrlp.vim` is installed. Once called one can easily jump to any generic declaration available.
  * I wrote two blog posts about these new features in more detail. I recommend you to read it: [Treating Go types as objects in Vim](https://medium.com/@farslan/treating-go-types-as-objects-in-vim-ed6b3fad9287#.mbwaisevp) and [Navigation between functions and types in vim-go](https://medium.com/@farslan/navigation-between-functions-and-types-in-vim-go-f9dd7de8ca37#.2sdf8tbbe)
* A new `:GoAlternate` command that toggles to the test
  file of the current file. It also has new appropriate mappings to open the
  alternate file in split or tabs. [[GH-704]](https://github.com/fatih/vim-go/pull/704)
* Now commands can choose whether they want to open a
  `quickfix` or a `location list` via the setting `g:go_list_type`. Also all
  the commands have now some sensible settings, some will open a qf window,
  some will open a location list [[GH-700]](https://github.com/fatih/vim-go/pull/700)

IMPROVEMENTS:

* Add support for goimport's new `-srcdir`. Goimports now succesfully suports `vendor/` folders with this release. [[GH-735]](https://github.com/fatih/vim-go/pull/735)
* Add `g:go_gorename_prefill` setting which disabled pre filling the argument for `:GoRename` [[GH-711]](https://github.com/fatih/vim-go/pull/711)
* Improve `:GoRun` to complete to filenames [[GH-742]](https://github.com/fatih/vim-go/pull/742)
* Highlight `//go:generate` comment directives [[GH-757]](https://github.com/fatih/vim-go/pull/757)
* Indent code in Go HTML templates [[GH-709]](https://github.com/fatih/vim-go/pull/709)
* Improve negative numbers of all types, octals, imaginary numbers with exponents [[GH-752]](https://github.com/fatih/vim-go/pull/752)
* Improved internal usage of retrieving offsets [[GH-762]](https://github.com/fatih/vim-go/pull/762)
* Improve by substitute all backslashes to slashes for filename [[GH-703]](https://github.com/fatih/vim-go/pull/703)
* Improve internal Go package path function [[GH-702]](https://github.com/fatih/vim-go/pull/702)
* Improved typo and grammar errors in docs [[GH-714]](https://github.com/fatih/vim-go/pull/714)
* Improved internal `:GoInfo` automatic call [[GH-759]](https://github.com/fatih/vim-go/pull/759)

BUG FIXES:

* Fix oracle scope not working if trailing slash exists in scope [[GH-751]](https://github.com/fatih/vim-go/pull/751)
* Fix `:GoErrCheck` checking abspath [[GH-671]](https://github.com/fatih/vim-go/pull/671)
* Fix `:GoInstall` correctly parsing errors [[GH-692]](https://github.com/fatih/vim-go/pull/692)
* Fix `:GoInstall` correctly parsing errors [[GH-692]](https://github.com/fatih/vim-go/pull/692)
* Fix `:GoTestFunc` for neovim [[GH-695]](https://github.com/fatih/vim-go/pull/695)
* Fix `:GoRun` accepting arguments for neovim [[GH-730]](https://github.com/fatih/vim-go/pull/730)
* Fix `go run` mappings not working [[GH-542]](https://github.com/fatih/vim-go/pull/542)
* Fix autodetect gopath picking up non existing GB vendor folder
* Fix gofmt errors showing per buffer instead of per script [[GH-721]](https://github.com/fatih/vim-go/pull/721)
* Fix some of the neosnippet snippets

## 1.4 (Jan 18, 2016)

FEATURES:

* You waited for it for a long time. And here you have it: **Neovim support!**
  This is a huge feature. It's fully compatible with Vim and kicks only in if
  vim-go is being used within Neovim. Checkout the full list of changes
  [[GH-607]](https://github.com/fatih/vim-go/pull/607):
  * An async launcher and base foundation was implemented for the `go` command.
  This will be used in the future for all upcoming subcommands of the `go`
  tool.
  * `:GoBuild` is now called asynchronously (it doesn't block the UI anymore).
  * A new `go#jobcontrol#Statusline()` can be used to plug into the statusline.
  This will show the status of the job running asynchronously. The statusline
  is improved to show the status per package instead of file. Assume you have
  three files open, all belonging to the same package, if the package build
  (`:GoBuild`) is successful, all statusline's will be empty (means SUCCESS),
  if it fails all files statusline's will show `FAILED`.
  * `:GoRun` opens a new vertical terminal emulator inside Neovim and runs the
  command there. The terminal mode can be changed with `g:go_term_mode`,
  which is by default `vsplit`. Current options are `vsplit, split or tab`.
  We also have three new mappings to open `:GoRun` command in different
  terminal split modes: `<Plug>(go-run-vertical)`,  `<Plug>(go-run-split)`
  and  `<Plug>(go-run-tab)`
  * `:GoTest`, `:GoTestFunc` and `:GoTestCompile` opens and runs in a new
  terminal. The view mode (split,vertical, tab) is defined with
  `g:go_term_mode`.  The `g:go_term_enabled` setting can be use to change the
  behavior of `:GoTestXXX` commands .If set to `1`, it opens the test
  commands inside a terminal, if not it runs them in background just like
  `:GoBuild` and displays the result in the statusline.
  * We have two settings for terminal sizes: `g:go_term_height` and
  `g:go_term_width`. By default a vertical or horizontal view is equally
  splitted by vim automatically. However with these settings we can for
  example have a terminal with a smaller height when we split it
  horizontally.
  * If a command inside the term fails (such as `go run`, `go test` ...) we
  parse now the errors and list them inside a location list.
* Instead of quickfix window, vim-go now uses the `location list` feature of
  Vim. These are associated with each window independently of each other. This
  enables us to have multiple, independent location lists per window (example
  usages: `:GoBuild` with errors that needs to be fixed, `:GoLint` with
  warnings that we want to check, `:GoReferrers` with a list of referred
  identifiers) [[GH-626]](https://github.com/fatih/vim-go/pull/626)
* a new **`:AsmFmt`** command which is integrated to work with [asmfmt](https://github.com/klauspost/asmfmt) [[GH-673]](https://github.com/fatih/vim-go/pull/673)
* the full identifier information of a completed identifier is echoed in
  statusline. This is very useful to see a function signatures arguments.
  [[GH-685]](https://github.com/fatih/vim-go/pull/685)

IMPROVEMENTS:

* Improve `:GoFmt` by checking if the binary is indeed installed on the system [[GH-617]](https://github.com/fatih/vim-go/pull/617)
* Improve `:GoMetaLinter` by adding the option to run the metalinter on save
  and adding the option to limit the output to the currently active buffer. Set
  `let g:go_metalinter_autosave = 1` to enable autosave and use `let
  g:go_metalinter_autosave_enabled = ['vet', 'golint']` to change your options.
  [[GH-631]](https://github.com/fatih/vim-go/pull/631)
* Improved `:GoDef`. If `vimproc` is installed `godef` will make use of it [[GH-670]](https://github.com/fatih/vim-go/pull/670)
* Improve completion of godoce when vimproc is used [[GH-620]](https://github.com/fatih/vim-go/pull/620)
* Improve internal error matching prodecure to not match false positives [[GH-618]](https://github.com/fatih/vim-go/pull/618)
* A new option to highlight interface variables with `go_highlight_interfaces` [[GH-681]](https://github.com/fatih/vim-go/pull/681)

BUG FIXES

* Fix `:GoFmt` changing the fileformat of the current buffer [[GH-615]](https://github.com/fatih/vim-go/pull/615)
* Fix `:GoRename` to output the original error if parsing fails [[GH-675]](https://github.com/fatih/vim-go/pull/675)
* Fix `:GoTest` to output the original error if parsing fails [[GH-676]](https://github.com/fatih/vim-go/pull/676)
* Fixed `fmt.Fprintln` not to highlight as builtin [[GH-628]](https://github.com/fatih/vim-go/pull/628)
* Fixed wrong highlighting of channels of channels [[GH-678]](https://github.com/fatih/vim-go/pull/678)

## 1.3 (Nov 22, 2015)

FEATURES:

* A new `:GoOracleTags` command was added to pass build tags to Oracle's `-tags` flag. [[GH-573]](https://github.com/fatih/vim-go/pull/573)

IMPROVEMENTS:

* Change `:GoTest` command to timeout after 10 seconds. Vim UI is blocking and
  tests with large running times makes Vim blocking for a long time. This is
  also customizable with the new option `g:go_test_timeout`. [[GH-578]](https://github.com/fatih/vim-go/pull/578)
* Improve `:GoRename` to collect and populate quickfix window with errors.
  [[GH-577]](https://github.com/fatih/vim-go/pull/577)
* Improve `:GoRun` by dropping bad filenames from quickfix window. This allows
  us to have only valid entries which can be jumped to [[GH-547]](https://github.com/fatih/vim-go/pull/547)
* Improve `:GoMetaLinter` quickfix output by using absolute paths. This enables
  us to jump to errors for all cases. [[GH-565]](https://github.com/fatih/vim-go/pull/565)
* Improve `:GoMetaLinter` command by adding a new option
  `g:go_metalinter_deadline` which cancels the linters after 5 seconds
  (previous default).  [[GH-576]](https://github.com/fatih/vim-go/pull/576)
* Improve `:GoMetaLinter` by jumping to the first encountered error from the quickfix window.
* Automatically resize quickfix window based on the number of errors [[GH-602]](https://github.com/fatih/vim-go/pull/602)
* Improve build constraints to show invalid cases (such as `// +buildfoo`, not
  having an empty line between the package statement, etc..). Also add missing
  `GOARCH` values sucha s `arm64`. There are many other useful improvements,
  for more detail please have a look at
  [[GH-589]](https://github.com/fatih/vim-go/pull/589)
* Add support for all values of `GOARCH` [[GH-601]](https://github.com/fatih/vim-go/pull/601)
* Add note about Syntastic usage as this problem comes up a lot [[GH-580]](https://github.com/fatih/vim-go/pull/580)
* Add note about `:GoUpdateBinaries` [[GH-606]](https://github.com/fatih/vim-go/pull/606)

BUG FIXES:

* Fixed `:GoErrCheck` showing the correct output when executed inside the source folder [[GH-564]](https://github.com/fatih/vim-go/pull/564)
* Fixed `:GoBuild` by not using `/dev/null` anymore for build output (not
  supported by `go`). We pass a temporary file now. [[GH-567]](https://github.com/fatih/vim-go/pull/567)
* Fixed `:GoFmt` passing `g:go_fmt_options` options to `goimports`. This option
  is only valid with `gofmt`. [[GH-590]](https://github.com/fatih/vim-go/pull/590)
* Fix vim-go for `cygwin` users. [[GH-575]](https://github.com/fatih/vim-go/pull/575)
* Fixed identifier in template files to be highlighted correctly [[GH-559]](https://github.com/fatih/vim-go/pull/559)
* Fixed character region in template files to be highlighted correctly [[GH-603]](https://github.com/fatih/vim-go/pull/603)
* Fixed variables in template files to be highlighted correctly [[GH-611]](https://github.com/fatih/vim-go/pull/611)
* Do not treat builtins as keywords. Now `make` will not highlighted but
  `make()` will be highlighted (gh-605)

## 1.2 (Oct 2, 2015)

FEATURES:

* A new `:GoMetaLinter` command which invokes [gometalinter](https://github.com/alecthomas/gometalinter). Please check the PR [[GH-553]](https://github.com/fatih/vim-go/pull/553) for more detail on customizing and usage of `:GoMetaLinter`.

IMPROVEMENTS:

* Improve `:GoImport` to trim spaces when including import paths of form `"fmt "`
* Avoid setting `filetype` twice. Previously it was doing it twice, which was expensive
* Improve handling of GOPATH's with trailing `/` characters, such as `/home/user/go/`
* Add a new `g:go_highlight_string_spellcheck` feature, which is enabled by feature. Now if spell is enabled, go strings are also checked.
* Specify our limited but functional [gb](http://getgb.io/) support

BUG FIXES:
* Fixed `:GoRun` to display errors when `g:go_dispatch_enabled` was enabled
* Fixed `:GoDrop` displaying "Not enough arguments" (regression)
* Fixed `:GoErrCheck` not showing `PASS` message if the command was successful
* Fixed `:GoErrCheck` not executing in the directory of the currently edited file
* Close quickfix window after a successful second round of `:GoInstall`
* Fix passing files rather than packages to certain oracle commands.
* Escape files passed to oracle command. This could lead to some serious things.
* Clear `g:go_oracle_scope` when the scope was reseted. Previously it was set to empty string, which was causing false positives.
* Correct various misspellings.

## 1.1 (Jul 25, 2015)

With this release the version will now increase in `minor` levels. So the next
release will be `1.2`, the other one `1.3`, etc.. This provides us more
flexibility (like releasing patch versions if needed).

FEATURES:
* A new `:GoGenerate` command is now available which can be used to invoke `go generate` within vim
* Vim-go didn't had any license, now we use BSD 3-Clause License (the same as Go). This is needed for Linux distributions to package vim-go and is also something that people asked for.

IMPROVEMENTS:
* Improve commands `GoRun, GoTest{,Func,Compile}, GoCoverage,
  GoGenerate, GoErrcheck, GoLint, and GoVet` to handle multiple arguments.
  Previously this feature was limited to only certain commands. What this means
  is, for example `:GoVet . -all` will invoke `go tool vet . -all`
  automatically instead of plan `go vet`. This is one of the big changes in
  this release, so give it a try :)
* Improved `:GoFmt` command, which now uses the `-w` flag to
  write to the source code directly, instead of outputting it to stdout. This
  makes `:GoFmt` much more faster than the current implementation. This is one
  of the big changes in this release, so feedback is welcome!
* Improve `:GoImport` to have a `!` feature. Now when when called
  with a `!` appended it will go get it. i.e: `:GoImport!
  github.com/fatih/color`. Useful if `:GoImport` fails and you want to download
  it.
* Automatic GOPATH detections can now detect `gb` vendored folders. Some commands should now work without any problem when invoked on a `gb` project.
* All command arguments are now properly escaped for shell invocation.
* Added the `-f` flag to :GoInstallBinaries command to support `git url.<base>.insteadOf` configuration
* Improve width and precision highlighting, such as `%s %5s %-5s %5.5f %.5f`
* Show an error if a region is not selected when `:GoFreeVars` is called

BUG FIXES:
* Fix`:GoDef` for files containing spaces. We know escape the files before passing to `:GoDef`
* Fix `:GoFmt` not picking up the correct GOPATH when the fmt command was set to `goimports`
* Fix and simplify README.md, add Wiki reference
* Fixed tagbar integration to show correct imports.


## 1.0.5 (May 26, 2015)

FEATURES:
* A new `:GoOracleScope` is added to change the oracle scope on-the-fly. It
  accepts import paths as arguments. If no arguments are passed it prints the
  current custom oracle scope. `:GoOracleScope` also supports completion of
  import paths, so it's very fast and handy to use. `:GoOracleScope ""` clears
  the current custom scope.
* A new `:GoPath` command that displays the current `GOPATH`. A path can be
  passed to change the `GOPATH` (i.e `:GoPath ~/foo/src`). `:GoPath ""` clears
  and resets the `GOPATH` to the initial value.
* A new "autodetect GOPATH" feature is added. This automatically detects if the
  project is using `godep` or is under a `src` root directory which is not in
  `GOPATH` and changes/modifies the `GOPATH` so all commands work based on this
  GOPATH. What this means is, commands such as `:GoDef`, `:GoBuild`, etc.. will
  include the Godeps folder. For example any go-to-definition via `:GoDef` will
  jump to the source code inside Godeps. This is enabled by default, but can
  disabled with `let g:go_autodetect_gopath = 0`. This new feature is also the
  foundation for other tools such as `gb` or `wgo`.

IMPROVEMENTS:
* Improve `:GoFmt` (gofmt and goimports) speed. Now it's 2x faster than the previous implementation.
* Add Dispatch support for `:GoBuild` and `:GoRun`. For more info about
  dispatch see https://github.com/tpope/vim-dispatch . By default it's
  disabled, to enable it add `let g:go_dispatch_enabled = 1` to your vimrc.
* Add support for the bang `!` attribute for all `go` tool commands. What this
  does it, if `:GoBuild` is called it will jump to the error. But `:GoBuild!`
  will not jump to any error. This has the same behavior as the internal
  `:make` command in vim. We had this feature already for `:GoBuild` and
  `:GoRun`. But not for `:GoInstall`, `:GoTest`, etc.. Now all commands are
  unified.
* Add autojump to error for `:GoInstall`.
* Add autowrite feature for `:GoInstall`, `:GoTestXXX` functions and `:GoVet`
* Support `git url.<base>.insteadOf` and custom import paths of binaries. This
  improves the commands `:GoInstallBinaries` and `:GoUpdateBinaries`.
* Add support for highlighting go templates with `*.tmpl` extensions. Based on
  the work from @cespare from https://github.com/cespare/vim-go-templates

BUG FIXES:
* Fix clearing the status bar when `:GoErrCheck` is called
* Fix godocNotFound to not match 'os' pkg contents. This improves the command
  `:GoDoc`
* Fix parsing and jumping to error locations when used Vim from a different
  directory than the current buffer's directory
* Fix completion showing duplicates paths for completion results, such as
  github.com/fatih/color and github.com/fatih/color/.

## 1.0.4 (Apr 28, 2015)

FEATURES:

* A new `:GoTestFunc` command (with appropriate
  mappings) is added. Run tests function which surrounds the current cursor
  location. Useful to test single tests.
* Highlight all Go operators. Previously not all
  operators were highlighted. As previously, to highlight options, enable it
  with by setting `g:go_highlight_operators` to 1 in your vimrc.

IMPROVEMENTS:

* Improved certain `:GoDoc` usages to show a better error message
* Improved `:GoRename` to have a default value for rename input. Avoids retyping similar words.
* Synced with latest Oracle version. `callgraph` is removed.
* Removed our custom referrers mode. New version of oracle now displays the matching lines.

BUG FIXES:

* Fixed the internal `executeInDir` function which was failing when ignorelist was not set properly.
* Fixed trailing slash for package completion with `:GoImport`
* Fixed paths in error list for Windows users.
* Fixed not showing "import cycle not allowed" error message when called `:GoBuild` or `:GoRun`
* Fixed users using vimproc requiring arguments to functions to be escaped.
* Fixed depth for test snippets
* Fixed neosnippet support loading snippet files the second time if necessary.

## 1.0.3 (Mar 7, 2015)

FEATURES:
* A new `:GoTestCompile` command (with appropriate mappings) is added. Useful to compile a test binary or show/fix compile errors in quickfix window

IMPROVEMENTS:
* `referrer` mode is improved to show referring lines in the quickfix window
* A new `errt` snippet is added, which expands to `if err != nil { t.Fatal(err) }`
* A new `errh` snippet is added, useful to be used in a `http.Handler`
* UltiSnips snippets are improved to take advance of Vim's `Visual` mode. For example selecting a block and typing `if` will create an if scope around the block.
* Cleanup README.md

BUG FIXES:
* Fix trimming brackets if completion was invoked on a previous completion
* Fix Oracle scope settings. Added docs about usage.
* Fixed previously broken `var` and `vars` snippets
* Fix duplicate docs
* Fix fallback binary path for Windows users. The fallback mechanism is used to discover the necessary Go tools, such as `godef`, `gocode`, etc...

## 1.0.2 (Feb 17, 2015)

FEATURES:

* New snippets are added, mostly for testing ( [changes](https://github.com/fatih/vim-go/pull/321/files))

IMPROVEMENTS:

* Enable all Oracle commands. Docs, mappings and commands are also added. It uses Quickfix list instead of a custom UI.
* Clarify installation process in Readme, add instructions for vim-plug, NeoBundle and manual.

BUG FIXES:

* Fix shiftwidth parsing, it was broken in the previous release for old Vim versions
* Fix experimantal mode


## 1.0.1 (Feb 9, 2015)

FEATURES:

* New feature to highlight build constraints (disabled by default)

IMPROVEMENTS:

* Updated godef import path
* Updated Readme for possible problems with `csh`
* Documentation for text objects are updated, typo fixes are merged
* If vimproc is installed, Windows users will use it for autocompletion
* Improve UltiSnips snippets to pick Visual selection (demo: http://quick.as/0dvigz5)
* Packages with extensions, like "gopkg.in/yaml.v2" can be now displayed
* Packages with different import paths, like "github.com/bitly/go-simplejson" can be now displayed

BUG FIXES:

* Fatal errors are now parsed successfully and populated to quickfix list
* Shiftwidth is changed to use shiftwidth() function. Fixes usage with plugins like vim-sleuth and possible mis usage (like setting shiftwidth to zero)
* Added a new [Donation](https://github.com/fatih/vim-go#donations) section to Readme, for those who ask for it.
* Fix parsing of errcheck error syntax
* Fix consistency between Neosnippet and UltiSnips snippets


## 1.0 (Dec 24, 2014)

We don't tag any changes or releases, so let's start with `1.0`. Our Windows
support is now in a good shape, tons of bugs are fixed, many new features and
improvements is being added and it's getting better with each day (thanks to
the community contributions).

## 0.0 (Mar 24, 2014)

Initial commit: https://github.com/fatih/vim-go/commit/78c5caa82c111c50e9c219f222d65b07694f8f5a

<!--
 vim: et ts=2 sw=2
-->
