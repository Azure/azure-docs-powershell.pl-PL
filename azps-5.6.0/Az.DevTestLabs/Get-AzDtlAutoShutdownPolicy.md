---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 52DD0511-915F-4144-B47F-E4B7AF403AA5
online version: https://docs.microsoft.com/powershell/module/az.devtestlabs/get-azdtlautoshutdownpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAutoShutdownPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAutoShutdownPolicy.md
ms.openlocfilehash: f15d2c660fe3d4d166c1e8fe6a66cdba543fd01a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001578"
---
# Get-AzDtlAutoShutdownPolicy

## SYNOPSIS
Pobiera zasady automatycznego zamykania laboratorium w laboratorium testów deweloperów.

## SKŁADNIA

```
Get-AzDtlAutoShutdownPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzDtlAutoShutdownPolicy** pobiera zasady automatycznego zamykania laboratorium, które umożliwia automatyczne zamykanie wszystkich maszyn wirtualnych w laboratorium o określonej godzinie.
Polecenie cmdlet zwraca, czy jest włączony stan zasad i godzina dnia ustawiona na automatyczne zamykanie maszyn wirtualnych laboratorium.

## PRZYKŁADY

### Przykład 1

Pobiera zasady automatycznego zamykania laboratorium w laboratorium testów deweloperów. (wygenerowane automatycznie)

```powershell <!-- Aladdin Generated Example --> 
Get-AzDtlAutoShutdownPolicy -LabName <String> -ResourceGroupName MyResourceGroup
```

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

### — LabName
Określa nazwę laboratorium, dla którego to polecenie cmdlet otrzymuje zasady automatycznego zamykania systemu.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów, do której należy laboratorium.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### System.String

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule

## NOTATKI

## LINKI POKREWNE

[Set-AzDtlAutoShutdownPolicy](./Set-AzDtlAutoShutdownPolicy.md)


