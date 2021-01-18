---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/remove-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWarePrivateCloud.md
ms.openlocfilehash: accf225acfb05fdcaf49eb5dde4d1bae0332d300
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98498154"
---
# <span data-ttu-id="7baec-101">Remove-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="7baec-101">Remove-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="7baec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7baec-102">SYNOPSIS</span></span>
<span data-ttu-id="7baec-103">Usuwanie prywatnej chmury</span><span class="sxs-lookup"><span data-stu-id="7baec-103">Delete a private cloud</span></span>

## <span data-ttu-id="7baec-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7baec-104">SYNTAX</span></span>

### <span data-ttu-id="7baec-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="7baec-105">Delete (Default)</span></span>
```
Remove-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7baec-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7baec-106">DeleteViaIdentity</span></span>
```
Remove-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7baec-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7baec-107">DESCRIPTION</span></span>
<span data-ttu-id="7baec-108">Usuwanie prywatnej chmury</span><span class="sxs-lookup"><span data-stu-id="7baec-108">Delete a private cloud</span></span>

## <span data-ttu-id="7baec-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7baec-109">EXAMPLES</span></span>

### <span data-ttu-id="7baec-110">Przykład 1: usuwanie prywatnej chmury</span><span class="sxs-lookup"><span data-stu-id="7baec-110">Example 1: Delete private cloud</span></span>
```powershell
PS C:\> Remove-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud

```

<span data-ttu-id="7baec-111">Usuń chmurę prywatną</span><span class="sxs-lookup"><span data-stu-id="7baec-111">Delete private cloud</span></span>

## <span data-ttu-id="7baec-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7baec-112">PARAMETERS</span></span>

### <span data-ttu-id="7baec-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7baec-113">-AsJob</span></span>
<span data-ttu-id="7baec-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="7baec-114">Run the command as a job</span></span>

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

### <span data-ttu-id="7baec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7baec-115">-DefaultProfile</span></span>
<span data-ttu-id="7baec-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7baec-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7baec-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7baec-117">-InputObject</span></span>
<span data-ttu-id="7baec-118">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="7baec-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7baec-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7baec-119">-Name</span></span>
<span data-ttu-id="7baec-120">Nazwa prywatnej chmury</span><span class="sxs-lookup"><span data-stu-id="7baec-120">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7baec-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="7baec-121">-NoWait</span></span>
<span data-ttu-id="7baec-122">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="7baec-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7baec-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7baec-123">-PassThru</span></span>
<span data-ttu-id="7baec-124">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="7baec-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="7baec-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7baec-125">-ResourceGroupName</span></span>
<span data-ttu-id="7baec-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7baec-126">The name of the resource group.</span></span>
<span data-ttu-id="7baec-127">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="7baec-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="7baec-128">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="7baec-128">-SubscriptionId</span></span>
<span data-ttu-id="7baec-129">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="7baec-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="7baec-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7baec-130">-Confirm</span></span>
<span data-ttu-id="7baec-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7baec-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7baec-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7baec-132">-WhatIf</span></span>
<span data-ttu-id="7baec-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7baec-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7baec-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7baec-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7baec-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7baec-135">CommonParameters</span></span>
<span data-ttu-id="7baec-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7baec-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7baec-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7baec-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7baec-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7baec-138">INPUTS</span></span>

### <span data-ttu-id="7baec-139">Microsoft. Azure. PowerShell. cmdlets. VMWare. modele. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="7baec-139">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="7baec-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7baec-140">OUTPUTS</span></span>

### <span data-ttu-id="7baec-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7baec-141">System.Boolean</span></span>

## <span data-ttu-id="7baec-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7baec-142">NOTES</span></span>

<span data-ttu-id="7baec-143">PISUJE</span><span class="sxs-lookup"><span data-stu-id="7baec-143">ALIASES</span></span>

<span data-ttu-id="7baec-144">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7baec-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7baec-145">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="7baec-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7baec-146">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7baec-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7baec-147">INPUTobject <IVMWareIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="7baec-147">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7baec-148">`[AuthorizationName <String>]`: Nazwa autoryzacji obwodu ExpressRoute w prywatnej chmurze</span><span class="sxs-lookup"><span data-stu-id="7baec-148">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="7baec-149">`[ClusterName <String>]`: Nazwa klastra w prywatnej chmurze</span><span class="sxs-lookup"><span data-stu-id="7baec-149">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="7baec-150">`[HcxEnterpriseSiteName <String>]`: Nazwa witryny usługi HCX Enterprise w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="7baec-150">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="7baec-151">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="7baec-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7baec-152">`[Location <String>]`: Region platformy Azure</span><span class="sxs-lookup"><span data-stu-id="7baec-152">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="7baec-153">`[PrivateCloudName <String>]`: Nazwa chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="7baec-153">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="7baec-154">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7baec-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="7baec-155">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="7baec-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="7baec-156">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="7baec-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="7baec-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7baec-157">RELATED LINKS</span></span>

