---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationService.md
ms.openlocfilehash: 46455cbf411228f008bdc15c27f78715ccea0e89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718927"
---
# New-AzureRmDataMigrationService

## STRESZCZENIe
Tworzy nowe wystąpienie usługi migracji bazy danych platformy Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
New-AzureRmDataMigrationService -ResourceGroupName <String> -ServiceName <String> -Location <String>
 -Sku <String> -VirtualSubnetId <String> [-DefaultProfile <IAzureContextContainer>]
```

## Opis
Polecenie cmdlet New-AzureRmDataMigrationService tworzy nowe wystąpienie usługi migracji bazy danych platformy Azure. To polecenie cmdlet przyjmuje nazwę istniejącej grupy zasobów platformy Azure, unikatową nazwę nowego wystąpienia usługi migracji bazy danych platformy Azure, która ma zostać utworzona, region, w którym jest inicjowana instancja, nazwa SKU procesu roboczego DMS oraz nazwa podsieci wirtualnej platformy Azure, w której ma się znajdować usługa. Brak parametru dla nazwy subskrypcji, ponieważ oczekuje się, że użytkownik określi domyślną subskrypcję sesji logowania platformy Azure lub wykona Get-AzureRmSubscription-Subscriptionname "Moja subskrypcja" | Select-AzureRmSubscription, aby wybrać inny abonament.

## Przykłady

### Przykład 1
```
PS C:\> New-AzureRmDataMigrationService -ResourceGroupName myResourceGroup -ServiceName TestService -Location "Central US" -Sku Basic_2vCores -VirtualSubnetId $virtualSubNetId
```

W powyższym przykładzie pokazano, jak utworzyć nowe wystąpienie usługi migracji bazy danych platformy Azure o nazwie TestService w regionie Central Stanów Zjednoczonych.


## PARAMETRÓW

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
Lokalizacja wystąpienia usługi migracji bazy danych platformy Azure do utworzenia, które odpowiada obszarowi platformy Azure.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceName
Nazwa wystąpienia usługi migracji bazy danych platformy Azure.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SKU
Jednostka SKU wystąpienia usługi migracji bazy danych platformy Azure. Możliwe wartości są obecnie Basic_1vCore, Basic_2vCores GeneralPurpose_4vCores

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualSubnetId
Nazwa podsieci w określonej sieci wirtualnej używanej dla wystąpienia usługi migracji bazy danych platformy Azure.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```




## WYSYŁA

### Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService


## INFORMACYJN

## LINKI POKREWNE

