---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/new-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/New-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/New-AzDedicatedHsm.md
ms.openlocfilehash: ff1fc53d7fec9a56564bbf536469ea9f745f9265
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221240"
---
# <span data-ttu-id="1b0b0-101">New-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="1b0b0-101">New-AzDedicatedHsm</span></span>

## <span data-ttu-id="1b0b0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1b0b0-102">SYNOPSIS</span></span>
<span data-ttu-id="1b0b0-103">Tworzenie lub aktualizowanie dedykowanego modułu HSM w określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1b0b0-103">Create or Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="1b0b0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1b0b0-104">SYNTAX</span></span>

```
New-AzDedicatedHsm -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-NetworkInterface <INetworkInterface[]>] [-Sku <String>] [-StampId <String>] [-SubnetId <String>]
 [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="1b0b0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1b0b0-105">DESCRIPTION</span></span>
<span data-ttu-id="1b0b0-106">Tworzenie lub aktualizowanie dedykowanego modułu HSM w określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1b0b0-106">Create or Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="1b0b0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1b0b0-107">EXAMPLES</span></span>

### <span data-ttu-id="1b0b0-108">Przykład 1. tworzenie dedykowanego modułu HSM w istniejącej sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="1b0b0-108">Example 1: Create a Dedicated HSM into an existing virtual network</span></span>
```powershell
PS C:\> New-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Location eastus -Sku "SafeNet Luna Network HSM A790" -StampId stamp1 -SubnetId "/subscriptions/xxxx-xxxx-xxx-xxx/resourceGroups/dedicatedhsm-rg-n359cz/providers/Microsoft.Network/virtualNetworks/vnetq30la9/subnets/hsmsubnet" -NetworkInterface @{PrivateIPAddress = '10.2.1.120' }

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="1b0b0-109">To polecenie tworzy dedykowany HSM w istniejącej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1b0b0-109">This command creates a Dedicated HSM into an existing virtual network.</span></span>

<span data-ttu-id="1b0b0-110">**Uwaga:** Obecnie `New-AzDedicatedHsm` istnieje ograniczenie, które zwraca przed pełnym zainicjowaniem modułu HSM na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="1b0b0-110">**NOTE:** Currently `New-AzDedicatedHsm` has a limitation that it returns before the HSM is fully provisioned on Azure.</span></span>
<span data-ttu-id="1b0b0-111">Dlatego po utworzeniu nowego modułu HSM Zbadaj jego stan i upewnij się, `Get-AzDedicatedHsm` że `Provisioning State` jest `Succeeded` on przed jego użyciem.</span><span class="sxs-lookup"><span data-stu-id="1b0b0-111">Therefore after creating a new HSM, please query its state by `Get-AzDedicatedHsm` and make sure its `Provisioning State` is `Succeeded` before using it.</span></span>

## <span data-ttu-id="1b0b0-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1b0b0-112">PARAMETERS</span></span>

### <span data-ttu-id="1b0b0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1b0b0-113">-AsJob</span></span>
<span data-ttu-id="1b0b0-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="1b0b0-114">Run the command as a job</span></span>

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

### <span data-ttu-id="1b0b0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b0b0-115">-DefaultProfile</span></span>
<span data-ttu-id="1b0b0-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1b0b0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b0b0-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="1b0b0-117">-Location</span></span>
<span data-ttu-id="1b0b0-118">Obsługiwana lokalizacja platformy Azure, w której ma zostać utworzony dedykowany HSM.</span><span class="sxs-lookup"><span data-stu-id="1b0b0-118">The supported Azure location where the dedicated HSM should be created.</span></span>

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

### <span data-ttu-id="1b0b0-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1b0b0-119">-Name</span></span>
<span data-ttu-id="1b0b0-120">Nazwa dedykowanego modułu HSM</span><span class="sxs-lookup"><span data-stu-id="1b0b0-120">Name of the dedicated Hsm</span></span>

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

### <span data-ttu-id="1b0b0-121">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="1b0b0-121">-NetworkInterface</span></span>
<span data-ttu-id="1b0b0-122">Określa listę identyfikatorów zasobów dla interfejsów sieciowych skojarzonych z dedykowanym HSM.</span><span class="sxs-lookup"><span data-stu-id="1b0b0-122">Specifies the list of resource Ids for the network interfaces associated with the dedicated HSM.</span></span>
<span data-ttu-id="1b0b0-123">Aby skonstruować, zobacz sekcję notatki dla właściwości NETWORKINTERFACE i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="1b0b0-123">To construct, see NOTES section for NETWORKINTERFACE properties and create a hash table.</span></span>

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

### <span data-ttu-id="1b0b0-124">-Nowait</span><span class="sxs-lookup"><span data-stu-id="1b0b0-124">-NoWait</span></span>
<span data-ttu-id="1b0b0-125">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="1b0b0-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1b0b0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b0b0-126">-ResourceGroupName</span></span>
<span data-ttu-id="1b0b0-127">Nazwa grupy zasobów, do której należy dany zasób.</span><span class="sxs-lookup"><span data-stu-id="1b0b0-127">The name of the Resource Group to which the resource belongs.</span></span>

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

### <span data-ttu-id="1b0b0-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="1b0b0-128">-Sku</span></span>
<span data-ttu-id="1b0b0-129">SKU dedykowanego modułu HSM</span><span class="sxs-lookup"><span data-stu-id="1b0b0-129">SKU of the dedicated HSM</span></span>

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

### <span data-ttu-id="1b0b0-130">-StampId</span><span class="sxs-lookup"><span data-stu-id="1b0b0-130">-StampId</span></span>
<span data-ttu-id="1b0b0-131">To pole będzie używane, gdy RP nie obsługuje stref dostępności.</span><span class="sxs-lookup"><span data-stu-id="1b0b0-131">This field will be used when RP does not support Availability zones.</span></span>

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

### <span data-ttu-id="1b0b0-132">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="1b0b0-132">-SubnetId</span></span>
<span data-ttu-id="1b0b0-133">Identyfikator zasobu ARM w formie/subscriptions/{SubscriptionId}/resourceGroups/{ResourceGroupName}/...</span><span class="sxs-lookup"><span data-stu-id="1b0b0-133">The ARM resource id in the form of /subscriptions/{SubscriptionId}/resourceGroups/{ResourceGroupName}/...</span></span>

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

### <span data-ttu-id="1b0b0-134">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="1b0b0-134">-SubscriptionId</span></span>
<span data-ttu-id="1b0b0-135">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1b0b0-135">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1b0b0-136">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="1b0b0-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1b0b0-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="1b0b0-137">-Tag</span></span>
<span data-ttu-id="1b0b0-138">Znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="1b0b0-138">Resource tags</span></span>

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

### <span data-ttu-id="1b0b0-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="1b0b0-139">-Zone</span></span>
<span data-ttu-id="1b0b0-140">Dedykowane strefy HSM.</span><span class="sxs-lookup"><span data-stu-id="1b0b0-140">The Dedicated Hsm zones.</span></span>

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

### <span data-ttu-id="1b0b0-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1b0b0-141">-Confirm</span></span>
<span data-ttu-id="1b0b0-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b0b0-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b0b0-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b0b0-143">-WhatIf</span></span>
<span data-ttu-id="1b0b0-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b0b0-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b0b0-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1b0b0-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b0b0-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b0b0-146">CommonParameters</span></span>
<span data-ttu-id="1b0b0-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b0b0-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b0b0-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1b0b0-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b0b0-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1b0b0-149">INPUTS</span></span>

## <span data-ttu-id="1b0b0-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1b0b0-150">OUTPUTS</span></span>

### <span data-ttu-id="1b0b0-151">Microsoft. Azure. PowerShell. polecenia. DedicatedHsm. models. Api20181031. IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="1b0b0-151">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="1b0b0-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1b0b0-152">NOTES</span></span>

<span data-ttu-id="1b0b0-153">PISUJE</span><span class="sxs-lookup"><span data-stu-id="1b0b0-153">ALIASES</span></span>

<span data-ttu-id="1b0b0-154">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1b0b0-154">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1b0b0-155">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="1b0b0-155">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1b0b0-156">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1b0b0-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1b0b0-157">NETWORKINTERFACE <INetworkInterface [] >: określa listę identyfikatorów zasobów dla interfejsów sieciowych skojarzonych z dedykowanym HSM.</span><span class="sxs-lookup"><span data-stu-id="1b0b0-157">NETWORKINTERFACE <INetworkInterface[]>: Specifies the list of resource Ids for the network interfaces associated with the dedicated HSM.</span></span>
  - <span data-ttu-id="1b0b0-158">`[PrivateIPAddress <String>]`: Prywatny adres IP interfejsu</span><span class="sxs-lookup"><span data-stu-id="1b0b0-158">`[PrivateIPAddress <String>]`: Private Ip address of the interface</span></span>

## <span data-ttu-id="1b0b0-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1b0b0-159">RELATED LINKS</span></span>

