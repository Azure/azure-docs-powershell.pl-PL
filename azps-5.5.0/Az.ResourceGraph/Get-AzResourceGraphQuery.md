---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/get-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Get-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Get-AzResourceGraphQuery.md
ms.openlocfilehash: 6d7dbb9acbcc03f266d698d1f9d8ce89f320d04b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176419"
---
# <span data-ttu-id="d157d-101">Get-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="d157d-101">Get-AzResourceGraphQuery</span></span>

## <span data-ttu-id="d157d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d157d-102">SYNOPSIS</span></span>
<span data-ttu-id="d157d-103">Pobierz jedno zapytanie wykresu według jego nazwy zasobu.</span><span class="sxs-lookup"><span data-stu-id="d157d-103">Get a single graph query by its resourceName.</span></span>

## <span data-ttu-id="d157d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d157d-104">SYNTAX</span></span>

### <span data-ttu-id="d157d-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="d157d-105">List (Default)</span></span>
```
Get-AzResourceGraphQuery -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="d157d-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="d157d-106">Get</span></span>
```
Get-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d157d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d157d-107">GetViaIdentity</span></span>
```
Get-AzResourceGraphQuery -InputObject <IResourceGraphIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="d157d-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="d157d-108">DESCRIPTION</span></span>
<span data-ttu-id="d157d-109">Pobierz jedno zapytanie wykresu według jego nazwy zasobu.</span><span class="sxs-lookup"><span data-stu-id="d157d-109">Get a single graph query by its resourceName.</span></span>

## <span data-ttu-id="d157d-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d157d-110">EXAMPLES</span></span>

### <span data-ttu-id="d157d-111">Przykład 1. Uzyskiwanie wszystkich zapytań wykresu zasobów w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="d157d-111">Example 1: Get all resource graph query under a resource group</span></span>
```powershell
PS C:\> Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

<span data-ttu-id="d157d-112">To polecenie pobiera wszystkie zapytania wykresu zasobów w ramach grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d157d-112">This command gets all resource graph query under a resource group.</span></span>

### <span data-ttu-id="d157d-113">Przykład 2. Uzyskiwanie zapytania wykresu zasobów według nazwy</span><span class="sxs-lookup"><span data-stu-id="d157d-113">Example 2: Get a resource graph query by name</span></span>
```powershell
PS C:\> Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name SharedQuery-t01

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

<span data-ttu-id="d157d-114">To polecenie pobiera zapytanie wykresu zasobów według nazwy.</span><span class="sxs-lookup"><span data-stu-id="d157d-114">This command gets a resource graph query by name.</span></span>

### <span data-ttu-id="d157d-115">Przykład 2. Uzyskiwanie zapytania wykresu zasobów według objecy</span><span class="sxs-lookup"><span data-stu-id="d157d-115">Example 2: Get a resource graph query by objecy</span></span>
```powershell
PS C:\> $query = New-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t03 -Location 'global' -Query 'project id, name, type, location' -Description 'test'
PS C:\> Get-AzResourceGraphQuery -InputObject $query

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

<span data-ttu-id="d157d-116">To polecenie pobiera zapytanie wykresu zasobów według obiektów.</span><span class="sxs-lookup"><span data-stu-id="d157d-116">This command gets a resource graph query by object.</span></span>

## <span data-ttu-id="d157d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d157d-117">PARAMETERS</span></span>

### <span data-ttu-id="d157d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d157d-118">-DefaultProfile</span></span>
<span data-ttu-id="d157d-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d157d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d157d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d157d-120">-InputObject</span></span>
<span data-ttu-id="d157d-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="d157d-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d157d-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d157d-122">-Name</span></span>
<span data-ttu-id="d157d-123">Nazwa zasobu zapytanie programu Graph.</span><span class="sxs-lookup"><span data-stu-id="d157d-123">The name of the Graph Query resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d157d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d157d-124">-ResourceGroupName</span></span>
<span data-ttu-id="d157d-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d157d-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d157d-126">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d157d-126">-SubscriptionId</span></span>
<span data-ttu-id="d157d-127">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d157d-127">The Azure subscription Id.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d157d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d157d-128">CommonParameters</span></span>
<span data-ttu-id="d157d-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d157d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d157d-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d157d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d157d-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d157d-131">INPUTS</span></span>

### <span data-ttu-id="d157d-132">Microsoft.Azure.PowerShell.Cmdlet.ResourceGraph.Models.IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="d157d-132">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="d157d-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d157d-133">OUTPUTS</span></span>

### <span data-ttu-id="d157d-134">Microsoft.Azure.PowerShell.Cmdlet.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="d157d-134">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

## <span data-ttu-id="d157d-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d157d-135">NOTES</span></span>

<span data-ttu-id="d157d-136">ALIASY</span><span class="sxs-lookup"><span data-stu-id="d157d-136">ALIASES</span></span>

<span data-ttu-id="d157d-137">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="d157d-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d157d-138">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="d157d-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d157d-139">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d157d-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d157d-140">INPUTOBJECT: <IResourceGraphIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="d157d-140">INPUTOBJECT <IResourceGraphIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d157d-141">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="d157d-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d157d-142">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d157d-142">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="d157d-143">`[ResourceName <String>]`: nazwa zasobu zapytania programu Graph.</span><span class="sxs-lookup"><span data-stu-id="d157d-143">`[ResourceName <String>]`: The name of the Graph Query resource.</span></span>
  - <span data-ttu-id="d157d-144">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d157d-144">`[SubscriptionId <String>]`: The Azure subscription Id.</span></span>

## <span data-ttu-id="d157d-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d157d-145">RELATED LINKS</span></span>

