# Tutorial-BlazorWebAssembly

Blazor WebAssembly でアプリを作る

## [.Net Core 3.1 SDK](https://dotnet.microsoft.com/download/dotnet-core/3.1)のインストール

https://download.visualstudio.microsoft.com/download/pr/5aad9c2c-7bb6-45b1-97e7-98f12cb5b63b/6f6d7944c81b043bdb9a7241529a5504/dotnet-sdk-3.1.102-win-x64.exe

## [Blazor WebAssembly](https://docs.microsoft.com/ja-jp/aspnet/core/blazor/hosting-models?view=aspnetcore-3.1#blazor-webassembly) テンプレートのインストール

```ps
dotnet new -i Microsoft.AspNetCore.Blazor.Templates::3.2.0-preview1.20073.1
```

## Blazor プロジェクトの作成

```ps
dotnet new blazorwasm -o MyApp
cd MyApp
dotnet run
```

## 動作確認

[https://localhost:5000](https://localhost:5000)

## Item の追加

### ページの追加

以下のページを追加

- `Pages\Item.razor`

以下のファイルを開き、ナビゲーションにメニュー項目を追加

- `Shared\NavMenu.razor`

### モデルの追加

以下のファイルを追加

- `Item.cs`

## ローカルストレージを利用した永続化

[Blazored/LocalStorage](https://github.com/Blazored/LocalStorage) をインストールして、ローカルストレージを利用した永続化を行う

```ps
$ dotnet add package Newtonsoft.Json
$ dotnet add package Blazored.LocalStorage
```

- `Program.cs`

```cs
using Blazored.LocalStorage;

            builder.Services.AddBlazoredLocalStorage();
```

- `Pages\Item.razor`

---

Copyright (c) 2020 YA-androidapp(https://github.com/YA-androidapp) All rights reserved.
