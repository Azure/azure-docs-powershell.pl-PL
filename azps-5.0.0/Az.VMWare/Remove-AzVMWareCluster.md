---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/remove-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWareCluster.md
ms.openlocfilehash: 936ed70f7040f9558db891b4e75299759c647bf9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316830"
---
# <span data-ttu-id="41676-101">Remove-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="41676-101">Remove-AzVMWareCluster</span></span>

## <span data-ttu-id="41676-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="41676-102">SYNOPSIS</span></span>
<span data-ttu-id="41676-103">Usuwanie klastra w prywatnej chmurze</span><span class="sxs-lookup"><span data-stu-id="41676-103">Delete a cluster in a private cloud</span></span>

## <span data-ttu-id="41676-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="41676-104">SYNTAX</span></span>

### <span data-ttu-id="41676-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="41676-105">Delete (Default)</span></span>
```
Remove-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="41676-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="41676-106">DeleteViaIdentity</span></span>
```
Remove-AzVMWareCluster -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="41676-107">Opis</span><span class="sxs-lookup"><span data-stu-id="41676-107">DESCRIPTION</span></span>
<span data-ttu-id="41676-108">Usuwanie klastra w prywatnej chmurze</span><span class="sxs-lookup"><span data-stu-id="41676-108">Delete a cluster in a private cloud</span></span>

## <span data-ttu-id="41676-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="41676-109">EXAMPLES</span></span>

### <span data-ttu-id="41676-110">Przykład 1: usuwanie klastra w prywatnej chmurze</span><span class="sxs-lookup"><span data-stu-id="41676-110">Example 1: Delete cluster in private cloud</span></span>
```powershell
PS C:\> Remove-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

```

<span data-ttu-id="41676-111">Usuwanie klastra w prywatnej chmurze</span><span class="sxs-lookup"><span data-stu-id="41676-111">Delete cluster in private cloud</span></span>

## <span data-ttu-id="41676-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="41676-112">PARAMETERS</span></span>

### <span data-ttu-id="41676-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41676-113">-AsJob</span></span>
<span data-ttu-id="41676-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="41676-114">Run the command as a job</span></span>

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

### <span data-ttu-id="41676-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41676-115">-DefaultProfile</span></span>
<span data-ttu-id="41676-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="41676-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41676-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="41676-117">-InputObject</span></span>
<span data-ttu-id="41676-118">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="41676-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41676-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="41676-119">-Name</span></span>
<span data-ttu-id="41676-120">Nazwa klastra w prywatnej chmurze</span><span class="sxs-lookup"><span data-stu-id="41676-120">Name of the cluster in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41676-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="41676-121">-NoWait</span></span>
<span data-ttu-id="41676-122">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="41676-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="41676-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="41676-123">-PassThru</span></span>
<span data-ttu-id="41676-124">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="41676-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="41676-125">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="41676-125">-PrivateCloudName</span></span>
<span data-ttu-id="41676-126">Nazwa prywatnej chmury</span><span class="sxs-lookup"><span data-stu-id="41676-126">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41676-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41676-127">-ResourceGroupName</span></span>
<span data-ttu-id="41676-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="41676-128">The name of the resource group.</span></span>
<span data-ttu-id="41676-129">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="41676-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41676-130">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="41676-130">-SubscriptionId</span></span>
<span data-ttu-id="41676-131">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="41676-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41676-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="41676-132">-Confirm</span></span>
<span data-ttu-id="41676-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41676-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41676-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41676-134">-WhatIf</span></span>
<span data-ttu-id="41676-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41676-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41676-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="41676-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41676-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41676-137">CommonParameters</span></span>
<span data-ttu-id="41676-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41676-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41676-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="41676-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41676-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="41676-140">INPUTS</span></span>

### <span data-ttu-id="41676-141">Microsoft. Azure. PowerShell. cmdlets. VMWare. modele. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="41676-141">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="41676-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="41676-142">OUTPUTS</span></span>

### <span data-ttu-id="41676-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="41676-143">System.Boolean</span></span>

## <span data-ttu-id="41676-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="41676-144">NOTES</span></span>

<span data-ttu-id="41676-145">PISUJE</span><span class="sxs-lookup"><span data-stu-id="41676-145">ALIASES</span></span>

<span data-ttu-id="41676-146">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="41676-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="41676-147">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="41676-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="41676-148">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="41676-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="41676-149">INPUTobject <IVMWareIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="41676-149">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="41676-150">`[AuthorizationName <String>]`: Nazwa autoryzacji obwodu ExpressRoute w prywatnej chmurze</span><span class="sxs-lookup"><span data-stu-id="41676-150">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="41676-151">`[ClusterName <String>]`: Nazwa klastra w prywatnej chmurze</span><span class="sxs-lookup"><span data-stu-id="41676-151">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="41676-152">`[HcxEnterpriseSiteName <String>]`: Nazwa witryny usługi HCX Enterprise w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="41676-152">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="41676-153">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="41676-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="41676-154">`[Location <String>]`: Region platformy Azure</span><span class="sxs-lookup"><span data-stu-id="41676-154">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="41676-155">`[PrivateCloudName <String>]`: Nazwa chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="41676-155">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="41676-156">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="41676-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="41676-157">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="41676-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="41676-158">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="41676-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="41676-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="41676-159">RELATED LINKS</span></span>

