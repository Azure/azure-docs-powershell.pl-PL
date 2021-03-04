---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/powershell/module/az.portal/get-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Get-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Get-AzPortalDashboard.md
ms.openlocfilehash: fc888161df56e3edbf1a51014c7173542e395ad3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989031"
---
# <span data-ttu-id="8004c-101">Get-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="8004c-101">Get-AzPortalDashboard</span></span>

## <span data-ttu-id="8004c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8004c-102">SYNOPSIS</span></span>
<span data-ttu-id="8004c-103">Pobiera pulpit nawigacyjny.</span><span class="sxs-lookup"><span data-stu-id="8004c-103">Gets the Dashboard.</span></span>

## <span data-ttu-id="8004c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8004c-104">SYNTAX</span></span>

### <span data-ttu-id="8004c-105">Lista1 (domyślna)</span><span class="sxs-lookup"><span data-stu-id="8004c-105">List1 (Default)</span></span>
```
Get-AzPortalDashboard [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8004c-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="8004c-106">Get</span></span>
```
Get-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8004c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8004c-107">GetViaIdentity</span></span>
```
Get-AzPortalDashboard -InputObject <IPortalIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8004c-108">Lista</span><span class="sxs-lookup"><span data-stu-id="8004c-108">List</span></span>
```
Get-AzPortalDashboard -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="8004c-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="8004c-109">DESCRIPTION</span></span>
<span data-ttu-id="8004c-110">Pobiera pulpit nawigacyjny.</span><span class="sxs-lookup"><span data-stu-id="8004c-110">Gets the Dashboard.</span></span>

## <span data-ttu-id="8004c-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8004c-111">EXAMPLES</span></span>

### <span data-ttu-id="8004c-112">Przykład 1. Lista wszystkich pulpitów nawigacyjnych w subskrypcji</span><span class="sxs-lookup"><span data-stu-id="8004c-112">Example 1: List all dashboards in a subscription</span></span>
```powershell
PS C:> Get-AzPortalDashboard                                                                                                                     
Location Name                                           Type
-------- ----                                           ----
eastasia my-custom-dashboard1                           Microsoft.Portal/dashboards
westus   my-second-custom-dashboard1                    Microsoft.Portal/dashboards

```

<span data-ttu-id="8004c-113">Lista wszystkich pulpitów nawigacyjnych w subskrypcji</span><span class="sxs-lookup"><span data-stu-id="8004c-113">List all dashboards in a subscription</span></span>

### <span data-ttu-id="8004c-114">Przykład 2. Uzyskiwanie szczegółów dotyczących pojedynczego pulpitu nawigacyjnego portalu</span><span class="sxs-lookup"><span data-stu-id="8004c-114">Example 2: Get details for a single Portal Dashboard</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -Name mydashboard

Location Name        Type
-------- ----        ----
eastus   mydashboard Microsoft.Portal/dashboards
```

<span data-ttu-id="8004c-115">Uzyskiwanie szczegółowych informacji na temat jednego pulpitu nawigacyjnego</span><span class="sxs-lookup"><span data-stu-id="8004c-115">Get details for a single dashboard</span></span>

## <span data-ttu-id="8004c-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8004c-116">PARAMETERS</span></span>

### <span data-ttu-id="8004c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8004c-117">-DefaultProfile</span></span>
<span data-ttu-id="8004c-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8004c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8004c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8004c-119">-InputObject</span></span>
<span data-ttu-id="8004c-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="8004c-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8004c-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8004c-121">-Name</span></span>
<span data-ttu-id="8004c-122">Nazwa pulpitu nawigacyjnego.</span><span class="sxs-lookup"><span data-stu-id="8004c-122">The name of the dashboard.</span></span>

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

### <span data-ttu-id="8004c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8004c-123">-ResourceGroupName</span></span>
<span data-ttu-id="8004c-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8004c-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="8004c-125">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8004c-125">-SubscriptionId</span></span>
<span data-ttu-id="8004c-126">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8004c-126">The Azure subscription ID.</span></span>
<span data-ttu-id="8004c-127">Jest to ciąg w formacie IDENTYFIKATORA GUID (np. 000000000-0000-0000-0000-00000000000000)</span><span class="sxs-lookup"><span data-stu-id="8004c-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="8004c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8004c-128">CommonParameters</span></span>
<span data-ttu-id="8004c-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8004c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8004c-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8004c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8004c-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8004c-131">INPUTS</span></span>

### <span data-ttu-id="8004c-132">Microsoft.Azure.PowerShell.Cmdlet.Portal.Models.IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="8004c-132">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="8004c-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8004c-133">OUTPUTS</span></span>

### <span data-ttu-id="8004c-134">Microsoft.Azure.PowerShell.Cmdlet.Portal.Models.Api201901Preview.IDashboard</span><span class="sxs-lookup"><span data-stu-id="8004c-134">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="8004c-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8004c-135">NOTES</span></span>

<span data-ttu-id="8004c-136">ALIASY</span><span class="sxs-lookup"><span data-stu-id="8004c-136">ALIASES</span></span>

<span data-ttu-id="8004c-137">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8004c-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8004c-138">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="8004c-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8004c-139">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8004c-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8004c-140">INPUTOBJECT: <IPortalIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="8004c-140">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8004c-141">`[DashboardName <String>]`: nazwa pulpitu nawigacyjnego.</span><span class="sxs-lookup"><span data-stu-id="8004c-141">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="8004c-142">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="8004c-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8004c-143">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8004c-143">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="8004c-144">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8004c-144">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="8004c-145">Jest to ciąg w formacie IDENTYFIKATORA GUID (np. 000000000-0000-0000-0000-00000000000000)</span><span class="sxs-lookup"><span data-stu-id="8004c-145">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="8004c-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8004c-146">RELATED LINKS</span></span>

