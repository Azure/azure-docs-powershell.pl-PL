---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/start-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Start-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Start-AzCloudService.md
ms.openlocfilehash: 2e2fe8534c1af369a8d095ba4ba3d74106700297
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199411"
---
# <span data-ttu-id="8726a-101">Start-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="8726a-101">Start-AzCloudService</span></span>

## <span data-ttu-id="8726a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8726a-102">SYNOPSIS</span></span>
<span data-ttu-id="8726a-103">Uruchamia usługę w chmurze.</span><span class="sxs-lookup"><span data-stu-id="8726a-103">Starts the cloud service.</span></span>

## <span data-ttu-id="8726a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8726a-104">SYNTAX</span></span>

### <span data-ttu-id="8726a-105">Start (domyślne)</span><span class="sxs-lookup"><span data-stu-id="8726a-105">Start (Default)</span></span>
```
Start-AzCloudService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8726a-106">StartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8726a-106">StartViaIdentity</span></span>
```
Start-AzCloudService -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8726a-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="8726a-107">DESCRIPTION</span></span>
<span data-ttu-id="8726a-108">Uruchamia usługę w chmurze.</span><span class="sxs-lookup"><span data-stu-id="8726a-108">Starts the cloud service.</span></span>

## <span data-ttu-id="8726a-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8726a-109">EXAMPLES</span></span>

### <span data-ttu-id="8726a-110">Przykład 1. Uruchamianie usługi w chmurze</span><span class="sxs-lookup"><span data-stu-id="8726a-110">Example 1: Start cloud service</span></span>
```powershell
PS C:\> Start-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS"
```

<span data-ttu-id="8726a-111">To polecenie uruchamia wszystkie wystąpienia ról, które należą do usługi w chmurze o nazwie ContosoCS.</span><span class="sxs-lookup"><span data-stu-id="8726a-111">This command starts all the role instances that belong to the the cloud service named ContosoCS.</span></span>

## <span data-ttu-id="8726a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8726a-112">PARAMETERS</span></span>

### <span data-ttu-id="8726a-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="8726a-113">-AsJob</span></span>
<span data-ttu-id="8726a-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="8726a-114">Run the command as a job</span></span>

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

### <span data-ttu-id="8726a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8726a-115">-DefaultProfile</span></span>
<span data-ttu-id="8726a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8726a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8726a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8726a-117">-InputObject</span></span>
<span data-ttu-id="8726a-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="8726a-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: StartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8726a-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8726a-119">-Name</span></span>
<span data-ttu-id="8726a-120">Nazwa usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="8726a-120">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8726a-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8726a-121">-NoWait</span></span>
<span data-ttu-id="8726a-122">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="8726a-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8726a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8726a-123">-PassThru</span></span>
<span data-ttu-id="8726a-124">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="8726a-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="8726a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8726a-125">-ResourceGroupName</span></span>
<span data-ttu-id="8726a-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8726a-126">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8726a-127">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8726a-127">-SubscriptionId</span></span>
<span data-ttu-id="8726a-128">Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8726a-128">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8726a-129">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="8726a-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8726a-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8726a-130">-Confirm</span></span>
<span data-ttu-id="8726a-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8726a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8726a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8726a-132">-WhatIf</span></span>
<span data-ttu-id="8726a-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8726a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8726a-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8726a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8726a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8726a-135">CommonParameters</span></span>
<span data-ttu-id="8726a-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8726a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8726a-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8726a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8726a-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8726a-138">INPUTS</span></span>

### <span data-ttu-id="8726a-139">Microsoft.Azure.PowerShell.cmdlet.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="8726a-139">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="8726a-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8726a-140">OUTPUTS</span></span>

### <span data-ttu-id="8726a-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8726a-141">System.Boolean</span></span>

## <span data-ttu-id="8726a-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8726a-142">NOTES</span></span>

<span data-ttu-id="8726a-143">ALIASY</span><span class="sxs-lookup"><span data-stu-id="8726a-143">ALIASES</span></span>

<span data-ttu-id="8726a-144">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8726a-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8726a-145">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="8726a-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8726a-146">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8726a-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8726a-147">INPUTOBJECT: <ICloudServiceIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="8726a-147">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8726a-148">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="8726a-148">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="8726a-149">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="8726a-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8726a-150">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="8726a-150">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="8726a-151">`[RoleInstanceName <String>]`: nazwa wystąpienia roli.</span><span class="sxs-lookup"><span data-stu-id="8726a-151">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="8726a-152">`[RoleName <String>]`: nazwa roli.</span><span class="sxs-lookup"><span data-stu-id="8726a-152">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="8726a-153">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8726a-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="8726a-154">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="8726a-154">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="8726a-155">`[UpdateDomain <Int32?>]`: określa wartość całkowitą identyfikującą domenę aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="8726a-155">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="8726a-156">Domeny aktualizacji są identyfikowane za pomocą indeksu opartego na zeru: pierwsza domena aktualizacji ma identyfikator 0, druga ma identyfikator 1 i tak dalej.</span><span class="sxs-lookup"><span data-stu-id="8726a-156">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="8726a-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8726a-157">RELATED LINKS</span></span>

