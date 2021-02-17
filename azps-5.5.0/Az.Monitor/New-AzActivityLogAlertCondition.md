---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactivitylogalertcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
ms.openlocfilehash: 85cf08b0ade67042c4aa4c4c5ff3253b6af9f2ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192203"
---
# New-AzActivityLogAlertCondition

## SYNOPSIS
Tworzy w pamięci nowy obiekt warunku alertu dziennika aktywności.

## SKŁADNIA

```
New-AzActivityLogAlertCondition -Field <String> -Equal <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet New-AzActivityLogAlertCondition** tworzy w pamięci nowy obiekt warunku dziennika aktywności.

## PRZYKŁADY

### Przykład 1. Tworzenie nowego obiektu alertu dziennika aktywności w pamięci.
```
PS C:\>$Condition = New-AzActivityLogAlertCondition -Field "Requests" -Equal "OtherField"
PS C:\>Write-Host "Field property value: $($Condition.Field)"
PS C:\>Write-Host "Equals property value: $($Condition.Equals)"

Field property value: Requests
Equals property value: OtherField
```

To polecenie tworzy w pamięci nowy obiekt warunku alertu dziennika aktywności.
**UWAGA:** po użyciu tego polecenia cmdlet z parametrem [Set-AzActivityLogAlert](https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azactivitylogalert) co najmniej jeden z tych obiektów przekazanych jako parametry musi mieć wartość "Category" (Kategoria). W przeciwnym razie zaplecza odpowiada, odpowiadając 400 (BadRequest).

## PARAMETERS

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure

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

### -Equal
Określa właściwość równa się dla warunku liścia.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### - Pole
Określa pole warunku.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### System.String

## OUTPUTS

### Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition

## NOTATKI

## LINKI POKREWNE

[Set-AzActivityLogAlert](./Set-AzActivityLogAlert.md)

[Enable-AzActivityLogAlert](./Enable-AzActivityLogAlert.md)

[Disable-AzActivityLogAlert](./Disable-AzActivityLogAlert.md)

[Get-AzActivityLogAlert](./Get-AzActivityLogAlert.md)

[Remove-AzActivityLogAlert](./Remove-AzActivityLogAlert.md)

[New-AzActionGroup](./Get-AzActionGroup.md)
