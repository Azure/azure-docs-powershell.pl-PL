---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/remove-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWarePrivateCloud.md
ms.openlocfilehash: accf225acfb05fdcaf49eb5dde4d1bae0332d300
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345013"
---
# <span data-ttu-id="e8178-101">Remove-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="e8178-101">Remove-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="e8178-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e8178-102">SYNOPSIS</span></span>
<span data-ttu-id="e8178-103">Usuwanie prywatnej chmury</span><span class="sxs-lookup"><span data-stu-id="e8178-103">Delete a private cloud</span></span>

## <span data-ttu-id="e8178-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e8178-104">SYNTAX</span></span>

### <span data-ttu-id="e8178-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="e8178-105">Delete (Default)</span></span>
```
Remove-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e8178-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e8178-106">DeleteViaIdentity</span></span>
```
Remove-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e8178-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e8178-107">DESCRIPTION</span></span>
<span data-ttu-id="e8178-108">Usuwanie prywatnej chmury</span><span class="sxs-lookup"><span data-stu-id="e8178-108">Delete a private cloud</span></span>

## <span data-ttu-id="e8178-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e8178-109">EXAMPLES</span></span>

### <span data-ttu-id="e8178-110">Przykład 1: usuwanie prywatnej chmury</span><span class="sxs-lookup"><span data-stu-id="e8178-110">Example 1: Delete private cloud</span></span>
```powershell
PS C:\> Remove-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud

```

<span data-ttu-id="e8178-111">Usuń chmurę prywatną</span><span class="sxs-lookup"><span data-stu-id="e8178-111">Delete private cloud</span></span>

## <span data-ttu-id="e8178-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e8178-112">PARAMETERS</span></span>

### <span data-ttu-id="e8178-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e8178-113">-AsJob</span></span>
<span data-ttu-id="e8178-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="e8178-114">Run the command as a job</span></span>

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

### <span data-ttu-id="e8178-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8178-115">-DefaultProfile</span></span>
<span data-ttu-id="e8178-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e8178-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8178-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e8178-117">-InputObject</span></span>
<span data-ttu-id="e8178-118">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="e8178-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e8178-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e8178-119">-Name</span></span>
<span data-ttu-id="e8178-120">Nazwa prywatnej chmury</span><span class="sxs-lookup"><span data-stu-id="e8178-120">Name of the private cloud</span></span>

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

### <span data-ttu-id="e8178-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="e8178-121">-NoWait</span></span>
<span data-ttu-id="e8178-122">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="e8178-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e8178-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e8178-123">-PassThru</span></span>
<span data-ttu-id="e8178-124">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="e8178-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e8178-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8178-125">-ResourceGroupName</span></span>
<span data-ttu-id="e8178-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e8178-126">The name of the resource group.</span></span>
<span data-ttu-id="e8178-127">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="e8178-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e8178-128">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="e8178-128">-SubscriptionId</span></span>
<span data-ttu-id="e8178-129">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="e8178-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e8178-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e8178-130">-Confirm</span></span>
<span data-ttu-id="e8178-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8178-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8178-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8178-132">-WhatIf</span></span>
<span data-ttu-id="e8178-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8178-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8178-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e8178-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8178-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8178-135">CommonParameters</span></span>
<span data-ttu-id="e8178-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8178-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8178-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8178-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8178-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e8178-138">INPUTS</span></span>

### <span data-ttu-id="e8178-139">Microsoft. Azure. PowerShell. cmdlets. VMWare. modele. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="e8178-139">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="e8178-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e8178-140">OUTPUTS</span></span>

### <span data-ttu-id="e8178-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e8178-141">System.Boolean</span></span>

## <span data-ttu-id="e8178-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e8178-142">NOTES</span></span>

<span data-ttu-id="e8178-143">PISUJE</span><span class="sxs-lookup"><span data-stu-id="e8178-143">ALIASES</span></span>

<span data-ttu-id="e8178-144">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e8178-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e8178-145">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="e8178-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e8178-146">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e8178-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e8178-147">INPUTobject <IVMWareIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="e8178-147">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e8178-148">`[AuthorizationName <String>]`: Nazwa autoryzacji obwodu ExpressRoute w prywatnej chmurze</span><span class="sxs-lookup"><span data-stu-id="e8178-148">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="e8178-149">`[ClusterName <String>]`: Nazwa klastra w prywatnej chmurze</span><span class="sxs-lookup"><span data-stu-id="e8178-149">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="e8178-150">`[HcxEnterpriseSiteName <String>]`: Nazwa witryny usługi HCX Enterprise w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="e8178-150">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="e8178-151">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="e8178-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e8178-152">`[Location <String>]`: Region platformy Azure</span><span class="sxs-lookup"><span data-stu-id="e8178-152">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="e8178-153">`[PrivateCloudName <String>]`: Nazwa chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="e8178-153">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="e8178-154">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e8178-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e8178-155">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="e8178-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="e8178-156">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="e8178-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="e8178-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e8178-157">RELATED LINKS</span></span>

