---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/add-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: 4546be57a2a2bd7f3f450290be2e0bf144e09817
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893998"
---
# <span data-ttu-id="b3161-101">Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="b3161-101">Add-AzsScaleUnitNode</span></span>

## <span data-ttu-id="b3161-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b3161-102">SYNOPSIS</span></span>
<span data-ttu-id="b3161-103">Skalować jednostkę skali.</span><span class="sxs-lookup"><span data-stu-id="b3161-103">Scales out a scale unit.</span></span>

## <span data-ttu-id="b3161-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b3161-104">SYNTAX</span></span>

### <span data-ttu-id="b3161-105">ScaleExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b3161-105">ScaleExpanded (Default)</span></span>
```
Add-AzsScaleUnitNode -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-AwaitStorageConvergence] [-NodeList <IScaleOutScaleUnitParameters[]>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b3161-106">Skali</span><span class="sxs-lookup"><span data-stu-id="b3161-106">Scale</span></span>
```
Add-AzsScaleUnitNode -ScaleUnit <String> -ScaleUnitNodeParameter <IScaleOutScaleUnitParametersList>
 [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b3161-107">ScaleViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b3161-107">ScaleViaIdentity</span></span>
```
Add-AzsScaleUnitNode -InputObject <IFabricAdminIdentity>
 -ScaleUnitNodeParameter <IScaleOutScaleUnitParametersList> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b3161-108">ScaleViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b3161-108">ScaleViaIdentityExpanded</span></span>
```
Add-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-AwaitStorageConvergence]
 [-NodeList <IScaleOutScaleUnitParameters[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b3161-109">Opis</span><span class="sxs-lookup"><span data-stu-id="b3161-109">DESCRIPTION</span></span>
<span data-ttu-id="b3161-110">Skalować jednostkę skali.</span><span class="sxs-lookup"><span data-stu-id="b3161-110">Scales out a scale unit.</span></span>

## <span data-ttu-id="b3161-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b3161-111">EXAMPLES</span></span>

### <span data-ttu-id="b3161-112">Przykład 1: Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="b3161-112">Example 1: Add-AzsScaleUnitNode</span></span>
```powershell
PS C:\> Add-AzsScaleUnitNode -NodeList $Nodes -ScaleUnit $ScaleUnitName

Adds a list of nodes to the scale unit.
```

<span data-ttu-id="b3161-113">Dodaj nowy węzeł jednostka skali do klastra jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="b3161-113">Add a new scale unit node to your scale unit cluster.</span></span>

## <span data-ttu-id="b3161-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b3161-114">PARAMETERS</span></span>

### <span data-ttu-id="b3161-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b3161-115">-AsJob</span></span>
<span data-ttu-id="b3161-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="b3161-116">Run the command as a job</span></span>

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

### <span data-ttu-id="b3161-117">-AwaitStorageConvergence</span><span class="sxs-lookup"><span data-stu-id="b3161-117">-AwaitStorageConvergence</span></span>
<span data-ttu-id="b3161-118">Flaga wskazuje, czy operacja powinna czekać na odłączenie miejsca do magazynowania przed powrotem.</span><span class="sxs-lookup"><span data-stu-id="b3161-118">Flag indicates if the operation should wait for storage to converge before returning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ScaleExpanded, ScaleViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b3161-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3161-119">-DefaultProfile</span></span>
<span data-ttu-id="b3161-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b3161-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3161-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b3161-121">-InputObject</span></span>
<span data-ttu-id="b3161-122">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="b3161-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: ScaleViaIdentity, ScaleViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="b3161-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b3161-123">-Location</span></span>
<span data-ttu-id="b3161-124">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="b3161-124">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Scale, ScaleExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b3161-125">-NodeList</span><span class="sxs-lookup"><span data-stu-id="b3161-125">-NodeList</span></span>
<span data-ttu-id="b3161-126">Lista węzłów w jednostkach skali.</span><span class="sxs-lookup"><span data-stu-id="b3161-126">List of nodes in the scale unit.</span></span>
<span data-ttu-id="b3161-127">Aby skonstruować, zobacz sekcję notatki dla właściwości NODELIST i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="b3161-127">To construct, see NOTES section for NODELIST properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleOutScaleUnitParameters[]
Parameter Sets: ScaleExpanded, ScaleViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b3161-128">-Nowait</span><span class="sxs-lookup"><span data-stu-id="b3161-128">-NoWait</span></span>
<span data-ttu-id="b3161-129">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="b3161-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b3161-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b3161-130">-PassThru</span></span>
<span data-ttu-id="b3161-131">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="b3161-131">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b3161-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3161-132">-ResourceGroupName</span></span>
<span data-ttu-id="b3161-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b3161-133">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Scale, ScaleExpanded
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b3161-134">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="b3161-134">-ScaleUnit</span></span>
<span data-ttu-id="b3161-135">Nazwa jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="b3161-135">Name of the scale units.</span></span>

```yaml
Type: System.String
Parameter Sets: Scale, ScaleExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b3161-136">-ScaleUnitNodeParameter</span><span class="sxs-lookup"><span data-stu-id="b3161-136">-ScaleUnitNodeParameter</span></span>
<span data-ttu-id="b3161-137">Lista danych wejściowych umożliwiających dodanie zestawu węzłów jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="b3161-137">A list of input data that allows for adding a set of scale unit nodes.</span></span>
<span data-ttu-id="b3161-138">Aby skonstruować, zobacz sekcję notatki dla właściwości SCALEUNITNODEPARAMETER i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="b3161-138">To construct, see NOTES section for SCALEUNITNODEPARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleOutScaleUnitParametersList
Parameter Sets: Scale, ScaleViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="b3161-139">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="b3161-139">-SubscriptionId</span></span>
<span data-ttu-id="b3161-140">Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b3161-140">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b3161-141">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="b3161-141">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Scale, ScaleExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b3161-142">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b3161-142">-Confirm</span></span>
<span data-ttu-id="b3161-143">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3161-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3161-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3161-144">-WhatIf</span></span>
<span data-ttu-id="b3161-145">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3161-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3161-146">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b3161-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3161-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3161-147">CommonParameters</span></span>
<span data-ttu-id="b3161-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3161-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3161-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3161-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3161-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b3161-150">INPUTS</span></span>

### <span data-ttu-id="b3161-151">Microsoft. Azure. PowerShell. polecenia. FabricAdmin. models. Api20160501. IScaleOutScaleUnitParametersList</span><span class="sxs-lookup"><span data-stu-id="b3161-151">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleOutScaleUnitParametersList</span></span>

### <span data-ttu-id="b3161-152">Microsoft. Azure. PowerShell. polecenia. FabricAdmin. models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="b3161-152">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="b3161-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b3161-153">OUTPUTS</span></span>

### <span data-ttu-id="b3161-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b3161-154">System.Boolean</span></span>



## <span data-ttu-id="b3161-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b3161-155">NOTES</span></span>

<span data-ttu-id="b3161-156">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="b3161-156">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b3161-157">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b3161-157">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="b3161-158">INPUTobject <IFabricAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="b3161-158">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b3161-159">`[Drive <String>]`: Nazwa dysku magazynu.</span><span class="sxs-lookup"><span data-stu-id="b3161-159">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="b3161-160">`[EdgeGateway <String>]`: Nazwa bramy granicznej.</span><span class="sxs-lookup"><span data-stu-id="b3161-160">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="b3161-161">`[EdgeGatewayPool <String>]`: Nazwa puli bramy brzegowej.</span><span class="sxs-lookup"><span data-stu-id="b3161-161">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="b3161-162">`[FabricLocation <String>]`: Lokalizacja sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="b3161-162">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="b3161-163">`[FileShare <String>]`: Nazwa udziału plików w sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="b3161-163">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="b3161-164">`[IPPool <String>]`: Nazwa puli adresów IP.</span><span class="sxs-lookup"><span data-stu-id="b3161-164">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="b3161-165">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="b3161-165">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b3161-166">`[InfraRole <String>]`: Nazwa roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="b3161-166">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="b3161-167">`[InfraRoleInstance <String>]`: Nazwa wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="b3161-167">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="b3161-168">`[Location <String>]`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="b3161-168">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="b3161-169">`[LogicalNetwork <String>]`: Nazwa sieci logicznej.</span><span class="sxs-lookup"><span data-stu-id="b3161-169">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="b3161-170">`[LogicalSubnet <String>]`: Nazwa podsieci logicznej.</span><span class="sxs-lookup"><span data-stu-id="b3161-170">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="b3161-171">`[MacAddressPool <String>]`: Nazwa puli adresów MAC.</span><span class="sxs-lookup"><span data-stu-id="b3161-171">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="b3161-172">`[Operation <String>]`: Identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="b3161-172">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="b3161-173">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b3161-173">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="b3161-174">`[ScaleUnit <String>]`: Nazwa jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="b3161-174">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="b3161-175">`[ScaleUnitNode <String>]`: Nazwa węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="b3161-175">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="b3161-176">`[SlbMuxInstance <String>]`: Nazwa wystąpienia MULTIPLEKSERa modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="b3161-176">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="b3161-177">`[StorageSubSystem <String>]`: Nazwa systemu przechowywania.</span><span class="sxs-lookup"><span data-stu-id="b3161-177">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="b3161-178">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b3161-178">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b3161-179">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="b3161-179">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="b3161-180">`[Volume <String>]`: Nazwa woluminu magazynu.</span><span class="sxs-lookup"><span data-stu-id="b3161-180">`[Volume <String>]`: Name of the storage volume.</span></span>

<span data-ttu-id="b3161-181">NODELIST <IScaleOutScaleUnitParameters [] >: lista węzłów w jednostkach skali.</span><span class="sxs-lookup"><span data-stu-id="b3161-181">NODELIST <IScaleOutScaleUnitParameters[]>: List of nodes in the scale unit.</span></span>
  - <span data-ttu-id="b3161-182">`[BmciPv4Address <String>]`: Adres BMC komputera fizycznego.</span><span class="sxs-lookup"><span data-stu-id="b3161-182">`[BmciPv4Address <String>]`: BMC address of the physical machine.</span></span>
  - <span data-ttu-id="b3161-183">`[ComputerName <String>]`: Nazwa komputera fizycznego.</span><span class="sxs-lookup"><span data-stu-id="b3161-183">`[ComputerName <String>]`: Computer name of the physical machine.</span></span>

<span data-ttu-id="b3161-184">SCALEUNITNODEPARAMETER <IScaleOutScaleUnitParametersList> : Lista danych wejściowych umożliwiających dodanie zestawu węzłów jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="b3161-184">SCALEUNITNODEPARAMETER <IScaleOutScaleUnitParametersList>: A list of input data that allows for adding a set of scale unit nodes.</span></span>
  - <span data-ttu-id="b3161-185">`[AwaitStorageConvergence <Boolean?>]`: Flaga wskazuje, czy operacja powinna czekać na odłączenie miejsca do magazynowania przed powrotem.</span><span class="sxs-lookup"><span data-stu-id="b3161-185">`[AwaitStorageConvergence <Boolean?>]`: Flag indicates if the operation should wait for storage to converge before returning.</span></span>
  - <span data-ttu-id="b3161-186">`[NodeList <IScaleOutScaleUnitParameters[]>]`: Lista węzłów w jednostkach skali.</span><span class="sxs-lookup"><span data-stu-id="b3161-186">`[NodeList <IScaleOutScaleUnitParameters[]>]`: List of nodes in the scale unit.</span></span>
    - <span data-ttu-id="b3161-187">`[BmciPv4Address <String>]`: Adres BMC komputera fizycznego.</span><span class="sxs-lookup"><span data-stu-id="b3161-187">`[BmciPv4Address <String>]`: BMC address of the physical machine.</span></span>
    - <span data-ttu-id="b3161-188">`[ComputerName <String>]`: Nazwa komputera fizycznego.</span><span class="sxs-lookup"><span data-stu-id="b3161-188">`[ComputerName <String>]`: Computer name of the physical machine.</span></span>

## <span data-ttu-id="b3161-189">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b3161-189">RELATED LINKS</span></span>

