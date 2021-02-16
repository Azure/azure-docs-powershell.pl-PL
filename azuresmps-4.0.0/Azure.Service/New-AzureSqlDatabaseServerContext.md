---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7B29875-D2E5-4E96-AD4B-83032AB18D02
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5312556cb49d02ea901b4cb2526a36f7237f66d1
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100404177"
---
# New-AzureSqlDatabaseServerContext

## SYNOPSIS
Tworzy kontekst połączenia z serwerem.

## SKŁADNIA

### ByServerNameWithSqlAuth (Domyślne)
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

## OPIS
Polecenie **cmdlet New-AzureSqlDatabaseServerContext** tworzy kontekst połączenia z serwerem usługi Azure SQL Database.
Uwierzytelnianie programu SQL Server umożliwia utworzenie kontekstu połączenia z serwerem bazy danych SQL przy użyciu określonych poświadczeń.
Serwer bazy danych SQL można określić według nazwy, w pełni kwalifikowanej nazwy lub adresu URL.
Aby uzyskać poświadczenia, użyj polecenia cmdlet Get-Credential monit o podanie nazwy użytkownika i hasła.

Użyj polecenia cmdlet **New-AzureSqlDatabaseServerContext** z uwierzytelnianiem opartym na certyfikatach, aby utworzyć kontekst połączenia z określonym serwerem bazy danych SQL przy użyciu określonych danych subskrypcji platformy Azure.
Serwer bazy danych SQL można określić według nazwy lub w pełni kwalifikowanej nazwy.
Możesz określić dane subskrypcji jako parametr lub pobrać je z bieżącej subskrypcji platformy Azure.
Użyj polecenia cmdlet Select-AzureSubscription, https://msdn.microsoft.com/library/windowsazure/jj152833.aspx aby wybrać bieżącą subskrypcję platformy Azure.

## PRZYKŁADY

### Przykład 1. Tworzenie kontekstu przy użyciu uwierzytelniania programu SQL Server
```
PS C:\> $Credential = Get-Credential
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -Credential $Credential
PS C:\> $Database17 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database17" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

W tym przykładzie użyto uwierzytelniania programu SQL Server.

Pierwsze polecenie monituje o poświadczenia administratora serwera i zapisuje poświadczenia w $Credential danych.

Drugie polecenie łączy się z serwerem bazy danych SQL o nazwie lpqd0zbr8y przy użyciu $Credential.

Ostatnie polecenie tworzy na serwerze bazę danych o nazwie Database17, która stanowi część kontekstu w $Context.

### Przykład 2. Tworzenie kontekstu przy użyciu uwierzytelniania na podstawie certyfikatu
```
PS C:\> $SubscriptionId = <Subscription ID>
PS C:\> $Thumbprint = <Certificate Thumbprint>
PS C:\> $Certificate = Get-Item "Cert:\CurrentUser\My\$Thumbprint"
PS C:\> Set-AzureSubscription -SubscriptionName "Subscription07" -SubscriptionId $SubscriptionId -Certificate $Certificate
PS C:\> Select-AzureSubscription -SubscriptionName "Subscription07"
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -UseSubscription
```

W tym przykładzie jest używane uwierzytelnianie na podstawie certyfikatu.

Pierwsze dwa polecenia przypiszą wartości do zmiennych $SubscriptionId i $Thumbprint zmiennych.

Trzecie polecenie pobiera certyfikat oznaczony kciukiem w programie $Thumbprint i przechowuje go w $Certificate.

Czwarte polecenie ustawia subskrypcję jako subskrypcję 07, a piąte polecenie wybiera tę subskrypcję.

Ostatnie polecenie tworzy kontekst w bieżącej subskrypcji dla serwera o nazwie lpqd0zbr8y.

## PARAMETERS

### - Credential
Określa obiekt poświadczeń, który zapewnia uwierzytelnianie programu SQL Server w celu uzyskania dostępu do serwera.

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
Określa w pełni kwalifikowaną nazwę domeny (FQDN) dla serwera usługi Azure SQL Database.
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

### - ManageUrl
Określa adres URL używany przez to polecenie cmdlet do uzyskiwania dostępu do portalu Azure SQL DatabaseManagement dla serwera.

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

### — Profil
Określa profil platformy Azure, z którego będzie odczytywane to polecenie cmdlet.
Jeśli nie określisz profilu, to polecenie cmdlet zostanie odczytane z lokalnego profilu domyślnego.

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

### -ServerName
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

### -SubscriptionName
Określa nazwę subskrypcji platformy Azure, za pomocą których to polecenie cmdlet tworzy kontekst połączenia.
Jeśli nie określisz wartości dla tego parametru, polecenie cmdlet użyje bieżącej subskrypcji.
Uruchom Select-AzureSubscription cmdlet, aby zmienić bieżącą subskrypcję.

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

### —UseSubscription
Wskazuje, że to polecenie cmdlet tworzy kontekst połączenia za pomocą subskrypcji platformy Azure.

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

## OUTPUTS

### Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.IServerDataServiceContext

## NOTATKI
* Jeśli uwierzytelnianie nie określa domeny, a w przypadku korzystania z programu Windows PowerShell 2.0 polecenie cmdlet Get-Credential zwraca ukośnik odwrotny () przed nazwą użytkownika, na przykład \\ \user. Program Windows PowerShell 3.0 nie dodaje ukośnika odwrotnego. Ten ukośnik odwrotny nie jest rozpoznawany przez parametr *Credential* polecenia cmdlet **New-AzureSqlDatabaseServerContext.** Aby go usunąć, użyj poleceń podobnych do następujących:

  `PS C:\\\> $Credential = Get-Credential`
`PS C:\\\> $Credential = New-Object -TypeName 'System.Management.Automation.PSCredential' -ArgumentList $Credential.Username.Replace("\",""),$Credential.Password`

## LINKI POKREWNE



[Get-AzureSqlDatabase](./Get-AzureSqlDatabase.md)

[New-AzureSqlDatabase](./New-AzureSqlDatabase.md)

[Remove-AzureSqlDatabase](./Remove-AzureSqlDatabase.md)

[Set-AzureSqlDatabase](./Set-AzureSqlDatabase.md)


