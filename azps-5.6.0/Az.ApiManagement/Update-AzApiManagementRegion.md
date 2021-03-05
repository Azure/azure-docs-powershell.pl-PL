---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/update-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
ms.openlocfilehash: c2e01d4a3f6ee3466151202a1c1d681c9f4e5486
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001914"
---
# Update-AzApiManagementRegion

## SYNOPSIS
Aktualizuje istniejący region wdrażania w wystąpieniu programu PsApiManagement.

## SKŁADNIA

```
Update-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## OPIS
Polecenie cmdlet **Update-AzApiManagementRegion** aktualizuje istniejące wystąpienie typu **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** w zbiorze **obiektów AdditionalRegions** podanego wystąpienia typu **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement.**
To polecenie cmdlet nie wdraża niczego, ale aktualizuje wystąpienie programu **PsApiManagement** w pamięci.
Aby zaktualizować wdrożenie zarządzania interfejsem API, użyj zmodyfikowanego polecenia **cmdlet PsApiManagementInstance** Set-AzApiManagement cmdlet.

## PRZYKŁADY

### Przykład 1. Zwiększenie pojemności dodatkowego regionu w wystąpieniu programu PsApiManagement
```powershell
PS C:\>$apimService = Get-AzApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName
PS C:\>$apimService = Update-AzApiManagementRegion -ApiManagement $apimService -Location "North Central US" -Capacity 2 -Sku Premium
PS C:\>$apimService = Set-AzApiManagement -InputObject $apimService -PassThru
```

To polecenie otrzymuje usługę SKU API Management Premium z regionami w południowo-środkowych Stanów Zjednoczonych i Północno-Środkowych Stanów Zjednoczonych. Następnie zwiększa wydajność regionu północno-środkowego Stanów Zjednoczonych do 2, używając **ustawienia Set-AzApiManagement.** Następne polecenie cmdlet **Set-AzApiManagement** stosuje zmianę konfiguracji do usługi zarządzania interfejsami API.

### Przykład 2

Aktualizuje istniejący region wdrażania w wystąpieniu programu PsApiManagement. (wygenerowane automatycznie)

```powershell
<!-- Aladdin Generated Example --> 
Update-AzApiManagementRegion -ApiManagement <PsApiManagement> -Capacity 2 -Location 'North Central US' -Sku Developer -VirtualNetwork <PsApiManagementVirtualNetwork>
```

## PARAMETERS

### -ApiManagement
Określa wystąpienie **PsApiManagement,** w przypadku których ma być aktualizowane istniejący region wdrażania.

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

### — Pojemność
Określa nową wartość pojemności SKU dla regionu wdrażania.

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
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

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
Określa lokalizację regionu wdrażania do zaktualizowania.
Określa lokalizację nowego regionu wdrażania pośród obsługiwanego regionu usługi zarządzania interfejsami API.
Aby uzyskać prawidłowe lokalizacje, użyj polecenia cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | gdzie {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object lokalizacji

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

### - SKU
Określa nową wartość warstwy dla regionu wdrażania.
Prawidłowe wartości to:
- Deweloper
- Standardowe
- Premium

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

### — VirtualNetwork
Określa konfigurację sieci wirtualnej dla regionu wdrażania.
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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement

### System.String

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku

### System.Int32

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement

## NOTATKI

## LINKI POKREWNE

[Add-AzApiManagementRegion](./Add-AzApiManagementRegion.md)

[Remove-AzApiManagementRegion](./Remove-AzApiManagementRegion.md)

[Set-AzApiManagement](./Set-AzApiManagement.md)
