---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/new-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/New-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/New-AzDedicatedHsm.md
ms.openlocfilehash: ff1fc53d7fec9a56564bbf536469ea9f745f9265
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502642"
---
# <span data-ttu-id="76f1b-101">New-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="76f1b-101">New-AzDedicatedHsm</span></span>

## <span data-ttu-id="76f1b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="76f1b-102">SYNOPSIS</span></span>
<span data-ttu-id="76f1b-103">Tworzenie lub aktualizowanie dedykowanego modułu HSM w określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="76f1b-103">Create or Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="76f1b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="76f1b-104">SYNTAX</span></span>

```
New-AzDedicatedHsm -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-NetworkInterface <INetworkInterface[]>] [-Sku <String>] [-StampId <String>] [-SubnetId <String>]
 [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="76f1b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="76f1b-105">DESCRIPTION</span></span>
<span data-ttu-id="76f1b-106">Tworzenie lub aktualizowanie dedykowanego modułu HSM w określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="76f1b-106">Create or Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="76f1b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="76f1b-107">EXAMPLES</span></span>

### <span data-ttu-id="76f1b-108">Przykład 1. tworzenie dedykowanego modułu HSM w istniejącej sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="76f1b-108">Example 1: Create a Dedicated HSM into an existing virtual network</span></span>
```powershell
PS C:\> New-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Location eastus -Sku "SafeNet Luna Network HSM A790" -StampId stamp1 -SubnetId "/subscriptions/xxxx-xxxx-xxx-xxx/resourceGroups/dedicatedhsm-rg-n359cz/providers/Microsoft.Network/virtualNetworks/vnetq30la9/subnets/hsmsubnet" -NetworkInterface @{PrivateIPAddress = '10.2.1.120' }

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="76f1b-109">To polecenie tworzy dedykowany HSM w istniejącej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="76f1b-109">This command creates a Dedicated HSM into an existing virtual network.</span></span>

<span data-ttu-id="76f1b-110">**Uwaga:** Obecnie `New-AzDedicatedHsm` istnieje ograniczenie, które zwraca przed pełnym zainicjowaniem modułu HSM na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="76f1b-110">**NOTE:** Currently `New-AzDedicatedHsm` has a limitation that it returns before the HSM is fully provisioned on Azure.</span></span>
<span data-ttu-id="76f1b-111">Dlatego po utworzeniu nowego modułu HSM Zbadaj jego stan i upewnij się, `Get-AzDedicatedHsm` że `Provisioning State` jest `Succeeded` on przed jego użyciem.</span><span class="sxs-lookup"><span data-stu-id="76f1b-111">Therefore after creating a new HSM, please query its state by `Get-AzDedicatedHsm` and make sure its `Provisioning State` is `Succeeded` before using it.</span></span>

## <span data-ttu-id="76f1b-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="76f1b-112">PARAMETERS</span></span>

### <span data-ttu-id="76f1b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="76f1b-113">-AsJob</span></span>
<span data-ttu-id="76f1b-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="76f1b-114">Run the command as a job</span></span>

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

### <span data-ttu-id="76f1b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76f1b-115">-DefaultProfile</span></span>
<span data-ttu-id="76f1b-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="76f1b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76f1b-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="76f1b-117">-Location</span></span>
<span data-ttu-id="76f1b-118">Obsługiwana lokalizacja platformy Azure, w której ma zostać utworzony dedykowany HSM.</span><span class="sxs-lookup"><span data-stu-id="76f1b-118">The supported Azure location where the dedicated HSM should be created.</span></span>

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

### <span data-ttu-id="76f1b-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="76f1b-119">-Name</span></span>
<span data-ttu-id="76f1b-120">Nazwa dedykowanego modułu HSM</span><span class="sxs-lookup"><span data-stu-id="76f1b-120">Name of the dedicated Hsm</span></span>

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

### <span data-ttu-id="76f1b-121">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="76f1b-121">-NetworkInterface</span></span>
<span data-ttu-id="76f1b-122">Określa listę identyfikatorów zasobów dla interfejsów sieciowych skojarzonych z dedykowanym HSM.</span><span class="sxs-lookup"><span data-stu-id="76f1b-122">Specifies the list of resource Ids for the network interfaces associated with the dedicated HSM.</span></span>
<span data-ttu-id="76f1b-123">Aby skonstruować, zobacz sekcję notatki dla właściwości NETWORKINTERFACE i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="76f1b-123">To construct, see NOTES section for NETWORKINTERFACE properties and create a hash table.</span></span>

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

### <span data-ttu-id="76f1b-124">-Nowait</span><span class="sxs-lookup"><span data-stu-id="76f1b-124">-NoWait</span></span>
<span data-ttu-id="76f1b-125">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="76f1b-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="76f1b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76f1b-126">-ResourceGroupName</span></span>
<span data-ttu-id="76f1b-127">Nazwa grupy zasobów, do której należy dany zasób.</span><span class="sxs-lookup"><span data-stu-id="76f1b-127">The name of the Resource Group to which the resource belongs.</span></span>

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

### <span data-ttu-id="76f1b-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="76f1b-128">-Sku</span></span>
<span data-ttu-id="76f1b-129">SKU dedykowanego modułu HSM</span><span class="sxs-lookup"><span data-stu-id="76f1b-129">SKU of the dedicated HSM</span></span>

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

### <span data-ttu-id="76f1b-130">-StampId</span><span class="sxs-lookup"><span data-stu-id="76f1b-130">-StampId</span></span>
<span data-ttu-id="76f1b-131">To pole będzie używane, gdy RP nie obsługuje stref dostępności.</span><span class="sxs-lookup"><span data-stu-id="76f1b-131">This field will be used when RP does not support Availability zones.</span></span>

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

### <span data-ttu-id="76f1b-132">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="76f1b-132">-SubnetId</span></span>
<span data-ttu-id="76f1b-133">Identyfikator zasobu ARM w formie/subscriptions/{SubscriptionId}/resourceGroups/{ResourceGroupName}/...</span><span class="sxs-lookup"><span data-stu-id="76f1b-133">The ARM resource id in the form of /subscriptions/{SubscriptionId}/resourceGroups/{ResourceGroupName}/...</span></span>

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

### <span data-ttu-id="76f1b-134">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="76f1b-134">-SubscriptionId</span></span>
<span data-ttu-id="76f1b-135">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="76f1b-135">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="76f1b-136">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="76f1b-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="76f1b-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="76f1b-137">-Tag</span></span>
<span data-ttu-id="76f1b-138">Znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="76f1b-138">Resource tags</span></span>

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

### <span data-ttu-id="76f1b-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="76f1b-139">-Zone</span></span>
<span data-ttu-id="76f1b-140">Dedykowane strefy HSM.</span><span class="sxs-lookup"><span data-stu-id="76f1b-140">The Dedicated Hsm zones.</span></span>

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

### <span data-ttu-id="76f1b-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="76f1b-141">-Confirm</span></span>
<span data-ttu-id="76f1b-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76f1b-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76f1b-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76f1b-143">-WhatIf</span></span>
<span data-ttu-id="76f1b-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76f1b-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76f1b-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="76f1b-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76f1b-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76f1b-146">CommonParameters</span></span>
<span data-ttu-id="76f1b-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76f1b-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76f1b-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76f1b-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76f1b-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="76f1b-149">INPUTS</span></span>

## <span data-ttu-id="76f1b-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="76f1b-150">OUTPUTS</span></span>

### <span data-ttu-id="76f1b-151">Microsoft. Azure. PowerShell. polecenia. DedicatedHsm. models. Api20181031. IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="76f1b-151">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="76f1b-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="76f1b-152">NOTES</span></span>

<span data-ttu-id="76f1b-153">PISUJE</span><span class="sxs-lookup"><span data-stu-id="76f1b-153">ALIASES</span></span>

<span data-ttu-id="76f1b-154">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="76f1b-154">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="76f1b-155">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="76f1b-155">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="76f1b-156">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="76f1b-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="76f1b-157">NETWORKINTERFACE <INetworkInterface [] >: określa listę identyfikatorów zasobów dla interfejsów sieciowych skojarzonych z dedykowanym HSM.</span><span class="sxs-lookup"><span data-stu-id="76f1b-157">NETWORKINTERFACE <INetworkInterface[]>: Specifies the list of resource Ids for the network interfaces associated with the dedicated HSM.</span></span>
  - <span data-ttu-id="76f1b-158">`[PrivateIPAddress <String>]`: Prywatny adres IP interfejsu</span><span class="sxs-lookup"><span data-stu-id="76f1b-158">`[PrivateIPAddress <String>]`: Private Ip address of the interface</span></span>

## <span data-ttu-id="76f1b-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="76f1b-159">RELATED LINKS</span></span>

