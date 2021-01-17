---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/remove-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksWorkspace.md
ms.openlocfilehash: 629b12a7db506b0a96633396b97e0df3d66e1760
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362271"
---
# <span data-ttu-id="05aa9-101">Remove-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="05aa9-101">Remove-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="05aa9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="05aa9-102">SYNOPSIS</span></span>
<span data-ttu-id="05aa9-103">Usuwa obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="05aa9-103">Deletes the workspace.</span></span>

## <span data-ttu-id="05aa9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="05aa9-104">SYNTAX</span></span>

### <span data-ttu-id="05aa9-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="05aa9-105">Delete (Default)</span></span>
```
Remove-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="05aa9-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="05aa9-106">DeleteViaIdentity</span></span>
```
Remove-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="05aa9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="05aa9-107">DESCRIPTION</span></span>
<span data-ttu-id="05aa9-108">Usuwa obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="05aa9-108">Deletes the workspace.</span></span>

## <span data-ttu-id="05aa9-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="05aa9-109">EXAMPLES</span></span>

### <span data-ttu-id="05aa9-110">Przykład 1. Usuń obszar roboczy datacegły</span><span class="sxs-lookup"><span data-stu-id="05aa9-110">Example 1: Remove a Databricks workspace</span></span>
```powershell
PS C:\> Remove-AzDatabricksWorkspace -ResourceGroupName testgroup -Name databricks-test
```

<span data-ttu-id="05aa9-111">To polecenie umożliwia usunięcie obszaru roboczego datakostki z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="05aa9-111">This command removes a Databricks workspace from a resource group.</span></span>

### <span data-ttu-id="05aa9-112">Przykład 2: Usuwanie obszaru roboczego datakostkowe według obiektu</span><span class="sxs-lookup"><span data-stu-id="05aa9-112">Example 2: Remove a Databricks workspace by object</span></span>
```powershell
PS C:\> $dbr = Get-AzDatabricksWorkspace -ResourceGroupName testgroup -Name databricks-test02
PS C:\> Remove-AzDatabricksWorkspace -InputObject $dbr
```

<span data-ttu-id="05aa9-113">To polecenie umożliwia usunięcie obszaru roboczego datakostki z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="05aa9-113">This command removes a Databricks workspace from a resource group.</span></span>

## <span data-ttu-id="05aa9-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="05aa9-114">PARAMETERS</span></span>

### <span data-ttu-id="05aa9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="05aa9-115">-AsJob</span></span>
<span data-ttu-id="05aa9-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="05aa9-116">Run the command as a job</span></span>

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

### <span data-ttu-id="05aa9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05aa9-117">-DefaultProfile</span></span>
<span data-ttu-id="05aa9-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="05aa9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05aa9-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="05aa9-119">-InputObject</span></span>
<span data-ttu-id="05aa9-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="05aa9-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05aa9-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="05aa9-121">-Name</span></span>
<span data-ttu-id="05aa9-122">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="05aa9-122">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05aa9-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="05aa9-123">-NoWait</span></span>
<span data-ttu-id="05aa9-124">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="05aa9-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="05aa9-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="05aa9-125">-PassThru</span></span>
<span data-ttu-id="05aa9-126">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="05aa9-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="05aa9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05aa9-127">-ResourceGroupName</span></span>
<span data-ttu-id="05aa9-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="05aa9-128">The name of the resource group.</span></span>
<span data-ttu-id="05aa9-129">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="05aa9-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="05aa9-130">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="05aa9-130">-SubscriptionId</span></span>
<span data-ttu-id="05aa9-131">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="05aa9-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="05aa9-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="05aa9-132">-Confirm</span></span>
<span data-ttu-id="05aa9-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05aa9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05aa9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05aa9-134">-WhatIf</span></span>
<span data-ttu-id="05aa9-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05aa9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05aa9-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="05aa9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05aa9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05aa9-137">CommonParameters</span></span>
<span data-ttu-id="05aa9-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05aa9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05aa9-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="05aa9-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05aa9-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="05aa9-140">INPUTS</span></span>

### <span data-ttu-id="05aa9-141">Microsoft. Azure. PowerShell. polecenia. datakosteks. models. IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="05aa9-141">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="05aa9-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="05aa9-142">OUTPUTS</span></span>

### <span data-ttu-id="05aa9-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="05aa9-143">System.Boolean</span></span>

## <span data-ttu-id="05aa9-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="05aa9-144">NOTES</span></span>

<span data-ttu-id="05aa9-145">PISUJE</span><span class="sxs-lookup"><span data-stu-id="05aa9-145">ALIASES</span></span>

<span data-ttu-id="05aa9-146">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="05aa9-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="05aa9-147">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="05aa9-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="05aa9-148">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="05aa9-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="05aa9-149">INPUTobject <IDatabricksIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="05aa9-149">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="05aa9-150">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="05aa9-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="05aa9-151">`[PeeringName <String>]`: Nazwa komunikacji równorzędnej w obszarze roboczym w sieci vNet.</span><span class="sxs-lookup"><span data-stu-id="05aa9-151">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="05aa9-152">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="05aa9-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="05aa9-153">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="05aa9-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="05aa9-154">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="05aa9-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="05aa9-155">`[WorkspaceName <String>]`: Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="05aa9-155">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="05aa9-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="05aa9-156">RELATED LINKS</span></span>

