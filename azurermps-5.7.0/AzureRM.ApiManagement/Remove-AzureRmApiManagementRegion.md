---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
ms.openlocfilehash: 0376c80e769153c448cdc23d8465966026584fcf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554323"
---
# Remove-AzureRmApiManagementRegion

## STRESZCZENIe
Usuwa istniejący region wdrożenia z wystąpienia PsApiManagement.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Remove-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Remove-AzureRmApiManagementRegion** usuwa wystąpienie typu **Microsoft. Azure. Commands. ApiManagement. models. PsApiManagementRegion** z kolekcji **AdditionalRegions** dostarczonych z wystąpienia typu **Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement**.
To polecenie cmdlet nie powoduje modyfikacji samego wdrożenia, ale aktualizuje wystąpienie **PsApiManagement** w pamięci.
Aby zaktualizować wdrożenie funkcji zarządzania interfejsem API, przepuszczanie zmodyfikowanej **PsApiManagementInstance** w celu **zaktualizowania AzureRmApiManagement**.

## Przykłady

### Przykład 1: usuwanie regionu z wystąpienia programu PsApiManagement
```
PS C:\>Remove-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

To polecenie usuwa region o nazwie wschód my z wystąpienia **PsApiManagement** .

### Przykład 2: usuwanie regionu z wystąpienia programu PsApiManagement przy użyciu serii poleceń
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzureRmApiManagementRegion -Location "East US" | Update-AzureRmApiManagementDeployment
```

To pierwsze polecenie uzyskuje wystąpienie **PsApiManagement** z grupy zasobów o nazwie contoso o nazwie ContosoApi.
Polecenie ostatnie powoduje usunięcie regionu o nazwie wschód USA z tego wystąpienia, a następnie zaktualizowanie wdrożenia.

## PARAMETRÓW

### -ApiManagement
Określa wystąpienie **PsApiManagement** , z którego to polecenie cmdlet usuwa dodatkowy region wdrożenia.

```yaml
Type: PsApiManagement
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Lokalizacja
Określa lokalizację obszaru, który jest usuwany przez to polecenie cmdlet.

Określa lokalizację nowego obszaru wdrożenia w obsługiwanym regionie usługi zarządzania interfejsem API.
Aby uzyskać prawidłowe lokalizacje, użyj polecenia cmdlet Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | gdzie {$ _. ResourceTypes [0]. ResourceTypeName-EQ "usługa"} | Lokalizacje Select-Object

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### PsApiManagement
Parametr "ApiManagement" akceptuje wartość typu "PsApiManagement" z rurociągu

## WYSYŁA

### Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement

## INFORMACYJN

## LINKI POKREWNE

[Dodaj-AzureRmApiManagementRegion](./Add-AzureRmApiManagementRegion.md)

[Update-AzureRmApiManagementRegion](./Update-AzureRmApiManagementRegion.md)


