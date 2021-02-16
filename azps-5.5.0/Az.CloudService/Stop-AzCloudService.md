---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/stop-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Stop-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Stop-AzCloudService.md
ms.openlocfilehash: 1417cc797935a532decf886f0c814ef32deee3aa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199402"
---
# <span data-ttu-id="3bfff-101">Stop-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="3bfff-101">Stop-AzCloudService</span></span>

## <span data-ttu-id="3bfff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3bfff-102">SYNOPSIS</span></span>
<span data-ttu-id="3bfff-103">Wyłączanie usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="3bfff-103">Power off the cloud service.</span></span>
<span data-ttu-id="3bfff-104">Pamiętaj, że zasoby są nadal dołączone i naliczana jest opłata za zasoby.</span><span class="sxs-lookup"><span data-stu-id="3bfff-104">Note that resources are still attached and you are getting charged for the resources.</span></span>

## <span data-ttu-id="3bfff-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3bfff-105">SYNTAX</span></span>

### <span data-ttu-id="3bfff-106">PowerOff (domyślne)</span><span class="sxs-lookup"><span data-stu-id="3bfff-106">PowerOff (Default)</span></span>
```
Stop-AzCloudService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3bfff-107">PowerOffViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3bfff-107">PowerOffViaIdentity</span></span>
```
Stop-AzCloudService -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3bfff-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="3bfff-108">DESCRIPTION</span></span>
<span data-ttu-id="3bfff-109">Wyłączanie usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="3bfff-109">Power off the cloud service.</span></span>
<span data-ttu-id="3bfff-110">Pamiętaj, że zasoby są nadal dołączone i naliczana jest opłata za zasoby.</span><span class="sxs-lookup"><span data-stu-id="3bfff-110">Note that resources are still attached and you are getting charged for the resources.</span></span>

## <span data-ttu-id="3bfff-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3bfff-111">EXAMPLES</span></span>

### <span data-ttu-id="3bfff-112">Przykład 1. Zatrzymywanie usługi w chmurze</span><span class="sxs-lookup"><span data-stu-id="3bfff-112">Example 1: Stop cloud service</span></span>
```powershell
PS C:\> Stop-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS"
```

<span data-ttu-id="3bfff-113">To polecenie zatrzymuje wszystkie wystąpienia ról, które należą do usługi w chmurze o nazwie ContosoCS.</span><span class="sxs-lookup"><span data-stu-id="3bfff-113">This command stops all the role instances that belong to the the cloud service named ContosoCS.</span></span>

## <span data-ttu-id="3bfff-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3bfff-114">PARAMETERS</span></span>

### <span data-ttu-id="3bfff-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="3bfff-115">-AsJob</span></span>
<span data-ttu-id="3bfff-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="3bfff-116">Run the command as a job</span></span>

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

### <span data-ttu-id="3bfff-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bfff-117">-DefaultProfile</span></span>
<span data-ttu-id="3bfff-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3bfff-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bfff-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3bfff-119">-InputObject</span></span>
<span data-ttu-id="3bfff-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="3bfff-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: PowerOffViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3bfff-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3bfff-121">-Name</span></span>
<span data-ttu-id="3bfff-122">Nazwa usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="3bfff-122">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bfff-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3bfff-123">-NoWait</span></span>
<span data-ttu-id="3bfff-124">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="3bfff-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3bfff-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3bfff-125">-PassThru</span></span>
<span data-ttu-id="3bfff-126">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="3bfff-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3bfff-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bfff-127">-ResourceGroupName</span></span>
<span data-ttu-id="3bfff-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3bfff-128">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bfff-129">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3bfff-129">-SubscriptionId</span></span>
<span data-ttu-id="3bfff-130">Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3bfff-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3bfff-131">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="3bfff-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bfff-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3bfff-132">-Confirm</span></span>
<span data-ttu-id="3bfff-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3bfff-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bfff-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bfff-134">-WhatIf</span></span>
<span data-ttu-id="3bfff-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3bfff-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bfff-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3bfff-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bfff-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bfff-137">CommonParameters</span></span>
<span data-ttu-id="3bfff-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bfff-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bfff-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3bfff-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bfff-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3bfff-140">INPUTS</span></span>

### <span data-ttu-id="3bfff-141">Microsoft.Azure.PowerShell.Cmdlet.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="3bfff-141">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="3bfff-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3bfff-142">OUTPUTS</span></span>

### <span data-ttu-id="3bfff-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3bfff-143">System.Boolean</span></span>

## <span data-ttu-id="3bfff-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3bfff-144">NOTES</span></span>

<span data-ttu-id="3bfff-145">ALIASY</span><span class="sxs-lookup"><span data-stu-id="3bfff-145">ALIASES</span></span>

<span data-ttu-id="3bfff-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="3bfff-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3bfff-147">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="3bfff-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3bfff-148">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3bfff-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3bfff-149">INPUTOBJECT: <ICloudServiceIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="3bfff-149">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3bfff-150">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="3bfff-150">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="3bfff-151">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="3bfff-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3bfff-152">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="3bfff-152">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="3bfff-153">`[RoleInstanceName <String>]`: nazwa wystąpienia roli.</span><span class="sxs-lookup"><span data-stu-id="3bfff-153">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="3bfff-154">`[RoleName <String>]`: nazwa roli.</span><span class="sxs-lookup"><span data-stu-id="3bfff-154">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="3bfff-155">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3bfff-155">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="3bfff-156">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="3bfff-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="3bfff-157">`[UpdateDomain <Int32?>]`: określa wartość całkowitą identyfikującą domenę aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="3bfff-157">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="3bfff-158">Domeny aktualizacji są identyfikowane za pomocą indeksu opartego na zeru: pierwsza domena aktualizacji ma identyfikator 0, druga ma identyfikator 1 i tak dalej.</span><span class="sxs-lookup"><span data-stu-id="3bfff-158">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="3bfff-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3bfff-159">RELATED LINKS</span></span>

