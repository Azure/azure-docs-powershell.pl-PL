---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 2605B232-10CA-4426-9917-7C9719C15166
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/enable-azurermbackupcontainerreregistration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupContainerReregistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupContainerReregistration.md
ms.openlocfilehash: 6ae660eae9e597d92e162529ff244431d4720418
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541972"
---
# Enable-AzureRmBackupContainerReregistration

## STRESZCZENIe
Powoduje ponowne zarejestrowanie serwera w celu nawiązania połączenia z magazynem kopii zapasowych.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Enable-AzureRmBackupContainerReregistration [-Container] <AzureRMBackupContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **enable-AzureRmBackupContainerReregistration** umożliwia ponowne zarejestrowanie serwera w celu nawiązania połączenia z magazynem kopii zapasowych platformy Azure i kontynuowanie łańcucha punktów odzyskiwania kopii zapasowych.
W przypadku zniszczenia serwera wszystkie punkty kopii zapasowej w chmurze pozostaną w magazynie kopii zapasowych.
Jeśli utworzysz serwer zastępczy i przypiszesz mu tę samą w pełni kwalifikowaną nazwę domeny, możesz połączyć serwer z powrotem do tego samego magazynu.
To polecenie cmdlet umożliwia wykonywanie kopii zapasowych i dodawanie nowych punktów kopii zapasowej do istniejącego zestawu.
Nowy serwer nadal znajduje się w łańcuchu kopii zapasowych.

## Przykłady

## PARAMETRÓW

### -Kontener
Określa kontener, który zostanie ponownie przerejestrowany przez ten aplet polecenia.
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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Microsoft. Azure. Commands. AzureBackup. models. AzureRMBackupContainer
Parametry: kontener (ByValue)

## WYSYŁA

### System. void

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRmBackupContainer](./Get-AzureRmBackupContainer.md)

[Rejestr — AzureRmBackupContainer](./Register-AzureRmBackupContainer.md)


