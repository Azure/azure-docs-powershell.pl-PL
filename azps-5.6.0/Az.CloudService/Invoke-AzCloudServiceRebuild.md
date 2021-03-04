---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/invoke-azcloudservicerebuild
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceRebuild.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceRebuild.md
ms.openlocfilehash: aa9f128021aba1dff08f1c8757c8135676ddc003
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975930"
---
# <span data-ttu-id="e552a-101">Invoke-AzCloudServiceRebuild</span><span class="sxs-lookup"><span data-stu-id="e552a-101">Invoke-AzCloudServiceRebuild</span></span>

## <span data-ttu-id="e552a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e552a-102">SYNOPSIS</span></span>
<span data-ttu-id="e552a-103">Odbudowanie wystąpień ról ponownie instaluje system operacyjny w wystąpieniach ról sieci Web lub ról pracowników i inicjuje używane przez nich zasoby magazynu.</span><span class="sxs-lookup"><span data-stu-id="e552a-103">Rebuild Role Instances reinstalls the operating system on instances of web roles or worker roles and initializes the storage resources that are used by them.</span></span>
<span data-ttu-id="e552a-104">Jeśli nie chcesz inicjować zasobów magazynu, możesz użyć wystąpienia ról w celu ponownego zainicjowania.</span><span class="sxs-lookup"><span data-stu-id="e552a-104">If you do not want to initialize storage resources, you can use Reimage Role Instances.</span></span>

## <span data-ttu-id="e552a-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e552a-105">SYNTAX</span></span>

### <span data-ttu-id="e552a-106">RebuildExpanded (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="e552a-106">RebuildExpanded (Default)</span></span>
```
Invoke-AzCloudServiceRebuild -CloudServiceName <String> -ResourceGroupName <String> -RoleInstance <String[]>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="e552a-107">RebuildViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e552a-107">RebuildViaIdentityExpanded</span></span>
```
Invoke-AzCloudServiceRebuild -InputObject <ICloudServiceIdentity> -RoleInstance <String[]>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e552a-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="e552a-108">DESCRIPTION</span></span>
<span data-ttu-id="e552a-109">Odbudowanie wystąpień ról ponownie instaluje system operacyjny w wystąpieniach ról sieci Web lub ról pracowników i inicjuje używane przez nich zasoby magazynu.</span><span class="sxs-lookup"><span data-stu-id="e552a-109">Rebuild Role Instances reinstalls the operating system on instances of web roles or worker roles and initializes the storage resources that are used by them.</span></span>
<span data-ttu-id="e552a-110">Jeśli nie chcesz inicjować zasobów magazynu, możesz użyć wystąpienia ról w celu ponownego zainicjowania.</span><span class="sxs-lookup"><span data-stu-id="e552a-110">If you do not want to initialize storage resources, you can use Reimage Role Instances.</span></span>

## <span data-ttu-id="e552a-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e552a-111">EXAMPLES</span></span>

### <span data-ttu-id="e552a-112">Przykład 1. Odbudowywanie wystąpień ról usługi w chmurze</span><span class="sxs-lookup"><span data-stu-id="e552a-112">Example 1: Rebuild role instances of cloud service</span></span>
```powershell
PS C:\> $roleInstances = @("ContosoFrontEnd_IN_0", "ContosoBackEnd_IN_1")
PS C:\> Invoke-AzCloudServiceRebuild -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance $roleInstances
```

<span data-ttu-id="e552a-113">To polecenie odbuduje 2 wystąpienia ról ContosoFrontEnd_IN_0 i ContosoBackEnd_IN_1 usługi w chmurze o nazwie ContosoCS, które należą do grupy zasobów o nazwie ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="e552a-113">This command rebuilds 2 role instances ContosoFrontEnd_IN_0 and ContosoBackEnd_IN_1 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="e552a-114">Przykład 2. Odbudowywanie wszystkich ról usługi w chmurze</span><span class="sxs-lookup"><span data-stu-id="e552a-114">Example 2: Rebuild all roles of cloud service</span></span>
```powershell
PS C:\> Invoke-AzCloudServiceRebuild -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance "*"
```

<span data-ttu-id="e552a-115">To polecenie odbuduje wszystkie wystąpienia ról usługi w chmurze o nazwie ContosoCS, które należą do grupy zasobów o nazwie ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="e552a-115">This command rebuilds all role instances of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="e552a-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e552a-116">PARAMETERS</span></span>

### <span data-ttu-id="e552a-117">— AsJob</span><span class="sxs-lookup"><span data-stu-id="e552a-117">-AsJob</span></span>
<span data-ttu-id="e552a-118">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="e552a-118">Run the command as a job</span></span>

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

### <span data-ttu-id="e552a-119">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="e552a-119">-CloudServiceName</span></span>
<span data-ttu-id="e552a-120">Nazwa usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="e552a-120">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: RebuildExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e552a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e552a-121">-DefaultProfile</span></span>
<span data-ttu-id="e552a-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e552a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e552a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e552a-123">-InputObject</span></span>
<span data-ttu-id="e552a-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="e552a-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: RebuildViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e552a-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e552a-125">-NoWait</span></span>
<span data-ttu-id="e552a-126">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="e552a-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e552a-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e552a-127">-PassThru</span></span>
<span data-ttu-id="e552a-128">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="e552a-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e552a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e552a-129">-ResourceGroupName</span></span>
<span data-ttu-id="e552a-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e552a-130">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RebuildExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e552a-131">-RoleInstance</span><span class="sxs-lookup"><span data-stu-id="e552a-131">-RoleInstance</span></span>
<span data-ttu-id="e552a-132">Lista nazw wystąpień ról usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="e552a-132">List of cloud service role instance names.</span></span>
<span data-ttu-id="e552a-133">Wartość "\*" oznacza wszystkie wystąpienia ról usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="e552a-133">Value of '\*' will signify all role instances of the cloud service.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e552a-134">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e552a-134">-SubscriptionId</span></span>
<span data-ttu-id="e552a-135">Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e552a-135">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e552a-136">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="e552a-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: RebuildExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e552a-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e552a-137">-Confirm</span></span>
<span data-ttu-id="e552a-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e552a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e552a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e552a-139">-WhatIf</span></span>
<span data-ttu-id="e552a-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e552a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e552a-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e552a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e552a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e552a-142">CommonParameters</span></span>
<span data-ttu-id="e552a-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e552a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e552a-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e552a-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e552a-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e552a-145">INPUTS</span></span>

### <span data-ttu-id="e552a-146">Microsoft.Azure.PowerShell.cmdlet.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="e552a-146">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="e552a-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e552a-147">OUTPUTS</span></span>

### <span data-ttu-id="e552a-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e552a-148">System.Boolean</span></span>

## <span data-ttu-id="e552a-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e552a-149">NOTES</span></span>

<span data-ttu-id="e552a-150">ALIASY</span><span class="sxs-lookup"><span data-stu-id="e552a-150">ALIASES</span></span>

<span data-ttu-id="e552a-151">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e552a-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e552a-152">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="e552a-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e552a-153">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e552a-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e552a-154">INPUTOBJECT: <ICloudServiceIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="e552a-154">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e552a-155">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="e552a-155">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="e552a-156">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="e552a-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e552a-157">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="e552a-157">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="e552a-158">`[RoleInstanceName <String>]`: nazwa wystąpienia roli.</span><span class="sxs-lookup"><span data-stu-id="e552a-158">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="e552a-159">`[RoleName <String>]`: nazwa roli.</span><span class="sxs-lookup"><span data-stu-id="e552a-159">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="e552a-160">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e552a-160">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e552a-161">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="e552a-161">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="e552a-162">`[UpdateDomain <Int32?>]`: określa wartość całkowitą identyfikującą domenę aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="e552a-162">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="e552a-163">Domeny aktualizacji są identyfikowane za pomocą indeksu opartego na zeru: pierwsza domena aktualizacji ma identyfikator 0, druga ma identyfikator 1 i tak dalej.</span><span class="sxs-lookup"><span data-stu-id="e552a-163">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="e552a-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e552a-164">RELATED LINKS</span></span>

