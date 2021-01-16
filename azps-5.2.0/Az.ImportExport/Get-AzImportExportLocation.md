---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexportlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
ms.openlocfilehash: c603c01619128d1697256174e9d0bc00a1cea8ff
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325939"
---
# <span data-ttu-id="1eba6-101">Get-AzImportExportLocation</span><span class="sxs-lookup"><span data-stu-id="1eba6-101">Get-AzImportExportLocation</span></span>

## <span data-ttu-id="1eba6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1eba6-102">SYNOPSIS</span></span>
<span data-ttu-id="1eba6-103">Zwraca szczegóły dotyczące lokalizacji, do której można wysłać dyski skojarzone z zadaniem importu lub eksportu.</span><span class="sxs-lookup"><span data-stu-id="1eba6-103">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="1eba6-104">Lokalizacja to obszar platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1eba6-104">A location is an Azure region.</span></span>

## <span data-ttu-id="1eba6-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1eba6-105">SYNTAX</span></span>

### <span data-ttu-id="1eba6-106">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="1eba6-106">List (Default)</span></span>
```
Get-AzImportExportLocation [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1eba6-107">Pobierz</span><span class="sxs-lookup"><span data-stu-id="1eba6-107">Get</span></span>
```
Get-AzImportExportLocation -Name <String> [-AcceptLanguage <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="1eba6-108">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1eba6-108">GetViaIdentity</span></span>
```
Get-AzImportExportLocation -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="1eba6-109">Opis</span><span class="sxs-lookup"><span data-stu-id="1eba6-109">DESCRIPTION</span></span>
<span data-ttu-id="1eba6-110">Zwraca szczegóły dotyczące lokalizacji, do której można wysłać dyski skojarzone z zadaniem importu lub eksportu.</span><span class="sxs-lookup"><span data-stu-id="1eba6-110">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="1eba6-111">Lokalizacja to obszar platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1eba6-111">A location is an Azure region.</span></span>

## <span data-ttu-id="1eba6-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1eba6-112">EXAMPLES</span></span>

### <span data-ttu-id="1eba6-113">Przykład 1. Uzyskaj wszystkie szczegóły lokalizacji na platformie Azure z kontekstem domyślnym</span><span class="sxs-lookup"><span data-stu-id="1eba6-113">Example 1: Get all Azure region location details with default context</span></span>
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

<span data-ttu-id="1eba6-114">To polecenie cmdlet uzyskuje wszystkie szczegóły lokalizacji na platformie Azure z kontekstem domyślnym.</span><span class="sxs-lookup"><span data-stu-id="1eba6-114">This cmdlet gets all Azure region location details with default context.</span></span>

### <span data-ttu-id="1eba6-115">Przykład 2: szczegółowe informacje o lokalizacji w systemie Azure według nazwy lokalizacji</span><span class="sxs-lookup"><span data-stu-id="1eba6-115">Example 2: Get Azure region location details by location name</span></span>
```powershell
PS C:\> Get-AzImportExportLocation -Name eastus
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

<span data-ttu-id="1eba6-116">To polecenie cmdlet pobiera dane lokalizacji regionu platformy Azure według nazwy lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="1eba6-116">This cmdlet gets Azure region location details by location name.</span></span>

### <span data-ttu-id="1eba6-117">Przykład 3: uzyskiwanie szczegółowych informacji o lokalizacji w systemie Azure według tożsamości</span><span class="sxs-lookup"><span data-stu-id="1eba6-117">Example 3: Get Azure region location details by identity</span></span>
```powershell
PS C:\> $Id = "/providers/Microsoft.ImportExport/locations/eastus"
PS C:\> Get-AzImportExportLocation -InputObject $Id
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

<span data-ttu-id="1eba6-118">Te listy poleceń cmdlet pobierają dane lokalizacji regionu platformy Azure według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="1eba6-118">This cmdlet lists gets Azure region location details by identity.</span></span>

## <span data-ttu-id="1eba6-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1eba6-119">PARAMETERS</span></span>

### <span data-ttu-id="1eba6-120">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="1eba6-120">-AcceptLanguage</span></span>
<span data-ttu-id="1eba6-121">Określa preferowany język odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="1eba6-121">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="1eba6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1eba6-122">-DefaultProfile</span></span>
<span data-ttu-id="1eba6-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1eba6-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1eba6-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1eba6-124">-InputObject</span></span>
<span data-ttu-id="1eba6-125">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="1eba6-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1eba6-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1eba6-126">-Name</span></span>
<span data-ttu-id="1eba6-127">Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="1eba6-127">The name of the location.</span></span>
<span data-ttu-id="1eba6-128">Na przykład w przypadku zachodniego, USA lub zachodniego.</span><span class="sxs-lookup"><span data-stu-id="1eba6-128">For example, West US or westus.</span></span>

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

### <span data-ttu-id="1eba6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1eba6-129">CommonParameters</span></span>
<span data-ttu-id="1eba6-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1eba6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1eba6-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1eba6-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1eba6-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1eba6-132">INPUTS</span></span>

### <span data-ttu-id="1eba6-133">Microsoft. Azure. PowerShell. polecenia. ImportExport. models. IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="1eba6-133">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="1eba6-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1eba6-134">OUTPUTS</span></span>

### <span data-ttu-id="1eba6-135">Microsoft. Azure. PowerShell. polecenia. ImportExport. models. Api20161101. ILocation</span><span class="sxs-lookup"><span data-stu-id="1eba6-135">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.ILocation</span></span>

## <span data-ttu-id="1eba6-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1eba6-136">NOTES</span></span>

<span data-ttu-id="1eba6-137">PISUJE</span><span class="sxs-lookup"><span data-stu-id="1eba6-137">ALIASES</span></span>

<span data-ttu-id="1eba6-138">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1eba6-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1eba6-139">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="1eba6-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1eba6-140">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1eba6-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1eba6-141">INPUTobject <IImportExportIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="1eba6-141">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1eba6-142">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="1eba6-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1eba6-143">`[JobName <String>]`: Nazwa zadania importu/eksportu.</span><span class="sxs-lookup"><span data-stu-id="1eba6-143">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="1eba6-144">`[LocationName <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="1eba6-144">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="1eba6-145">Na przykład w przypadku zachodniego, USA lub zachodniego.</span><span class="sxs-lookup"><span data-stu-id="1eba6-145">For example, West US or westus.</span></span>
  - <span data-ttu-id="1eba6-146">`[ResourceGroupName <String>]`: Nazwa grupy zasobów jednoznacznie identyfikuje grupę zasobów w ramach abonamentu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="1eba6-146">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="1eba6-147">`[SubscriptionId <String>]`: Identyfikator subskrypcji użytkownika platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1eba6-147">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="1eba6-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1eba6-148">RELATED LINKS</span></span>

