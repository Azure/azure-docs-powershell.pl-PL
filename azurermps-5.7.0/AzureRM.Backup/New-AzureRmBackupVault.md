---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 015E3BC9-C535-4EA2-8A30-C728385DBFF8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/new-azurermbackupvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupVault.md
ms.openlocfilehash: 77c2df1ec61b42aaded458bea564cf6c953c90ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550663"
---
# New-AzureRmBackupVault

## STRESZCZENIe
Tworzy magazyn kopii zapasowych.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
New-AzureRmBackupVault [-ResourceGroupName] <String> [-Name] <String> [-Region] <String>
 [[-Storage] <AzureBackupVaultStorageType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzureRmBackupVault** tworzy magazyn kopii zapasowych platformy Azure.
To polecenie cmdlet zwraca obiekt **AzureRmBackupVault** , który działa jako odwołanie do jednostki magazynu.

## Przykłady

### Przykład 1. Tworzenie magazynu kopii zapasowych
```
PS C:\>New-AzureRmBackupVault -ResourceGroupName "ResourceGroup01" -Name "Vault03" -Region "westus"
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup01/providers/Microsoft.Backup
                    /BackupVault/Vault03
Name              : Vault03
ResourceGroupName : ResourceGroup01
Region            : westus
Storage           : GeoRedundant
```

To polecenie tworzy magazyn kopii zapasowych Azure o nazwie Vault03.
Magazyn znajduje się w grupie zasobów o nazwie ResourceGroup01 w zachodnim regionie Stanów Zjednoczonych.
Magazyn używa domyślnego typu magazynu nadmiarowego.

### Przykład 2: Tworzenie magazynu kopii zapasowych używającego lokalnie nadmiarowego miejsca do magazynowania
```
PS C:\>New-AzureRmBackupVault -ResourceGroupName "ResourceGroup02" -Name "Vault03" -Region "westus" -Storage LocallyRedundant
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup02/providers/Microsoft.Backup
                    /BackupVault/Vault03
Name              : Vault03
ResourceGroupName : ResourceGroup02
Region            : westus
Storage           : LocallyRedundant
```

To polecenie tworzy magazyn kopii zapasowych Azure o nazwie Vault03.
Magazyn znajduje się w grupie zasobów o nazwie ResourceGroup02 w zachodnim regionie Stanów Zjednoczonych.
Magazyn używa typu magazynu LocallyRedundant.

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

### -Name (nazwa)
Określa nazwę magazynu kopii zapasowych platformy Azure.
Nazwa musi być unikatowa w grupie zasobów.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Region
Określa obszar platformy Azure, w którym istnieje magazyn kopii zapasowych.
W przypadku scenariuszy hybrydowych kopii zapasowych zalecamy utworzenie magazynu w regionie blisko lokalnego serwera w celu skrócenia czasu oczekiwania.
Aby utworzyć kopię zapasową infrastruktury platformy Azure jako maszyn wirtualnych usługi (IaaS), magazyn staje się punktem odnajdowania lokalnych maszyn wirtualnych.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę istniejącej grupy zasobów platformy Azure, w której to polecenie cmdlet tworzy magazyn kopii zapasowych.
Aby utworzyć grupę zasobów, użyj polecenia cmdlet New-AzureRMResourceGroup.
Grupa zasobów i magazyn kopii zapasowych Azure nie muszą znajdować się w tym samym regionie.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Storage
Określa typ magazynu dla danych kopii zapasowej.
Dopuszczalne wartości tego parametru to: LocallyRedundant i geo.
Wartość domyślna jest zbyt nadmiarowa.

```yaml
Type: AzureBackupVaultStorageType
Parameter Sets: (All)
Aliases: 
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono

## WYSYŁA

### AzureRmBackupVault

## INFORMACYJN
* Znaleziono

## LINKI POKREWNE

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)

[Remove-AzureRmBackupVault](./Remove-AzureRmBackupVault.md)

[Set-AzureRmBackupVault](./Set-AzureRmBackupVault.md)


