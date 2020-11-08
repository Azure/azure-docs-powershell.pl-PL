---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/remove-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWareCluster.md
ms.openlocfilehash: 936ed70f7040f9558db891b4e75299759c647bf9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94061910"
---
# <span data-ttu-id="2d177-101">Remove-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="2d177-101">Remove-AzVMWareCluster</span></span>

## <span data-ttu-id="2d177-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2d177-102">SYNOPSIS</span></span>
<span data-ttu-id="2d177-103">Usuwanie klastra w prywatnej chmurze</span><span class="sxs-lookup"><span data-stu-id="2d177-103">Delete a cluster in a private cloud</span></span>

## <span data-ttu-id="2d177-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2d177-104">SYNTAX</span></span>

### <span data-ttu-id="2d177-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="2d177-105">Delete (Default)</span></span>
```
Remove-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="2d177-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2d177-106">DeleteViaIdentity</span></span>
```
Remove-AzVMWareCluster -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2d177-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2d177-107">DESCRIPTION</span></span>
<span data-ttu-id="2d177-108">Usuwanie klastra w prywatnej chmurze</span><span class="sxs-lookup"><span data-stu-id="2d177-108">Delete a cluster in a private cloud</span></span>

## <span data-ttu-id="2d177-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2d177-109">EXAMPLES</span></span>

### <span data-ttu-id="2d177-110">Przykład 1: usuwanie klastra w prywatnej chmurze</span><span class="sxs-lookup"><span data-stu-id="2d177-110">Example 1: Delete cluster in private cloud</span></span>
```powershell
PS C:\> Remove-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

```

<span data-ttu-id="2d177-111">Usuwanie klastra w prywatnej chmurze</span><span class="sxs-lookup"><span data-stu-id="2d177-111">Delete cluster in private cloud</span></span>

## <span data-ttu-id="2d177-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2d177-112">PARAMETERS</span></span>

### <span data-ttu-id="2d177-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d177-113">-AsJob</span></span>
<span data-ttu-id="2d177-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="2d177-114">Run the command as a job</span></span>

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

### <span data-ttu-id="2d177-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d177-115">-DefaultProfile</span></span>
<span data-ttu-id="2d177-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2d177-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d177-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2d177-117">-InputObject</span></span>
<span data-ttu-id="2d177-118">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="2d177-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2d177-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2d177-119">-Name</span></span>
<span data-ttu-id="2d177-120">Nazwa klastra w prywatnej chmurze</span><span class="sxs-lookup"><span data-stu-id="2d177-120">Name of the cluster in the private cloud</span></span>

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

### <span data-ttu-id="2d177-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="2d177-121">-NoWait</span></span>
<span data-ttu-id="2d177-122">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="2d177-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2d177-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d177-123">-PassThru</span></span>
<span data-ttu-id="2d177-124">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="2d177-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2d177-125">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="2d177-125">-PrivateCloudName</span></span>
<span data-ttu-id="2d177-126">Nazwa prywatnej chmury</span><span class="sxs-lookup"><span data-stu-id="2d177-126">Name of the private cloud</span></span>

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

### <span data-ttu-id="2d177-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d177-127">-ResourceGroupName</span></span>
<span data-ttu-id="2d177-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2d177-128">The name of the resource group.</span></span>
<span data-ttu-id="2d177-129">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="2d177-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="2d177-130">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="2d177-130">-SubscriptionId</span></span>
<span data-ttu-id="2d177-131">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="2d177-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="2d177-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2d177-132">-Confirm</span></span>
<span data-ttu-id="2d177-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d177-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d177-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d177-134">-WhatIf</span></span>
<span data-ttu-id="2d177-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d177-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d177-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2d177-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d177-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d177-137">CommonParameters</span></span>
<span data-ttu-id="2d177-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d177-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d177-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2d177-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d177-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2d177-140">INPUTS</span></span>

### <span data-ttu-id="2d177-141">Microsoft. Azure. PowerShell. cmdlets. VMWare. modele. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="2d177-141">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="2d177-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2d177-142">OUTPUTS</span></span>

### <span data-ttu-id="2d177-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2d177-143">System.Boolean</span></span>

## <span data-ttu-id="2d177-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2d177-144">NOTES</span></span>

<span data-ttu-id="2d177-145">PISUJE</span><span class="sxs-lookup"><span data-stu-id="2d177-145">ALIASES</span></span>

<span data-ttu-id="2d177-146">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2d177-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2d177-147">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="2d177-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2d177-148">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2d177-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2d177-149">INPUTobject <IVMWareIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="2d177-149">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2d177-150">`[AuthorizationName <String>]`: Nazwa autoryzacji obwodu ExpressRoute w prywatnej chmurze</span><span class="sxs-lookup"><span data-stu-id="2d177-150">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="2d177-151">`[ClusterName <String>]`: Nazwa klastra w prywatnej chmurze</span><span class="sxs-lookup"><span data-stu-id="2d177-151">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="2d177-152">`[HcxEnterpriseSiteName <String>]`: Nazwa witryny usługi HCX Enterprise w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="2d177-152">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="2d177-153">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="2d177-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2d177-154">`[Location <String>]`: Region platformy Azure</span><span class="sxs-lookup"><span data-stu-id="2d177-154">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="2d177-155">`[PrivateCloudName <String>]`: Nazwa chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="2d177-155">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="2d177-156">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2d177-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="2d177-157">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="2d177-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="2d177-158">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="2d177-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="2d177-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2d177-159">RELATED LINKS</span></span>

