---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/repair-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: b9a285e650f0ed47dd0144a460b324ecdae49f7d
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/24/2020
ms.locfileid: "94054268"
---
# <span data-ttu-id="939b2-101">Repair-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="939b2-101">Repair-AzsScaleUnitNode</span></span>

## <span data-ttu-id="939b2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="939b2-102">SYNOPSIS</span></span>
<span data-ttu-id="939b2-103">Naprawianie węzła klastra.</span><span class="sxs-lookup"><span data-stu-id="939b2-103">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="939b2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="939b2-104">SYNTAX</span></span>

### <span data-ttu-id="939b2-105">RepairExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="939b2-105">RepairExpanded (Default)</span></span>
```
Repair-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-BiosVersion <String>] [-BmciPv4Address <String>] [-ClusterName <String>]
 [-ComputerName <String>] [-Force] [-MacAddress <String>] [-Model <String>] [-SerialNumber <String>]
 [-Vendor <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="939b2-106">Mont</span><span class="sxs-lookup"><span data-stu-id="939b2-106">Repair</span></span>
```
Repair-AzsScaleUnitNode -Name <String> -BareMetalNode <IBareMetalNodeDescription> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="939b2-107">RepairViaIdentity</span><span class="sxs-lookup"><span data-stu-id="939b2-107">RepairViaIdentity</span></span>
```
Repair-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> -BareMetalNode <IBareMetalNodeDescription>
 [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="939b2-108">RepairViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="939b2-108">RepairViaIdentityExpanded</span></span>
```
Repair-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-BiosVersion <String>] [-BmciPv4Address <String>]
 [-ClusterName <String>] [-ComputerName <String>] [-Force] [-MacAddress <String>] [-Model <String>]
 [-SerialNumber <String>] [-Vendor <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="939b2-109">Opis</span><span class="sxs-lookup"><span data-stu-id="939b2-109">DESCRIPTION</span></span>
<span data-ttu-id="939b2-110">Naprawianie węzła klastra.</span><span class="sxs-lookup"><span data-stu-id="939b2-110">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="939b2-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="939b2-111">EXAMPLES</span></span>

### <span data-ttu-id="939b2-112">Przykład 1:</span><span class="sxs-lookup"><span data-stu-id="939b2-112">Example 1:</span></span>
```powershell
PS C:\> Repair-AzsScaleUnitNode -Name "AZS-ERCO03" -BMCIPv4Address ***.***.***.***

```

<span data-ttu-id="939b2-113">Naprawianie węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="939b2-113">Repair a scale unit node.</span></span>


## <span data-ttu-id="939b2-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="939b2-114">PARAMETERS</span></span>

### <span data-ttu-id="939b2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="939b2-115">-AsJob</span></span>
<span data-ttu-id="939b2-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="939b2-116">Run the command as a job</span></span>

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

### <span data-ttu-id="939b2-117">-BareMetalNode</span><span class="sxs-lookup"><span data-stu-id="939b2-117">-BareMetalNode</span></span>
<span data-ttu-id="939b2-118">Opis węzła systemu operacyjnego, który jest wykorzystywany do działania ScaleOut w klastrze.</span><span class="sxs-lookup"><span data-stu-id="939b2-118">Description of a bare metal node used for ScaleOut operation on a cluster.</span></span>
<span data-ttu-id="939b2-119">Aby skonstruować, zobacz sekcję notatki dla właściwości BAREMETALNODE i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="939b2-119">To construct, see NOTES section for BAREMETALNODE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IBareMetalNodeDescription
Parameter Sets: Repair, RepairViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="939b2-120">-BiosVersion</span><span class="sxs-lookup"><span data-stu-id="939b2-120">-BiosVersion</span></span>
<span data-ttu-id="939b2-121">Wersja systemu BIOS komputera fizycznego.</span><span class="sxs-lookup"><span data-stu-id="939b2-121">Bios version of the physical machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="939b2-122">-BmciPv4Address</span><span class="sxs-lookup"><span data-stu-id="939b2-122">-BmciPv4Address</span></span>
<span data-ttu-id="939b2-123">Adres BMC komputera fizycznego.</span><span class="sxs-lookup"><span data-stu-id="939b2-123">BMC address of the physical machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="939b2-124">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="939b2-124">-ClusterName</span></span>
<span data-ttu-id="939b2-125">Nazwa klastra.</span><span class="sxs-lookup"><span data-stu-id="939b2-125">Name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="939b2-126">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="939b2-126">-ComputerName</span></span>
<span data-ttu-id="939b2-127">Nazwa komputera.</span><span class="sxs-lookup"><span data-stu-id="939b2-127">Name of the computer.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="939b2-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="939b2-128">-DefaultProfile</span></span>
<span data-ttu-id="939b2-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="939b2-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="939b2-130">-Force</span><span class="sxs-lookup"><span data-stu-id="939b2-130">-Force</span></span>
<span data-ttu-id="939b2-131">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="939b2-131">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="939b2-132">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="939b2-132">-InputObject</span></span>
<span data-ttu-id="939b2-133">Aby skonstruować, zobacz sekcję notatki dla właściwości INPUTobject i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="939b2-133">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: RepairViaIdentity, RepairViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="939b2-134">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="939b2-134">-Location</span></span>
<span data-ttu-id="939b2-135">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="939b2-135">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair, RepairExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="939b2-136">-MacAddress</span><span class="sxs-lookup"><span data-stu-id="939b2-136">-MacAddress</span></span>
<span data-ttu-id="939b2-137">Nazwa adresu MAC węzła bez metalu.</span><span class="sxs-lookup"><span data-stu-id="939b2-137">Name of the MAC address of the bare metal node.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="939b2-138">-Model</span><span class="sxs-lookup"><span data-stu-id="939b2-138">-Model</span></span>
<span data-ttu-id="939b2-139">Model maszyny fizycznej.</span><span class="sxs-lookup"><span data-stu-id="939b2-139">Model of the physical machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="939b2-140">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="939b2-140">-Name</span></span>
<span data-ttu-id="939b2-141">Nazwa węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="939b2-141">Name of the scale unit node.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair, RepairExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="939b2-142">-Nowait</span><span class="sxs-lookup"><span data-stu-id="939b2-142">-NoWait</span></span>
<span data-ttu-id="939b2-143">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="939b2-143">Run the command asynchronously</span></span>

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

### <span data-ttu-id="939b2-144">-PassThru</span><span class="sxs-lookup"><span data-stu-id="939b2-144">-PassThru</span></span>
<span data-ttu-id="939b2-145">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="939b2-145">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="939b2-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="939b2-146">-ResourceGroupName</span></span>
<span data-ttu-id="939b2-147">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="939b2-147">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair, RepairExpanded
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="939b2-148">-Numer seryjny</span><span class="sxs-lookup"><span data-stu-id="939b2-148">-SerialNumber</span></span>
<span data-ttu-id="939b2-149">Numer seryjny maszyny fizycznej.</span><span class="sxs-lookup"><span data-stu-id="939b2-149">Serial number of the physical machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="939b2-150">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="939b2-150">-SubscriptionId</span></span>
<span data-ttu-id="939b2-151">Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="939b2-151">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="939b2-152">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="939b2-152">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair, RepairExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="939b2-153">-Vendor</span><span class="sxs-lookup"><span data-stu-id="939b2-153">-Vendor</span></span>
<span data-ttu-id="939b2-154">Dostawca komputera fizycznego.</span><span class="sxs-lookup"><span data-stu-id="939b2-154">Vendor of the physical machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="939b2-155">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="939b2-155">-Confirm</span></span>
<span data-ttu-id="939b2-156">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="939b2-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="939b2-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="939b2-157">-WhatIf</span></span>
<span data-ttu-id="939b2-158">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="939b2-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="939b2-159">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="939b2-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="939b2-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="939b2-160">CommonParameters</span></span>
<span data-ttu-id="939b2-161">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="939b2-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="939b2-162">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="939b2-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="939b2-163">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="939b2-163">INPUTS</span></span>

### <span data-ttu-id="939b2-164">Microsoft. Azure. PowerShell. polecenia. FabricAdmin. models. Api20160501. IBareMetalNodeDescription</span><span class="sxs-lookup"><span data-stu-id="939b2-164">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IBareMetalNodeDescription</span></span>

### <span data-ttu-id="939b2-165">Microsoft. Azure. PowerShell. polecenia. FabricAdmin. models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="939b2-165">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="939b2-166">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="939b2-166">OUTPUTS</span></span>

### <span data-ttu-id="939b2-167">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="939b2-167">System.Boolean</span></span>



## <span data-ttu-id="939b2-168">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="939b2-168">NOTES</span></span>

<span data-ttu-id="939b2-169">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="939b2-169">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="939b2-170">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="939b2-170">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="939b2-171">BAREMETALNODE <IBareMetalNodeDescription> : parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="939b2-171">BAREMETALNODE <IBareMetalNodeDescription>: Identity Parameter</span></span>
  - <span data-ttu-id="939b2-172">`[BiosVersion <String>]`: Wersja systemu BIOS komputera fizycznego.</span><span class="sxs-lookup"><span data-stu-id="939b2-172">`[BiosVersion <String>]`: Bios version of the physical machine.</span></span>
  - <span data-ttu-id="939b2-173">`[BmciPv4Address <String>]`: Adres BMC komputera fizycznego.</span><span class="sxs-lookup"><span data-stu-id="939b2-173">`[BmciPv4Address <String>]`: BMC address of the physical machine.</span></span>
  - <span data-ttu-id="939b2-174">`[ClusterName <String>]`: Nazwa klastra.</span><span class="sxs-lookup"><span data-stu-id="939b2-174">`[ClusterName <String>]`: Name of the cluster.</span></span>
  - <span data-ttu-id="939b2-175">`[ComputerName <String>]`: Nazwa komputera.</span><span class="sxs-lookup"><span data-stu-id="939b2-175">`[ComputerName <String>]`: Name of the computer.</span></span>
  - <span data-ttu-id="939b2-176">`[MacAddress <String>]`: Nazwa adresu MAC węzła systemu operacyjnego z niemetalową wersją.</span><span class="sxs-lookup"><span data-stu-id="939b2-176">`[MacAddress <String>]`: Name of the MAC address of the bare metal node.</span></span>
  - <span data-ttu-id="939b2-177">`[Model <String>]`: Model maszyny fizycznej.</span><span class="sxs-lookup"><span data-stu-id="939b2-177">`[Model <String>]`: Model of the physical machine.</span></span>
  - <span data-ttu-id="939b2-178">`[SerialNumber <String>]`: Numer seryjny maszyny fizycznej.</span><span class="sxs-lookup"><span data-stu-id="939b2-178">`[SerialNumber <String>]`: Serial number of the physical machine.</span></span>
  - <span data-ttu-id="939b2-179">`[Vendor <String>]`: Dostawca komputera fizycznego.</span><span class="sxs-lookup"><span data-stu-id="939b2-179">`[Vendor <String>]`: Vendor of the physical machine.</span></span>

<span data-ttu-id="939b2-180">INPUTobject <IFabricAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="939b2-180">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="939b2-181">`[Drive <String>]`: Nazwa dysku magazynu.</span><span class="sxs-lookup"><span data-stu-id="939b2-181">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="939b2-182">`[EdgeGateway <String>]`: Nazwa bramy granicznej.</span><span class="sxs-lookup"><span data-stu-id="939b2-182">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="939b2-183">`[EdgeGatewayPool <String>]`: Nazwa puli bramy brzegowej.</span><span class="sxs-lookup"><span data-stu-id="939b2-183">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="939b2-184">`[FabricLocation <String>]`: Lokalizacja sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="939b2-184">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="939b2-185">`[FileShare <String>]`: Nazwa udziału plików w sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="939b2-185">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="939b2-186">`[IPPool <String>]`: Nazwa puli adresów IP.</span><span class="sxs-lookup"><span data-stu-id="939b2-186">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="939b2-187">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="939b2-187">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="939b2-188">`[InfraRole <String>]`: Nazwa roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="939b2-188">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="939b2-189">`[InfraRoleInstance <String>]`: Nazwa wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="939b2-189">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="939b2-190">`[Location <String>]`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="939b2-190">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="939b2-191">`[LogicalNetwork <String>]`: Nazwa sieci logicznej.</span><span class="sxs-lookup"><span data-stu-id="939b2-191">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="939b2-192">`[LogicalSubnet <String>]`: Nazwa podsieci logicznej.</span><span class="sxs-lookup"><span data-stu-id="939b2-192">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="939b2-193">`[MacAddressPool <String>]`: Nazwa puli adresów MAC.</span><span class="sxs-lookup"><span data-stu-id="939b2-193">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="939b2-194">`[Operation <String>]`: Identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="939b2-194">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="939b2-195">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="939b2-195">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="939b2-196">`[ScaleUnit <String>]`: Nazwa jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="939b2-196">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="939b2-197">`[ScaleUnitNode <String>]`: Nazwa węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="939b2-197">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="939b2-198">`[SlbMuxInstance <String>]`: Nazwa wystąpienia MULTIPLEKSERa modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="939b2-198">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="939b2-199">`[StoragePool <String>]`: Nazwa puli magazynu.</span><span class="sxs-lookup"><span data-stu-id="939b2-199">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="939b2-200">`[StorageSubSystem <String>]`: Nazwa systemu przechowywania.</span><span class="sxs-lookup"><span data-stu-id="939b2-200">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="939b2-201">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="939b2-201">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="939b2-202">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="939b2-202">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="939b2-203">`[Volume <String>]`: Nazwa woluminu magazynu.</span><span class="sxs-lookup"><span data-stu-id="939b2-203">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="939b2-204">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="939b2-204">RELATED LINKS</span></span>

