---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/invoke-azcloudserviceroleinstancerebuild
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceRoleInstanceRebuild.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceRoleInstanceRebuild.md
ms.openlocfilehash: d998e29fc254b1bf507ab7d7732bc3bdcf68f54b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177811"
---
# <span data-ttu-id="31f03-101">Invoke-AzCloudServiceRoleInstanceRebuild</span><span class="sxs-lookup"><span data-stu-id="31f03-101">Invoke-AzCloudServiceRoleInstanceRebuild</span></span>

## <span data-ttu-id="31f03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31f03-102">SYNOPSIS</span></span>
<span data-ttu-id="31f03-103">Asynchroniczne działanie wystąpienia ról odbudowywania ponownie instaluje system operacyjny w wystąpieniach ról sieci Web lub ról pracowników i inicjuje używane przez nich zasoby magazynu.</span><span class="sxs-lookup"><span data-stu-id="31f03-103">The Rebuild Role Instance asynchronous operation reinstalls the operating system on instances of web roles or worker roles and initializes the storage resources that are used by them.</span></span>
<span data-ttu-id="31f03-104">Jeśli nie chcesz zainicjować zasobów magazynu, możesz użyć wystąpienia roli w celu ponownego zainicjowania.</span><span class="sxs-lookup"><span data-stu-id="31f03-104">If you do not want to initialize storage resources, you can use Reimage Role Instance.</span></span>

## <span data-ttu-id="31f03-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="31f03-105">SYNTAX</span></span>

### <span data-ttu-id="31f03-106">Odbudowywanie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="31f03-106">Rebuild (Default)</span></span>
```
Invoke-AzCloudServiceRoleInstanceRebuild -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="31f03-107">RebuildViaIdentity</span><span class="sxs-lookup"><span data-stu-id="31f03-107">RebuildViaIdentity</span></span>
```
Invoke-AzCloudServiceRoleInstanceRebuild -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="31f03-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="31f03-108">DESCRIPTION</span></span>
<span data-ttu-id="31f03-109">Asynchroniczne działanie wystąpienia ról odbudowywania ponownie instaluje system operacyjny w wystąpieniach ról sieci Web lub ról pracowników i inicjuje używane przez nich zasoby magazynu.</span><span class="sxs-lookup"><span data-stu-id="31f03-109">The Rebuild Role Instance asynchronous operation reinstalls the operating system on instances of web roles or worker roles and initializes the storage resources that are used by them.</span></span>
<span data-ttu-id="31f03-110">Jeśli nie chcesz zainicjować zasobów magazynu, możesz użyć wystąpienia roli w celu ponownego zainicjowania.</span><span class="sxs-lookup"><span data-stu-id="31f03-110">If you do not want to initialize storage resources, you can use Reimage Role Instance.</span></span>

## <span data-ttu-id="31f03-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="31f03-111">EXAMPLES</span></span>

### <span data-ttu-id="31f03-112">Przykład 1. Odbudowywanie wystąpienia roli usługi w chmurze</span><span class="sxs-lookup"><span data-stu-id="31f03-112">Example 1: Rebuild role instance of a cloud service</span></span>
```powershell
PS C:\> Invoke-AzCloudServiceRoleInstanceRebuild -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"
```

<span data-ttu-id="31f03-113">To polecenie pozwala ponownie zaimportować wystąpienie roli o nazwie ContosoFrontEnd_IN_0 o nazwie ContosoCS, która należy do grupy zasobów o nazwie ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="31f03-113">This command reimages role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="31f03-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31f03-114">PARAMETERS</span></span>

### <span data-ttu-id="31f03-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="31f03-115">-AsJob</span></span>
<span data-ttu-id="31f03-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="31f03-116">Run the command as a job</span></span>

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

### <span data-ttu-id="31f03-117">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="31f03-117">-CloudServiceName</span></span>
<span data-ttu-id="31f03-118">.</span><span class="sxs-lookup"><span data-stu-id="31f03-118">.</span></span>

```yaml
Type: System.String
Parameter Sets: Rebuild
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31f03-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31f03-119">-DefaultProfile</span></span>
<span data-ttu-id="31f03-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="31f03-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31f03-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31f03-121">-InputObject</span></span>
<span data-ttu-id="31f03-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="31f03-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: RebuildViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31f03-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="31f03-123">-NoWait</span></span>
<span data-ttu-id="31f03-124">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="31f03-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="31f03-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="31f03-125">-PassThru</span></span>
<span data-ttu-id="31f03-126">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="31f03-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="31f03-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31f03-127">-ResourceGroupName</span></span>
<span data-ttu-id="31f03-128">.</span><span class="sxs-lookup"><span data-stu-id="31f03-128">.</span></span>

```yaml
Type: System.String
Parameter Sets: Rebuild
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31f03-129">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="31f03-129">-RoleInstanceName</span></span>
<span data-ttu-id="31f03-130">Nazwa wystąpienia roli.</span><span class="sxs-lookup"><span data-stu-id="31f03-130">Name of the role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Rebuild
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31f03-131">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="31f03-131">-SubscriptionId</span></span>
<span data-ttu-id="31f03-132">Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="31f03-132">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="31f03-133">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="31f03-133">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Rebuild
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31f03-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="31f03-134">-Confirm</span></span>
<span data-ttu-id="31f03-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="31f03-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31f03-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31f03-136">-WhatIf</span></span>
<span data-ttu-id="31f03-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31f03-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31f03-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="31f03-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31f03-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31f03-139">CommonParameters</span></span>
<span data-ttu-id="31f03-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31f03-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31f03-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="31f03-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31f03-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="31f03-142">INPUTS</span></span>

### <span data-ttu-id="31f03-143">Microsoft.Azure.PowerShell.cmdlet.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="31f03-143">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="31f03-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="31f03-144">OUTPUTS</span></span>

### <span data-ttu-id="31f03-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="31f03-145">System.Boolean</span></span>

## <span data-ttu-id="31f03-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="31f03-146">NOTES</span></span>

<span data-ttu-id="31f03-147">ALIASY</span><span class="sxs-lookup"><span data-stu-id="31f03-147">ALIASES</span></span>

<span data-ttu-id="31f03-148">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="31f03-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="31f03-149">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="31f03-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="31f03-150">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="31f03-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="31f03-151">INPUTOBJECT: <ICloudServiceIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="31f03-151">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="31f03-152">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="31f03-152">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="31f03-153">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="31f03-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="31f03-154">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="31f03-154">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="31f03-155">`[RoleInstanceName <String>]`: nazwa wystąpienia roli.</span><span class="sxs-lookup"><span data-stu-id="31f03-155">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="31f03-156">`[RoleName <String>]`: nazwa roli.</span><span class="sxs-lookup"><span data-stu-id="31f03-156">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="31f03-157">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="31f03-157">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="31f03-158">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="31f03-158">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="31f03-159">`[UpdateDomain <Int32?>]`: określa wartość całkowitą identyfikującą domenę aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="31f03-159">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="31f03-160">Domeny aktualizacji są identyfikowane za pomocą indeksu opartego na zeru: pierwsza domena aktualizacji ma identyfikator 0, druga ma identyfikator 1 i tak dalej.</span><span class="sxs-lookup"><span data-stu-id="31f03-160">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="31f03-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="31f03-161">RELATED LINKS</span></span>

