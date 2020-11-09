---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/update-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Update-AzVMWareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Update-AzVMWareCluster.md
ms.openlocfilehash: b8e1f819c01edac24ff23c629de130036442c9e5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316825"
---
# <span data-ttu-id="9a673-101">Update-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="9a673-101">Update-AzVMWareCluster</span></span>

## <span data-ttu-id="9a673-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9a673-102">SYNOPSIS</span></span>
<span data-ttu-id="9a673-103">Aktualizowanie klastra w prywatnej chmurze</span><span class="sxs-lookup"><span data-stu-id="9a673-103">Update a cluster in a private cloud</span></span>

## <span data-ttu-id="9a673-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9a673-104">SYNTAX</span></span>

### <span data-ttu-id="9a673-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9a673-105">UpdateExpanded (Default)</span></span>
```
Update-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClusterSize <Int32>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9a673-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="9a673-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzVMWareCluster -InputObject <IVMWareIdentity> [-ClusterSize <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9a673-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9a673-107">DESCRIPTION</span></span>
<span data-ttu-id="9a673-108">Aktualizowanie klastra w prywatnej chmurze</span><span class="sxs-lookup"><span data-stu-id="9a673-108">Update a cluster in a private cloud</span></span>

## <span data-ttu-id="9a673-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9a673-109">EXAMPLES</span></span>

### <span data-ttu-id="9a673-110">Przykład 1: aktualizowanie rozmiaru klastra według nazwy</span><span class="sxs-lookup"><span data-stu-id="9a673-110">Example 1: Update cluster size by name</span></span>
```powershell
PS C:\> Update-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group -ClusterSize 4

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="9a673-111">Aktualizowanie rozmiaru klastra według nazwy</span><span class="sxs-lookup"><span data-stu-id="9a673-111">Update cluster size by name</span></span>

### <span data-ttu-id="9a673-112">Przykład 2: aktualizowanie rozmiaru klastra według obiektu wejścia</span><span class="sxs-lookup"><span data-stu-id="9a673-112">Example 2: Update cluster size by input object</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group | Update-AzVMWareCluster -ClusterSize 4

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="9a673-113">Aktualizowanie rozmiaru klastra według obiektu wejścia</span><span class="sxs-lookup"><span data-stu-id="9a673-113">Update cluster size by input object</span></span>

## <span data-ttu-id="9a673-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9a673-114">PARAMETERS</span></span>

### <span data-ttu-id="9a673-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9a673-115">-AsJob</span></span>
<span data-ttu-id="9a673-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="9a673-116">Run the command as a job</span></span>

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

### <span data-ttu-id="9a673-117">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="9a673-117">-ClusterSize</span></span>
<span data-ttu-id="9a673-118">Rozmiar klastra</span><span class="sxs-lookup"><span data-stu-id="9a673-118">The cluster size</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a673-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a673-119">-DefaultProfile</span></span>
<span data-ttu-id="9a673-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9a673-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a673-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9a673-121">-InputObject</span></span>
<span data-ttu-id="9a673-122">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="9a673-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a673-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9a673-123">-Name</span></span>
<span data-ttu-id="9a673-124">Nazwa klastra w prywatnej chmurze</span><span class="sxs-lookup"><span data-stu-id="9a673-124">Name of the cluster in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a673-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="9a673-125">-NoWait</span></span>
<span data-ttu-id="9a673-126">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="9a673-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9a673-127">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="9a673-127">-PrivateCloudName</span></span>
<span data-ttu-id="9a673-128">Nazwa prywatnej chmury</span><span class="sxs-lookup"><span data-stu-id="9a673-128">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a673-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a673-129">-ResourceGroupName</span></span>
<span data-ttu-id="9a673-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9a673-130">The name of the resource group.</span></span>
<span data-ttu-id="9a673-131">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="9a673-131">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a673-132">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="9a673-132">-SubscriptionId</span></span>
<span data-ttu-id="9a673-133">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="9a673-133">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a673-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9a673-134">-Confirm</span></span>
<span data-ttu-id="9a673-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a673-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a673-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a673-136">-WhatIf</span></span>
<span data-ttu-id="9a673-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a673-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a673-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9a673-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a673-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a673-139">CommonParameters</span></span>
<span data-ttu-id="9a673-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a673-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a673-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9a673-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a673-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9a673-142">INPUTS</span></span>

### <span data-ttu-id="9a673-143">Microsoft. Azure. PowerShell. cmdlets. VMWare. modele. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="9a673-143">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="9a673-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9a673-144">OUTPUTS</span></span>

### <span data-ttu-id="9a673-145">Microsoft. Azure. PowerShell. cmdlet. VMWare. modele. Api20200320. ICluster</span><span class="sxs-lookup"><span data-stu-id="9a673-145">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="9a673-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9a673-146">NOTES</span></span>

<span data-ttu-id="9a673-147">PISUJE</span><span class="sxs-lookup"><span data-stu-id="9a673-147">ALIASES</span></span>

<span data-ttu-id="9a673-148">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9a673-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9a673-149">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="9a673-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9a673-150">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9a673-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9a673-151">INPUTobject <IVMWareIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="9a673-151">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9a673-152">`[AuthorizationName <String>]`: Nazwa autoryzacji obwodu ExpressRoute w prywatnej chmurze</span><span class="sxs-lookup"><span data-stu-id="9a673-152">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="9a673-153">`[ClusterName <String>]`: Nazwa klastra w prywatnej chmurze</span><span class="sxs-lookup"><span data-stu-id="9a673-153">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="9a673-154">`[HcxEnterpriseSiteName <String>]`: Nazwa witryny usługi HCX Enterprise w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="9a673-154">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="9a673-155">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="9a673-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9a673-156">`[Location <String>]`: Region platformy Azure</span><span class="sxs-lookup"><span data-stu-id="9a673-156">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="9a673-157">`[PrivateCloudName <String>]`: Nazwa chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="9a673-157">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="9a673-158">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9a673-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="9a673-159">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="9a673-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="9a673-160">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="9a673-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="9a673-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9a673-161">RELATED LINKS</span></span>

