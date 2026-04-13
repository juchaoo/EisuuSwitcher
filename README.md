# EisuuSwitcher（中/日/E readme only）

## 软件简介

EisuuSwitcher 是一款专为 macOS 设计的输入法快速切换工具，允许您通过按英数键（keycode 102）快速切换到您选择的默认输入法（如微信输入法）。

## 安装方法

### 1. 编译应用程序（还未上传项目）

- 打开 Xcode 项目 `EisuuSwitcher.xcodeproj`
- 选择目标设备为 "My Mac"
- 点击 "Run" 按钮或按 `Cmd+R` 编译并运行应用程序

### 2. 手动运行

- 编译完成后，应用程序会自动运行
- 应用程序会在状态栏中显示一个带有 "あ" 字样的图标

## 首次使用

### 1. 选择默认输入法

- 首次运行时，应用程序会自动弹出输入法选择菜单
- 从列表中选择您想要默认切换到的输入法（如微信输入法）
- 点击选择后，应用程序会记住您的选择

### 2. 授权辅助功能权限

- 首次运行时，系统会提示您授予辅助功能权限
- 请在系统设置的 "安全性与隐私" → "隐私" → "辅助功能" 中启用 EisuuSwitcher
- 这是确保软件能够监听键盘事件的必要权限

## 日常使用

### 1. 切换输入法

- 当您需要切换到默认输入法时，按英数键（通常位于键盘右上角）
- 软件会自动切换到您之前选择的默认输入法（如微信输入法）
- 切换过程中，软件会短暂切换到访达，然后切回当前应用，以确保输入法切换生效（窗口闪一下是正常的！）

### 2. 重新选择输入法

- 点击状态栏中的 "あ" 图标
- 选择 "重新选择输入法" 选项
- 从弹出的菜单中选择新的默认输入法

### 3. 退出软件

- 点击状态栏中的 "あ" 图标
- 选择 "退出" 选项

## 开机启动设置

### 1. 启用开机启动

- 点击状态栏中的 "あ" 图标
- 选择 "开机启动" 选项，使其状态变为勾选
- 这样，软件会在系统启动时自动运行

### 2. 禁用开机启动

- 点击状态栏中的 "あ" 图标
- 再次选择 "开机启动" 选项，使其状态变为未勾选
- 这样，软件不会在系统启动时自动运行


## 常见问题及解决方案

### 1. 输入法切换后实际输入没生效

- 软件已经通过切换到访达然后切回的方式解决了这个问题
- 确保您已经授予了辅助功能权限
- 如果问题仍然存在，尝试重新选择默认输入法

### 2. 软件在 Dock 中显示图标

- 不会显示在dock

### 3. 按英数键没有反应

- 检查是否已授予辅助功能权限
- 确认英数键的 keycode 是否为 102（可在系统设置中查看）
- 尝试重新启动软件

## 注意事项

### 1. 权限要求

- 软件需要辅助功能权限才能监听键盘事件
- 请确保在系统设置中启用了相关权限

### 2. 兼容性

- 软件适用于 macOS 系统
- 已在最新版本的 macOS 上测试通过

### 3. 性能影响

- 软件运行时占用资源较少，不会影响系统性能
- 切换应用的过程是瞬间完成的，不会明显影响用户体验

### 4. 稳定性

- 软件采用了可靠的输入法切换机制，确保切换操作的稳定性
- 如果遇到任何问题，尝试重新启动软件或重新选择默认输入法

## 技术原理

EisuuSwitcher 通过以下步骤确保输入法切换生效：
1. 监听英数键的按下事件
2. 调用系统 API 切换到用户选择的默认输入法
3. 短暂切换到系统偏好设置或访达，然后切回当前应用
4. 再次切换输入法，确保切换操作完全生效

这种方法可以强制系统重新处理输入法状态，解决了从日语输入法切换回其他输入法时可能出现的生效问题。

## 项目结构

```
EisuuSwitcher/
├── EisuuSwitcher/
│   ├── App.swift
│   ├── InputSwitcher.swift
│   ├── InputSourceManager.swift
│   ├── ViewController.swift
│   ├── Info.plist
│   └── Assets.xcassets/
│       ├── AppIcon.appiconset/
│       └── AccentColor.colorset/
├── EisuuSwitcher.xcodeproj/
└── README.md
```

## 许可证

本项目仅供学习和个人使用。

## 贡献

欢迎提交问题和改进建议！

---

希望本使用说明能够帮助您顺利使用 EisuuSwitcher 软件。如果您有任何其他问题或建议，欢迎反馈。

---

## 日本語版

# EisuuSwitcher

## ソフトウェアの概要

EisuuSwitcher は macOS 用の入力方法切り替えツールで、英数キー（keycode 102）を押すことで、選択したデフォルト入力方法（WeChat 入力法など）に素早く切り替えることができます。

## インストール方法

### 1. アプリケーションをコンパイルする

- Xcode プロジェクト `EisuuSwitcher.xcodeproj` を開く
- ターゲットデバイスを "My Mac" に設定する
- "Run" ボタンをクリックするか、`Cmd+R` を押してアプリケーションをコンパイルして実行する

### 2. 手動で実行する

- コンパイルが完了すると、アプリケーションが自動的に実行されます
- アプリケーションはステータスバーに "あ" という文字のアイコンを表示します

## 初回使用

### 1. デフォルト入力方法を選択する

- 初回実行時、アプリケーションは自動的に入力方法選択メニューを表示します
- デフォルトで切り替えたい入力方法（WeChat 入力法など）をリストから選択します
- 選択すると、アプリケーションが選択を記憶します

### 2. アクセシビリティ権限を付与する

- 初回実行時、システムはアクセシビリティ権限の付与を要求します
- システム設定の「セキュリティとプライバシー」→「プライバシー」→「アクセシビリティ」で EisuuSwitcher を有効にしてください
- これはソフトウェアがキーボードイベントを監視できるようにするために必要な権限です

## 日常使用

### 1. 入力方法を切り替える

- デフォルト入力方法に切り替えたいときは、英数キー（通常はキーボードの右上隅にあります）を押します
- ソフトウェアは自動的に以前に選択したデフォルト入力方法（WeChat 入力法など）に切り替えます
- 切り替えの過程で、ソフトウェアはFinderに一時的に切り替えてから現在のアプリケーションに戻るため、入力方法の切り替えが確実に有効になります（ウィンドウが一瞬点滅するのは正常です！）

### 2. 入力方法を再選択する

- ステータスバーの "あ" アイコンをクリックします
- 「再選択输入法」オプションを選択します
- 表示されたメニューから新しいデフォルト入力方法を選択します

### 3. ソフトウェアを終了する

- ステータスバーの "あ" アイコンをクリックします
- 「退出」オプションを選択します

## 起動時に自動実行する設定

### 1. 起動時に自動実行を有効にする

- ステータスバーの "あ" アイコンをクリックします
- 「开机启动」オプションを選択し、チェック状態にします
- これにより、ソフトウェアがシステム起動時に自動的に実行されます

### 2. 起動時に自動実行を無効にする

- ステータスバーの "あ" アイコンをクリックします
- 「开机启动」オプションを再度選択し、チェック状態を解除します
- これにより、ソフトウェアがシステム起動時に自動的に実行されなくなります

## よくある問題と解決策

### 1. 入力方法が切り替わったが実際の入力が有効にならない

- ソフトウェアはFinderに切り替えてから戻ることでこの問題を解決しています
- アクセシビリティ権限が付与されていることを確認してください
- 問題が解決しない場合は、デフォルト入力方法を再選択してみてください

### 2. ソフトウェアがDockに表示される

- Dockには表示されません

### 3. 英数キーを押しても反応がない

- アクセシビリティ権限が付与されていることを確認してください
- 英数キーのkeycodeが102であることを確認してください（システム設定で確認できます）
- ソフトウェアを再起動してみてください

## 注意事項

### 1. 権限の要求

- ソフトウェアはキーボードイベントを監視するためにアクセシビリティ権限が必要です
- システム設定で関連する権限を有効にしてください

### 2. 互換性

- ソフトウェアはmacOSシステムに対応しています
- 最新バージョンのmacOSでテスト済みです

### 3. パフォーマンスへの影響

- ソフトウェアの実行中のリソース使用率は低く、システムパフォーマンスに影響を与えません
- アプリケーションの切り替えは瞬時に完了し、ユーザーエクスペリエンスに明らかな影響を与えません

### 4. 安定性

- ソフトウェアは信頼性の高い入力方法切り替えメカニズムを採用しており、切り替え操作の安定性を確保しています
- 問題が発生した場合は、ソフトウェアを再起動するか、デフォルト入力方法を再選択してみてください

## 技術原理

EisuuSwitcher は以下の手順で入力方法の切り替えを確実にする：
1. 英数キーの押下イベントを監視する
2. システムAPIを呼び出して、ユーザーが選択したデフォルト入力方法に切り替える
3. システム環境設定またはFinderに一時的に切り替えた後、現在のアプリケーションに戻る
4. 入力方法を再度切り替えて、切り替え操作が完全に有効になるようにする

この方法により、システムに入力方法の状態を再処理させることができ、日本語入力方法から他の入力方法に切り替えたときに発生する可能性のある有効性の問題を解決します。

---

## English Version

# EisuuSwitcher

## Software Introduction

EisuuSwitcher is a keyboard input method switching tool designed for macOS, allowing you to quickly switch to your selected default input method (such as WeChat Input Method) by pressing the Eisu key (keycode 102).

## Installation Method

### 1. Compile the Application

- Open the Xcode project `EisuuSwitcher.xcodeproj`
- Select the target device as "My Mac"
- Click the "Run" button or press `Cmd+R` to compile and run the application

### 2. Run Manually

- After compilation is complete, the application will run automatically
- The application will display an icon with the character "あ" in the status bar

## First-time Use

### 1. Select Default Input Method

- When running for the first time, the application will automatically display the input method selection menu
- Select the input method you want to switch to by default (such as WeChat Input Method) from the list
- After selection, the application will remember your choice

### 2. Authorize Accessibility Permissions

- When running for the first time, the system will prompt you to grant accessibility permissions
- Please enable EisuuSwitcher in System Settings → "Security & Privacy" → "Privacy" → "Accessibility"
- This is a necessary permission to ensure the software can monitor keyboard events

## Daily Use

### 1. Switch Input Method

- When you need to switch to the default input method, press the Eisu key (usually located in the upper right corner of the keyboard)
- The software will automatically switch to the default input method you selected earlier (such as WeChat Input Method)
- During the switching process, the software will briefly switch to Finder and then return to the current application to ensure the input method switch takes effect (it's normal for the window to flash!)

### 2. Re-select Input Method

- Click the "あ" icon in the status bar
- Select the "重新选择输入法" (Re-select Input Method) option
- Select a new default input method from the pop-up menu

### 3. Exit Software

- Click the "あ" icon in the status bar
- Select the "退出" (Exit) option

## Startup Settings

### 1. Enable Startup at Login

- Click the "あ" icon in the status bar
- Select the "开机启动" (Startup at Login) option to check it
- This way, the software will run automatically when the system starts

### 2. Disable Startup at Login

- Click the "あ" icon in the status bar
- Select the "开机启动" (Startup at Login) option again to uncheck it
- This way, the software will not run automatically when the system starts

## Common Issues and Solutions

### 1. Input Method Switches but Actual Input Doesn't Work

- The software has solved this problem by switching to Finder and then returning
- Ensure you have granted accessibility permissions
- If the problem persists, try re-selecting the default input method

### 2. Software Displays in Dock

- It will not display in the Dock

### 3. No Response When Pressing Eisu Key

- Check if accessibility permissions have been granted
- Confirm if the Eisu key's keycode is 102 (can be checked in system settings)
- Try restarting the software

## Notes

### 1. Permission Requirements

- The software needs accessibility permissions to monitor keyboard events
- Please ensure relevant permissions are enabled in system settings

### 2. Compatibility

- The software is suitable for macOS systems
- Tested on the latest version of macOS

### 3. Performance Impact

- The software consumes minimal resources during operation and does not affect system performance
- The application switching process is completed instantly and does not significantly affect user experience

### 4. Stability

- The software adopts a reliable input method switching mechanism to ensure the stability of switching operations
- If you encounter any issues, try restarting the software or re-selecting the default input method

## Technical Principle

EisuuSwitcher ensures input method switching takes effect through the following steps:
1. Monitor the press event of the Eisu key
2. Call system API to switch to the user-selected default input method
3. Briefly switch to System Preferences or Finder, then return to the current application
4. Switch the input method again to ensure the switching operation is fully effective

This method forces the system to reprocess the input method state, solving the activation issue that may occur when switching from Japanese input method to other input methods.

