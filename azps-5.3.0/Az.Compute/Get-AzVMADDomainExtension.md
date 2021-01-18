---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMADDomainExtension.md
ms.openlocfilehash: 0d511a944ecf02e212bdd734fdda6c604deee28d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501921"
---
# Get-AzVMADDomainExtension

## STRESZCZENIe
Pobiera informacje o rozszerzeniu domeny usługi AD.

## POLECENIA

```
Get-AzVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzVMADDomainExtension** pobiera informacje o określonym rozszerzeniu domeny usługi Azure Active Directory (AD).

## Przykłady

### Przykład 1

Pobiera informacje o rozszerzeniu domeny usługi AD. (autogenerowana)

```powershell <!-- Aladdin Generated Example --> 
Get-AzVMADDomainExtension -Name 'AgentPool01' -ResourceGroupName myresourcegroup -VMName 'VM01'
```

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

### -Name (nazwa)
Określa nazwę rozszerzenia domeny.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów.

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

### -Status
Wskazuje, że to polecenie cmdlet pobiera widok wystąpienia rozszerzenia domeny.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Określa nazwę maszyny wirtualnej.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### System. String

### System. Management. Automation. SwitchParameter

## WYSYŁA

### Microsoft. Azure. Commands. COMPUTE. models. VirtualMachineADDomainExtensionContext

## INFORMACYJN

## LINKI POKREWNE

[Set-AzVMADDomainExtension](./Set-AzVMADDomainExtension.md)


