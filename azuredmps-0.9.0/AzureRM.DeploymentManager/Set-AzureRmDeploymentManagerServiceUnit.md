---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/set-azurermdeploymentmanagerserviceunit
schema: 2.0.0
ms.openlocfilehash: b04819f61f37b9bb47818a8b17e93db9a7cdb05d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523510"
---
# Set-AzureRmDeploymentManagerServiceUnit

## STRESZCZENIe
Aktualizuje jednostkę usługi.

## POLECENIA

```
Set-AzureRmDeploymentManagerServiceUnit [-ServiceUnit] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzureRmDeploymentManagerServiceUnit** aktualizuje jednostkę usługi za pomocą określonego obiektu jednostki usługi.
Polecenie cmdlet zwraca zaktualizowany obiekt jednostki usługi.

## Przykłady

### Przykład 1
```powershell
PS C:\> Set-AzureRmDeploymentManagerServiceUnit -ServiceUnit $serviceUnitObject
```

To polecenie aktualizuje jednostkę usługi, której nazwa, nazwa usługi, nazwa topologii usługi i przydziały zasobów są odpowiednio zgodne z właściwościami Name, ServiceName, servicetopologyname i ResourceGroupName w $serviceUnitObject.
Polecenie zwraca zaktualizowany obiekt jednostki usługi.

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

### -Serviceunit
Obiekt jednostki usługi.

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource
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

### Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSServiceUnitResource

## WYSYŁA

### Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSServiceUnitResource

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzureRmDeploymentManagerServiceUnit](./New-AzureRmDeploymentManagerServiceUnit.md)

[Get-AzureRmDeploymentManagerServiceUnit](./Set-AzureRmDeploymentManagerServiceUnit.md)

[Remove-AzureRmDeploymentManagerServiceUnit](./Remove-AzureRmDeploymentManagerServiceUnit.md)