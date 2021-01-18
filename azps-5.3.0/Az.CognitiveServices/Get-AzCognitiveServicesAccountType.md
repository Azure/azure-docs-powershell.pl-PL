---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccounttype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
ms.openlocfilehash: a99ca4bb636ba1767fc5f50611d3c5a9eb991312
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501981"
---
# Get-AzCognitiveServicesAccountType

## STRESZCZENIe
Pobiera dostępne typy kont usług poznawczych.

## POLECENIA

### GetAccountTypes (domyślny)
```
Get-AzCognitiveServicesAccountType [-Location <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetAccountTypeWithName
```
Get-AzCognitiveServicesAccountType -TypeName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzCognitiveServicesAccountType** Pobiera dostępne typy konta usług poznawczych w ramach tej subskrypcji.

## Przykłady

### Przykład 1
```powershell
PS C:\> Get-AzCognitiveServicesAccountType
```

Pobierz listę dostępnych typów.

### Przykład 2
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -Location westus
```

Pobierz listę dostępnych typów w zachód.

### Przykład 3
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -TypeName Face

Face
```

Sprawdź `Face` , czy jest to prawidłowa nazwa typu, czy nazwa będzie zwracana, jeśli jest to prawidłowa nazwa.

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

### — Lokalizacja
Lokalizacja konta usług poznawczych.

```yaml
Type: System.String
Parameter Sets: GetAccountTypes
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TypeName
Nazwa typu konta usług poznawczych.

```yaml
Type: System.String
Parameter Sets: GetAccountTypeWithName
Aliases: CognitiveServicesAccountTypeName, AccountTypeName, KindName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### System. String

## WYSYŁA

### System. String []

### System. String

## INFORMACYJN

## LINKI POKREWNE
