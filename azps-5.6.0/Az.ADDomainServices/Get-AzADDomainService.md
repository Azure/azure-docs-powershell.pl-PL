---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/powershell/module/az.addomainservices/get-azaddomainservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Get-AzADDomainService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Get-AzADDomainService.md
ms.openlocfilehash: 19ae45bf50c9ae54075e46a8db8fc66cc08e488a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997039"
---
# <span data-ttu-id="8d73a-101">Get-AzADDomainService</span><span class="sxs-lookup"><span data-stu-id="8d73a-101">Get-AzADDomainService</span></span>

## <span data-ttu-id="8d73a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d73a-102">SYNOPSIS</span></span>
<span data-ttu-id="8d73a-103">Operacja Pobierz usługę domeny pobiera reprezentację json usługi domeny.</span><span class="sxs-lookup"><span data-stu-id="8d73a-103">The Get Domain Service operation retrieves a json representation of the Domain Service.</span></span>

## <span data-ttu-id="8d73a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8d73a-104">SYNTAX</span></span>

### <span data-ttu-id="8d73a-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="8d73a-105">List (Default)</span></span>
```
Get-AzADDomainService [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8d73a-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="8d73a-106">Get</span></span>
```
Get-AzADDomainService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8d73a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8d73a-107">GetViaIdentity</span></span>
```
Get-AzADDomainService -InputObject <IAdDomainServicesIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="8d73a-108">Lista1</span><span class="sxs-lookup"><span data-stu-id="8d73a-108">List1</span></span>
```
Get-AzADDomainService -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="8d73a-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="8d73a-109">DESCRIPTION</span></span>
<span data-ttu-id="8d73a-110">Operacja Pobierz usługę domeny pobiera reprezentację json usługi domeny.</span><span class="sxs-lookup"><span data-stu-id="8d73a-110">The Get Domain Service operation retrieves a json representation of the Domain Service.</span></span>

## <span data-ttu-id="8d73a-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8d73a-111">EXAMPLES</span></span>

### <span data-ttu-id="8d73a-112">Przykład 1. Domyślnie pobierz wszystkie usługi ADDomainService</span><span class="sxs-lookup"><span data-stu-id="8d73a-112">Example 1: Get All ADDomainService By default</span></span>
```powershell
PS C:\> Get-AzADDomainService

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="8d73a-113">Domyślnie pobierz wszystkie usługi ADDomainService</span><span class="sxs-lookup"><span data-stu-id="8d73a-113">Get All ADDomainService By default</span></span>

### <span data-ttu-id="8d73a-114">Przykład 2. Uzyskiwanie usługi ADDomainService By ResourceGroup i nazwy</span><span class="sxs-lookup"><span data-stu-id="8d73a-114">Example 2: Get ADDomainService By ResourceGroup and name</span></span>
```powershell
PS C:\> Get-AzADDomainService -Name youriADdomain -ResourceGroupName youriADdomain

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="8d73a-115">Uzyskiwanie usługi ADDomainService By ResourceGroup i nazwy</span><span class="sxs-lookup"><span data-stu-id="8d73a-115">Get ADDomainService By ResourceGroup and name</span></span>

### <span data-ttu-id="8d73a-116">Przykład 3. Uzyskiwanie wszystkich usług ADDomainService by ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8d73a-116">Example 3: Get all ADDomainService By ResourceGroup</span></span>
```powershell
PS C:\> Get-AzADDomainService -ResourceGroupName youriADdomain

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="8d73a-117">Uzyskiwanie wszystkich usług ADDomainService by ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8d73a-117">Get all ADDomainService By ResourceGroup</span></span>

### <span data-ttu-id="8d73a-118">Przykład 4. Uzyskiwanie usługi ADDomainService by InputObject</span><span class="sxs-lookup"><span data-stu-id="8d73a-118">Example 4: Get ADDomainService By InputObject</span></span>
```powershell
PS C:\> $getAzAddomain = Get-AzADDomainService -Name youriADdomain -ResourceGroupName youriADdomain
Get-AzADDomainService -InputObject $getAzAddomain

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="8d73a-119">Uzyskiwanie usługi ADDomainService by InputObject</span><span class="sxs-lookup"><span data-stu-id="8d73a-119">Get ADDomainService By InputObject</span></span>

## <span data-ttu-id="8d73a-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d73a-120">PARAMETERS</span></span>

### <span data-ttu-id="8d73a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d73a-121">-DefaultProfile</span></span>
<span data-ttu-id="8d73a-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8d73a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d73a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8d73a-123">-InputObject</span></span>
<span data-ttu-id="8d73a-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="8d73a-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d73a-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8d73a-125">-Name</span></span>
<span data-ttu-id="8d73a-126">Nazwa usługi domeny.</span><span class="sxs-lookup"><span data-stu-id="8d73a-126">The name of the domain service.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DomainServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d73a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d73a-127">-ResourceGroupName</span></span>
<span data-ttu-id="8d73a-128">Nazwa grupy zasobów w ramach subskrypcji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="8d73a-128">The name of the resource group within the user's subscription.</span></span>
<span data-ttu-id="8d73a-129">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="8d73a-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="8d73a-130">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8d73a-130">-SubscriptionId</span></span>
<span data-ttu-id="8d73a-131">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8d73a-131">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="8d73a-132">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="8d73a-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8d73a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d73a-133">CommonParameters</span></span>
<span data-ttu-id="8d73a-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d73a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d73a-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8d73a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d73a-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8d73a-136">INPUTS</span></span>

### <span data-ttu-id="8d73a-137">Microsoft.Azure.PowerShell.Cmdlet.ADDomainServices.Models.IAdDomainServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="8d73a-137">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity</span></span>

## <span data-ttu-id="8d73a-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8d73a-138">OUTPUTS</span></span>

### <span data-ttu-id="8d73a-139">Microsoft.Azure.PowerShell.Cmdlet.ADDomainServices.Models.Api202001.IDomainService</span><span class="sxs-lookup"><span data-stu-id="8d73a-139">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span></span>

## <span data-ttu-id="8d73a-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8d73a-140">NOTES</span></span>

<span data-ttu-id="8d73a-141">ALIASY</span><span class="sxs-lookup"><span data-stu-id="8d73a-141">ALIASES</span></span>

<span data-ttu-id="8d73a-142">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8d73a-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8d73a-143">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="8d73a-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8d73a-144">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8d73a-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8d73a-145">INPUTOBJECT: <IAdDomainServicesIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="8d73a-145">INPUTOBJECT <IAdDomainServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8d73a-146">`[DomainServiceName <String>]`: nazwa usługi domeny.</span><span class="sxs-lookup"><span data-stu-id="8d73a-146">`[DomainServiceName <String>]`: The name of the domain service.</span></span>
  - <span data-ttu-id="8d73a-147">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="8d73a-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8d73a-148">`[ResourceGroupName <String>]`: nazwa grupy zasobów w ramach subskrypcji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="8d73a-148">`[ResourceGroupName <String>]`: The name of the resource group within the user's subscription.</span></span> <span data-ttu-id="8d73a-149">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="8d73a-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="8d73a-150">`[SubscriptionId <String>]`: pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8d73a-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="8d73a-151">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="8d73a-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="8d73a-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8d73a-152">RELATED LINKS</span></span>

