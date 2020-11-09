---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/get-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Get-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Get-AzDedicatedHsm.md
ms.openlocfilehash: a8f6e3d6d7818a03f0e284b9c08a1ffdcd646710
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305035"
---
# <span data-ttu-id="093d4-101">Get-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="093d4-101">Get-AzDedicatedHsm</span></span>

## <span data-ttu-id="093d4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="093d4-102">SYNOPSIS</span></span>
<span data-ttu-id="093d4-103">Pobiera określony dedykowany HSM platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="093d4-103">Gets the specified Azure dedicated HSM.</span></span>

## <span data-ttu-id="093d4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="093d4-104">SYNTAX</span></span>

### <span data-ttu-id="093d4-105">List1 (domyślny)</span><span class="sxs-lookup"><span data-stu-id="093d4-105">List1 (Default)</span></span>
```
Get-AzDedicatedHsm [-SubscriptionId <String[]>] [-Top <Int32>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="093d4-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="093d4-106">Get</span></span>
```
Get-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="093d4-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="093d4-107">GetViaIdentity</span></span>
```
Get-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="093d4-108">Lista</span><span class="sxs-lookup"><span data-stu-id="093d4-108">List</span></span>
```
Get-AzDedicatedHsm -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Top <Int32>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="093d4-109">Opis</span><span class="sxs-lookup"><span data-stu-id="093d4-109">DESCRIPTION</span></span>
<span data-ttu-id="093d4-110">Pobiera określony dedykowany HSM platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="093d4-110">Gets the specified Azure dedicated HSM.</span></span>

## <span data-ttu-id="093d4-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="093d4-111">EXAMPLES</span></span>

### <span data-ttu-id="093d4-112">Przykład 1: uzyskiwanie wszystkich dedykowanych HSM w ramach abonamentu</span><span class="sxs-lookup"><span data-stu-id="093d4-112">Example 1: Get all Dedicated HSM under a subscription</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
yeminghsm  Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="093d4-113">To polecenie pobiera cały dedykowany HSM w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="093d4-113">This command gets all Dedicated HSM under a subscription</span></span>

### <span data-ttu-id="093d4-114">Przykład 2: pobieranie całego dedykowanego modułu HSM w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="093d4-114">Example 2: Get all Dedicated HSM under a resource group.</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm -ResourceGroupName dedicatedhsm-rg-n359cz

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="093d4-115">To polecenie pobiera wszystkie dedykowane HSM w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="093d4-115">This command gets all Dedicated HSM under a resource group.</span></span>

### <span data-ttu-id="093d4-116">Przykład 3: uzyskiwanie dedykowanego modułu HSM według nazwy</span><span class="sxs-lookup"><span data-stu-id="093d4-116">Example 3: Get a Dedicated HSM by name</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName dedicatedhsm-rg-n359cz

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="093d4-117">To polecenie pobiera dedykowany HSM o nazwie.</span><span class="sxs-lookup"><span data-stu-id="093d4-117">This command gets a Dedicated HSM by name.</span></span>

### <span data-ttu-id="093d4-118">Przykład 4: uzyskiwanie dedykowanego modułu HSM według obiektu</span><span class="sxs-lookup"><span data-stu-id="093d4-118">Example 4: Get a Dedicated HSM by object</span></span>
```powershell
PS C:\> $hsm = New-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Location eastus -Sku "SafeNet Luna Network HSM A790" -StampId stamp1 -SubnetId "/subscriptions/xxxx-xxxx-xxx-xxx/resourceGroups/dedicatedhsm-rg-n359cz/providers/Microsoft.Network/virtualNetworks/vnetq30la9/subnets/hsmsubnet" -NetworkInterface @{PrivateIPAddress = '10.2.1.120' }
PS C:\> Get-AzDedicatedHsm -InputObject $hsm

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="093d4-119">To polecenie uzyskuje dedykowany obiekt HSM.</span><span class="sxs-lookup"><span data-stu-id="093d4-119">This command gets a Dedicated HSM by object.</span></span>

## <span data-ttu-id="093d4-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="093d4-120">PARAMETERS</span></span>

### <span data-ttu-id="093d4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="093d4-121">-DefaultProfile</span></span>
<span data-ttu-id="093d4-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="093d4-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="093d4-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="093d4-123">-InputObject</span></span>
<span data-ttu-id="093d4-124">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="093d4-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="093d4-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="093d4-125">-Name</span></span>
<span data-ttu-id="093d4-126">Nazwa dedykowanego modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="093d4-126">The name of the dedicated HSM.</span></span>

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

### <span data-ttu-id="093d4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="093d4-127">-ResourceGroupName</span></span>
<span data-ttu-id="093d4-128">Nazwa grupy zasobów, do której należy dedykowany HSM.</span><span class="sxs-lookup"><span data-stu-id="093d4-128">The name of the Resource Group to which the dedicated hsm belongs.</span></span>

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

### <span data-ttu-id="093d4-129">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="093d4-129">-SubscriptionId</span></span>
<span data-ttu-id="093d4-130">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="093d4-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="093d4-131">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="093d4-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="093d4-132">-Początek</span><span class="sxs-lookup"><span data-stu-id="093d4-132">-Top</span></span>
<span data-ttu-id="093d4-133">Maksymalna liczba wyników do zwrócenia.</span><span class="sxs-lookup"><span data-stu-id="093d4-133">Maximum number of results to return.</span></span>

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

### <span data-ttu-id="093d4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="093d4-134">CommonParameters</span></span>
<span data-ttu-id="093d4-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="093d4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="093d4-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="093d4-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="093d4-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="093d4-137">INPUTS</span></span>

### <span data-ttu-id="093d4-138">Microsoft. Azure. PowerShell. polecenia. DedicatedHsm. models. IDedicatedHsmIdentity</span><span class="sxs-lookup"><span data-stu-id="093d4-138">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="093d4-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="093d4-139">OUTPUTS</span></span>

### <span data-ttu-id="093d4-140">Microsoft. Azure. PowerShell. polecenia. DedicatedHsm. models. Api20181031. IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="093d4-140">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="093d4-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="093d4-141">NOTES</span></span>

<span data-ttu-id="093d4-142">PISUJE</span><span class="sxs-lookup"><span data-stu-id="093d4-142">ALIASES</span></span>

<span data-ttu-id="093d4-143">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="093d4-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="093d4-144">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="093d4-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="093d4-145">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="093d4-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="093d4-146">INPUTobject <IDedicatedHsmIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="093d4-146">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="093d4-147">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="093d4-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="093d4-148">`[Name <String>]`: Nazwa dedykowanego modułu HSM</span><span class="sxs-lookup"><span data-stu-id="093d4-148">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="093d4-149">`[ResourceGroupName <String>]`: Nazwa grupy zasobów, do której należy zasób.</span><span class="sxs-lookup"><span data-stu-id="093d4-149">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="093d4-150">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="093d4-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="093d4-151">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="093d4-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="093d4-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="093d4-152">RELATED LINKS</span></span>

