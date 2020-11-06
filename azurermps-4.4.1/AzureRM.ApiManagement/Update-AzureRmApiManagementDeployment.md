---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 56604912-53A0-496D-9BDC-472BCE45A6A2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementDeployment.md
ms.openlocfilehash: e4170dbe2a1ac4ed8ad39bdb7a5db6d7174555e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525741"
---
# Update-AzureRmApiManagementDeployment

## STRESZCZENIe
Aktualizuje wdrożenie usługi zarządzania interfejsem API.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### Określona usługa zarządzania interfejsem API (domyślnie)
```
Update-AzureRmApiManagementDeployment -ResourceGroupName <String> -Name <String> -Location <String>
 -Sku <PsApiManagementSku> -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-VpnType <PsApiManagementVpnType>]
 [-AdditionalRegions <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Aktualizacja z wystąpienia PsApiManagement
```
Update-AzureRmApiManagementDeployment -ApiManagement <PsApiManagement> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Update-AzureRmApiManagementDeployment** aktualizuje bieżące wdrożenia usługi zarządzania interfejsem API.

## Przykłady

### Przykład 1: aktualizowanie wdrożenia wystąpienia programu ApiManagement
```
PS C:\>Update-AzureRmApiManagementDeployment -ResourceGroupName "Contoso" -Name "ContosoApi" -Sku "Standard" -Capacity 3
```

To polecenie aktualizuje wdrożenie wystąpienia zarządzania interfejsem API na trzy standardowe pojemności jednostki.

### Przykład 2: Pobieranie wystąpienia ApiManagement i skalowanie go
```
PS C:\>$ApiManagement = Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi"
PS C:\> $ApiManagement.Sku = "Premium"
PS C:\> $ApiManagement.Capacity = 5
PS C:\> $ApiManagement.AddRegion("Central US", "Premium", 3)
PS C:\> Update-AzureRmApiManagementDeployment -ApiManagement $ApiManagement
```

W tym przykładzie otrzymano instancję zarządzania interfejsem API, przeskaluje ją do pięciu jednostek Premium, a następnie dodaje kolejne trzy jednostki do regionu Premium.

### Przykład 3: wdrożenie aktualizacji (zewnętrzna Sieć wirtualna)
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-West-US/providers/Microsoft.ClassicNetwork/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $virtualNetwork -VpnType "External"
```

To polecenie aktualizuje istniejące wdrożenie zarządzania interfejsem API i dołącza do zewnętrznego *VpnType*.

### Przykład 4: wdrożenie aktualizacji (wewnętrzna sieć wirtualna)
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-West-US/providers/Microsoft.ClassicNetwork/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $virtualNetwork -VpnType "Internal"
```

To polecenie aktualizuje istniejące wdrożenie zarządzania interfejsem API i łączy z *VpnType* wewnętrznym.

## PARAMETRÓW

### -AdditionalRegions
Określa dodatkowe regiony wdrażania usługi Azure API Management.

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion]
Parameter Sets: Specific API Management service
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ApiManagement
Określa wystąpienie **PsApiManagement** , z którego ma zostać pozyskana konfiguracja wdrożenia.
Tego parametru należy użyć, jeśli wystąpienie zawiera już wszystkie wymagane zmiany.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: Update from PsApiManagement instance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Pojemność
Określa pojemność jednostki SKU głównego obszaru wdrażania zarządzania interfejsem API platformy Azure.

```yaml
Type: System.Int32
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Lokalizacja
Określa lokalizację regionu wdrażania zarządzania głównym interfejsem API.

Dopuszczalne wartości tego parametru to:

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
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę zarządzania interfejsem API, które jest aktualizowane przez to polecenie cmdlet.

```yaml
Type: System.String
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Zwraca obiekt reprezentujący element, z którym pracujesz.
Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.

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

### -ResourceGroupName
Określa nazwę grupy zasobów, pod którą istnieje zarządzanie interfejsem API.

```yaml
Type: System.String
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SKU
Określa warstwę regionu wdrażania zarządzania INTERFEJSem głównym platformy Azure.

Dopuszczalne wartości tego parametru to:

- Deweloper
- Standard
- Ubezpieczeni

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: Specific API Management service
Aliases: 
Accepted values: Developer, Standard, Premium

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetwork
Określa konfigurację sieci wirtualnej regionu wdrażania zarządzania INTERFEJSem głównym platformy Azure.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: Specific API Management service
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VpnType
Określa typ sieci wirtualnej wdrożenia funkcji zarządzania interfejsem API.
Dopuszczalne wartości tego parametru to:

- Znaleziono.
Wdrożenie zarządzania interfejsem API nie jest częścią żadnej sieci wirtualnej.
Jest to wartość domyślna. 
- Zewnętrz.
Wdrożenie zarządzania interfejsem API ma zewnętrzny, stojący adres wirtualny. 
- Wspólnego.
Wdrożenie zarządzania interfejsem API ma adres wirtualny w intranecie.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVpnType
Parameter Sets: Specific API Management service
Aliases: 
Accepted values: None, External, Internal

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

[Get-AzureRmApiManagement](./Get-AzureRmApiManagement.md)


