---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/new-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/New-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/New-AzDedicatedHsm.md
ms.openlocfilehash: ff1fc53d7fec9a56564bbf536469ea9f745f9265
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200522"
---
# <span data-ttu-id="b701f-101">New-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="b701f-101">New-AzDedicatedHsm</span></span>

## <span data-ttu-id="b701f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b701f-102">SYNOPSIS</span></span>
<span data-ttu-id="b701f-103">Tworzenie lub aktualizowanie dedykowanego modułu HSM w określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b701f-103">Create or Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="b701f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b701f-104">SYNTAX</span></span>

```
New-AzDedicatedHsm -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-NetworkInterface <INetworkInterface[]>] [-Sku <String>] [-StampId <String>] [-SubnetId <String>]
 [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="b701f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b701f-105">DESCRIPTION</span></span>
<span data-ttu-id="b701f-106">Tworzenie lub aktualizowanie dedykowanego modułu HSM w określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b701f-106">Create or Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="b701f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b701f-107">EXAMPLES</span></span>

### <span data-ttu-id="b701f-108">Przykład 1. Tworzenie dedykowanego modułu HSM w istniejącej sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="b701f-108">Example 1: Create a Dedicated HSM into an existing virtual network</span></span>
```powershell
PS C:\> New-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Location eastus -Sku "SafeNet Luna Network HSM A790" -StampId stamp1 -SubnetId "/subscriptions/xxxx-xxxx-xxx-xxx/resourceGroups/dedicatedhsm-rg-n359cz/providers/Microsoft.Network/virtualNetworks/vnetq30la9/subnets/hsmsubnet" -NetworkInterface @{PrivateIPAddress = '10.2.1.120' }

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="b701f-109">To polecenie tworzy dedykowany moduł HSM w istniejącej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b701f-109">This command creates a Dedicated HSM into an existing virtual network.</span></span>

<span data-ttu-id="b701f-110">**UWAGA:** Obecnie istnieje ograniczenie, które zwraca przed pełnym inicjowaniem obsługi `New-AzDedicatedHsm` systemu HSM na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="b701f-110">**NOTE:** Currently `New-AzDedicatedHsm` has a limitation that it returns before the HSM is fully provisioned on Azure.</span></span>
<span data-ttu-id="b701f-111">Dlatego po utworzeniu nowego hsm należy sprawdzić jego stan i upewnić się, że jest przed `Get-AzDedicatedHsm` `Provisioning State` jego `Succeeded` użyciem.</span><span class="sxs-lookup"><span data-stu-id="b701f-111">Therefore after creating a new HSM, please query its state by `Get-AzDedicatedHsm` and make sure its `Provisioning State` is `Succeeded` before using it.</span></span>

## <span data-ttu-id="b701f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b701f-112">PARAMETERS</span></span>

### <span data-ttu-id="b701f-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="b701f-113">-AsJob</span></span>
<span data-ttu-id="b701f-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="b701f-114">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b701f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b701f-115">-DefaultProfile</span></span>
<span data-ttu-id="b701f-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b701f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b701f-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b701f-117">-Location</span></span>
<span data-ttu-id="b701f-118">Obsługiwana lokalizacja platformy Azure, w której należy utworzyć dedykowany moduł HSM.</span><span class="sxs-lookup"><span data-stu-id="b701f-118">The supported Azure location where the dedicated HSM should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b701f-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b701f-119">-Name</span></span>
<span data-ttu-id="b701f-120">Nazwa dedykowanego hsm</span><span class="sxs-lookup"><span data-stu-id="b701f-120">Name of the dedicated Hsm</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b701f-121">- NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b701f-121">-NetworkInterface</span></span>
<span data-ttu-id="b701f-122">Określa listę identyfikatorów zasobów dla interfejsów sieciowych skojarzonych ze dedykowanym modułem HSM.</span><span class="sxs-lookup"><span data-stu-id="b701f-122">Specifies the list of resource Ids for the network interfaces associated with the dedicated HSM.</span></span>
<span data-ttu-id="b701f-123">Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach NETWORKINTERFACE i utworzyć tabelę skrótów.</span><span class="sxs-lookup"><span data-stu-id="b701f-123">To construct, see NOTES section for NETWORKINTERFACE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.INetworkInterface[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b701f-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b701f-124">-NoWait</span></span>
<span data-ttu-id="b701f-125">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="b701f-125">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b701f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b701f-126">-ResourceGroupName</span></span>
<span data-ttu-id="b701f-127">Nazwa grupy zasobów, do której należy zasób.</span><span class="sxs-lookup"><span data-stu-id="b701f-127">The name of the Resource Group to which the resource belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b701f-128">- SKU</span><span class="sxs-lookup"><span data-stu-id="b701f-128">-Sku</span></span>
<span data-ttu-id="b701f-129">SKU dedykowanego hsm</span><span class="sxs-lookup"><span data-stu-id="b701f-129">SKU of the dedicated HSM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b701f-130">- StampId</span><span class="sxs-lookup"><span data-stu-id="b701f-130">-StampId</span></span>
<span data-ttu-id="b701f-131">To pole będzie używane, gdy JNW nie obsługuje stref dostępności.</span><span class="sxs-lookup"><span data-stu-id="b701f-131">This field will be used when RP does not support Availability zones.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b701f-132">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="b701f-132">-SubnetId</span></span>
<span data-ttu-id="b701f-133">Identyfikator ARM w postaci /subscriptions/{SubscriptionId}/resourceGroups/{ResourceGroupName}/...</span><span class="sxs-lookup"><span data-stu-id="b701f-133">The ARM resource id in the form of /subscriptions/{SubscriptionId}/resourceGroups/{ResourceGroupName}/...</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b701f-134">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b701f-134">-SubscriptionId</span></span>
<span data-ttu-id="b701f-135">Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b701f-135">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b701f-136">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="b701f-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b701f-137">— Tag</span><span class="sxs-lookup"><span data-stu-id="b701f-137">-Tag</span></span>
<span data-ttu-id="b701f-138">Tagi zasobów</span><span class="sxs-lookup"><span data-stu-id="b701f-138">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b701f-139">— Strefa</span><span class="sxs-lookup"><span data-stu-id="b701f-139">-Zone</span></span>
<span data-ttu-id="b701f-140">Dedykowane strefy Hsm.</span><span class="sxs-lookup"><span data-stu-id="b701f-140">The Dedicated Hsm zones.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b701f-141">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b701f-141">-Confirm</span></span>
<span data-ttu-id="b701f-142">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b701f-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b701f-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b701f-143">-WhatIf</span></span>
<span data-ttu-id="b701f-144">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b701f-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b701f-145">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b701f-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b701f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b701f-146">CommonParameters</span></span>
<span data-ttu-id="b701f-147">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b701f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b701f-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b701f-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b701f-149">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b701f-149">INPUTS</span></span>

## <span data-ttu-id="b701f-150">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b701f-150">OUTPUTS</span></span>

### <span data-ttu-id="b701f-151">Microsoft.Azure.PowerShell.Cmdlet.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="b701f-151">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="b701f-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b701f-152">NOTES</span></span>

<span data-ttu-id="b701f-153">ALIASY</span><span class="sxs-lookup"><span data-stu-id="b701f-153">ALIASES</span></span>

<span data-ttu-id="b701f-154">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="b701f-154">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b701f-155">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="b701f-155">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b701f-156">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b701f-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b701f-157">NETWORKINTERFACE <INetworkInterface[]>: Określa listę identyfikatorów zasobów dla interfejsów sieciowych skojarzonych ze dedykowanym modułem HSM.</span><span class="sxs-lookup"><span data-stu-id="b701f-157">NETWORKINTERFACE <INetworkInterface[]>: Specifies the list of resource Ids for the network interfaces associated with the dedicated HSM.</span></span>
  - <span data-ttu-id="b701f-158">`[PrivateIPAddress <String>]`: prywatny adres IP interfejsu</span><span class="sxs-lookup"><span data-stu-id="b701f-158">`[PrivateIPAddress <String>]`: Private Ip address of the interface</span></span>

## <span data-ttu-id="b701f-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b701f-159">RELATED LINKS</span></span>

