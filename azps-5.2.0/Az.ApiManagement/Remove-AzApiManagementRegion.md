---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
ms.openlocfilehash: 70816b054acc7667d2246ea72901c65890f9389e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339802"
---
# Remove-AzApiManagementRegion

## STRESZCZENIe
Usuwa istniejący region wdrożenia z wystąpienia PsApiManagement.

## POLECENIA

```
Remove-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Remove-AzApiManagementRegion** usuwa wystąpienie typu **Microsoft. Azure. Commands. ApiManagement. models. PsApiManagementRegion** z kolekcji **AdditionalRegions** dostarczonych z wystąpienia typu **Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement**.
To polecenie cmdlet nie powoduje modyfikacji samego wdrożenia, ale aktualizuje wystąpienie **PsApiManagement** w pamięci.
Aby zaktualizować wdrożenie funkcji zarządzania interfejsem API, przekazanie zmodyfikowanego **PsApiManagementInstance** w celu **Ustawienia AzApiManagement**.

## Przykłady

### Przykład 1: usuwanie regionu z wystąpienia programu PsApiManagement
```
PS C:\>Remove-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

To polecenie usuwa region o nazwie wschód my z wystąpienia **PsApiManagement** .

### Przykład 2: usuwanie regionu z wystąpienia programu PsApiManagement przy użyciu serii poleceń
```
PS C:\>Get-AzApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzApiManagementRegion -Location "East US" | Set-AzApiManagement
```

To pierwsze polecenie uzyskuje wystąpienie **PsApiManagement** z grupy zasobów o nazwie contoso o nazwie ContosoApi.
Polecenie ostatnie powoduje usunięcie regionu o nazwie wschód USA z tego wystąpienia, a następnie zaktualizowanie wdrożenia.

## PARAMETRÓW

### -ApiManagement
Określa wystąpienie **PsApiManagement** , z którego to polecenie cmdlet usuwa dodatkowy region wdrożenia.

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
Określa lokalizację obszaru, który jest usuwany przez to polecenie cmdlet.
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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement

### System. String

## WYSYŁA

### Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement

## INFORMACYJN

## LINKI POKREWNE

[Dodaj-AzApiManagementRegion](./Add-AzApiManagementRegion.md)

[Update-AzApiManagementRegion](./Update-AzApiManagementRegion.md)


