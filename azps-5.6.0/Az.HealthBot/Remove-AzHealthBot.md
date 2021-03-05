---
external help file: ''
Module Name: Az.HealthBot
online version: https://docs.microsoft.com/powershell/module/az.healthbot/remove-azhealthbot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Remove-AzHealthBot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Remove-AzHealthBot.md
ms.openlocfilehash: 2b2a4eba0a062b90866479409e80bbe7e55c1984
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013217"
---
# <span data-ttu-id="c1cdc-101">Remove-AzHealthBot</span><span class="sxs-lookup"><span data-stu-id="c1cdc-101">Remove-AzHealthBot</span></span>

## <span data-ttu-id="c1cdc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1cdc-102">SYNOPSIS</span></span>
<span data-ttu-id="c1cdc-103">Usuwanie robota HealthBot.</span><span class="sxs-lookup"><span data-stu-id="c1cdc-103">Delete a HealthBot.</span></span>

## <span data-ttu-id="c1cdc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c1cdc-104">SYNTAX</span></span>

### <span data-ttu-id="c1cdc-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="c1cdc-105">Delete (Default)</span></span>
```
Remove-AzHealthBot -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c1cdc-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c1cdc-106">DeleteViaIdentity</span></span>
```
Remove-AzHealthBot -InputObject <IHealthBotIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c1cdc-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="c1cdc-107">DESCRIPTION</span></span>
<span data-ttu-id="c1cdc-108">Usuwanie robota HealthBot.</span><span class="sxs-lookup"><span data-stu-id="c1cdc-108">Delete a HealthBot.</span></span>

## <span data-ttu-id="c1cdc-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c1cdc-109">EXAMPLES</span></span>

### <span data-ttu-id="c1cdc-110">Przykład 1. Usuwanie robota HealthBot według nazwy i nazwy grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="c1cdc-110">Example 1: Delete HealthBot by ResourceGroupName and Name</span></span>
```powershell
PS C:\> Remove-AzHealthBot -Name yourihealthbot -ResourceGroupName youriTest

```

<span data-ttu-id="c1cdc-111">Delete HealthBot by ResourceGroupName and Name</span><span class="sxs-lookup"><span data-stu-id="c1cdc-111">Delete HealthBot by ResourceGroupName and Name</span></span>

### <span data-ttu-id="c1cdc-112">Przykład 2. Usuwanie robota HealthBot przez inputObject</span><span class="sxs-lookup"><span data-stu-id="c1cdc-112">Example 2: Delete HealthBot by InputObject</span></span>
```powershell
PS C:\> $gethealthbot = Get-AzHealthBot -Name yourihealthbot1 -ResourceGroupName youriTest
Remove-AzHealthBot -InputObject $gethealthbot

```

<span data-ttu-id="c1cdc-113">Delete HealthBot by InputObject</span><span class="sxs-lookup"><span data-stu-id="c1cdc-113">Delete HealthBot by InputObject</span></span>

## <span data-ttu-id="c1cdc-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c1cdc-114">PARAMETERS</span></span>

### <span data-ttu-id="c1cdc-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="c1cdc-115">-AsJob</span></span>
<span data-ttu-id="c1cdc-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="c1cdc-116">Run the command as a job</span></span>

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

### <span data-ttu-id="c1cdc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1cdc-117">-DefaultProfile</span></span>
<span data-ttu-id="c1cdc-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c1cdc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1cdc-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c1cdc-119">-InputObject</span></span>
<span data-ttu-id="c1cdc-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="c1cdc-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1cdc-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c1cdc-121">-Name</span></span>
<span data-ttu-id="c1cdc-122">Nazwa zasobu bota.</span><span class="sxs-lookup"><span data-stu-id="c1cdc-122">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: BotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1cdc-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c1cdc-123">-NoWait</span></span>
<span data-ttu-id="c1cdc-124">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="c1cdc-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c1cdc-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c1cdc-125">-PassThru</span></span>
<span data-ttu-id="c1cdc-126">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="c1cdc-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c1cdc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1cdc-127">-ResourceGroupName</span></span>
<span data-ttu-id="c1cdc-128">Nazwa grupy zasobów bota w subskrypcji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="c1cdc-128">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="c1cdc-129">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c1cdc-129">-SubscriptionId</span></span>
<span data-ttu-id="c1cdc-130">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c1cdc-130">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="c1cdc-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c1cdc-131">-Confirm</span></span>
<span data-ttu-id="c1cdc-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c1cdc-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1cdc-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1cdc-133">-WhatIf</span></span>
<span data-ttu-id="c1cdc-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1cdc-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1cdc-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c1cdc-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1cdc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1cdc-136">CommonParameters</span></span>
<span data-ttu-id="c1cdc-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1cdc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1cdc-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c1cdc-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1cdc-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c1cdc-139">INPUTS</span></span>

### <span data-ttu-id="c1cdc-140">Microsoft.Azure.PowerShell.Cmdlet.HealthBot.Models.IHealthBotIdentity</span><span class="sxs-lookup"><span data-stu-id="c1cdc-140">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span></span>

## <span data-ttu-id="c1cdc-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c1cdc-141">OUTPUTS</span></span>

### <span data-ttu-id="c1cdc-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c1cdc-142">System.Boolean</span></span>

## <span data-ttu-id="c1cdc-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c1cdc-143">NOTES</span></span>

<span data-ttu-id="c1cdc-144">ALIASY</span><span class="sxs-lookup"><span data-stu-id="c1cdc-144">ALIASES</span></span>

<span data-ttu-id="c1cdc-145">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c1cdc-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c1cdc-146">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="c1cdc-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c1cdc-147">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c1cdc-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c1cdc-148">INPUTOBJECT: <IHealthBotIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="c1cdc-148">INPUTOBJECT <IHealthBotIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c1cdc-149">`[BotName <String>]`: nazwa zasobu bota.</span><span class="sxs-lookup"><span data-stu-id="c1cdc-149">`[BotName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="c1cdc-150">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="c1cdc-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c1cdc-151">`[ResourceGroupName <String>]`: nazwa grupy zasobów bota w subskrypcji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="c1cdc-151">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="c1cdc-152">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c1cdc-152">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="c1cdc-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c1cdc-153">RELATED LINKS</span></span>

