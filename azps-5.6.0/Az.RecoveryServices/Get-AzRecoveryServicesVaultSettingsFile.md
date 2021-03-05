---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: b71da123933cd190038164b67d37fb81b0d5c973
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003178"
---
# Get-AzRecoveryServicesVaultSettingsFile

## SYNOPSIS
Pobiera plik ustawień magazynu usługi Azure Site Recovery.

## SKŁADNIA

### ForSiteWithCertificate
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -SiteIdentifier <String>
 -Certificate <String> -SiteFriendlyName <String> [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByDefaultWithCertificate
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -Certificate <String>
 [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ForBackupVaultTypeWithCertificate
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -Certificate <String> [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzRecoveryServicesVaultSettingsFile** pobiera plik ustawień dla magazynu odzyskiwania witryny platformy Azure.

## PRZYKŁADY

### Przykład 1. Rejestrowanie komputera z systemem Windows Server lub dpm na platformie Azure Backup
```powershell
PS C:\> $Vault01 = Get-AzRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

Pierwsze polecenie pobiera magazyn o nazwie TestVault, a następnie przechowuje go w zmiennej $Vault 01.
Drugie polecenie ustawia zmienną $CredsPath C:\Downloads.
Ostatnie polecenie pobiera plik poświadczeń magazynu dla $Vault 01 przy użyciu poświadczeń w usłudze $CredsPath dla usługi Azure Backup.

### Przykład 2
```powershell
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

Polecenie pobiera plik poświadczeń magazynu dla $Vault 01 typu magazynu siteRecovery.

### Przykład 3. Rejestrowanie komputera z systemem Windows Server lub dpm na platformie Azure Backup
```powershell
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

Polecenie pobiera plik poświadczeń magazynu dla $Vault 01.

## PARAMETERS

### — Kopia zapasowa
Wskazuje, że plik poświadczeń magazynu ma zastosowanie do usługi Azure Backup.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForBackupVaultTypeWithCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Certyfikat
{{Fill Certificate Description}}

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Ścieżka
Określa ścieżkę do pliku ustawień magazynu usługi Azure Site Recovery.
Możesz pobrać ten plik z portalu magazynu usługi Azure Site Recovery i przechowywać go lokalnie.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteFriendlyName
Określa przyjazną nazwę witryny.
Użyj tego parametru, jeśli pobierasz poświadczenia magazynu dla witryny hyper-V.

```yaml
Type: System.String
Parameter Sets: ForSiteWithCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteIdentifier
Określa identyfikator witryny.
Użyj tego parametru, jeśli pobierasz poświadczenia magazynu dla witryny hyper-V.

```yaml
Type: System.String
Parameter Sets: ForSiteWithCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteRecovery
Wskazuje, że plik poświadczeń magazynu ma zastosowanie do usługi Azure Site Recovery.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForSiteWithCertificate, ByDefaultWithCertificate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — magazyn
Określa obiekt magazynu usługi Azure Site Recovery.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.RecoveryServices.ARSVault

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath

## NOTATKI

## LINKI POKREWNE

[Get-AzRecoveryServicesVault](./Get-AzRecoveryServicesVault.md)

[New-AzRecoveryServicesVault](./New-AzRecoveryServicesVault.md)

[Remove-AzRecoveryServicesVault](./Remove-AzRecoveryServicesVault.md)


