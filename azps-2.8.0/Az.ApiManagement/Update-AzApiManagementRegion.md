---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
ms.openlocfilehash: 7fa565eb16ced9e9146b219d7850354e499ef06e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706877"
---
# Update-AzApiManagementRegion

## STRESZCZENIe
Aktualizuje istniejący region wdrożenia w wystąpieniu PsApiManagement.

## POLECENIA

```
Update-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Update-AzApiManagementRegion** aktualizuje istniejące wystąpienie typu **Microsoft. Azure. Commands. ApiManagement. models. PsApiManagementRegion** w kolekcji obiektów **AdditionalRegions** udostępnionego wystąpienia typu **Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement**.
To polecenie cmdlet nie rozmieszcza żadnych elementów, ale aktualizuje wystąpienie **PsApiManagement** w pamięci.
Aby zaktualizować wdrożenie funkcji zarządzania interfejsem API, użyj zmodyfikowanego **PsApiManagementInstance** do polecenia cmdlet Set-AzApiManagement.

## Przykłady

### Przykład 1: zwiększanie pojemności dodatkowego regionu w wystąpieniu PsApiManagement
```powershell
PS C:\>$apimService = Get-AzApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName
PS C:\>$apimService = Update-AzApiManagementRegion -ApiManagement $apimService -Location "North Central US" -Capacity 2 -Sku Premium
PS C:\>$apimService = Set-AzApiManagement -InputObject $apimService -PassThru
```

To polecenie pobiera usługę SKU zarządzania interfejsem API, posiadającą regiony w Ameryce Południowej centralach w STANach Zjednoczonych i Północno-środkowe. Następnie zwiększa się zdolność centralnego regionu północno-USA do 2 przy użyciu **zestawu-AzApiManagement**. Następny zestaw poleceń cmdlet **-AzApiManagement** stosuje zmianę konfiguracji do usługi zarządzania interfejsem API.

## PARAMETRÓW

### -ApiManagement
Umożliwia określenie wystąpienia **PsApiManagement** , w którym ma zostać zaktualizowany istniejący region wdrożenia.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Pojemność
Określa nową wartość pojemności jednostki SKU dla obszaru wdrożenia.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### — Lokalizacja
Określa lokalizację obszaru wdrożenia, który ma zostać zaktualizowany.
Określa lokalizację nowego obszaru wdrożenia w obsługiwanym regionie usługi zarządzania interfejsem API.
Aby uzyskać prawidłowe lokalizacje, użyj polecenia cmdlet Get-AzResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | gdzie {$ _. ResourceTypes [0]. ResourceTypeName-EQ "usługa"} | Lokalizacje Select-Object

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

### -SKU
Określa nową wartość warstwy obszaru wdrożenia.
Prawidłowe wartości:
- Deweloper
- Standard
- Ubezpieczeni

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium, Basic, Consumption

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetwork
Określa konfigurację sieci wirtualnej dla obszaru wdrożenia.
Przekazanie $null spowoduje usunięcie konfiguracji sieci wirtualnej dla tego regionu.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement

### System. String

### Microsoft. Azure. Commands. ApiManagement. models. PsApiManagementSku

### System. Int32

### Microsoft. Azure. Commands. ApiManagement. models. PsApiManagementVirtualNetwork

## WYSYŁA

### Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement

## INFORMACYJN

## LINKI POKREWNE

[Dodaj-AzApiManagementRegion](./Add-AzApiManagementRegion.md)

[Remove-AzApiManagementRegion](./Remove-AzApiManagementRegion.md)

[Set-AzApiManagement](./Set-AzApiManagement.md)
