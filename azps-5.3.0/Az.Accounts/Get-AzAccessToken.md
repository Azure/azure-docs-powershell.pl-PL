---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azaccesstoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
ms.openlocfilehash: 696ae59cb5115181605b7e6e647e2eb7d2792fd8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502601"
---
# Get-AzAccessToken

## STRESZCZENIe
Uzyskaj token dostępu surowego. Gdy korzystasz z funkcji-ResourceUrl, upewnij się, że wartość jest zgodna z bieżącym środowiskiem platformy Azure. Możesz odwołać się do wartości `(Get-AzContext).Environment` .

## POLECENIA

### KnownResourceTypeName (domyślny)
```
Get-AzAccessToken [-ResourceTypeName <String>] [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceUrl
```
Get-AzAccessToken -ResourceUrl <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Uzyskaj token dostępu

## Przykłady

### Przykład 1 Uzyskaj token dostępu surowego dla punktu końcowego ARM
```powershell
PS C:\> Get-AzAccessToken
```

Uzyskiwanie tokenu dostępu dla punktu końcowego programu Access dla bieżącego konta

### Przykład 2 Uzyskaj token dostępu surowego dla punktu końcowego wykresu w usłudze AAD
```powershell
PS C:\> Get-AzAccessToken -ResourceTypeName AadGraph
```

Uzyskiwanie tokenu dostępu dla punktu końcowego programu Access Graph dla bieżącego konta

### Przykład 3 Uzyskaj token dostępu surowego dla punktu końcowego wykresu w usłudze AAD
```powershell
PS C:\> Get-AzAccessToken -Resource "https://graph.windows.net/"
```

Uzyskiwanie tokenu dostępu dla punktu końcowego programu Access Graph dla bieżącego konta

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceTypeName
Opcjonalna nazwa typu Resouce, obsługiwane wartości: AadGraph, AnalysisServices, ARM, atestacja, partia, datalake, magazyn, OperationalInsights, ResourceManager, Synapse. Wartość domyślna to ramię, jeśli nie zostało określone.

```yaml
Type: System.String
Parameter Sets: KnownResourceTypeName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceUrl
Adres URL zasobu, dla którego żądasz tokenu, na przykład ' http://graph.windows.net/ '.

```yaml
Type: System.String
Parameter Sets: ResourceUrl
Aliases: Resource, ResourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Dzierżawy
Opcjonalny identyfikator dzierżawy. Użyj identyfikatora dzierżawy domyślnego, jeśli nie jest określony.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### Znaleziono

## WYSYŁA

### System. String

## INFORMACYJN

## LINKI POKREWNE
