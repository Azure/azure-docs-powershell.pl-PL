---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/powershell/module/az.dedicatedhsm/get-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Get-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Get-AzDedicatedHsm.md
ms.openlocfilehash: b4e00745655be6eb050141bb04dcef4797bde256
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966410"
---
# <span data-ttu-id="8bb03-101">Get-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="8bb03-101">Get-AzDedicatedHsm</span></span>

## <span data-ttu-id="8bb03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8bb03-102">SYNOPSIS</span></span>
<span data-ttu-id="8bb03-103">Pobiera określony dedykowany moduł HSM platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8bb03-103">Gets the specified Azure dedicated HSM.</span></span>

## <span data-ttu-id="8bb03-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8bb03-104">SYNTAX</span></span>

### <span data-ttu-id="8bb03-105">Lista1 (domyślna)</span><span class="sxs-lookup"><span data-stu-id="8bb03-105">List1 (Default)</span></span>
```
Get-AzDedicatedHsm [-SubscriptionId <String[]>] [-Top <Int32>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="8bb03-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="8bb03-106">Get</span></span>
```
Get-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8bb03-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8bb03-107">GetViaIdentity</span></span>
```
Get-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8bb03-108">Lista</span><span class="sxs-lookup"><span data-stu-id="8bb03-108">List</span></span>
```
Get-AzDedicatedHsm -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Top <Int32>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="8bb03-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="8bb03-109">DESCRIPTION</span></span>
<span data-ttu-id="8bb03-110">Pobiera określony dedykowany moduł HSM platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8bb03-110">Gets the specified Azure dedicated HSM.</span></span>

## <span data-ttu-id="8bb03-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8bb03-111">EXAMPLES</span></span>

### <span data-ttu-id="8bb03-112">Przykład 1. Uzyskiwanie wszystkich dedykowanych zabezpieczeń HSM w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="8bb03-112">Example 1: Get all Dedicated HSM under a subscription</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
yeminghsm  Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="8bb03-113">To polecenie pobiera wszystkie moduł HSM dedykowanych w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="8bb03-113">This command gets all Dedicated HSM under a subscription</span></span>

### <span data-ttu-id="8bb03-114">Przykład 2. Wszystkie dedykowany moduł HSM należy do grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8bb03-114">Example 2: Get all Dedicated HSM under a resource group.</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm -ResourceGroupName dedicatedhsm-rg-n359cz

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="8bb03-115">To polecenie pobiera cały moduł HSM dedykowany w ramach grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8bb03-115">This command gets all Dedicated HSM under a resource group.</span></span>

### <span data-ttu-id="8bb03-116">Przykład 3. Uzyskiwanie dedykowanego modułu HSM według nazwy</span><span class="sxs-lookup"><span data-stu-id="8bb03-116">Example 3: Get a Dedicated HSM by name</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName dedicatedhsm-rg-n359cz

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="8bb03-117">To polecenie otrzymuje według nazwy dedykowany moduł HSM.</span><span class="sxs-lookup"><span data-stu-id="8bb03-117">This command gets a Dedicated HSM by name.</span></span>

### <span data-ttu-id="8bb03-118">Przykład 4. Uzyskiwanie dedykowanego modułu HSM według obiektu</span><span class="sxs-lookup"><span data-stu-id="8bb03-118">Example 4: Get a Dedicated HSM by object</span></span>
```powershell
PS C:\> $hsm = New-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Location eastus -Sku "SafeNet Luna Network HSM A790" -StampId stamp1 -SubnetId "/subscriptions/xxxx-xxxx-xxx-xxx/resourceGroups/dedicatedhsm-rg-n359cz/providers/Microsoft.Network/virtualNetworks/vnetq30la9/subnets/hsmsubnet" -NetworkInterface @{PrivateIPAddress = '10.2.1.120' }
PS C:\> Get-AzDedicatedHsm -InputObject $hsm

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="8bb03-119">To polecenie pobiera obiekt dedykowany HSM.</span><span class="sxs-lookup"><span data-stu-id="8bb03-119">This command gets a Dedicated HSM by object.</span></span>

## <span data-ttu-id="8bb03-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8bb03-120">PARAMETERS</span></span>

### <span data-ttu-id="8bb03-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bb03-121">-DefaultProfile</span></span>
<span data-ttu-id="8bb03-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8bb03-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bb03-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8bb03-123">-InputObject</span></span>
<span data-ttu-id="8bb03-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="8bb03-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8bb03-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8bb03-125">-Name</span></span>
<span data-ttu-id="8bb03-126">Nazwa dedykowanego modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="8bb03-126">The name of the dedicated HSM.</span></span>

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

### <span data-ttu-id="8bb03-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bb03-127">-ResourceGroupName</span></span>
<span data-ttu-id="8bb03-128">Nazwa grupy zasobów, do której należy dedykowany hsm.</span><span class="sxs-lookup"><span data-stu-id="8bb03-128">The name of the Resource Group to which the dedicated hsm belongs.</span></span>

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

### <span data-ttu-id="8bb03-129">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8bb03-129">-SubscriptionId</span></span>
<span data-ttu-id="8bb03-130">Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8bb03-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8bb03-131">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="8bb03-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8bb03-132">— Na górze</span><span class="sxs-lookup"><span data-stu-id="8bb03-132">-Top</span></span>
<span data-ttu-id="8bb03-133">Maksymalna liczba wyników do zwrócenia.</span><span class="sxs-lookup"><span data-stu-id="8bb03-133">Maximum number of results to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bb03-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bb03-134">CommonParameters</span></span>
<span data-ttu-id="8bb03-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bb03-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bb03-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8bb03-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bb03-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8bb03-137">INPUTS</span></span>

### <span data-ttu-id="8bb03-138">Microsoft.Azure.PowerShell.Cmdlet.DedicatedHsm.Models.IDedicatedHsmIdentity</span><span class="sxs-lookup"><span data-stu-id="8bb03-138">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="8bb03-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8bb03-139">OUTPUTS</span></span>

### <span data-ttu-id="8bb03-140">Microsoft.Azure.PowerShell.Cmdlet.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="8bb03-140">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="8bb03-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8bb03-141">NOTES</span></span>

<span data-ttu-id="8bb03-142">ALIASY</span><span class="sxs-lookup"><span data-stu-id="8bb03-142">ALIASES</span></span>

<span data-ttu-id="8bb03-143">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8bb03-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8bb03-144">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="8bb03-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8bb03-145">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8bb03-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8bb03-146">INPUTOBJECT: <IDedicatedHsmIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="8bb03-146">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8bb03-147">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="8bb03-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8bb03-148">`[Name <String>]`: nazwa dedykowanego hsm</span><span class="sxs-lookup"><span data-stu-id="8bb03-148">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="8bb03-149">`[ResourceGroupName <String>]`: nazwa grupy zasobów, do której należy zasób.</span><span class="sxs-lookup"><span data-stu-id="8bb03-149">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="8bb03-150">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8bb03-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="8bb03-151">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="8bb03-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="8bb03-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8bb03-152">RELATED LINKS</span></span>

