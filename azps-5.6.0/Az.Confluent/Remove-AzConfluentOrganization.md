---
external help file: ''
Module Name: Az.Confluent
online version: https://docs.microsoft.com/powershell/module/az.confluent/remove-azconfluentorganization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Remove-AzConfluentOrganization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Remove-AzConfluentOrganization.md
ms.openlocfilehash: d35de003bd4822758fd75c7dbbcf616ebecbbccb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012554"
---
# <span data-ttu-id="62984-101">Remove-AzConfluentOrganization</span><span class="sxs-lookup"><span data-stu-id="62984-101">Remove-AzConfluentOrganization</span></span>

## <span data-ttu-id="62984-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62984-102">SYNOPSIS</span></span>
<span data-ttu-id="62984-103">Usuwanie zasobu organizacji</span><span class="sxs-lookup"><span data-stu-id="62984-103">Delete Organization resource</span></span>

## <span data-ttu-id="62984-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="62984-104">SYNTAX</span></span>

### <span data-ttu-id="62984-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="62984-105">Delete (Default)</span></span>
```
Remove-AzConfluentOrganization -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="62984-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="62984-106">DeleteViaIdentity</span></span>
```
Remove-AzConfluentOrganization -InputObject <IConfluentIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="62984-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="62984-107">DESCRIPTION</span></span>
<span data-ttu-id="62984-108">Usuwanie zasobu organizacji</span><span class="sxs-lookup"><span data-stu-id="62984-108">Delete Organization resource</span></span>

## <span data-ttu-id="62984-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="62984-109">EXAMPLES</span></span>

### <span data-ttu-id="62984-110">Przykład 1. Usuwanie organizacji, która się ujmuje, według nazwy</span><span class="sxs-lookup"><span data-stu-id="62984-110">Example 1: Remove a confluent organization by name</span></span>
```powershell
PS C:\> Remove-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-01-portal

```

<span data-ttu-id="62984-111">To polecenie usuwa organizację, która się ułozyła, według nazwy</span><span class="sxs-lookup"><span data-stu-id="62984-111">This command removes a confluent organization by name</span></span>

### <span data-ttu-id="62984-112">Przykład 2. Usuwanie organizacji sypkiej według potoku</span><span class="sxs-lookup"><span data-stu-id="62984-112">Example 2: Remove a confluent organization by pipeline</span></span>
```powershell
PS C:\>  Get-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-02-pwsh | Remove-AzConfluentOrganization

```

<span data-ttu-id="62984-113">To polecenie usuwa organizację, która się ujmuje, według potoku.</span><span class="sxs-lookup"><span data-stu-id="62984-113">This command removes a confluent organization by pipeline.</span></span>

## <span data-ttu-id="62984-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62984-114">PARAMETERS</span></span>

### <span data-ttu-id="62984-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="62984-115">-AsJob</span></span>
<span data-ttu-id="62984-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="62984-116">Run the command as a job</span></span>

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

### <span data-ttu-id="62984-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62984-117">-DefaultProfile</span></span>
<span data-ttu-id="62984-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="62984-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62984-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62984-119">-InputObject</span></span>
<span data-ttu-id="62984-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="62984-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62984-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="62984-121">-Name</span></span>
<span data-ttu-id="62984-122">Nazwa zasobu organizacji</span><span class="sxs-lookup"><span data-stu-id="62984-122">Organization resource name</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: OrganizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62984-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="62984-123">-NoWait</span></span>
<span data-ttu-id="62984-124">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="62984-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="62984-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="62984-125">-PassThru</span></span>
<span data-ttu-id="62984-126">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="62984-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="62984-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62984-127">-ResourceGroupName</span></span>
<span data-ttu-id="62984-128">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="62984-128">Resource group name</span></span>

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

### <span data-ttu-id="62984-129">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="62984-129">-SubscriptionId</span></span>
<span data-ttu-id="62984-130">Identyfikator subskrypcji platformy Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="62984-130">Microsoft Azure subscription id</span></span>

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

### <span data-ttu-id="62984-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="62984-131">-Confirm</span></span>
<span data-ttu-id="62984-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="62984-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62984-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62984-133">-WhatIf</span></span>
<span data-ttu-id="62984-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62984-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62984-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="62984-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62984-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62984-136">CommonParameters</span></span>
<span data-ttu-id="62984-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62984-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62984-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="62984-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62984-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="62984-139">INPUTS</span></span>

### <span data-ttu-id="62984-140">Microsoft.Azure.PowerShell.Cmdlet.Confluent.Models.IConfluentIdentity</span><span class="sxs-lookup"><span data-stu-id="62984-140">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity</span></span>

## <span data-ttu-id="62984-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="62984-141">OUTPUTS</span></span>

### <span data-ttu-id="62984-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="62984-142">System.Boolean</span></span>

## <span data-ttu-id="62984-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="62984-143">NOTES</span></span>

<span data-ttu-id="62984-144">ALIASY</span><span class="sxs-lookup"><span data-stu-id="62984-144">ALIASES</span></span>

<span data-ttu-id="62984-145">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="62984-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="62984-146">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="62984-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="62984-147">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="62984-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="62984-148">INPUTOBJECT: <IConfluentIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="62984-148">INPUTOBJECT <IConfluentIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="62984-149">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="62984-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="62984-150">`[OrganizationName <String>]`: nazwa zasobu organizacji</span><span class="sxs-lookup"><span data-stu-id="62984-150">`[OrganizationName <String>]`: Organization resource name</span></span>
  - <span data-ttu-id="62984-151">`[ResourceGroupName <String>]`: nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="62984-151">`[ResourceGroupName <String>]`: Resource group name</span></span>
  - <span data-ttu-id="62984-152">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="62984-152">`[SubscriptionId <String>]`: Microsoft Azure subscription id</span></span>

## <span data-ttu-id="62984-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="62984-153">RELATED LINKS</span></span>

