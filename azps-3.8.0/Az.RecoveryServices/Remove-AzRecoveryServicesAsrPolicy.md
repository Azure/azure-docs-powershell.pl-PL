---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 6ff0031c5bb8571c69287968f984565daf58b530
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051607"
---
# Remove-AzRecoveryServicesAsrPolicy

## STRESZCZENIe
Usuwa określone zasady replikacji ASR z magazynu usług odzyskiwania.

## POLECENIA

```
Remove-AzRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Remove-AzRecoveryServicesAsrPolicy** usunęło określone zasady replikacji z magazynu usług odzyskiwania.

## Przykłady

### Przykład 1
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrPolicy -Policy $Policy
```

Rozpoczyna usuwanie określonych zasad replikacji i zwraca zadanie ASR użyte do śledzenia operacji.

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

### -Inputobject
Obiekt wejściowy do polecenia cmdlet: obiekt zasad replikacji ASR odpowiadający zasadom replikacji, które mają zostać usunięte.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet. Polecenie cmdlet nie jest uruchamiane.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy

## WYSYŁA

### Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob

## INFORMACYJN

## LINKI POKREWNE

[Get-AzRecoveryServicesAsrPolicy](./Get-AzRecoveryServicesAsrPolicy.md)

[Nowe — AzRecoveryServicesAsrPolicy](./New-AzRecoveryServicesAsrPolicy.md)
