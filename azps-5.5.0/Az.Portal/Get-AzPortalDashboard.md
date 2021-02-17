---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/get-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Get-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Get-AzPortalDashboard.md
ms.openlocfilehash: aa11a9828c422069823226b2d5df57efc84f8c7b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186643"
---
# <span data-ttu-id="949fb-101">Get-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="949fb-101">Get-AzPortalDashboard</span></span>

## <span data-ttu-id="949fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="949fb-102">SYNOPSIS</span></span>
<span data-ttu-id="949fb-103">Pobiera pulpit nawigacyjny.</span><span class="sxs-lookup"><span data-stu-id="949fb-103">Gets the Dashboard.</span></span>

## <span data-ttu-id="949fb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="949fb-104">SYNTAX</span></span>

### <span data-ttu-id="949fb-105">Lista1 (domyślna)</span><span class="sxs-lookup"><span data-stu-id="949fb-105">List1 (Default)</span></span>
```
Get-AzPortalDashboard [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="949fb-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="949fb-106">Get</span></span>
```
Get-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="949fb-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="949fb-107">GetViaIdentity</span></span>
```
Get-AzPortalDashboard -InputObject <IPortalIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="949fb-108">Lista</span><span class="sxs-lookup"><span data-stu-id="949fb-108">List</span></span>
```
Get-AzPortalDashboard -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="949fb-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="949fb-109">DESCRIPTION</span></span>
<span data-ttu-id="949fb-110">Pobiera pulpit nawigacyjny.</span><span class="sxs-lookup"><span data-stu-id="949fb-110">Gets the Dashboard.</span></span>

## <span data-ttu-id="949fb-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="949fb-111">EXAMPLES</span></span>

### <span data-ttu-id="949fb-112">Przykład 1. Lista wszystkich pulpitów nawigacyjnych w subskrypcji</span><span class="sxs-lookup"><span data-stu-id="949fb-112">Example 1: List all dashboards in a subscription</span></span>
```powershell
PS C:> Get-AzPortalDashboard                                                                                                                     
Location Name                                           Type
-------- ----                                           ----
eastasia my-custom-dashboard1                           Microsoft.Portal/dashboards
westus   my-second-custom-dashboard1                    Microsoft.Portal/dashboards

```

<span data-ttu-id="949fb-113">Lista wszystkich pulpitów nawigacyjnych w subskrypcji</span><span class="sxs-lookup"><span data-stu-id="949fb-113">List all dashboards in a subscription</span></span>

### <span data-ttu-id="949fb-114">Przykład 2. Uzyskiwanie szczegółów dotyczących pojedynczego pulpitu nawigacyjnego portalu</span><span class="sxs-lookup"><span data-stu-id="949fb-114">Example 2: Get details for a single Portal Dashboard</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -Name mydashboard

Location Name        Type
-------- ----        ----
eastus   mydashboard Microsoft.Portal/dashboards
```

<span data-ttu-id="949fb-115">Uzyskiwanie szczegółów dotyczących pojedynczego pulpitu nawigacyjnego</span><span class="sxs-lookup"><span data-stu-id="949fb-115">Get details for a single dashboard</span></span>

## <span data-ttu-id="949fb-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="949fb-116">PARAMETERS</span></span>

### <span data-ttu-id="949fb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="949fb-117">-DefaultProfile</span></span>
<span data-ttu-id="949fb-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="949fb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="949fb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="949fb-119">-InputObject</span></span>
<span data-ttu-id="949fb-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="949fb-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="949fb-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="949fb-121">-Name</span></span>
<span data-ttu-id="949fb-122">Nazwa pulpitu nawigacyjnego.</span><span class="sxs-lookup"><span data-stu-id="949fb-122">The name of the dashboard.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="949fb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="949fb-123">-ResourceGroupName</span></span>
<span data-ttu-id="949fb-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="949fb-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="949fb-125">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="949fb-125">-SubscriptionId</span></span>
<span data-ttu-id="949fb-126">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="949fb-126">The Azure subscription ID.</span></span>
<span data-ttu-id="949fb-127">Jest to ciąg w formacie IDENTYFIKATORA GUID (np. 000000000-0000-0000-0000-00000000000000)</span><span class="sxs-lookup"><span data-stu-id="949fb-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="949fb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="949fb-128">CommonParameters</span></span>
<span data-ttu-id="949fb-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="949fb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="949fb-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="949fb-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="949fb-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="949fb-131">INPUTS</span></span>

### <span data-ttu-id="949fb-132">Microsoft.Azure.PowerShell.Cmdlet.Portal.Models.IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="949fb-132">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="949fb-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="949fb-133">OUTPUTS</span></span>

### <span data-ttu-id="949fb-134">Microsoft.Azure.PowerShell.Cmdlet.Portal.Models.Api201901Preview.IDashboard</span><span class="sxs-lookup"><span data-stu-id="949fb-134">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="949fb-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="949fb-135">NOTES</span></span>

<span data-ttu-id="949fb-136">ALIASY</span><span class="sxs-lookup"><span data-stu-id="949fb-136">ALIASES</span></span>

<span data-ttu-id="949fb-137">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="949fb-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="949fb-138">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="949fb-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="949fb-139">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="949fb-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="949fb-140">INPUTOBJECT: <IPortalIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="949fb-140">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="949fb-141">`[DashboardName <String>]`: nazwa pulpitu nawigacyjnego.</span><span class="sxs-lookup"><span data-stu-id="949fb-141">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="949fb-142">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="949fb-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="949fb-143">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="949fb-143">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="949fb-144">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="949fb-144">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="949fb-145">Jest to ciąg w formacie IDENTYFIKATORA GUID (np. 000000000-0000-0000-0000-00000000000000)</span><span class="sxs-lookup"><span data-stu-id="949fb-145">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="949fb-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="949fb-146">RELATED LINKS</span></span>

