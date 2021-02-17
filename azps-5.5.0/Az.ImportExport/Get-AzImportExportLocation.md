---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexportlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
ms.openlocfilehash: c603c01619128d1697256174e9d0bc00a1cea8ff
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243411"
---
# <span data-ttu-id="fdb79-101">Get-AzImportExportLocation</span><span class="sxs-lookup"><span data-stu-id="fdb79-101">Get-AzImportExportLocation</span></span>

## <span data-ttu-id="fdb79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fdb79-102">SYNOPSIS</span></span>
<span data-ttu-id="fdb79-103">Zwraca szczegółowe informacje o lokalizacji, w której można wysłać dyskietną skojarzoną z zadaniem importu lub eksportu.</span><span class="sxs-lookup"><span data-stu-id="fdb79-103">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="fdb79-104">Lokalizacja to region platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fdb79-104">A location is an Azure region.</span></span>

## <span data-ttu-id="fdb79-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fdb79-105">SYNTAX</span></span>

### <span data-ttu-id="fdb79-106">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="fdb79-106">List (Default)</span></span>
```
Get-AzImportExportLocation [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="fdb79-107">Pobierz</span><span class="sxs-lookup"><span data-stu-id="fdb79-107">Get</span></span>
```
Get-AzImportExportLocation -Name <String> [-AcceptLanguage <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="fdb79-108">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fdb79-108">GetViaIdentity</span></span>
```
Get-AzImportExportLocation -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="fdb79-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="fdb79-109">DESCRIPTION</span></span>
<span data-ttu-id="fdb79-110">Zwraca szczegółowe informacje o lokalizacji, do której można wysłać dyskietki skojarzone z zadaniem importu lub eksportu.</span><span class="sxs-lookup"><span data-stu-id="fdb79-110">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="fdb79-111">Lokalizacja to region platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fdb79-111">A location is an Azure region.</span></span>

## <span data-ttu-id="fdb79-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fdb79-112">EXAMPLES</span></span>

### <span data-ttu-id="fdb79-113">Przykład 1. Uzyskiwanie wszystkich szczegółów lokalizacji regionu platformy Azure z kontekstem domyślnym</span><span class="sxs-lookup"><span data-stu-id="fdb79-113">Example 1: Get all Azure region location details with default context</span></span>
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

<span data-ttu-id="fdb79-114">To polecenie cmdlet pobiera wszystkie szczegóły lokalizacji regionu platformy Azure z kontekstem domyślnym.</span><span class="sxs-lookup"><span data-stu-id="fdb79-114">This cmdlet gets all Azure region location details with default context.</span></span>

### <span data-ttu-id="fdb79-115">Przykład 2. Uzyskiwanie szczegółów lokalizacji regionu platformy Azure według nazwy lokalizacji</span><span class="sxs-lookup"><span data-stu-id="fdb79-115">Example 2: Get Azure region location details by location name</span></span>
```powershell
PS C:\> Get-AzImportExportLocation -Name eastus
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

<span data-ttu-id="fdb79-116">To polecenie cmdlet pobiera szczegółowe informacje o lokalizacji regionu platformy Azure według nazwy lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="fdb79-116">This cmdlet gets Azure region location details by location name.</span></span>

### <span data-ttu-id="fdb79-117">Przykład 3. Uzyskiwanie szczegółów lokalizacji regionu platformy Azure według tożsamości</span><span class="sxs-lookup"><span data-stu-id="fdb79-117">Example 3: Get Azure region location details by identity</span></span>
```powershell
PS C:\> $Id = "/providers/Microsoft.ImportExport/locations/eastus"
PS C:\> Get-AzImportExportLocation -InputObject $Id
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

<span data-ttu-id="fdb79-118">Te listy polecenia cmdlet pobierają szczegółowe informacje o lokalizacji regionu platformy Azure według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="fdb79-118">This cmdlet lists gets Azure region location details by identity.</span></span>

## <span data-ttu-id="fdb79-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fdb79-119">PARAMETERS</span></span>

### <span data-ttu-id="fdb79-120">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="fdb79-120">-AcceptLanguage</span></span>
<span data-ttu-id="fdb79-121">Określa preferowany język odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="fdb79-121">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="fdb79-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdb79-122">-DefaultProfile</span></span>
<span data-ttu-id="fdb79-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fdb79-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdb79-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fdb79-124">-InputObject</span></span>
<span data-ttu-id="fdb79-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="fdb79-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="fdb79-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fdb79-126">-Name</span></span>
<span data-ttu-id="fdb79-127">Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="fdb79-127">The name of the location.</span></span>
<span data-ttu-id="fdb79-128">Na przykład Stany Zjednoczone Lub Zachód.</span><span class="sxs-lookup"><span data-stu-id="fdb79-128">For example, West US or westus.</span></span>

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

### <span data-ttu-id="fdb79-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdb79-129">CommonParameters</span></span>
<span data-ttu-id="fdb79-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdb79-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdb79-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fdb79-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdb79-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fdb79-132">INPUTS</span></span>

### <span data-ttu-id="fdb79-133">Microsoft.Azure.PowerShell.Cmdlet.ImportExport.Models.IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="fdb79-133">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="fdb79-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fdb79-134">OUTPUTS</span></span>

### <span data-ttu-id="fdb79-135">Microsoft.Azure.PowerShell.cmdlet.ImportExport.Models.Api20161101.ILocation</span><span class="sxs-lookup"><span data-stu-id="fdb79-135">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.ILocation</span></span>

## <span data-ttu-id="fdb79-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fdb79-136">NOTES</span></span>

<span data-ttu-id="fdb79-137">ALIASY</span><span class="sxs-lookup"><span data-stu-id="fdb79-137">ALIASES</span></span>

<span data-ttu-id="fdb79-138">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="fdb79-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fdb79-139">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="fdb79-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fdb79-140">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fdb79-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fdb79-141">INPUTOBJECT: <IImportExportIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="fdb79-141">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fdb79-142">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="fdb79-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fdb79-143">`[JobName <String>]`: nazwa zadania importu/eksportu.</span><span class="sxs-lookup"><span data-stu-id="fdb79-143">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="fdb79-144">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="fdb79-144">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="fdb79-145">Na przykład Stany Zjednoczone Lub Zachód.</span><span class="sxs-lookup"><span data-stu-id="fdb79-145">For example, West US or westus.</span></span>
  - <span data-ttu-id="fdb79-146">`[ResourceGroupName <String>]`: Nazwa grupy zasobów jednoznacznie identyfikuje grupę zasobów w ramach subskrypcji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="fdb79-146">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="fdb79-147">`[SubscriptionId <String>]`: Identyfikator subskrypcji dla użytkownika platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fdb79-147">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="fdb79-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fdb79-148">RELATED LINKS</span></span>

