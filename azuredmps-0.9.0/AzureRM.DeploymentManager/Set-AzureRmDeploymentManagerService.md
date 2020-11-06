---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/set-azurermdeploymentmanagerservice
schema: 2.0.0
ms.openlocfilehash: 2f4cab266cf63e1c33c35c051e9cc2b838f5b066
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523041"
---
# Set-AzureRmDeploymentManagerService

## STRESZCZENIe
Aktualizuje usługę w topologii usługi.

## POLECENIA

```
Set-AzureRmDeploymentManagerService [-Service] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzureRmDeploymentManagerService** aktualizuje usługę z określonym obiektem usługi.
Polecenie cmdlet zwraca zaktualizowany obiekt usługi.

## Przykłady

### Przykład 1
```powershell
PS C:\> Set-AzureRmDeploymentManagerService -Service $serviceObject
```

To polecenie aktualizuje usługę, której nazwa, nazwa topologii usługi i element Resources są zgodne z właściwościami Name, servicetopologyname i ResourceGroupName w $serviceObject.
Usługa zostanie zaktualizowana do właściwości ustawionych w $serviceObject.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Service
Obiekt usługi.

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSServiceResource

## WYSYŁA

### Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSServiceResource

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzureRmDeploymentManagerService](./New-AzureRmDeploymentManagerService.md)

[Get-AzureRmDeploymentManagerService](./Set-AzureRmDeploymentManagerService.md)

[Remove-AzureRmDeploymentManagerService](./Remove-AzureRmDeploymentManagerService.md)