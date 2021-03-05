---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/powershell/module/az.importexport/get-azimportexportlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
ms.openlocfilehash: 928ac0254619a2924421a0b52bf20212b8ba19a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962986"
---
# Get-AzImportExportLocation

## SYNOPSIS
Zwraca szczegółowe informacje o lokalizacji, do której można wysłać dyskietki skojarzone z zadaniem importu lub eksportu.
Lokalizacja to region platformy Azure.

## SKŁADNIA

### Lista (domyślna)
```
Get-AzImportExportLocation [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Pobierz
```
Get-AzImportExportLocation -Name <String> [-AcceptLanguage <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzImportExportLocation -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## OPIS
Zwraca szczegółowe informacje o lokalizacji, do której można wysłać dyskietki skojarzone z zadaniem importu lub eksportu.
Lokalizacja to region platformy Azure.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie wszystkich szczegółów lokalizacji regionu platformy Azure z kontekstem domyślnym
```powershell
PS C:\> Get-AzImportExportLocation
Name                 Type
----                 ----
Australia East       Microsoft.ImportExport/locations
Australia Southeast  Microsoft.ImportExport/locations
Brazil South         Microsoft.ImportExport/locations
Canada Central       Microsoft.ImportExport/locations
Canada East          Microsoft.ImportExport/locations
...
West Central US      Microsoft.ImportExport/locations
West Europe          Microsoft.ImportExport/locations
West India           Microsoft.ImportExport/locations
West US              Microsoft.ImportExport/locations
West US 2            Microsoft.ImportExport/locations
```

To polecenie cmdlet pobiera wszystkie szczegóły lokalizacji regionu platformy Azure z kontekstem domyślnym.

### Przykład 2. Uzyskiwanie szczegółów lokalizacji regionu platformy Azure według nazwy lokalizacji
```powershell
PS C:\> Get-AzImportExportLocation -Name eastus
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

To polecenie cmdlet pobiera szczegółowe informacje o lokalizacji regionu platformy Azure według nazwy lokalizacji.

### Przykład 3. Uzyskiwanie szczegółów lokalizacji regionu platformy Azure według tożsamości
```powershell
PS C:\> $Id = "/providers/Microsoft.ImportExport/locations/eastus"
PS C:\> Get-AzImportExportLocation -InputObject $Id
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

Te listy polecenia cmdlet pobierają szczegółowe informacje o lokalizacji regionu platformy Azure według tożsamości.

## PARAMETERS

### -AcceptLanguage
Określa preferowany język odpowiedzi.

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

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### — Nazwa
Nazwa lokalizacji.
Na przykład Stany Zjednoczone Lub Zachód.

```yaml
Type: System.String
Parameter Sets: Get
Aliases: LocationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Microsoft.Azure.PowerShell.Cmdlet.ImportExport.Models.IImportExportIdentity

## DANE WYJŚCIOWE

### Microsoft.Azure.PowerShell.cmdlet.ImportExport.Models.Api20161101.ILocation

## NOTATKI

ALIASY

ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW

Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości. Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.


INPUTOBJECT: <IImportExportIdentity> Parametr tożsamości
  - `[Id <String>]`: ścieżka tożsamości zasobu
  - `[JobName <String>]`: nazwa zadania importu/eksportu.
  - `[LocationName <String>]`: nazwa lokalizacji. Na przykład Stany Zjednoczone Lub Zachód.
  - `[ResourceGroupName <String>]`: Nazwa grupy zasobów jednoznacznie identyfikuje grupę zasobów w ramach subskrypcji użytkownika.
  - `[SubscriptionId <String>]`: Identyfikator subskrypcji dla użytkownika platformy Azure.

## LINKI POKREWNE

