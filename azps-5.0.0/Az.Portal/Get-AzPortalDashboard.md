---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/get-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Get-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Get-AzPortalDashboard.md
ms.openlocfilehash: aa11a9828c422069823226b2d5df57efc84f8c7b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233653"
---
# <span data-ttu-id="98ac6-101">Get-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="98ac6-101">Get-AzPortalDashboard</span></span>

## <span data-ttu-id="98ac6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="98ac6-102">SYNOPSIS</span></span>
<span data-ttu-id="98ac6-103">Pobiera pulpit nawigacyjny.</span><span class="sxs-lookup"><span data-stu-id="98ac6-103">Gets the Dashboard.</span></span>

## <span data-ttu-id="98ac6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="98ac6-104">SYNTAX</span></span>

### <span data-ttu-id="98ac6-105">List1 (domyślny)</span><span class="sxs-lookup"><span data-stu-id="98ac6-105">List1 (Default)</span></span>
```
Get-AzPortalDashboard [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="98ac6-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="98ac6-106">Get</span></span>
```
Get-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="98ac6-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="98ac6-107">GetViaIdentity</span></span>
```
Get-AzPortalDashboard -InputObject <IPortalIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="98ac6-108">Lista</span><span class="sxs-lookup"><span data-stu-id="98ac6-108">List</span></span>
```
Get-AzPortalDashboard -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="98ac6-109">Opis</span><span class="sxs-lookup"><span data-stu-id="98ac6-109">DESCRIPTION</span></span>
<span data-ttu-id="98ac6-110">Pobiera pulpit nawigacyjny.</span><span class="sxs-lookup"><span data-stu-id="98ac6-110">Gets the Dashboard.</span></span>

## <span data-ttu-id="98ac6-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="98ac6-111">EXAMPLES</span></span>

### <span data-ttu-id="98ac6-112">Przykład 1: wyświetlanie wszystkich pulpitów nawigacyjnych w subskrypcji</span><span class="sxs-lookup"><span data-stu-id="98ac6-112">Example 1: List all dashboards in a subscription</span></span>
```powershell
PS C:> Get-AzPortalDashboard                                                                                                                     
Location Name                                           Type
-------- ----                                           ----
eastasia my-custom-dashboard1                           Microsoft.Portal/dashboards
westus   my-second-custom-dashboard1                    Microsoft.Portal/dashboards

```

<span data-ttu-id="98ac6-113">Wyświetlanie listy wszystkich pulpitów nawigacyjnych w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="98ac6-113">List all dashboards in a subscription</span></span>

### <span data-ttu-id="98ac6-114">Przykład 2: uzyskiwanie szczegółowych informacji o jednym pulpicie nawigacyjnym portalu</span><span class="sxs-lookup"><span data-stu-id="98ac6-114">Example 2: Get details for a single Portal Dashboard</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -Name mydashboard

Location Name        Type
-------- ----        ----
eastus   mydashboard Microsoft.Portal/dashboards
```

<span data-ttu-id="98ac6-115">Uzyskiwanie szczegółowych informacji o jednym pulpicie nawigacyjnym</span><span class="sxs-lookup"><span data-stu-id="98ac6-115">Get details for a single dashboard</span></span>

## <span data-ttu-id="98ac6-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="98ac6-116">PARAMETERS</span></span>

### <span data-ttu-id="98ac6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98ac6-117">-DefaultProfile</span></span>
<span data-ttu-id="98ac6-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="98ac6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98ac6-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="98ac6-119">-InputObject</span></span>
<span data-ttu-id="98ac6-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="98ac6-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="98ac6-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="98ac6-121">-Name</span></span>
<span data-ttu-id="98ac6-122">Nazwa pulpitu nawigacyjnego.</span><span class="sxs-lookup"><span data-stu-id="98ac6-122">The name of the dashboard.</span></span>

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

### <span data-ttu-id="98ac6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98ac6-123">-ResourceGroupName</span></span>
<span data-ttu-id="98ac6-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="98ac6-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="98ac6-125">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="98ac6-125">-SubscriptionId</span></span>
<span data-ttu-id="98ac6-126">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="98ac6-126">The Azure subscription ID.</span></span>
<span data-ttu-id="98ac6-127">Jest to ciąg sformatowany przy użyciu identyfikatora GUID (na przykład 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="98ac6-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="98ac6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98ac6-128">CommonParameters</span></span>
<span data-ttu-id="98ac6-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98ac6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98ac6-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98ac6-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98ac6-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="98ac6-131">INPUTS</span></span>

### <span data-ttu-id="98ac6-132">Microsoft. Azure. PowerShell. polecenia cmdlet. Portal. models. IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="98ac6-132">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="98ac6-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="98ac6-133">OUTPUTS</span></span>

### <span data-ttu-id="98ac6-134">Microsoft. Azure. PowerShell. cmdlet. Portal. models. Api201901Preview. IDashboard</span><span class="sxs-lookup"><span data-stu-id="98ac6-134">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="98ac6-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="98ac6-135">NOTES</span></span>

<span data-ttu-id="98ac6-136">PISUJE</span><span class="sxs-lookup"><span data-stu-id="98ac6-136">ALIASES</span></span>

<span data-ttu-id="98ac6-137">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="98ac6-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="98ac6-138">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="98ac6-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="98ac6-139">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="98ac6-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="98ac6-140">INPUTobject <IPortalIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="98ac6-140">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="98ac6-141">`[DashboardName <String>]`: Nazwa pulpitu nawigacyjnego.</span><span class="sxs-lookup"><span data-stu-id="98ac6-141">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="98ac6-142">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="98ac6-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="98ac6-143">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="98ac6-143">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="98ac6-144">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="98ac6-144">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="98ac6-145">Jest to ciąg sformatowany przy użyciu identyfikatora GUID (na przykład 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="98ac6-145">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="98ac6-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="98ac6-146">RELATED LINKS</span></span>

