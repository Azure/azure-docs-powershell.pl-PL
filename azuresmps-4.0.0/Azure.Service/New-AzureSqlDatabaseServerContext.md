---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7B29875-D2E5-4E96-AD4B-83032AB18D02
online version: ''
schema: 2.0.0
ms.openlocfilehash: cdcd4788e3eefdce858cb88c0bf1885353f8a673
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054936"
---
# New-AzureSqlDatabaseServerContext

## STRESZCZENIe
Tworzy kontekst połączenia z serwerem.

## POLECENIA

### ByServerNameWithSqlAuth (domyślny)
```
New-AzureSqlDatabaseServerContext -ServerName <String> -Credential <PSCredential> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### ByManageUrlWithSqlAuth
```
New-AzureSqlDatabaseServerContext [-ServerName <String>] -ManageUrl <Uri> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByServerNameWithCertAuth
```
New-AzureSqlDatabaseServerContext -ServerName <String> [-UseSubscription] [-SubscriptionName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByFullyQualifiedServerNameWithSqlAuth
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByFullyQualifiedServerNameWithCertAuth
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> [-UseSubscription]
 [-SubscriptionName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzureSqlDatabaseServerContext** służy do tworzenia kontekstu połączenia serwera bazy danych Azure SQL Server.
Użyj uwierzytelniania programu SQL Server, aby utworzyć kontekst połączenia z serwerem bazy danych SQL, używając określonych poświadczeń.
Możesz określić serwer bazy danych SQL według nazwy, w pełni kwalifikowanej nazwy lub według adresu URL.
Aby uzyskać poświadczenie, użyj polecenia cmdlet Get-Credential, w którym jest wyświetlany monit o określenie nazwy użytkownika i hasła.

Użyj polecenia cmdlet **New-AzureSqlDatabaseServerContext** z uwierzytelnianiem opartym na certyfikatach, aby utworzyć kontekst połączenia dla określonego serwera bazy danych SQL, używając określonych danych subskrypcji platformy Azure.
Możesz określić serwer bazy danych SQL według nazwy lub w pełni kwalifikowanej nazwy.
Możesz określić dane abonamentu jako parametr lub można go pobrać z bieżącej subskrypcji platformy Azure.
Użyj polecenia cmdlet Select-AzureSubscription https://msdn.microsoft.com/library/windowsazure/jj152833.aspx w celu wybrania bieżącej subskrypcji platformy Azure.

## Przykłady

### Przykład 1. Tworzenie kontekstu za pomocą uwierzytelniania programu SQL Server
```
PS C:\> $Credential = Get-Credential
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -Credential $Credential
PS C:\> $Database17 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database17" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

W tym przykładzie użyto uwierzytelniania programu SQL Server.

Pierwsze polecenie monituje o podanie poświadczeń administratora serwera i zapisuje poświadczenia w zmiennej $Credential.

Drugie polecenie nawiązuje połączenie z serwerem bazy danych SQL o nazwie lpqd0zbr8y przy użyciu $Credential.

Polecenie ostatnie tworzy bazę danych o nazwie Database17 na serwerze, który jest częścią kontekstu w $Context.

### Przykład 2: Tworzenie kontekstu przy użyciu uwierzytelniania opartego na certyfikatach
```
PS C:\> $SubscriptionId = <Subscription ID>
PS C:\> $Thumbprint = <Certificate Thumbprint>
PS C:\> $Certificate = Get-Item "Cert:\CurrentUser\My\$Thumbprint"
PS C:\> Set-AzureSubscription -SubscriptionName "Subscription07" -SubscriptionId $SubscriptionId -Certificate $Certificate
PS C:\> Select-AzureSubscription -SubscriptionName "Subscription07"
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -UseSubscription
```

W tym przykładzie użyto uwierzytelniania opartego na certyfikatach.

Pierwsze dwa polecenia przypisują wartości do zmiennych $SubscriptionId i $Thumbprint.

Trzecia komenda uzyskuje certyfikat zidentyfikowany przez odcisk palca w $Thumbprint i zapisuje go w $Certificate.

Czwarte polecenie ustawia abonament na Subscription07, a w piątym poleceniu jest wybrana ta subskrypcja.

Polecenie ostatnie powoduje utworzenie kontekstu w bieżącej subskrypcji dla serwera o nazwie lpqd0zbr8y.

## PARAMETRÓW

### — Poświadczenie
Określa obiekt poświadczeń, który umożliwia uwierzytelnianie programu SQL Server w celu uzyskania dostępu do serwera.

```yaml
Type: PSCredential
Parameter Sets: ByServerNameWithSqlAuth, ByManageUrlWithSqlAuth, ByFullyQualifiedServerNameWithSqlAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FullyQualifiedServerName
Określa w pełni kwalifikowaną nazwę domeny (FQDN) dla serwera bazy danych SQL Azure.
Na przykład Server02.database.windows.net.

```yaml
Type: String
Parameter Sets: ByFullyQualifiedServerNameWithSqlAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManageUrl
Określa adres URL używany przez ten aplet polecenia w celu uzyskania dostępu do portalu usługi Azure SQL DatabaseManagement dla serwera.

```yaml
Type: Uri
Parameter Sets: ByManageUrlWithSqlAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.
Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nazwa_serwera
Określa nazwę serwera bazy danych.

```yaml
Type: String
Parameter Sets: ByServerNameWithSqlAuth, ByServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByManageUrlWithSqlAuth
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Subscriptionname
Określa nazwę subskrypcji platformy Azure używanej przez to polecenie cmdlet do tworzenia kontekstu połączenia.
Jeśli nie określisz wartości dla tego parametru, polecenie cmdlet użyje bieżącej subskrypcji.
Uruchom polecenie cmdlet Select-AzureSubscription, aby zmienić bieżącą subskrypcję.

```yaml
Type: String
Parameter Sets: ByServerNameWithCertAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UseSubscription
Wskazuje, że w tym poleceniu cmdlet jest używany abonament platformy Azure służący do tworzenia kontekstu połączenia.

```yaml
Type: SwitchParameter
Parameter Sets: ByServerNameWithCertAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

### Microsoft. platformy windowsazure. Commands. SQLDatabase. Services. Server. IServerDataServiceContext

## INFORMACYJN
* Jeśli uwierzytelniasz bez określania domeny, a jeśli korzystasz z programu Windows PowerShell 2,0, polecenie cmdlet Get-Credential zwraca ukośnik odwrotny ( \\ ) poprzedzony znakiem username (), na przykład \User. Program Windows PowerShell 3,0 nie dodaje ukośnika odwrotnego. Ten ukośnik nie jest rozpoznawany przez parametr *Credential* polecenia cmdlet **New-AzureSqlDatabaseServerContext** . Aby ją usunąć, Użyj poleceń podobnych do następujących:

  `PS C:\\\> $Credential = Get-Credential`
`PS C:\\\> $Credential = New-Object -TypeName 'System.Management.Automation.PSCredential' -ArgumentList $Credential.Username.Replace("\",""),$Credential.Password`

## LINKI POKREWNE

[Polecenia cmdlet usługi Azure SQL Database](./Azure.SQLDatabase.md)

[Get-AzureSqlDatabase](./Get-AzureSqlDatabase.md)

[Nowe — AzureSqlDatabase](./New-AzureSqlDatabase.md)

[Remove-AzureSqlDatabase](./Remove-AzureSqlDatabase.md)

[Set-AzureSqlDatabase](./Set-AzureSqlDatabase.md)


