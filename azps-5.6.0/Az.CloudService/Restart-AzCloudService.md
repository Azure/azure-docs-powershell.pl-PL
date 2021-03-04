---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/restart-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Restart-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Restart-AzCloudService.md
ms.openlocfilehash: e61eea1d00468937a46f90fdd6a995f5f53ff468
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956442"
---
# <span data-ttu-id="d32f9-101">Restart-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="d32f9-101">Restart-AzCloudService</span></span>

## <span data-ttu-id="d32f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d32f9-102">SYNOPSIS</span></span>
<span data-ttu-id="d32f9-103">Powoduje ponowne uruchomienie jednego lub większej liczby wystąpień ról w usłudze w chmurze.</span><span class="sxs-lookup"><span data-stu-id="d32f9-103">Restarts one or more role instances in a cloud service.</span></span>

## <span data-ttu-id="d32f9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d32f9-104">SYNTAX</span></span>

### <span data-ttu-id="d32f9-105">RestartExpanded (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="d32f9-105">RestartExpanded (Default)</span></span>
```
Restart-AzCloudService -Name <String> -ResourceGroupName <String> -RoleInstance <String[]>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="d32f9-106">RestartViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d32f9-106">RestartViaIdentityExpanded</span></span>
```
Restart-AzCloudService -InputObject <ICloudServiceIdentity> -RoleInstance <String[]>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d32f9-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d32f9-107">DESCRIPTION</span></span>
<span data-ttu-id="d32f9-108">Powoduje ponowne uruchomienie jednego lub większej liczby wystąpień ról w usłudze w chmurze.</span><span class="sxs-lookup"><span data-stu-id="d32f9-108">Restarts one or more role instances in a cloud service.</span></span>

## <span data-ttu-id="d32f9-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d32f9-109">EXAMPLES</span></span>

### <span data-ttu-id="d32f9-110">Przykład 1. Ponowne uruchamianie wystąpień ról usługi w chmurze</span><span class="sxs-lookup"><span data-stu-id="d32f9-110">Example 1: Restart role instances of cloud service</span></span>
```powershell
PS C:\> $roleInstances = @("ContosoFrontEnd_IN_0", "ContosoBackEnd_IN_1")
PS C:\> Restart-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance $roleInstances
```

<span data-ttu-id="d32f9-111">To polecenie powoduje ponowne uruchomienie 2 wystąpień ContosoFrontEnd_IN_0 i ContosoBackEnd_IN_1 usługi w chmurze o nazwie ContosoCS, która należy do grupy zasobów o nazwie ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="d32f9-111">This command restarts 2 role instances ContosoFrontEnd_IN_0 and ContosoBackEnd_IN_1 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="d32f9-112">Przykład 2. Ponowne uruchamianie wszystkich ról usługi w chmurze</span><span class="sxs-lookup"><span data-stu-id="d32f9-112">Example 2: Restart all roles of cloud service</span></span>
```powershell
PS C:\> Restart-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance "*"
```

<span data-ttu-id="d32f9-113">To polecenie powoduje ponowne uruchomienie wszystkich wystąpień ról usługi w chmurze o nazwie ContosoCS, które należą do grupy zasobów o nazwie ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="d32f9-113">This command restarts all role instances of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="d32f9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d32f9-114">PARAMETERS</span></span>

### <span data-ttu-id="d32f9-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="d32f9-115">-AsJob</span></span>
<span data-ttu-id="d32f9-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="d32f9-116">Run the command as a job</span></span>

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

### <span data-ttu-id="d32f9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d32f9-117">-DefaultProfile</span></span>
<span data-ttu-id="d32f9-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d32f9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d32f9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d32f9-119">-InputObject</span></span>
<span data-ttu-id="d32f9-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="d32f9-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: RestartViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d32f9-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d32f9-121">-Name</span></span>
<span data-ttu-id="d32f9-122">Nazwa usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="d32f9-122">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartExpanded
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d32f9-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d32f9-123">-NoWait</span></span>
<span data-ttu-id="d32f9-124">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="d32f9-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d32f9-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d32f9-125">-PassThru</span></span>
<span data-ttu-id="d32f9-126">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="d32f9-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d32f9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d32f9-127">-ResourceGroupName</span></span>
<span data-ttu-id="d32f9-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d32f9-128">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d32f9-129">-RoleInstance</span><span class="sxs-lookup"><span data-stu-id="d32f9-129">-RoleInstance</span></span>
<span data-ttu-id="d32f9-130">Lista nazw wystąpień ról usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="d32f9-130">List of cloud service role instance names.</span></span>
<span data-ttu-id="d32f9-131">Wartość "\*" oznacza wszystkie wystąpienia ról usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="d32f9-131">Value of '\*' will signify all role instances of the cloud service.</span></span>

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

### <span data-ttu-id="d32f9-132">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d32f9-132">-SubscriptionId</span></span>
<span data-ttu-id="d32f9-133">Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d32f9-133">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d32f9-134">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="d32f9-134">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d32f9-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d32f9-135">-Confirm</span></span>
<span data-ttu-id="d32f9-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d32f9-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d32f9-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d32f9-137">-WhatIf</span></span>
<span data-ttu-id="d32f9-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d32f9-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d32f9-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d32f9-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d32f9-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d32f9-140">CommonParameters</span></span>
<span data-ttu-id="d32f9-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d32f9-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d32f9-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d32f9-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d32f9-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d32f9-143">INPUTS</span></span>

### <span data-ttu-id="d32f9-144">Microsoft.Azure.PowerShell.cmdlet.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="d32f9-144">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="d32f9-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d32f9-145">OUTPUTS</span></span>

### <span data-ttu-id="d32f9-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d32f9-146">System.Boolean</span></span>

## <span data-ttu-id="d32f9-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d32f9-147">NOTES</span></span>

<span data-ttu-id="d32f9-148">ALIASY</span><span class="sxs-lookup"><span data-stu-id="d32f9-148">ALIASES</span></span>

<span data-ttu-id="d32f9-149">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d32f9-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d32f9-150">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="d32f9-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d32f9-151">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d32f9-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d32f9-152">INPUTOBJECT: <ICloudServiceIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="d32f9-152">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d32f9-153">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="d32f9-153">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="d32f9-154">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="d32f9-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d32f9-155">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="d32f9-155">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="d32f9-156">`[RoleInstanceName <String>]`: nazwa wystąpienia roli.</span><span class="sxs-lookup"><span data-stu-id="d32f9-156">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="d32f9-157">`[RoleName <String>]`: nazwa roli.</span><span class="sxs-lookup"><span data-stu-id="d32f9-157">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="d32f9-158">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d32f9-158">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d32f9-159">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="d32f9-159">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="d32f9-160">`[UpdateDomain <Int32?>]`: określa wartość całkowitą identyfikującą domenę aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="d32f9-160">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="d32f9-161">Domeny aktualizacji są identyfikowane za pomocą indeksu opartego na zeru: pierwsza domena aktualizacji ma identyfikator 0, druga ma identyfikator 1 i tak dalej.</span><span class="sxs-lookup"><span data-stu-id="d32f9-161">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="d32f9-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d32f9-162">RELATED LINKS</span></span>

