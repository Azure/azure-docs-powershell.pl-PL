---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/restart-azcloudserviceroleinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Restart-AzCloudServiceRoleInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Restart-AzCloudServiceRoleInstance.md
ms.openlocfilehash: f184696dbcfce35bf6e52f889d2c787214330e70
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985307"
---
# <span data-ttu-id="762ed-101">Restart-AzCloudServiceRoleInstance</span><span class="sxs-lookup"><span data-stu-id="762ed-101">Restart-AzCloudServiceRoleInstance</span></span>

## <span data-ttu-id="762ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="762ed-102">SYNOPSIS</span></span>
<span data-ttu-id="762ed-103">Asynchroniczne działanie wystąpienia ról ponownego uruchomienia żąda ponownego uruchomienia wystąpienia roli w usłudze w chmurze.</span><span class="sxs-lookup"><span data-stu-id="762ed-103">The Reboot Role Instance asynchronous operation requests a reboot of a role instance in the cloud service.</span></span>

## <span data-ttu-id="762ed-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="762ed-104">SYNTAX</span></span>

### <span data-ttu-id="762ed-105">Ponowne uruchamianie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="762ed-105">Restart (Default)</span></span>
```
Restart-AzCloudServiceRoleInstance -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="762ed-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="762ed-106">RestartViaIdentity</span></span>
```
Restart-AzCloudServiceRoleInstance -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="762ed-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="762ed-107">DESCRIPTION</span></span>
<span data-ttu-id="762ed-108">Asynchroniczne działanie wystąpienia ról ponownego uruchomienia żąda ponownego uruchomienia wystąpienia roli w usłudze w chmurze.</span><span class="sxs-lookup"><span data-stu-id="762ed-108">The Reboot Role Instance asynchronous operation requests a reboot of a role instance in the cloud service.</span></span>

## <span data-ttu-id="762ed-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="762ed-109">EXAMPLES</span></span>

### <span data-ttu-id="762ed-110">Przykład 1. Ponowne uruchamianie wystąpienia roli usługi w chmurze</span><span class="sxs-lookup"><span data-stu-id="762ed-110">Example 1: Restart role instance of a cloud service</span></span>
```powershell
PS C:\> Restart-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"
```

<span data-ttu-id="762ed-111">To polecenie powoduje ponowne uruchomienie wystąpienia roli o ContosoFrontEnd_IN_0 o nazwie ContosoCS, która należy do grupy zasobów o nazwie ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="762ed-111">This command restarts role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="762ed-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="762ed-112">PARAMETERS</span></span>

### <span data-ttu-id="762ed-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="762ed-113">-AsJob</span></span>
<span data-ttu-id="762ed-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="762ed-114">Run the command as a job</span></span>

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

### <span data-ttu-id="762ed-115">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="762ed-115">-CloudServiceName</span></span>
<span data-ttu-id="762ed-116">.</span><span class="sxs-lookup"><span data-stu-id="762ed-116">.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="762ed-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="762ed-117">-DefaultProfile</span></span>
<span data-ttu-id="762ed-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="762ed-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="762ed-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="762ed-119">-InputObject</span></span>
<span data-ttu-id="762ed-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="762ed-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: RestartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="762ed-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="762ed-121">-NoWait</span></span>
<span data-ttu-id="762ed-122">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="762ed-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="762ed-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="762ed-123">-PassThru</span></span>
<span data-ttu-id="762ed-124">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="762ed-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="762ed-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="762ed-125">-ResourceGroupName</span></span>
<span data-ttu-id="762ed-126">.</span><span class="sxs-lookup"><span data-stu-id="762ed-126">.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="762ed-127">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="762ed-127">-RoleInstanceName</span></span>
<span data-ttu-id="762ed-128">Nazwa wystąpienia roli.</span><span class="sxs-lookup"><span data-stu-id="762ed-128">Name of the role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="762ed-129">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="762ed-129">-SubscriptionId</span></span>
<span data-ttu-id="762ed-130">Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="762ed-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="762ed-131">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="762ed-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="762ed-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="762ed-132">-Confirm</span></span>
<span data-ttu-id="762ed-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="762ed-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="762ed-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="762ed-134">-WhatIf</span></span>
<span data-ttu-id="762ed-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="762ed-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="762ed-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="762ed-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="762ed-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="762ed-137">CommonParameters</span></span>
<span data-ttu-id="762ed-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="762ed-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="762ed-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="762ed-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="762ed-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="762ed-140">INPUTS</span></span>

### <span data-ttu-id="762ed-141">Microsoft.Azure.PowerShell.cmdlet.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="762ed-141">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="762ed-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="762ed-142">OUTPUTS</span></span>

### <span data-ttu-id="762ed-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="762ed-143">System.Boolean</span></span>

## <span data-ttu-id="762ed-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="762ed-144">NOTES</span></span>

<span data-ttu-id="762ed-145">ALIASY</span><span class="sxs-lookup"><span data-stu-id="762ed-145">ALIASES</span></span>

<span data-ttu-id="762ed-146">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="762ed-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="762ed-147">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="762ed-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="762ed-148">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="762ed-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="762ed-149">INPUTOBJECT: <ICloudServiceIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="762ed-149">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="762ed-150">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="762ed-150">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="762ed-151">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="762ed-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="762ed-152">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="762ed-152">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="762ed-153">`[RoleInstanceName <String>]`: nazwa wystąpienia roli.</span><span class="sxs-lookup"><span data-stu-id="762ed-153">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="762ed-154">`[RoleName <String>]`: nazwa roli.</span><span class="sxs-lookup"><span data-stu-id="762ed-154">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="762ed-155">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="762ed-155">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="762ed-156">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="762ed-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="762ed-157">`[UpdateDomain <Int32?>]`: określa wartość całkowitą identyfikującą domenę aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="762ed-157">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="762ed-158">Domeny aktualizacji są identyfikowane za pomocą indeksu opartego na zeru: pierwsza domena aktualizacji ma identyfikator 0, druga ma identyfikator 1 i tak dalej.</span><span class="sxs-lookup"><span data-stu-id="762ed-158">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="762ed-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="762ed-159">RELATED LINKS</span></span>

