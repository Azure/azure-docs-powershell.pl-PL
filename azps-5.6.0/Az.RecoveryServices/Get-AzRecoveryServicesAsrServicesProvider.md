---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 3b32ba7f5818987e130595990a98df2668459385
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003201"
---
# Get-AzRecoveryServicesAsrServicesProvider

## SYNOPSIS
Pobiera szczegółowe informacje o dostawcach usług odzyskiwania asr zarejestrowanych w magazynie usług odzyskiwania.

## SKŁADNIA

### Domyślne (domyślne)
```
Get-AzRecoveryServicesAsrServicesProvider -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByName
```
Get-AzRecoveryServicesAsrServicesProvider -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFriendlyName
```
Get-AzRecoveryServicesAsrServicesProvider -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzRecoveryServicesAsrServicesProvider** pobiera informacje o dostawcach usługi Azure Site Recovery w magazynie.

## PRZYKŁADY

### Przykład 1
```powershell
PS C:\> $RSPs = Get-AzRecoveryServicesAsrFabric | Get-AzRecoveryServicesAsrServicesProvider
```

W tym miejscu należy wyświetlić listę wszystkich dostawców usług replikacji asr zarejestrowanych w magazynie usług odzyskiwania, który odpowiada określonego szkieletowi.

### Przykład 2

Pobiera szczegółowe informacje o dostawcach usług odzyskiwania asr zarejestrowanych w magazynie usług odzyskiwania. (wygenerowane automatycznie)

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesAsrServicesProvider -Fabric $Fabric
```

## PARAMETERS

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

### — Materiał
Określa obiekt z materiału ASR.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -FriendlyName
Określa przyjazną nazwę dostawcy usług odzyskiwania ASR, dla których mają być uzyskać szczegółowe informacje.

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Nazwa
Określa nazwę dostawcy usług odzyskiwania asr, dla których mają być szczegółowe informacje.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider

## NOTATKI

## LINKI POKREWNE

[Remove-AzRecoveryServicesAsrServicesProvider](./Remove-AzRecoveryServicesAsrServicesProvider.md)

[Update-AzRecoveryServicesAsrServicesProvider](./Update-AzRecoveryServicesAsrServicesProvider.md)
