---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/remove-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitor.md
ms.openlocfilehash: bcba06d87bce2f9ccc8016afc9f08dff75e29b1c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185826"
---
# <span data-ttu-id="d2b62-101">Remove-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="d2b62-101">Remove-AzSapMonitor</span></span>

## <span data-ttu-id="d2b62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2b62-102">SYNOPSIS</span></span>
<span data-ttu-id="d2b62-103">Usuwa monitor SAP z określoną subskrypcją, grupą zasobów i nazwą monitora.</span><span class="sxs-lookup"><span data-stu-id="d2b62-103">Deletes a SAP monitor with the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="d2b62-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d2b62-104">SYNTAX</span></span>

### <span data-ttu-id="d2b62-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="d2b62-105">Delete (Default)</span></span>
```
Remove-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d2b62-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d2b62-106">DeleteViaIdentity</span></span>
```
Remove-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d2b62-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d2b62-107">DESCRIPTION</span></span>
<span data-ttu-id="d2b62-108">Usuwa monitor SAP z określoną subskrypcją, grupą zasobów i nazwą monitora.</span><span class="sxs-lookup"><span data-stu-id="d2b62-108">Deletes a SAP monitor with the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="d2b62-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d2b62-109">EXAMPLES</span></span>

### <span data-ttu-id="d2b62-110">Przykład 1. Usuwanie monitora SAP według nazwy</span><span class="sxs-lookup"><span data-stu-id="d2b62-110">Example 1: Remove a SAP monitor by name</span></span>
```powershell
PS C:\> Remove-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t02

```

<span data-ttu-id="d2b62-111">To polecenie usuwa monitor SAP według nazwy.</span><span class="sxs-lookup"><span data-stu-id="d2b62-111">This command removes a SAP monitor by name.</span></span>

### <span data-ttu-id="d2b62-112">Przykład 2. Usuwanie monitora SAP według obiektu</span><span class="sxs-lookup"><span data-stu-id="d2b62-112">Example 2: Remove a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t01
PS C:\> Remove-AzSapMonitor -InputObject $sap

```

<span data-ttu-id="d2b62-113">To polecenie usuwa monitor SAP według obiektu.</span><span class="sxs-lookup"><span data-stu-id="d2b62-113">This command removes a SAP monitor by object.</span></span>

## <span data-ttu-id="d2b62-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2b62-114">PARAMETERS</span></span>

### <span data-ttu-id="d2b62-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="d2b62-115">-AsJob</span></span>
<span data-ttu-id="d2b62-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="d2b62-116">Run the command as a job</span></span>

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

### <span data-ttu-id="d2b62-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2b62-117">-DefaultProfile</span></span>
<span data-ttu-id="d2b62-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d2b62-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2b62-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2b62-119">-InputObject</span></span>
<span data-ttu-id="d2b62-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="d2b62-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2b62-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d2b62-121">-Name</span></span>
<span data-ttu-id="d2b62-122">Nazwa zasobu monitorowego SAP.</span><span class="sxs-lookup"><span data-stu-id="d2b62-122">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2b62-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d2b62-123">-NoWait</span></span>
<span data-ttu-id="d2b62-124">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="d2b62-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d2b62-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d2b62-125">-PassThru</span></span>
<span data-ttu-id="d2b62-126">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="d2b62-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d2b62-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2b62-127">-ResourceGroupName</span></span>
<span data-ttu-id="d2b62-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d2b62-128">Name of the resource group.</span></span>

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

### <span data-ttu-id="d2b62-129">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d2b62-129">-SubscriptionId</span></span>
<span data-ttu-id="d2b62-130">Identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d2b62-130">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d2b62-131">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="d2b62-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d2b62-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d2b62-132">-Confirm</span></span>
<span data-ttu-id="d2b62-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d2b62-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2b62-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2b62-134">-WhatIf</span></span>
<span data-ttu-id="d2b62-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2b62-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2b62-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d2b62-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2b62-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2b62-137">CommonParameters</span></span>
<span data-ttu-id="d2b62-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2b62-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2b62-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d2b62-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2b62-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d2b62-140">INPUTS</span></span>

### <span data-ttu-id="d2b62-141">Microsoft.Azure.PowerShell.Cmdlet.HanaOnAzure.Models.IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="d2b62-141">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="d2b62-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d2b62-142">OUTPUTS</span></span>

### <span data-ttu-id="d2b62-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d2b62-143">System.Boolean</span></span>

## <span data-ttu-id="d2b62-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d2b62-144">NOTES</span></span>

<span data-ttu-id="d2b62-145">ALIASY</span><span class="sxs-lookup"><span data-stu-id="d2b62-145">ALIASES</span></span>

<span data-ttu-id="d2b62-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="d2b62-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d2b62-147">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="d2b62-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d2b62-148">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d2b62-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d2b62-149">INPUTOBJECT: <IHanaOnAzureIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="d2b62-149">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d2b62-150">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="d2b62-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d2b62-151">`[Location <String>]`: lokalizacja usuniętego magazynu.</span><span class="sxs-lookup"><span data-stu-id="d2b62-151">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="d2b62-152">`[OperationKind <AccessPolicyUpdateKind?>]`: nazwa operacji</span><span class="sxs-lookup"><span data-stu-id="d2b62-152">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="d2b62-153">`[ProviderInstanceName <String>]`: nazwa wystąpienia dostawcy.</span><span class="sxs-lookup"><span data-stu-id="d2b62-153">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="d2b62-154">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d2b62-154">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="d2b62-155">`[ResourceName <String>]`: nazwa zasobu tożsamości.</span><span class="sxs-lookup"><span data-stu-id="d2b62-155">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="d2b62-156">`[SapMonitorName <String>]`: nazwa zasobu monitorów SAP.</span><span class="sxs-lookup"><span data-stu-id="d2b62-156">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="d2b62-157">`[Scope <String>]`: zakres dostawcy zasobów dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="d2b62-157">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="d2b62-158">Zasób nadrzędny jest rozszerzany przez tożsamości zarządzane.</span><span class="sxs-lookup"><span data-stu-id="d2b62-158">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="d2b62-159">`[SubscriptionId <String>]`: Identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d2b62-159">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d2b62-160">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="d2b62-160">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="d2b62-161">`[VaultName <String>]`: nazwa magazynu</span><span class="sxs-lookup"><span data-stu-id="d2b62-161">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="d2b62-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d2b62-162">RELATED LINKS</span></span>

