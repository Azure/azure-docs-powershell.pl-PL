---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/get-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksWorkspace.md
ms.openlocfilehash: 7f2bb3f1d378afec5b0774aec2977b507654b931
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242706"
---
# <span data-ttu-id="fd131-101">Get-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="fd131-101">Get-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="fd131-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd131-102">SYNOPSIS</span></span>
<span data-ttu-id="fd131-103">Pobiera obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="fd131-103">Gets the workspace.</span></span>

## <span data-ttu-id="fd131-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fd131-104">SYNTAX</span></span>

### <span data-ttu-id="fd131-105">Lista1 (domyślna)</span><span class="sxs-lookup"><span data-stu-id="fd131-105">List1 (Default)</span></span>
```
Get-AzDatabricksWorkspace [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="fd131-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="fd131-106">Get</span></span>
```
Get-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="fd131-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fd131-107">GetViaIdentity</span></span>
```
Get-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="fd131-108">Lista</span><span class="sxs-lookup"><span data-stu-id="fd131-108">List</span></span>
```
Get-AzDatabricksWorkspace -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="fd131-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="fd131-109">DESCRIPTION</span></span>
<span data-ttu-id="fd131-110">Pobiera obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="fd131-110">Gets the workspace.</span></span>

## <span data-ttu-id="fd131-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fd131-111">EXAMPLES</span></span>

### <span data-ttu-id="fd131-112">Przykład 1. Uzyskiwanie obszaru roboczego databricks z nazwą</span><span class="sxs-lookup"><span data-stu-id="fd131-112">Example 1: Get a Databricks workspace with name</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace -Name databricks-test -ResourceGroupName testgroup

Location Name            Type
-------- ----            ----
eastus   databricks-test Microsoft.Databricks/workspaces
```

<span data-ttu-id="fd131-113">To polecenie pobiera obszar roboczy databricks w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="fd131-113">This command gets a Databricks workspace in a resource group.</span></span>

### <span data-ttu-id="fd131-114">Przykład 2. Lista wszystkich obszarów roboczych usługi Databricks w subskrypcji</span><span class="sxs-lookup"><span data-stu-id="fd131-114">Example 2: List all Databricks workspaces in a subscription</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace

Location Name                           Type
-------- ----                           ----
eastus   databricks-test                Microsoft.Databricks/workspaces
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="fd131-115">To polecenie wyświetla listę wszystkich obszarów roboczych usługi Databricks w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="fd131-115">This command lists all Databricks workspaces in a subscription.</span></span>

### <span data-ttu-id="fd131-116">Przykład 3. Lista wszystkich obszarów roboczych obszaru roboczego danych w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="fd131-116">Example 3: List all Databricks workspaces in a resource group</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace -ResourceGroupName testgroup

Location Name                           Type
-------- ----                           ----
eastus   databricks-test                Microsoft.Databricks/workspaces
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="fd131-117">To polecenie wyświetla listę wszystkich obszarów roboczych obszaru roboczego programu Databricks w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="fd131-117">This command lists all Databricks workspaces in a resource group.</span></span>

## <span data-ttu-id="fd131-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd131-118">PARAMETERS</span></span>

### <span data-ttu-id="fd131-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd131-119">-DefaultProfile</span></span>
<span data-ttu-id="fd131-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fd131-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd131-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd131-121">-InputObject</span></span>
<span data-ttu-id="fd131-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="fd131-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd131-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fd131-123">-Name</span></span>
<span data-ttu-id="fd131-124">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="fd131-124">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd131-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd131-125">-ResourceGroupName</span></span>
<span data-ttu-id="fd131-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fd131-126">The name of the resource group.</span></span>
<span data-ttu-id="fd131-127">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="fd131-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="fd131-128">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fd131-128">-SubscriptionId</span></span>
<span data-ttu-id="fd131-129">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="fd131-129">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd131-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd131-130">CommonParameters</span></span>
<span data-ttu-id="fd131-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd131-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd131-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd131-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd131-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fd131-133">INPUTS</span></span>

### <span data-ttu-id="fd131-134">Microsoft.Azure.PowerShell.Cmdlet.Databricks.Models.IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="fd131-134">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="fd131-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fd131-135">OUTPUTS</span></span>

### <span data-ttu-id="fd131-136">Microsoft.Azure.PowerShell.Cmdlet.Databricks.Models.Api20180401.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="fd131-136">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="fd131-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fd131-137">NOTES</span></span>

<span data-ttu-id="fd131-138">ALIASY</span><span class="sxs-lookup"><span data-stu-id="fd131-138">ALIASES</span></span>

<span data-ttu-id="fd131-139">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fd131-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fd131-140">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="fd131-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fd131-141">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fd131-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fd131-142">INPUTOBJECT: <IDatabricksIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="fd131-142">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fd131-143">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="fd131-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fd131-144">`[PeeringName <String>]`: nazwa komunikacji równorzędnej vNet obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="fd131-144">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="fd131-145">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fd131-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="fd131-146">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="fd131-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="fd131-147">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="fd131-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="fd131-148">`[WorkspaceName <String>]`: nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="fd131-148">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="fd131-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fd131-149">RELATED LINKS</span></span>

