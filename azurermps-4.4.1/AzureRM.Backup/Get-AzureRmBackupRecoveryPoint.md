---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6778E018-B6CC-468A-823E-3DA047EA6B52
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupRecoveryPoint.md
ms.openlocfilehash: 0a5c5f42f7a6f4755335a5b8827fd2d23e096679
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528289"
---
# Get-AzureRmBackupRecoveryPoint

## STRESZCZENIe
Pobiera punkty odzyskiwania dla elementu z kopii zapasowej.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Get-AzureRmBackupRecoveryPoint [[-RecoveryPointId] <String>] [-Item] <AzureRMBackupItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRmBackupRecoveryPoint** pobiera punkty odzyskiwania dla kopii zapasowej elementu kopii zapasowej platformy Azure.
Po wykonaniu kopii zapasowej elementu kopia zapasowa przechowuje jeden lub więcej punktów odzyskiwania.

## Przykłady

### Przykład 1: uzyskiwanie punktów odzyskiwania dla elementu
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> $BackupItem = Get-AzureRmBackupItem -Container $Container
PS C:\> Get-AzureRmBackupRecoveryPoint -Item $BackupItem
RecoveryPointId    RecoveryPointType  RecoveryPointTime      ContainerName
---------------    -----------------  -----------------      -------------
15273496567119     AppConsistent      26-Aug-15 12:27:38 PM  iaasvmcontainer;conto02-vm;conto0...
```

Pierwsze polecenie uzyskuje magazyn o nazwie Vault03 przy użyciu polecenia cmdlet Get-AzureRmBackupVault.
Polecenie zapisuje ten obiekt w zmiennej $Vault.

Drugie polecenie pobiera kontener o określonej nazwie w magazynie w $Vault przy użyciu polecenia cmdlet **Get-AzureRmBackupContainer** .
Polecenie zapisuje ten obiekt w zmiennej $Container.

Trzecie polecenie pobiera element kopii zapasowej w kontenerze w $Container przy użyciu polecenia cmdlet **Get-AzureRmBackupItem** .
Polecenie zapisuje ten obiekt w zmiennej $BackupItem.

Polecenie ostatnie pobiera punkty odzyskiwania dla elementu w $BackupItem.

## PARAMETRÓW

### -Item
Określa element, dla którego to polecenie cmdlet umożliwia pobieranie punktów odzyskiwania.
Aby uzyskać **AzureRmBackupItem** , użyj polecenia cmdlet Get-AzureRmBackupItem.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RecoveryPointId
Określa identyfikator punktu odzyskiwania, który jest pobierany przez to polecenie cmdlet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
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

### AzureRmBackupItem

## WYSYŁA

### AzureRmBackupRecoveryPoint

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRmBackupContainer](./Get-AzureRmBackupContainer.md)

[Get-AzureRmBackupItem](./Get-AzureRmBackupItem.md)

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)


