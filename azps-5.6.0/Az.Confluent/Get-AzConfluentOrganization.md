---
external help file: ''
Module Name: Az.Confluent
online version: https://docs.microsoft.com/powershell/module/az.confluent/get-azconfluentorganization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Get-AzConfluentOrganization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Get-AzConfluentOrganization.md
ms.openlocfilehash: dcac6e7ce7e4c8daed2e2f8b43c44c2da82acd93
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012593"
---
# <span data-ttu-id="6c521-101">Get-AzConfluentOrganization</span><span class="sxs-lookup"><span data-stu-id="6c521-101">Get-AzConfluentOrganization</span></span>

## <span data-ttu-id="6c521-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c521-102">SYNOPSIS</span></span>
<span data-ttu-id="6c521-103">Pobierz właściwości określonego zasobu organizacji.</span><span class="sxs-lookup"><span data-stu-id="6c521-103">Get the properties of a specific Organization resource.</span></span>

## <span data-ttu-id="6c521-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6c521-104">SYNTAX</span></span>

### <span data-ttu-id="6c521-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="6c521-105">List (Default)</span></span>
```
Get-AzConfluentOrganization [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6c521-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="6c521-106">Get</span></span>
```
Get-AzConfluentOrganization -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6c521-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6c521-107">GetViaIdentity</span></span>
```
Get-AzConfluentOrganization -InputObject <IConfluentIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="6c521-108">Lista1</span><span class="sxs-lookup"><span data-stu-id="6c521-108">List1</span></span>
```
Get-AzConfluentOrganization -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="6c521-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="6c521-109">DESCRIPTION</span></span>
<span data-ttu-id="6c521-110">Pobierz właściwości określonego zasobu organizacji.</span><span class="sxs-lookup"><span data-stu-id="6c521-110">Get the properties of a specific Organization resource.</span></span>

## <span data-ttu-id="6c521-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6c521-111">EXAMPLES</span></span>

### <span data-ttu-id="6c521-112">Przykład 1. Lista wszystkich organizacji confluent w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="6c521-112">Example 1: List all confluent organizations under a subscription</span></span>
```powershell
PS C:\> Get-AzConfluentOrganization

Location      Name                     Type
--------      ----                     ----
westus2       RegionTestWestUS2        Microsoft.Confluent/organizations
westus2       RohitWUS2                Microsoft.Confluent/organizations
westus2       Rohit-Secret             Microsoft.Confluent/organizations
westus2       Rohit-Secret-2           Microsoft.Confluent/organizations
westus2       Rohit-Secret-WUS2-0      Microsoft.Confluent/organizations
westus2       RohitWus200              Microsoft.Confluent/organizations
westus2       RohitWUS300              Microsoft.Confluent/organizations
westus2       WestUS2-SSOTest          Microsoft.Confluent/organizations
westus2       dri-01-02-postman-stable Microsoft.Confluent/organizations
westus2       dri-02-02                Microsoft.Confluent/organizations
westcentralus RohitWCUS88              Microsoft.Confluent/organizations
```

<span data-ttu-id="6c521-113">To polecenie wyświetla listę wszystkich organizacji confluent w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="6c521-113">This command lists all confluent organizations under a subscription.</span></span>

### <span data-ttu-id="6c521-114">Przykład 2. Lista wszystkich organizacji confluentów w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="6c521-114">Example 2: List all confluent organizations under a resource group</span></span>
```powershell
PS C:\> Get-AzConfluentOrganization -ResourceGroupName azure-rg-test

Location    Name          Type
--------    ----          ----
eastus2euap ppe-metrics-2 Microsoft.Confluent/organizations
```

<span data-ttu-id="6c521-115">To polecenie wyświetla listę wszystkich organizacji confluentów w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="6c521-115">This command lists all confluent organizations under a resource group.</span></span>

### <span data-ttu-id="6c521-116">Przykład 3. Uzyskiwanie organizacji, która się ujmuje według nazwy</span><span class="sxs-lookup"><span data-stu-id="6c521-116">Example 3: Get a confluent organization by name</span></span>
```powershell
PS C:\> Get-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-01-portal

Location Name                   Type
-------- ----                   ----
eastus   confluentorg-01-portal Microsoft.Confluent/organizations
```

<span data-ttu-id="6c521-117">To polecenie pobiera organizację zesłaną według nazwy.</span><span class="sxs-lookup"><span data-stu-id="6c521-117">This command gets a confluent organization by name.</span></span>

### <span data-ttu-id="6c521-118">Przykład 4. Uzyskiwanie organizacji sypkiej według potoku</span><span class="sxs-lookup"><span data-stu-id="6c521-118">Example 4: Get a confluent organization by pipeline</span></span>
```powershell
PS C:\> New-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-02-pwsh -Location eastus -OfferDetailId "confluent-cloud-azure-prod" -OfferDetailPlanId "confluent-cloud-azure-payg-prod" -OfferDetailPlanName "Confluent Cloud - Pay as you Go" -OfferDetailPublisherId "confluentinc" -OfferDetailTermUnit "P1M" | Get-AzConfluentOrganization

Location Name                   Type
-------- ----                   ----
eastus   confluentorg-02-pwsh Microsoft.Confluent/organizations
```

<span data-ttu-id="6c521-119">To polecenie pobiera organizację zesłaną według potoku.</span><span class="sxs-lookup"><span data-stu-id="6c521-119">This command gets a confluent organization by pipeline.</span></span>

## <span data-ttu-id="6c521-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c521-120">PARAMETERS</span></span>

### <span data-ttu-id="6c521-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c521-121">-DefaultProfile</span></span>
<span data-ttu-id="6c521-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6c521-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c521-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c521-123">-InputObject</span></span>
<span data-ttu-id="6c521-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="6c521-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c521-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6c521-125">-Name</span></span>
<span data-ttu-id="6c521-126">Nazwa zasobu organizacji</span><span class="sxs-lookup"><span data-stu-id="6c521-126">Organization resource name</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: OrganizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c521-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c521-127">-ResourceGroupName</span></span>
<span data-ttu-id="6c521-128">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="6c521-128">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c521-129">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6c521-129">-SubscriptionId</span></span>
<span data-ttu-id="6c521-130">Identyfikator subskrypcji platformy Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="6c521-130">Microsoft Azure subscription id</span></span>

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

### <span data-ttu-id="6c521-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c521-131">CommonParameters</span></span>
<span data-ttu-id="6c521-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c521-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c521-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6c521-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c521-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6c521-134">INPUTS</span></span>

### <span data-ttu-id="6c521-135">Microsoft.Azure.PowerShell.Cmdlet.Confluent.Models.IConfluentIdentity</span><span class="sxs-lookup"><span data-stu-id="6c521-135">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity</span></span>

## <span data-ttu-id="6c521-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6c521-136">OUTPUTS</span></span>

### <span data-ttu-id="6c521-137">Microsoft.Azure.PowerShell.Cmdlet.Confluent.Models.Api20200301.IOrganizationResource</span><span class="sxs-lookup"><span data-stu-id="6c521-137">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IOrganizationResource</span></span>

## <span data-ttu-id="6c521-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6c521-138">NOTES</span></span>

<span data-ttu-id="6c521-139">ALIASY</span><span class="sxs-lookup"><span data-stu-id="6c521-139">ALIASES</span></span>

<span data-ttu-id="6c521-140">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6c521-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6c521-141">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="6c521-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6c521-142">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6c521-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6c521-143">INPUTOBJECT: <IConfluentIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="6c521-143">INPUTOBJECT <IConfluentIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6c521-144">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="6c521-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6c521-145">`[OrganizationName <String>]`: nazwa zasobu organizacji</span><span class="sxs-lookup"><span data-stu-id="6c521-145">`[OrganizationName <String>]`: Organization resource name</span></span>
  - <span data-ttu-id="6c521-146">`[ResourceGroupName <String>]`: nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="6c521-146">`[ResourceGroupName <String>]`: Resource group name</span></span>
  - <span data-ttu-id="6c521-147">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="6c521-147">`[SubscriptionId <String>]`: Microsoft Azure subscription id</span></span>

## <span data-ttu-id="6c521-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6c521-148">RELATED LINKS</span></span>

