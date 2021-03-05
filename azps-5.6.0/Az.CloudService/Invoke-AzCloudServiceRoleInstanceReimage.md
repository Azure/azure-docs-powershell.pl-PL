---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/invoke-azcloudserviceroleinstancereimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceRoleInstanceReimage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceRoleInstanceReimage.md
ms.openlocfilehash: 644912b841475c660852adcda2cba320d9026618
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965057"
---
# <span data-ttu-id="b673e-101">Invoke-AzCloudServiceRoleInstanceReimage</span><span class="sxs-lookup"><span data-stu-id="b673e-101">Invoke-AzCloudServiceRoleInstanceReimage</span></span>

## <span data-ttu-id="b673e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b673e-102">SYNOPSIS</span></span>
<span data-ttu-id="b673e-103">Asynchroniczne działanie wystąpienia ról w celu ponownego zainstalowania systemu operacyjnego w wystąpieniach ról sieci Web lub ról pracowników.</span><span class="sxs-lookup"><span data-stu-id="b673e-103">The Reimage Role Instance asynchronous operation reinstalls the operating system on instances of web roles or worker roles.</span></span>

## <span data-ttu-id="b673e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b673e-104">SYNTAX</span></span>

### <span data-ttu-id="b673e-105">Nowe ustawienia (domyślne)</span><span class="sxs-lookup"><span data-stu-id="b673e-105">Reimage (Default)</span></span>
```
Invoke-AzCloudServiceRoleInstanceReimage -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b673e-106">ReimageViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b673e-106">ReimageViaIdentity</span></span>
```
Invoke-AzCloudServiceRoleInstanceReimage -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b673e-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="b673e-107">DESCRIPTION</span></span>
<span data-ttu-id="b673e-108">Asynchroniczne działanie wystąpienia ról w celu ponownego zainstalowania systemu operacyjnego w wystąpieniach ról sieci Web lub ról pracowników.</span><span class="sxs-lookup"><span data-stu-id="b673e-108">The Reimage Role Instance asynchronous operation reinstalls the operating system on instances of web roles or worker roles.</span></span>

## <span data-ttu-id="b673e-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b673e-109">EXAMPLES</span></span>

### <span data-ttu-id="b673e-110">Przykład 1. Nowe wystąpienie roli usługi w chmurze</span><span class="sxs-lookup"><span data-stu-id="b673e-110">Example 1: Reimage role instance of a cloud service</span></span>
```powershell
PS C:\> Invoke-AzCloudServiceRoleInstanceReimage -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"
```

<span data-ttu-id="b673e-111">To polecenie pozwala ponownie zaimportować wystąpienie roli o nazwie ContosoFrontEnd_IN_0 o nazwie ContosoCS, która należy do grupy zasobów o nazwie ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="b673e-111">This command reimages role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="b673e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b673e-112">PARAMETERS</span></span>

### <span data-ttu-id="b673e-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="b673e-113">-AsJob</span></span>
<span data-ttu-id="b673e-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="b673e-114">Run the command as a job</span></span>

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

### <span data-ttu-id="b673e-115">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="b673e-115">-CloudServiceName</span></span>
<span data-ttu-id="b673e-116">.</span><span class="sxs-lookup"><span data-stu-id="b673e-116">.</span></span>

```yaml
Type: System.String
Parameter Sets: Reimage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b673e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b673e-117">-DefaultProfile</span></span>
<span data-ttu-id="b673e-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b673e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b673e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b673e-119">-InputObject</span></span>
<span data-ttu-id="b673e-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="b673e-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: ReimageViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b673e-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b673e-121">-NoWait</span></span>
<span data-ttu-id="b673e-122">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="b673e-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b673e-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b673e-123">-PassThru</span></span>
<span data-ttu-id="b673e-124">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="b673e-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b673e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b673e-125">-ResourceGroupName</span></span>
<span data-ttu-id="b673e-126">.</span><span class="sxs-lookup"><span data-stu-id="b673e-126">.</span></span>

```yaml
Type: System.String
Parameter Sets: Reimage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b673e-127">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="b673e-127">-RoleInstanceName</span></span>
<span data-ttu-id="b673e-128">Nazwa wystąpienia roli.</span><span class="sxs-lookup"><span data-stu-id="b673e-128">Name of the role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Reimage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b673e-129">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b673e-129">-SubscriptionId</span></span>
<span data-ttu-id="b673e-130">Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b673e-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b673e-131">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="b673e-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Reimage
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b673e-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b673e-132">-Confirm</span></span>
<span data-ttu-id="b673e-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b673e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b673e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b673e-134">-WhatIf</span></span>
<span data-ttu-id="b673e-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b673e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b673e-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b673e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b673e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b673e-137">CommonParameters</span></span>
<span data-ttu-id="b673e-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b673e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b673e-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b673e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b673e-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b673e-140">INPUTS</span></span>

### <span data-ttu-id="b673e-141">Microsoft.Azure.PowerShell.cmdlet.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="b673e-141">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="b673e-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b673e-142">OUTPUTS</span></span>

### <span data-ttu-id="b673e-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b673e-143">System.Boolean</span></span>

## <span data-ttu-id="b673e-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b673e-144">NOTES</span></span>

<span data-ttu-id="b673e-145">ALIASY</span><span class="sxs-lookup"><span data-stu-id="b673e-145">ALIASES</span></span>

<span data-ttu-id="b673e-146">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b673e-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b673e-147">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="b673e-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b673e-148">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b673e-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b673e-149">INPUTOBJECT: <ICloudServiceIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="b673e-149">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b673e-150">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="b673e-150">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="b673e-151">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="b673e-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b673e-152">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="b673e-152">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="b673e-153">`[RoleInstanceName <String>]`: nazwa wystąpienia roli.</span><span class="sxs-lookup"><span data-stu-id="b673e-153">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="b673e-154">`[RoleName <String>]`: nazwa roli.</span><span class="sxs-lookup"><span data-stu-id="b673e-154">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="b673e-155">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b673e-155">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b673e-156">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="b673e-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="b673e-157">`[UpdateDomain <Int32?>]`: określa wartość całkowitą identyfikującą domenę aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="b673e-157">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="b673e-158">Domeny aktualizacji są identyfikowane za pomocą indeksu opartego na zeru: pierwsza domena aktualizacji ma identyfikator 0, druga ma identyfikator 1 i tak dalej.</span><span class="sxs-lookup"><span data-stu-id="b673e-158">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="b673e-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b673e-159">RELATED LINKS</span></span>

