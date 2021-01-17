---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
ms.openlocfilehash: fcedf52f75b73cc35b7f0e4fd0856600bca6fc71
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363946"
---
# Get-AzRecoveryServicesVault

## STRESZCZENIe

Pobiera listę magazynów usług odzyskiwania.

## POLECENIA

### ByTagNameValueParameterSet
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] [-TagName <String>]
 [-TagValue <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByTagObjectParameterSet
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] -Tag <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis

Polecenie cmdlet **Get-AzRecoveryServicesVault** pobiera listę magazynów usług odzyskiwania w bieżącej subskrypcji.

## Przykłady

### Przykład 1

```powershell
PS C:\> Get-AzRecoveryServicesVault
```

Pobierz listę magazynów w wybranej subskrypcji.

### Przykład 2

```powershell
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

Pobierz listę magazynów w grupie zasób w wybranej subskrypcji.

### Przykład 3

```powershell
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
```

Pobierz magazyn w grupie zasobów o podanej nazwie.

## PARAMETRÓW

### -DefaultProfile

Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

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

### -Name (nazwa)

Określa nazwę magazynu, którego ma dotyczyć kwerenda.

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

### -ResourceGroupName

Określa nazwę grupy zasobów platformy Azure, z której ma zostać pobrany określony obiekt usług Recovery Services.

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

### -Tag

Określa Tagi do zbadania

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTagObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TagName

Określa klucz znacznika, dla którego ma zostać wyszukiwana kwerenda.

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TagValue

Określa wartość tagu, dla którego ma zostać wyszukiwana kwerenda.

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### Znaleziono

## WYSYŁA

### Microsoft. Azure. Commands. RecoveryServices. ARSVault

## INFORMACYJN
Get-AzRecoveryServicesVault w starej wersji AZ. RecoveryServices (<= 2.10.0) nie może działać z usługą AZ. accounts (>= 1.8.1) ze względu na niepoprawne odwołanie do zestawu. Moduł AZ. RecoveryServices musi zostać uaktualniony do 2.11.0 lub nowszego, jeśli używasz najnowszych lub AZ. kont.

## LINKI POKREWNE

[Get-AzRecoveryServicesVaultSettingsFile](./Get-AzRecoveryServicesVaultSettingsFile.md)

[Nowe — AzRecoveryServicesVault](./New-AzRecoveryServicesVault.md)

[Remove-AzRecoveryServicesVault](./Remove-AzRecoveryServicesVault.md)
