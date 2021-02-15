---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/invoke-azcloudservicereimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceReimage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceReimage.md
ms.openlocfilehash: 51fa4faa9491e4d119f3c14b1c5b44bee6fdd15e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200747"
---
# <span data-ttu-id="434ae-101">Invoke-AzCloudServiceReimage</span><span class="sxs-lookup"><span data-stu-id="434ae-101">Invoke-AzCloudServiceReimage</span></span>

## <span data-ttu-id="434ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="434ae-102">SYNOPSIS</span></span>
<span data-ttu-id="434ae-103">Aby ponownie rozpocząć asynchroniczne działanie, system operacyjny jest ponownie instalowany w wystąpieniach ról sieci Web lub ról pracowników.</span><span class="sxs-lookup"><span data-stu-id="434ae-103">Reimage asynchronous operation reinstalls the operating system on instances of web roles or worker roles.</span></span>

## <span data-ttu-id="434ae-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="434ae-104">SYNTAX</span></span>

### <span data-ttu-id="434ae-105">Nowość Nierozwiązywalna (domyślna)</span><span class="sxs-lookup"><span data-stu-id="434ae-105">ReimageExpanded (Default)</span></span>
```
Invoke-AzCloudServiceReimage -Name <String> -ResourceGroupName <String> -RoleInstance <String[]>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="434ae-106">ReimageViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="434ae-106">ReimageViaIdentityExpanded</span></span>
```
Invoke-AzCloudServiceReimage -InputObject <ICloudServiceIdentity> -RoleInstance <String[]>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="434ae-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="434ae-107">DESCRIPTION</span></span>
<span data-ttu-id="434ae-108">Aby ponownie rozpocząć asynchroniczne działanie, system operacyjny jest ponownie instalowany w wystąpieniach ról sieci Web lub ról pracowników.</span><span class="sxs-lookup"><span data-stu-id="434ae-108">Reimage asynchronous operation reinstalls the operating system on instances of web roles or worker roles.</span></span>

## <span data-ttu-id="434ae-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="434ae-109">EXAMPLES</span></span>

### <span data-ttu-id="434ae-110">Przykład 1. Nowe wystąpienia ról usługi w chmurze</span><span class="sxs-lookup"><span data-stu-id="434ae-110">Example 1: Reimage role instances of cloud service</span></span>
```powershell
PS C:\> $roleInstances = @("ContosoFrontEnd_IN_0", "ContosoBackEnd_IN_1")
PS C:\> Invoke-AzCloudServiceReimage -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance $roleInstances
```

<span data-ttu-id="434ae-111">To polecenie ponownie projektuje 2 wystąpienia ról ContosoFrontEnd_IN_0 i ContosoBackEnd_IN_1 usługi w chmurze o nazwie ContosoCS, która należy do grupy zasobów o nazwie ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="434ae-111">This command reimages 2 role instances ContosoFrontEnd_IN_0 and ContosoBackEnd_IN_1 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="434ae-112">Przykład 2. Ponowne zaimportowanie wszystkich ról usługi w chmurze</span><span class="sxs-lookup"><span data-stu-id="434ae-112">Example 2: Reimage all roles of cloud service</span></span>
```powershell
PS C:\> Invoke-AzCloudServiceReimage -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance "*"
```

<span data-ttu-id="434ae-113">To polecenie ponownie projektuje wszystkie wystąpienia ról usługi w chmurze o nazwie ContosoCS, które należą do grupy zasobów o nazwie ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="434ae-113">This command reimages all role instances of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="434ae-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="434ae-114">PARAMETERS</span></span>

### <span data-ttu-id="434ae-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="434ae-115">-AsJob</span></span>
<span data-ttu-id="434ae-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="434ae-116">Run the command as a job</span></span>

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

### <span data-ttu-id="434ae-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="434ae-117">-DefaultProfile</span></span>
<span data-ttu-id="434ae-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="434ae-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="434ae-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="434ae-119">-InputObject</span></span>
<span data-ttu-id="434ae-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="434ae-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: ReimageViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="434ae-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="434ae-121">-Name</span></span>
<span data-ttu-id="434ae-122">Nazwa usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="434ae-122">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: ReimageExpanded
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="434ae-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="434ae-123">-NoWait</span></span>
<span data-ttu-id="434ae-124">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="434ae-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="434ae-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="434ae-125">-PassThru</span></span>
<span data-ttu-id="434ae-126">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="434ae-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="434ae-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="434ae-127">-ResourceGroupName</span></span>
<span data-ttu-id="434ae-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="434ae-128">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ReimageExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="434ae-129">-RoleInstance</span><span class="sxs-lookup"><span data-stu-id="434ae-129">-RoleInstance</span></span>
<span data-ttu-id="434ae-130">Lista nazw wystąpień ról usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="434ae-130">List of cloud service role instance names.</span></span>
<span data-ttu-id="434ae-131">Wartość "\*" oznacza wszystkie wystąpienia ról usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="434ae-131">Value of '\*' will signify all role instances of the cloud service.</span></span>

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

### <span data-ttu-id="434ae-132">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="434ae-132">-SubscriptionId</span></span>
<span data-ttu-id="434ae-133">Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="434ae-133">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="434ae-134">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="434ae-134">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: ReimageExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="434ae-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="434ae-135">-Confirm</span></span>
<span data-ttu-id="434ae-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="434ae-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="434ae-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="434ae-137">-WhatIf</span></span>
<span data-ttu-id="434ae-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="434ae-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="434ae-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="434ae-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="434ae-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="434ae-140">CommonParameters</span></span>
<span data-ttu-id="434ae-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="434ae-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="434ae-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="434ae-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="434ae-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="434ae-143">INPUTS</span></span>

### <span data-ttu-id="434ae-144">Microsoft.Azure.PowerShell.Cmdlet.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="434ae-144">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="434ae-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="434ae-145">OUTPUTS</span></span>

### <span data-ttu-id="434ae-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="434ae-146">System.Boolean</span></span>

## <span data-ttu-id="434ae-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="434ae-147">NOTES</span></span>

<span data-ttu-id="434ae-148">ALIASY</span><span class="sxs-lookup"><span data-stu-id="434ae-148">ALIASES</span></span>

<span data-ttu-id="434ae-149">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="434ae-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="434ae-150">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="434ae-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="434ae-151">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="434ae-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="434ae-152">INPUTOBJECT: <ICloudServiceIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="434ae-152">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="434ae-153">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="434ae-153">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="434ae-154">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="434ae-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="434ae-155">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="434ae-155">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="434ae-156">`[RoleInstanceName <String>]`: nazwa wystąpienia roli.</span><span class="sxs-lookup"><span data-stu-id="434ae-156">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="434ae-157">`[RoleName <String>]`: nazwa roli.</span><span class="sxs-lookup"><span data-stu-id="434ae-157">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="434ae-158">`[SubscriptionId <String>]`: poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="434ae-158">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="434ae-159">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="434ae-159">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="434ae-160">`[UpdateDomain <Int32?>]`: określa wartość całkowitą identyfikującą domenę aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="434ae-160">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="434ae-161">Domeny aktualizacji są identyfikowane za pomocą indeksu opartego na zeru: pierwsza domena aktualizacji ma identyfikator 0, druga ma identyfikator 1 i tak dalej.</span><span class="sxs-lookup"><span data-stu-id="434ae-161">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="434ae-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="434ae-162">RELATED LINKS</span></span>

