---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 95FF3F7A-5CC6-4AA6-A393-5EBB5579D9A2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVault.md
ms.openlocfilehash: 18383ffeb35b1ce6bb2651be041e07b6164e55da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718962"
---
# Get-AzureRmBackupVault

## STRESZCZENIe
Pobiera magazyny kopii zapasowych.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Get-AzureRmBackupVault [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRmBackupVault** pobiera magazyny kopii zapasowych Azure.
To polecenie cmdlet zwraca obiekty **AzureRmBackupVault** , które mają być używane z innymi poleceniami cmdlet.

## Przykłady

### Przykład 1: wyświetlanie wszystkich magazynów kopii zapasowych
```
PS C:\>Get-AzureRmBackupVault
```

To polecenie pobiera wszystkie magazyny kopii zapasowych platformy Azure.

### Przykład 2: wyświetlanie wszystkich magazynów utworzonych w STANach na zachód
```
PS C:\>Get-AzureRmBackupVault | Where-Object { $_.Region -eq "westus" }
```

To polecenie pobiera wszystkie magazyny kopii zapasowych.
Polecenie przekazuje je do polecenia cmdlet Where-Object przy użyciu operatora potoku.
Polecenie cmdlet filtruje wyniki na podstawie właściwości **region** .
Aby uzyskać więcej informacji, wpisz tekst `Get-Help Where-Object` .

### Przykład 3: uzyskiwanie określonego magazynu
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03"
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup011/providers/Microsoft.Backup
                    /BackupVault/Vault
Name              : Vault03
ResourceGroupName : ResourceGroup01
Region            : westus
Storage           : GeoRedundant
```

To polecenie pobiera magazyn o nazwie Vault03.

### Przykład 4: zliczanie magazynów z lokalnie nadmiarowym magazynem
```
PS C:\>Get-AzureRmBackupVault | Where-Object { $_.Storage -match "LocallyRedundant" } | Measure-Object
Count    : 4
Average  : 
Sum      : 
Maximum  : 
Minimum  : 
Property :
```

To polecenie pobiera wszystkie magazyny kopii zapasowych platformy Azure.
Polecenie przekazuje je do **obiektu WHERE-Object** , który filtruje wyniki na podstawie właściwości **magazynu** .
Polecenie przekazuje te elementy, które mają wartość LocallyRedundant, do polecenia cmdlet Measure-Object, które zlicza wyniki.
Aby uzyskać więcej informacji, wpisz tekst `Get-Help Measure-Object` .

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
Określa nazwę magazynu kopii zapasowych, który jest pobierany przez to polecenie cmdlet.
Jeśli więcej niż jeden magazyn kopii zapasowych ma taką samą nazwę, to polecenie cmdlet zwróci je wszystkie.
Określ parametr *ResourceGroupName* , aby uzyskać unikatowy magazyn.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów platformy Azure, w której to polecenie cmdlet pobiera magazyn kopii zapasowych.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono
To polecenie cmdlet nie akceptuje żadnych danych wejściowych.

## WYSYŁA

### AzureRmBackupVault

## INFORMACYJN
* Znaleziono

## LINKI POKREWNE

[Get-AzureRmBackupContainer](./Get-AzureRmBackupContainer.md)

[Nowe — AzureRmBackupVault](./New-AzureRmBackupVault.md)

[Remove-AzureRmBackupVault](./Remove-AzureRmBackupVault.md)

[Set-AzureRmBackupVault](./Set-AzureRmBackupVault.md)


