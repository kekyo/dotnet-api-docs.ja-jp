> [!NOTE]
> .NET Core 2.0 以降では、次のように実行する必要ありません[ `dotnet restore` ](~/docs/core/tools/dotnet-restore.md)実行されるため、暗黙的にすべてのコマンドによってなど`dotnet build`と`dotnet run`、発生するために復元を必要とします。 これがここで、明示的な復元を行って、意味の特定のシナリオで有効なコマンドなど[Visual Studio Team Services での継続的インテグレーション ビルド](/vsts/build-release/apps/aspnet/build-aspnet-core)または明示的にする時間を制御する必要があるビルド システムで、復元が発生します。
