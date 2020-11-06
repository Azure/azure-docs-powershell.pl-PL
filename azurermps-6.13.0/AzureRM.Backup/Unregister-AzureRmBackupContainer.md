---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 922BEA08-6619-4D4C-86EC-58279C9E1D93
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/unregister-azurermbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Unregister-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Unregister-AzureRmBackupContainer.md
ms.openlocfilehash: 8c90137e142086d7ea7c0bcc34321b3f38a12d95
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541939"
---
# Unregister-AzureRmBackupContainer

## STRESZCZENIe
Wyrejestrowuje kontener z magazynu kopii zapasowych.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Unregister-AzureRmBackupContainer [-Force] [-Container] <AzureRMBackupContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Unregister-AzureRmBackupContainer** umożliwia Wyrejestrowanie maszyny wirtualnej systemu Windows Server lub platformy Azure z magazynu kopii zapasowych platformy Azure.
To polecenie cmdlet usuwa odwołania do kontenera z magazynu kopii zapasowych.
Przed wyrejestrowaniem kontenera musisz usunąć wszelkie chronione dane skojarzone z tym kontenerem.

## Przykłady

### Przykład 1: Wyrejestrowanie systemu Windows Server
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type Windows -Name "server01.contoso.com"
PS C:\> Unregister-AzureRmBackupContainer -Container $Container[0]
Unregister Server
This operation will delete all data in the backup vault that is associated with the server. Are you sure you want to unregister the server? 
[] Yes  [] No  [?] Help (default is "No"): Yes
```

Pierwsze polecenie uzyskuje magazyn o nazwie Vault03 przy użyciu polecenia cmdlet Get-AzureRmBackupVault.
Polecenie zapisuje ten obiekt w zmiennej $Vault.
Drugie polecenie pobiera kontener o określonej nazwie w magazynie w $Vault przy użyciu Get-AzureRmBackupContainer polecenia cmdlet.
Polecenie zapisuje ten obiekt w zmiennej $Container.
Polecenie ostatnie wyrejestrowuje określony serwer z magazynu kopii zapasowych platformy Azure.

### Przykład 2: Wyrejestrowanie serwera Windows bez potwierdzenia
```
PS C:\>Unregister-AzureRmBackupContainer -Container $Container[0] -Force
```

To polecenie wyrejestrowuje określony serwer z magazynu kopii zapasowych platformy Azure, tak jak w pierwszym przykładzie.
To polecenie określa parametr *Force* .
Dlatego polecenie nie monituje o potwierdzenie.

## PARAMETRÓW

### -Kontener
Określa, że wyrejestruje się to polecenie cmdlet w systemie Windows Server lub maszynie wirtualnej Azure.
Aby uzyskać **AzureRmBackupContainer** , użyj polecenia cmdlet Get-AzureRmBackupContainer.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

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

### -Force
Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.
Ten parametr dotyczy tylko obiektów **AzureBackupContainer** typu Windows.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.
Polecenie cmdlet nie jest uruchamiane.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Microsoft. Azure. Commands. AzureBackup. models. AzureRMBackupContainer
Parametry: kontener (ByValue)

## WYSYŁA

### Microsoft. Azure. Commands. AzureBackup. models. AzureRMBackupJob

## INFORMACYJN
* Znaleziono

## LINKI POKREWNE

[Get-AzureRmBackupContainer](./Get-AzureRmBackupContainer.md)

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)

[Rejestr — AzureRmBackupContainer](./Register-AzureRmBackupContainer.md)


