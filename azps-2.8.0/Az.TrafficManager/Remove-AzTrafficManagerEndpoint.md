---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 2129C457-592B-484C-A148-828BFD5895D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 60ce16c9c9933d326013ce03b74637b0fce4a3b0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888097"
---
# Remove-AzTrafficManagerEndpoint

## STRESZCZENIe
Umożliwia usunięcie punktu końcowego z usługi Traffic Manager.

## POLECENIA

### Field
```
Remove-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Stream
```
Remove-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Remove-AzTrafficManagerEndpoint** umożliwia usunięcie punktu końcowego z usługi Azure Traffic Manager.

To polecenie cmdlet umożliwia przekazanie każdej zmiany do usługi Traffic Manager.
Aby usunąć wiele punktów końcowych z obiektu profilu lokalnego Menedżera ruchu i przekazać zmiany w ramach jednej operacji, użyj polecenia cmdlet Remove-AzTrafficManagerEndpointConfig.

Za pomocą operatora potoku możesz przekazać obiekt **TrafficManagerEndpoint** do tego polecenia cmdlet lub określić obiekt **TrafficManagerEndpoint** przy użyciu parametru *TrafficManagerEndpoint* .

Możesz też określić nazwę i typ punktu końcowego przy użyciu parametrów *Nazwa* i *Typ* wraz z parametrami *refilename* i *ResourceGroupName* .

## Przykłady

### Przykład 1: Usuwanie punktu końcowego z profilu
```
PS C:\>Remove-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

To polecenie usuwa punkt końcowy Azure o nazwie contoso z profilu o nazwie ContosoProfile w grupie zasobów o nazwie ResourceGroup11.

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

### -Force
Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę punktu końcowego usługi Traffic Managera, który jest usuwany przez to polecenie cmdlet.

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Refilename
Określa nazwę profilu usługi Traffic Manager, z którego to polecenie cmdlet usuwa punkt końcowy.
Aby uzyskać profil, użyj polecenia cmdlet Get-AzTrafficManagerProfile.

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów.
To polecenie cmdlet umożliwia usunięcie punktu końcowego usługi Traffic managera z profilu usługi Traffic Manager w grupie, którą ten parametr określa.

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficManagerEndpoint
Określa punkt końcowy usługi Traffic Managera, który jest usuwany przez to polecenie cmdlet.
Aby uzyskać obiekt **TrafficManagerEndpoint** , użyj polecenia cmdlet Get-AzTrafficManagerEndpoint.

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Type
Określa typ punktu końcowego, który jest dodawany przez to polecenie cmdlet do profilu usługi Traffic Manager.
Prawidłowe wartości: 

- AzureEndpoints
- ExternalEndpoints
- NestedEndpoints

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.
Polecenie cmdlet nie jest uruchamiane.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Microsoft. Azure. Commands. Trafficmanager. modele. TrafficManagerEndpoint

## WYSYŁA

### System. Boolean

## INFORMACYJN

## LINKI POKREWNE

[Get-AzTrafficManagerEndpoint](./Get-AzTrafficManagerEndpoint.md)

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[Nowe — AzTrafficManagerEndpoint](./New-AzTrafficManagerEndpoint.md)

[Remove-AzTrafficManagerEndpointConfig](./Remove-AzTrafficManagerEndpointConfig.md)

[Set-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)


