---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurermkeyvault
schema: 2.0.0
ms.openlocfilehash: 7cbcf722b71919096ca2c7d1dc3201ad2fe42f2a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898919"
---
# Get-AzureRmKeyVault

## STRESZCZENIe
Pobiera kluczowe magazyny.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### GetVaultByName
```
Get-AzureRmKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByDeletedVault
```
Get-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ListVaultsByResourceGroup
```
Get-AzureRmKeyVault [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ListAllDeletedVaultsInSubscription
```
Get-AzureRmKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ListAllVaultsInSubscription
```
Get-AzureRmKeyVault [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRmKeyVault** pobiera informacje o najważniejszych magazynach w ramach abonamentu. Możesz wyświetlić wszystkie wystąpienia najważniejszych magazynów w subskrypcji lub filtrować wyniki według grupy zasobów lub konkretnego magazynu kluczy.

Należy zauważyć, że chociaż określenie grupy zasobów jest opcjonalne dla tego polecenia cmdlet, w przypadku pojedynczego magazynu kluczy należy to zrobić w celu uzyskania lepszej wydajności.

## Przykłady

### Przykład 1: pobieranie wszystkich najważniejszych magazynów w bieżącej subskrypcji
```
PS C:\>Get-AzureRMKeyVault
```

To polecenie pobiera wszystkie kluczowe magazyny w bieżącej subskrypcji.

### Przykład 2: uzyskiwanie określonego magazynu kluczy
```
PS C:\>$MyVault = Get-AzureRMKeyVault -VaultName 'Contoso03Vault'
```

To polecenie pobiera kluczowy magazyn o nazwie Contoso03Vault w bieżącej subskrypcji, a następnie zapisuje go w zmiennej $MyVault. Możesz sprawdzić właściwości $MyVault, aby uzyskać szczegółowe informacje o magazynie kluczy.

### Przykład 3: uzyskiwanie najważniejszych magazynów w grupie zasobów
```
PS C:\>Get-AzureRmKeyVault -ResourceGroupName 'ContosoPayRollResourceGroup'
```

To polecenie pobiera wszystkie główne magazyny z grupy zasobów o nazwie ContosoPayRollResourceGroup.

### Przykład 4: pobieranie wszystkich usuniętych magazynów kluczy w bieżącej subskrypcji
```
PS C:\>Get-AzureRmKeyVault -InRemovedState
```

To polecenie pobiera wszystkie usunięte magazyny kluczy w bieżącej subskrypcji.

### Przykład 5: uzyskiwanie usuniętego magazynu kluczy
```
PS C:\>Get-AzureRMKeyVault -VaultName 'Contoso03Vault'  -Location 'eastus2' -InRemovedState
```

To polecenie pobiera usunięte informacje o magazynie kluczy o nazwie Contoso03Vault w bieżącej subskrypcji i w regionie eastus2.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure

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

### -InRemovedState
Określa, czy w wyniku mają być pokazywane uprzednio usunięte magazyny.

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedVault, ListAllDeletedVaultsInSubscription
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Lokalizacja
Lokalizacja usuniętego magazynu.

```yaml
Type: String
Parameter Sets: ByDeletedVault
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów skojarzonej z badanym magazynem kluczy lub kluczami kluczy, których dotyczy zapytanie.

```yaml
Type: String
Parameter Sets: GetVaultByName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ListVaultsByResourceGroup
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Pary klucz-wartość w formie tabeli skrótów. Na przykład:

@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}

```yaml
Type: Hashtable
Parameter Sets: ListAllVaultsInSubscription
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Magazynname
Określa nazwę magazynu kluczy.

```yaml
Type: String
Parameter Sets: GetVaultByName, ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

### Microsoft. Azure. Commands. platforming. models. PSVault

### System. Collections. Generic. list "1 [Microsoft. Azure. Commands. platforming. modele. PSVaultIdentityItem]

### Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault

### System. Collections. Generic. list "1 [Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault]

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzureRmKeyVault](./New-AzureRmKeyVault.md)

[Remove-AzureRmKeyVault](./Remove-AzureRmKeyVault.md)
