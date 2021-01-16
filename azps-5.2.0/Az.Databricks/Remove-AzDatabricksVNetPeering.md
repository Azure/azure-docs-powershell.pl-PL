---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/remove-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksVNetPeering.md
ms.openlocfilehash: 1c75bb4e8f94fadfb3b56c2fbb44889c5eaff458
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338686"
---
# <span data-ttu-id="9d766-101">Remove-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="9d766-101">Remove-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="9d766-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9d766-102">SYNOPSIS</span></span>
<span data-ttu-id="9d766-103">Usuwa obszar roboczy vNetPeering.</span><span class="sxs-lookup"><span data-stu-id="9d766-103">Deletes the workspace vNetPeering.</span></span>

## <span data-ttu-id="9d766-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9d766-104">SYNTAX</span></span>

### <span data-ttu-id="9d766-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="9d766-105">Delete (Default)</span></span>
```
Remove-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="9d766-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9d766-106">DeleteViaIdentity</span></span>
```
Remove-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9d766-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9d766-107">DESCRIPTION</span></span>
<span data-ttu-id="9d766-108">Usuwa obszar roboczy vNetPeering.</span><span class="sxs-lookup"><span data-stu-id="9d766-108">Deletes the workspace vNetPeering.</span></span>

## <span data-ttu-id="9d766-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9d766-109">EXAMPLES</span></span>

### <span data-ttu-id="9d766-110">Przykład 1: usuwanie komunikacji równorzędnej sieci datakostka według nazwy</span><span class="sxs-lookup"><span data-stu-id="9d766-110">Example 1: Remove a vnet peering of databricks by name</span></span>
```powershell
PS C:\> Remove-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01

```

<span data-ttu-id="9d766-111">To polecenie usuwa elementy równorzędne wirtualnej z obiektów datakostka według nazwy</span><span class="sxs-lookup"><span data-stu-id="9d766-111">This command removes a vnet peering of databricks by name</span></span>

### <span data-ttu-id="9d766-112">Przykład 2: usuwanie komunikacji równorzędnej sieci datakostek według obiektów</span><span class="sxs-lookup"><span data-stu-id="9d766-112">Example 2: Remove a vnet peering of databricks by object</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -ResourceGroupName lucas-manual-test -WorkspaceName databricks-test01 -PeeringName MyPeering-test01 | Remove-AzDatabricksVNetPeering

```

<span data-ttu-id="9d766-113">To polecenie usuwa elementy równorzędne wirtualnej z obiektów datakostka według obiektu</span><span class="sxs-lookup"><span data-stu-id="9d766-113">This command removes a vnet peering of databricks by object</span></span>

## <span data-ttu-id="9d766-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9d766-114">PARAMETERS</span></span>

### <span data-ttu-id="9d766-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9d766-115">-AsJob</span></span>
<span data-ttu-id="9d766-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="9d766-116">Run the command as a job</span></span>

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

### <span data-ttu-id="9d766-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d766-117">-DefaultProfile</span></span>
<span data-ttu-id="9d766-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9d766-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d766-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9d766-119">-InputObject</span></span>
<span data-ttu-id="9d766-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="9d766-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9d766-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9d766-121">-Name</span></span>
<span data-ttu-id="9d766-122">Nazwa komunikacji równorzędnej w obszarze roboczym sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9d766-122">The name of the workspace vNet peering.</span></span>

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

### <span data-ttu-id="9d766-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="9d766-123">-NoWait</span></span>
<span data-ttu-id="9d766-124">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="9d766-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9d766-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9d766-125">-PassThru</span></span>
<span data-ttu-id="9d766-126">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="9d766-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9d766-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d766-127">-ResourceGroupName</span></span>
<span data-ttu-id="9d766-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9d766-128">The name of the resource group.</span></span>
<span data-ttu-id="9d766-129">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="9d766-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="9d766-130">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="9d766-130">-SubscriptionId</span></span>
<span data-ttu-id="9d766-131">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="9d766-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="9d766-132">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="9d766-132">-WorkspaceName</span></span>
<span data-ttu-id="9d766-133">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="9d766-133">The name of the workspace.</span></span>

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

### <span data-ttu-id="9d766-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9d766-134">-Confirm</span></span>
<span data-ttu-id="9d766-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d766-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d766-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d766-136">-WhatIf</span></span>
<span data-ttu-id="9d766-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d766-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d766-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9d766-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d766-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d766-139">CommonParameters</span></span>
<span data-ttu-id="9d766-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d766-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d766-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9d766-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d766-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9d766-142">INPUTS</span></span>

### <span data-ttu-id="9d766-143">Microsoft. Azure. PowerShell. polecenia. datakosteks. models. IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="9d766-143">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="9d766-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9d766-144">OUTPUTS</span></span>

### <span data-ttu-id="9d766-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9d766-145">System.Boolean</span></span>

## <span data-ttu-id="9d766-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9d766-146">NOTES</span></span>

<span data-ttu-id="9d766-147">PISUJE</span><span class="sxs-lookup"><span data-stu-id="9d766-147">ALIASES</span></span>

<span data-ttu-id="9d766-148">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9d766-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9d766-149">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="9d766-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9d766-150">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9d766-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9d766-151">INPUTobject <IDatabricksIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="9d766-151">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9d766-152">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="9d766-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9d766-153">`[PeeringName <String>]`: Nazwa komunikacji równorzędnej w obszarze roboczym w sieci vNet.</span><span class="sxs-lookup"><span data-stu-id="9d766-153">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="9d766-154">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9d766-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="9d766-155">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="9d766-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="9d766-156">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="9d766-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="9d766-157">`[WorkspaceName <String>]`: Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="9d766-157">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="9d766-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9d766-158">RELATED LINKS</span></span>

