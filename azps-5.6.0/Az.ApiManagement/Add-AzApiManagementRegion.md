---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/add-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
ms.openlocfilehash: ce1183588458dc0213bff77493caf41a9b1d2766
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994638"
---
# Add-AzApiManagementRegion

## SYNOPSIS
Dodaje nowe regiony wdrażania do wystąpienia programu PsApiManagement.

## SKŁADNIA

```
Add-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie cmdlet **Add-AzApiManagementRegion** dodaje nowe wystąpienie typu **PsApiManagementRegion** do kolekcji **AdditionalRegions** podanego wystąpienia typu **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement.**
To polecenie cmdlet nie wdraża niczego samodzielnie, ale aktualizuje wystąpienie programu **PsApiManagement** w pamięci.
Aby zaktualizować wdrożenie zarządzania interfejsem API, przekaż zmodyfikowane wystąpienie **zarządzania właściwością PsApiManagement** do ustawienia Set-AzApiManagement.

## PRZYKŁADY

### Przykład 1. Dodawanie nowych regionów wdrażania do wystąpienia programu PsApiManagement
```
PS C:\>Add-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

To polecenie dodaje dwie jednostki SKU premium i region o nazwie Wschód USA do wystąpienia **PsApiManagement.**

### Przykład 2. Dodawanie nowych regionów wdrażania do wystąpienia programu PsApiManagement, a następnie aktualizowanie wdrożenia
```powershell
PS C:\>$service = Get-AzApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi"
PS C:\>$service = Add-AzApiManagementRegion -ApiManagement $service -Location $secondarylocation -VirtualNetwork $additionalRegionVirtualNetwork
PS C:\>$service = Set-AzApiManagement -InputObject $service -PassThru
```

To polecenie pobiera **obiekt PsApiManagement,** dodaje dwie jednostki SKU premium dla regionu o nazwie Wschód USA, a następnie aktualizuje wdrożenie.

## PARAMETERS

### -ApiManagement
Określa wystąpienie **programu PsApiManagement,** do których to polecenie cmdlet dodaje dodatkowe regiony wdrożenia.

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
Określa pojemność sku w regionie wdrażania.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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
Określa lokalizację nowego regionu wdrażania pośród obsługiwanego regionu usługi zarządzania interfejsami API.
Aby uzyskać prawidłowe lokalizacje, użyj polecenia cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | gdzie {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object lokalizacji

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### - SKU
Określa warstwę obszaru wdrażania.
Prawidłowe wartości to: 
- Deweloper
- Standardowe
- Premium

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium, Basic, Consumption

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — VirtualNetwork
Określa konfigurację sieci wirtualnej.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement

## NOTATKI
* Polecenie cmdlet zapisuje w potoku zaktualizowane wystąpienie polecenia **PsApiManagement.**

## LINKI POKREWNE

[Remove-AzApiManagementRegion](./Remove-AzApiManagementRegion.md)

[Update-AzApiManagementRegion](./Update-AzApiManagementRegion.md)

[Set-AzApiManagement](./Set-AzApiManagement.md)


