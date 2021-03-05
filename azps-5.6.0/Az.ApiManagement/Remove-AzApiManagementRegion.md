---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
ms.openlocfilehash: 2e6ae18054f7ad3e122169522d111adfe612b955
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010049"
---
# Remove-AzApiManagementRegion

## SYNOPSIS
Usuwa istniejący region wdrażania z wystąpienia programu PsApiManagement.

## SKŁADNIA

```
Remove-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie cmdlet **Remove-AzApiManagementRegion** usuwa wystąpienie typu **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** z kolekcji **AdditionalRegions (DodatkoweRegiony)** pod warunkiem wystąpienia typu **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement.**
To polecenie cmdlet nie modyfikuje samego wdrożenia, ale aktualizuje wystąpienie polecenia **PsApiManagement** w pamięci.
Aby zaktualizować wdrożenie zarządzania interfejsami API, przekaż zmodyfikowaną wartość **PsApiManagementInstance** do **Set-AzApiManagement.**

## PRZYKŁADY

### Przykład 1. Usuwanie regionu z wystąpienia programu PsApiManagement
```
PS C:\>Remove-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

To polecenie usuwa region o nazwie Wschód USA z wystąpienia **PsApiManagement.**

### Przykład 2. Usuwanie regionu z wystąpienia polecenia PsApiManagement przy użyciu serii poleceń
```
PS C:\>Get-AzApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzApiManagementRegion -Location "East US" | Set-AzApiManagement
```

To pierwsze polecenie pobiera wystąpienie **polecenia PsApiManagement** z grupy zasobów o nazwie Contoso O nazwie ContosoApi.
Ostatnie polecenie spowoduje usunięcie z tego wystąpienia regionu o nazwie Wschód USA, a następnie aktualizacja wdrożenia.

## PARAMETERS

### -ApiManagement
Określa wystąpienie **polecenia PsApiManagement,** z których to polecenie cmdlet usuwa dodatkowy region wdrażania.

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

### -DefaultProfile

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
Określa lokalizację regionu, który usuwa to polecenie cmdlet.
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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement

### System.String

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement

## NOTATKI

## LINKI POKREWNE

[Add-AzApiManagementRegion](./Add-AzApiManagementRegion.md)

[Update-AzApiManagementRegion](./Update-AzApiManagementRegion.md)


