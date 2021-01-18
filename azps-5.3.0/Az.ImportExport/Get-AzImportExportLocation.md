---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexportlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
ms.openlocfilehash: c603c01619128d1697256174e9d0bc00a1cea8ff
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503532"
---
# Get-AzImportExportLocation

## STRESZCZENIe
Zwraca szczegóły dotyczące lokalizacji, do której można wysłać dyski skojarzone z zadaniem importu lub eksportu.
Lokalizacja to obszar platformy Azure.

## POLECENIA

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

## Opis
Zwraca szczegóły dotyczące lokalizacji, do której można wysłać dyski skojarzone z zadaniem importu lub eksportu.
Lokalizacja to obszar platformy Azure.

## Przykłady

### Przykład 1. Uzyskaj wszystkie szczegóły lokalizacji na platformie Azure z kontekstem domyślnym
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

To polecenie cmdlet uzyskuje wszystkie szczegóły lokalizacji na platformie Azure z kontekstem domyślnym.

### Przykład 2: szczegółowe informacje o lokalizacji w systemie Azure według nazwy lokalizacji
```powershell
PS C:\> Get-AzImportExportLocation -Name eastus
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

To polecenie cmdlet pobiera dane lokalizacji regionu platformy Azure według nazwy lokalizacji.

### Przykład 3: uzyskiwanie szczegółowych informacji o lokalizacji w systemie Azure według tożsamości
```powershell
PS C:\> $Id = "/providers/Microsoft.ImportExport/locations/eastus"
PS C:\> Get-AzImportExportLocation -InputObject $Id
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

Te listy poleceń cmdlet pobierają dane lokalizacji regionu platformy Azure według tożsamości.

## PARAMETRÓW

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
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

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

### -Inputobject
Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.

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

### -Name (nazwa)
Nazwa lokalizacji.
Na przykład w przypadku zachodniego, USA lub zachodniego.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### Microsoft. Azure. PowerShell. polecenia. ImportExport. models. IImportExportIdentity

## WYSYŁA

### Microsoft. Azure. PowerShell. polecenia. ImportExport. models. Api20161101. ILocation

## INFORMACYJN

PISUJE

ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW

Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości. Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.


INPUTobject <IImportExportIdentity> : parametr Identity
  - `[Id <String>]`: Ścieżka tożsamości zasobu
  - `[JobName <String>]`: Nazwa zadania importu/eksportu.
  - `[LocationName <String>]`: Nazwa lokalizacji. Na przykład w przypadku zachodniego, USA lub zachodniego.
  - `[ResourceGroupName <String>]`: Nazwa grupy zasobów jednoznacznie identyfikuje grupę zasobów w ramach abonamentu użytkownika.
  - `[SubscriptionId <String>]`: Identyfikator subskrypcji użytkownika platformy Azure.

## LINKI POKREWNE

