---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: F3774658-A5E4-40BE-9A85-B33C70BC0A09
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupContainer.md
ms.openlocfilehash: e20276d8a2dfec8ffb39665e5122cfe4be74dc42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716962"
---
# Get-AzureRmBackupContainer

## STRESZCZENIe
Pobiera kontenery kopii zapasowych.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Get-AzureRmBackupContainer [-Name <String>] -Type <AzureBackupContainerType>
 [-ManagedResourceGroupName <String>] [-Status <AzureBackupContainerRegistrationStatus>]
 [-Vault] <AzureRMBackupVault> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRmBackupContainer** pobiera kontenery kopii zapasowych Azure.
**AzureBackupContainer** hermetyzuje źródła danych, elementy chronione i punkty odzyskiwania.
**AzureBackupContainer** może być jednym z następujących: 
- Komputer z systemem Windows Server
- Serwer programu System Center Data Protection Manager (SCDPM) 
- Infrastruktura usługi Azure jako maszyna wirtualna usługi (IaaS) zanim kopia zapasowa może utworzyć kopię zapasową źródła danych lub elementu, należy zarejestrować kontener znajdujący się w usłudze kopii zapasowej Azure.
Aby można było wysyłać dane kopii zapasowej do magazynu kopii zapasowych, kontener musi być uwierzytelniony.
W przypadku komputerów z systemem Windows Server i serwerów SCDPM Rejestracja odbywa się przy użyciu w pełni kwalifikowanej nazwy domeny serwera.

## Przykłady

### Przykład 1: wyświetlanie wszystkich serwerów zarejestrowanych w magazynie
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupContainer -Vault $Vault -Type Windows
Name                         Type               Status
----                         ----               ------
SERVER01.CONTOSO.COM          Windows            Registered
SERVER02.CONTOSO.COM          Windows            Registered
```

Pierwsze polecenie uzyskuje magazyn o nazwie Vault03 przy użyciu polecenia cmdlet **Get-AzureRmBackupVault** .
Polecenie zapisuje ten obiekt w zmiennej $Vault.
Drugie polecenie pobiera wszystkie kontenery typu Windows z magazynu w $Vault.

### Przykład 2: uzyskiwanie określonego kontenera
```
PS C:\>Get-AzureRmBackupContainer -Vault $Vault -Type SCDPM -Name "DPMSERVER.CONTOSO.COM"
Name                         Type               Status
----                         ----               ------
DPMSERVER.CONTOSO.COM        SCDPM              Registered
```

To polecenie uzyskuje kontener o nazwie DPMSERVER. CONTOSO.COM.
To polecenie określa magazyn w $Vault i typ kontenera.

### Przykład 3: wyświetlanie wszystkich zarejestrowanych maszyn wirtualnych platformy Azure
```
PS C:\>Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Status Registered 
Name                         Type               Status
----                         ----               ------
co03-vm                      AzureVM            Registered
```

To polecenie umożliwia pobieranie zarejestrowanych maszyn wirtualnych z magazynu w $Vault.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure

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

### -ManagedResourceGroupName
Określa nazwę grupy zasobów skojarzonej z kontenerem.
Ta nazwa jest taka sama, jak wartość określona dla parametru *ServiceName* lub *ResourceGroupName* polecenia cmdlet Register-AzureRmBackupContainer.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę kontenera, który jest pobierany przez to polecenie cmdlet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Status
Określa bieżący stan kontenerów, które są pobierane przez to polecenie cmdlet.
Dopuszczalne wartości tego parametru to:
- NotRegistered 
- Zarejestrować 
- Rejestracj

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupContainerRegistrationStatus
Parameter Sets: (All)
Aliases:
Accepted values: Registered, Registering, NotRegistered

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Type
Określa typy kontenerów, które są pobierane przez to polecenie cmdlet.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupContainerType
Parameter Sets: (All)
Aliases:
Accepted values: Windows, SCDPM, AzureVM, AzureBackupServer, Other

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Magazyn
Określa magazyn kopii zapasowych, z którego to polecenie cmdlet pobiera kontenery.
Aby uzyskać **AzureRmBackupVault** , użyj polecenia cmdlet Get-AzureRmBackupVault.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Microsoft. Azure. Commands. AzureBackup. models. AzureRMBackupVault
Parametry: Magazyn (ByValue)

## WYSYŁA

### Microsoft. Azure. Commands. AzureBackup. models. AzureRMBackupContainer

## INFORMACYJN
* Znaleziono

## LINKI POKREWNE

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)

[Rejestr — AzureRmBackupContainer](./Register-AzureRmBackupContainer.md)

[Wyrejestrowanie — AzureRmBackupContainer](./Unregister-AzureRmBackupContainer.md)


