---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
ms.openlocfilehash: 5354737602f168245d6c4c8dca560698fa6cfac2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719541"
---
# Export-AzureAnalysisServicesInstance

## STRESZCZENIe
Eksportuje dziennik z wystąpienia serwera usług Analysis Services w aktualnie zarejestrowanym środowisku, określonym w Add-AzureAnalysisServicesAccount polecenia.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Export-AzureAnalysisServicesInstanceLog [-Instance] <String> [-OutputPath] <String> [-WhatIf] [-Force]
```

## Opis
Polecenie cmdlet Export-AzureAnalysisServicesInstance eksportuje dziennik z wystąpienia serwera usługi Azure Analysis Services do pliku

## Przykłady

### Przykład 1
```
PS C:\>Export-AzureAnalysisServicesInstanceLog -Instance testserver -OuptutPath C:\path\to\log\testserver.log
```

To polecenie spowoduje wyeksportowanie dziennika z serwera "testserver" w środowisku określonym w poleceniu Add-AzureAnalysisServicesAccount i zapisanie go w pliku określonym w OutputPath "C:\path\to\log\testserver.log".

## PARAMETRÓW

### -Instance
Nazwa wystąpienia serwera usług Analysis Services

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutputPath
Ścieżka wyjściowa do pliku w celu wyeksportowania dziennika

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Zastąp plik, jeśli istnieje, bez pytania

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## WEJŚCIOWE

## WYSYŁA

## INFORMACYJN
Alias: Export-AzureAsInstanceLog

## LINKI POKREWNE

