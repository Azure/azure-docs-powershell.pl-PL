---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
ms.openlocfilehash: 29dd6d1938228d3e76c0393ca27f49a3a9fe2564
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525734"
---
# Update-AzureRmApiManagementRegion

## STRESZCZENIe
Aktualizuje istniejący region wdrożenia w wystąpieniu PsApiManagement.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Update-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Update-AzureRmApiManagementRegion** aktualizuje istniejące wystąpienie typu **Microsoft. Azure. Commands. ApiManagement. models. PsApiManagementRegion** w kolekcji obiektów **AdditionalRegions** udostępnionego wystąpienia typu **Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement**.
To polecenie cmdlet nie rozmieszcza żadnych elementów, ale aktualizuje wystąpienie **PsApiManagement** w pamięci.
Aby zaktualizować wdrożenie funkcji zarządzania interfejsem API, użyj zmodyfikowanego **PsApiManagementInstance** do polecenia cmdlet Update-AzureRmApiManagementDeployment.

## Przykłady

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

### — Lokalizacja
Określa lokalizację obszaru wdrożenia, który ma zostać zaktualizowany.

Prawidłowe wartości:

- Północno-środkowe USA
- Południowa Centrala amerykańska
- Centralny stan
- Europa Zachodnia
- Europa Północna
- Zachodnie USA
- Wschodnie USA
- Wschód USA 2
- Japonia wschodni
- Japonia Zachodnia
- Brazylia Południowa
- Azja Południowo-Wschodnia
- Azja Wschodnia
- Australia Wschodnia
- Australia południowy

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
Accepted values: Developer, Standard, Premium

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

### PsApiManagement
Parametr "ApiManagement" akceptuje wartość typu "PsApiManagement" z rurociągu

## WYSYŁA

### Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement

## INFORMACYJN

## LINKI POKREWNE

[Dodaj-AzureRmApiManagementRegion](./Add-AzureRmApiManagementRegion.md)

[Remove-AzureRmApiManagementRegion](./Remove-AzureRmApiManagementRegion.md)

[Update-AzureRmApiManagementDeployment](./Update-AzureRmApiManagementDeployment.md)
