---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
ms.openlocfilehash: 4e4a86d5054a5554cb473c60550d32adffae5e46
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002490"
---
# New-AzStorageContext

## SYNOPSIS
Tworzy kontekst magazynu platformy Azure.

## SKŁADNIA

### OAuthAccount (domyślne)
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### AccountNameAndKey
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### AccountNameAndKeyEnvironment
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### AnonymousAccount
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### AnonymousAccountEnvironment
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### SasToken
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### SasTokenWithAzureEnvironment
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### OAuthAccountEnvironment
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### ConnectionString
```
New-AzStorageContext -ConnectionString <String> [<CommonParameters>]
```

### LocalDevelopment
```
New-AzStorageContext [-Local] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet New-AzStorageContext** tworzy kontekst magazynu platformy Azure.
Domyślnym uwierzytelnianiem kontekstu magazynu jest OAuth (Azure AD), jeśli jest to nazwa konta magazynu wejściowego.
Zobacz szczegóły uwierzytelniania usługi magazynu https://docs.microsoft.com/rest/api/storageservices/authorization-for-the-azure-storage-services w.

## PRZYKŁADY

### Przykład 1. Tworzenie kontekstu przez określenie nazwy i klucza konta magazynu
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

To polecenie tworzy kontekst dla konta o nazwie ContosoGeneral, które używa określonego klucza.

### Przykład 2. Tworzenie kontekstu przez określenie parametrów połączenia
```
PS C:\>New-AzStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

To polecenie tworzy kontekst na podstawie określonych parametrów połączenia dla konta ContosoGeneral.

### Przykład 3. Tworzenie kontekstu dla anonimowego konta magazynu
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

To polecenie tworzy kontekst do użytku anonimowego dla konta o nazwie ContosoGeneral.
To polecenie określa protokół HTTP jako protokół połączenia.

### Przykład 4. Tworzenie kontekstu przy użyciu konta magazynu dla rozwoju lokalnego
```
PS C:\>New-AzStorageContext -Local
```

To polecenie tworzy kontekst przy użyciu lokalnego konta magazynu programowego.
Polecenie określa *parametr Local.*

### Przykład 5. Uzyskiwanie kontenera dla lokalnego konta magazynu dewelopera
```
PS C:\>New-AzStorageContext -Local | Get-AzStorageContainer
```

To polecenie tworzy kontekst przy użyciu konta magazynu lokalnego rozwoju, a następnie przekazuje nowy kontekst do polecenia cmdlet **Get-AzStorageContainer** przy użyciu operatora potoku.
To polecenie pobiera kontener magazynu platformy Azure dla lokalnego konta magazynu dewelopera.

### Przykład 6. Uzyskiwanie wielu kontenerów
```
PS C:\>$Context01 = New-AzStorageContext -Local 
PS C:\> $Context02 = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzStorageContainer
```

Pierwsze polecenie tworzy kontekst przy użyciu konta magazynu rozwoju lokalnego, a następnie przechowuje ten kontekst w zmiennej $Context 01.
Drugie polecenie tworzy kontekst dla konta o nazwie ContosoGeneral, które używa określonego klucza, a następnie przechowuje ten kontekst w zmiennej $Context 02.
Końcowe polecenie pobiera kontenery dla kontekstów przechowywanych w programach $Context 01 i $Context 02 za pomocą narzędzia **Get-AzStorageContainer.**

### Przykład 7. Tworzenie kontekstu za pomocą punktu końcowego
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

To polecenie tworzy kontekst magazynu platformy Azure, który ma określony punkt końcowy magazynu.
Polecenie tworzy kontekst dla konta o nazwie ContosoGeneral, które używa określonego klucza.

### Przykład 8. Tworzenie kontekstu w określonym środowisku
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

To polecenie tworzy kontekst magazynu platformy Azure, który ma określone środowisko platformy Azure.
Polecenie tworzy kontekst dla konta o nazwie ContosoGeneral, które używa określonego klucza.

### Przykład 9. Tworzenie kontekstu przy użyciu tokenu SAS
```
PS C:\>$SasToken = New-AzStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzStorageBlob -Container "ContosoMain"
```

Pierwsze polecenie generuje token SAS przy użyciu polecenia cmdlet **New-AzStorageContainerSASToken** dla kontenera o nazwie ContosoMain, a następnie przechowuje ten token w zmiennej $SasToken danych.
Token ten jest do odczytu, dodawania, aktualizowania i usuwania uprawnień.
Drugie polecenie tworzy kontekst dla konta o nazwie ContosoGeneral, które używa tokenu SAS przechowywanego w programie $SasToken, a następnie przechowuje ten kontekst w $Context zmienną.
Końcowe polecenie wyświetla listę wszystkich obiektów blob skojarzonych z kontenerem o nazwie ContosoMain przy użyciu kontekstu przechowywanego w $Context.

### Przykład 10. Tworzenie kontekstu przy użyciu uwierzytelniania OAuth
```
PS C:\>Connect-AzAccount
PS C:\> $Context = New-AzStorageContext -StorageAccountName "myaccountname" -UseConnectedAccount
```

To polecenie tworzy kontekst przy użyciu uwierzytelniania OAuth (Azure AD).

## PARAMETERS

### — Anonimowe
Wskazuje, że to polecenie cmdlet tworzy kontekst magazynu platformy Azure dla anonimowego logowania.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AnonymousAccount, AnonymousAccountEnvironment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### - ConnectionString
Określa ciąg połączenia dla kontekstu magazynu platformy Azure.

```yaml
Type: System.String
Parameter Sets: ConnectionString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### - Punkt końcowy
Określa punkt końcowy dla kontekstu magazynu platformy Azure.

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AnonymousAccount, SasToken
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Środowisko
Określa środowisko platformy Azure.
Dopuszczalne wartości dla tego parametru to: AzureCloud i AzureChinaCloud.
Aby uzyskać więcej informacji, wpisz `Get-Help Get-AzEnvironment` .

```yaml
Type: System.String
Parameter Sets: AccountNameAndKeyEnvironment, AnonymousAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SasTokenWithAzureEnvironment, OAuthAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Lokalny
Wskazuje, że to polecenie cmdlet tworzy kontekst przy użyciu konta magazynu dla rozwoju lokalnego.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LocalDevelopment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Protokół
Transfer Protocol (https/http).

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, OAuthAccountEnvironment
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### - SasToken
Określa token SAS (Shared Access Signature) dla kontekstu.

```yaml
Type: System.String
Parameter Sets: SasToken, SasTokenWithAzureEnvironment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountKey
Określa klucz konta magazynu platformy Azure.
To polecenie cmdlet tworzy kontekst dla klucza, który określa ten parametr.

```yaml
Type: System.String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountName
Określa nazwę konta usługi Azure Storage.
To polecenie cmdlet tworzy kontekst dla konta, które określa ten parametr.

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, SasTokenWithAzureEnvironment, OAuthAccountEnvironment
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### —UseConnectedAccount
Wskazuje, że to polecenie cmdlet tworzy kontekst magazynu platformy Azure za pomocą uwierzytelniania OAuth (Azure AD).
Polecenie cmdlet domyślnie używa uwierzytelniania OAuth, gdy inne uwierzytelnianie nie zostanie określone.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OAuthAccount, OAuthAccountEnvironment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### System.String

## DANE WYJŚCIOWE

### Microsoft.WindowsAzure.Commands.Storage.AzureStorageContext

## NOTATKI

## LINKI POKREWNE

[Get-AzstorageBlob](./Get-AzStorageBlob.md)

[New-AzstorageContainerSASToken](./New-AzStorageContainerSASToken.md)


