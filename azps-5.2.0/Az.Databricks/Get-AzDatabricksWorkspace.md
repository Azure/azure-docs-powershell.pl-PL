---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/get-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksWorkspace.md
ms.openlocfilehash: 7f2bb3f1d378afec5b0774aec2977b507654b931
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368804"
---
# <span data-ttu-id="d24cd-101">Get-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="d24cd-101">Get-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="d24cd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d24cd-102">SYNOPSIS</span></span>
<span data-ttu-id="d24cd-103">Pobiera obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="d24cd-103">Gets the workspace.</span></span>

## <span data-ttu-id="d24cd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d24cd-104">SYNTAX</span></span>

### <span data-ttu-id="d24cd-105">List1 (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d24cd-105">List1 (Default)</span></span>
```
Get-AzDatabricksWorkspace [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d24cd-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="d24cd-106">Get</span></span>
```
Get-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d24cd-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d24cd-107">GetViaIdentity</span></span>
```
Get-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d24cd-108">Lista</span><span class="sxs-lookup"><span data-stu-id="d24cd-108">List</span></span>
```
Get-AzDatabricksWorkspace -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d24cd-109">Opis</span><span class="sxs-lookup"><span data-stu-id="d24cd-109">DESCRIPTION</span></span>
<span data-ttu-id="d24cd-110">Pobiera obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="d24cd-110">Gets the workspace.</span></span>

## <span data-ttu-id="d24cd-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d24cd-111">EXAMPLES</span></span>

### <span data-ttu-id="d24cd-112">Przykład 1: uzyskiwanie obszaru roboczego datakostki z nazwą</span><span class="sxs-lookup"><span data-stu-id="d24cd-112">Example 1: Get a Databricks workspace with name</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace -Name databricks-test -ResourceGroupName testgroup

Location Name            Type
-------- ----            ----
eastus   databricks-test Microsoft.Databricks/workspaces
```

<span data-ttu-id="d24cd-113">To polecenie umożliwia pobieranie obszaru roboczego datakostki w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="d24cd-113">This command gets a Databricks workspace in a resource group.</span></span>

### <span data-ttu-id="d24cd-114">Przykład 2: wyświetlanie wszystkich obszarów roboczych datacegły w subskrypcji</span><span class="sxs-lookup"><span data-stu-id="d24cd-114">Example 2: List all Databricks workspaces in a subscription</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace

Location Name                           Type
-------- ----                           ----
eastus   databricks-test                Microsoft.Databricks/workspaces
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="d24cd-115">To polecenie wyświetla listę wszystkich obszarów roboczych datacegły w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d24cd-115">This command lists all Databricks workspaces in a subscription.</span></span>

### <span data-ttu-id="d24cd-116">Przykład 3: wyświetlanie wszystkich obszarów roboczych datakostek w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="d24cd-116">Example 3: List all Databricks workspaces in a resource group</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace -ResourceGroupName testgroup

Location Name                           Type
-------- ----                           ----
eastus   databricks-test                Microsoft.Databricks/workspaces
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="d24cd-117">To polecenie wyświetla listę wszystkich obszarów roboczych datakostek w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="d24cd-117">This command lists all Databricks workspaces in a resource group.</span></span>

## <span data-ttu-id="d24cd-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d24cd-118">PARAMETERS</span></span>

### <span data-ttu-id="d24cd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d24cd-119">-DefaultProfile</span></span>
<span data-ttu-id="d24cd-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d24cd-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d24cd-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d24cd-121">-InputObject</span></span>
<span data-ttu-id="d24cd-122">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="d24cd-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d24cd-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d24cd-123">-Name</span></span>
<span data-ttu-id="d24cd-124">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="d24cd-124">The name of the workspace.</span></span>

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

### <span data-ttu-id="d24cd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d24cd-125">-ResourceGroupName</span></span>
<span data-ttu-id="d24cd-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d24cd-126">The name of the resource group.</span></span>
<span data-ttu-id="d24cd-127">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="d24cd-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d24cd-128">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="d24cd-128">-SubscriptionId</span></span>
<span data-ttu-id="d24cd-129">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="d24cd-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d24cd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d24cd-130">CommonParameters</span></span>
<span data-ttu-id="d24cd-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d24cd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d24cd-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d24cd-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d24cd-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d24cd-133">INPUTS</span></span>

### <span data-ttu-id="d24cd-134">Microsoft. Azure. PowerShell. polecenia. datakosteks. models. IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="d24cd-134">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="d24cd-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d24cd-135">OUTPUTS</span></span>

### <span data-ttu-id="d24cd-136">Microsoft. Azure. PowerShell. polecenia. datakosteks. models. Api20180401. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="d24cd-136">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="d24cd-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d24cd-137">NOTES</span></span>

<span data-ttu-id="d24cd-138">PISUJE</span><span class="sxs-lookup"><span data-stu-id="d24cd-138">ALIASES</span></span>

<span data-ttu-id="d24cd-139">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d24cd-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d24cd-140">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="d24cd-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d24cd-141">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d24cd-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d24cd-142">INPUTobject <IDatabricksIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="d24cd-142">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d24cd-143">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="d24cd-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d24cd-144">`[PeeringName <String>]`: Nazwa komunikacji równorzędnej w obszarze roboczym w sieci vNet.</span><span class="sxs-lookup"><span data-stu-id="d24cd-144">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="d24cd-145">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d24cd-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d24cd-146">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="d24cd-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="d24cd-147">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="d24cd-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d24cd-148">`[WorkspaceName <String>]`: Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="d24cd-148">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="d24cd-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d24cd-149">RELATED LINKS</span></span>

