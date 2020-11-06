---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistry.md
ms.openlocfilehash: 232d767130b789f61d7e4e21fa0bc7c0737c58dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528225"
---
# New-AzureRmContainerRegistry

## STRESZCZENIe
Tworzy rejestr kontenera.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
New-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Sku] <String>
 [-Location <String>] [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzureRmContainerRegistry** umożliwia utworzenie rejestru kontenera.

## Przykłady

### Przykład 1: tworzenie rejestru kontenera za pomocą nowego konta magazynu.
```
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic"

Id                 : /subscriptions/3eb31d8d-2879-4706-89b4-4dc4047726c6/resourceGroups/MyResourceGroup/providers/Microsoft.ContainerRegistry/registries/MyRegistry
ResourceGroupName  : MyResourceGroup
Name               : MyRegistry
Type               : Microsoft.ContainerRegistry/registries
Location           : westus
Tags               : {}
SkuName            : Basic
SkuTier            : Basic
LoginServer        : myregistry.azurecr.io
CreationDate       : 4/13/2017 3:48:57 PM
ProvisioningState  : Succeeded
AdminUserEnabled   : False
StorageAccountName : myregistry154817
```

To polecenie tworzy rejestr kontenerowy z nowym kontem magazynu w grupie zasób `MyResourceGroup` .

### Przykład 2: tworzenie rejestru kontenera z włączonym użytkownikiem administracyjnym.
```
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -EnableAdminUser

Id                 : /subscriptions/3eb31d8d-2879-4706-89b4-4dc4047726c6/resourceGroups/MyResourceGroup/providers/Microsoft.ContainerRegistry/registries/MyRegistry
ResourceGroupName  : MyResourceGroup
Name               : MyRegistry
Type               : Microsoft.ContainerRegistry/registries
Location           : westus
Tags               : {}
SkuName            : Basic
SkuTier            : Basic
LoginServer        : myregistry.azurecr.io
CreationDate       : 4/13/2017 3:48:57 PM
ProvisioningState  : Succeeded
AdminUserEnabled   : True
StorageAccountName : myregistry154817
```

To polecenie tworzy rejestr kontenerowy z włączonym użytkownikiem administracyjnym.

### Przykład 3: tworzenie rejestru kontenera za pomocą istniejącego konta magazynu.
```
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -StorageAccountName "mystorageaccount"

Id                 : /subscriptions/3eb31d8d-2879-4706-89b4-4dc4047726c6/resourceGroups/MyResourceGroup/providers/Microsoft.ContainerRegistry/registries/MyRegistry
ResourceGroupName  : MyResourceGroup
Name               : MyRegistry
Type               : Microsoft.ContainerRegistry/registries
Location           : westus
Tags               : {}
SkuName            : Basic
SkuTier            : Basic
LoginServer        : myregistry.azurecr.io
CreationDate       : 4/13/2017 3:48:57 PM
ProvisioningState  : Succeeded
AdminUserEnabled   : False
StorageAccountName : mystorageaccount
```

To polecenie tworzy rejestr kontenerowy z istniejącym kontem magazynu `mystorageaccount` w ramach tej samej subskrypcji.

## PARAMETRÓW

### -EnableAdminUser
Włącz użytkownika administracyjnego dla rejestru kontenera.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: EnableAdmin

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Lokalizacja
Lokalizacja rejestru kontenera.
Domyślnie jest to lokalizacja grupy zasobów.

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

### -Name (nazwa)
Nazwa rejestru kontenera.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów.

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

### -SKU
Wersja SKU rejestru kontenera.
Dozwolone wartości: podstawowe.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku
Accepted values: Basic

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountName
Nazwa istniejącego konta magazynu.

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

### -Tag
Znaczniki rejestru kontenera. pary klucz-wartość w formie tabeli skrótów. Na przykład:

@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

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
Default value: None
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
Default value: None
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

## WYSYŁA

### Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRmContainerRegistry](./Get-AzureRmContainerRegistry.md)

[Update-AzureRmContainerRegistry](./Update-AzureRmContainerRegistry.md)

[Remove-AzureRmContainerRegistry](./Remove-AzureRmContainerRegistry.md)
