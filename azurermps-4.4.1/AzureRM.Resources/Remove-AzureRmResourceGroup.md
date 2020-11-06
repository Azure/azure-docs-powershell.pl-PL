---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 880D321E-30F2-4CAE-B14A-5F6DD8E1DB99
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroup.md
ms.openlocfilehash: 6938cf80f3fa6fb20252e1e4a212133ecd1c62a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549868"
---
# Remove-AzureRmResourceGroup

## STRESZCZENIe
Usuwa grupę zasobów.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### Umożliwia wyświetlenie listy grup zasobów na podstawie nazwy. Domyślne
```
Remove-AzureRmResourceGroup [-Name] <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Umożliwia wyświetlenie listy grup zasobów na podstawie identyfikatora.
```
Remove-AzureRmResourceGroup [-Id] <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Remove-AzureRmResourceGroup** usuwa grupę zasobów platformy Azure oraz jej zasoby z bieżącej subskrypcji.
Aby usunąć zasób, ale pozostawić grupę zasobów, użyj polecenia cmdlet Remove-AzureRmResource.

## Przykłady

### Przykład 1. Usuń grupę zasobów
```
PS C:\>Remove-AzureRmResourceGroup -Name "ContosoRG01"
```

To polecenie usuwa grupę zasobów ContosoRG01 z subskrypcji.
Polecenie cmdlet monituje o potwierdzenie i nie zwraca wyników.

### Przykład 2: Usuwanie grupy zasobów bez potwierdzenia
```
PS C:\>Get-AzureRmResourceGroup -Name "ContosoRG01" | Remove-AzureRmResourceGroup -Verbose -Force
```

To polecenie używa polecenia cmdlet Get-AzureRmResourceGroup, aby uzyskać ContosoRG01 grupy zasobów, a następnie przekazuje je do polecenia **Remove-AzureRmResourceGroup** przy użyciu operatora potoku.
*Pełny* parametr Common jest pobierany na informacje o stanie operacji, a parametr *Force* pomija monit o potwierdzenie.

### Przykład 3: Usuwanie wszystkich grup zasobów
```
PS C:\>Get-AzureRmResourceGroup | Remove-AzureRmResourceGroup
```

To polecenie używa polecenia cmdlet **Get-AzureRmResourceGroup** w celu uzyskania wszystkich grup zasobów, a następnie przekazuje je do polecenia **Remove-AzureRmResourceGroup** przy użyciu operatora potoku.

## PARAMETRÓW

### -ApiVersion
Określa wersję API obsługiwaną przez dostawcę zasobów.
Możesz określić inną wersję niż wersja domyślna.

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

### -ID
Określa identyfikator grupy zasobów do usunięcia.
Znaki wieloznaczne są niedozwolone.

```yaml
Type: System.String
Parameter Sets: Lists the resource group based in the Id.
Aliases: ResourceGroupId, ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwy grup zasobów do usunięcia.
Znaki wieloznaczne są niedozwolone.

```yaml
Type: System.String
Parameter Sets: Lists the resource group based in the name.
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pre
Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono

## WYSYŁA

### Znaleziono

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRmResourceGroup](./Get-AzureRmResourceGroup.md)

[Nowe — AzureRmResourceGroup](./New-AzureRmResourceGroup.md)

[Set-AzureRmResourceGroup](./Set-AzureRmResourceGroup.md)


