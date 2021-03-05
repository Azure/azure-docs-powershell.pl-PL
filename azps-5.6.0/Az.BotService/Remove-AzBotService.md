---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/powershell/module/az.botservice/remove-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Remove-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Remove-AzBotService.md
ms.openlocfilehash: 486490a3b88025fb97b8790df202c944c05d888e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965073"
---
# <span data-ttu-id="034b5-101">Remove-AzBotService</span><span class="sxs-lookup"><span data-stu-id="034b5-101">Remove-AzBotService</span></span>

## <span data-ttu-id="034b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="034b5-102">SYNOPSIS</span></span>
<span data-ttu-id="034b5-103">Usuwa usługę bota z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="034b5-103">Deletes a Bot Service from the resource group.</span></span>

## <span data-ttu-id="034b5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="034b5-104">SYNTAX</span></span>

### <span data-ttu-id="034b5-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="034b5-105">Delete (Default)</span></span>
```
Remove-AzBotService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="034b5-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="034b5-106">DeleteViaIdentity</span></span>
```
Remove-AzBotService -InputObject <IBotServiceIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="034b5-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="034b5-107">DESCRIPTION</span></span>
<span data-ttu-id="034b5-108">Usuwa usługę bota z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="034b5-108">Deletes a Bot Service from the resource group.</span></span>

## <span data-ttu-id="034b5-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="034b5-109">EXAMPLES</span></span>

### <span data-ttu-id="034b5-110">Przykład 1. Usuwanie usługi BotService według nazw i nazw grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="034b5-110">Example 1: Delete the BotService By Name and ResourceGroupName</span></span>
```powershell
PS C:\> Remove-AzBotService -Name youri-bot -ResourceGroupName youriBotTest

```

<span data-ttu-id="034b5-111">Usuwanie usługi BotService Według nazwy i nazwy grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="034b5-111">Delete the BotService By Name and ResourceGroupName</span></span>

### <span data-ttu-id="034b5-112">Przykład 2. Usuwanie usługi BotService przez inputObject</span><span class="sxs-lookup"><span data-stu-id="034b5-112">Example 2: Delete the BotService By InputObject</span></span>
```powershell
PS C:\> $getservice = Get-AzBotService -Name youriechobottest -ResourceGroupName youriBotTest
Remove-AzBotService -InputObject $getservice

```

<span data-ttu-id="034b5-113">Usuwanie usługi BotService by InputObject</span><span class="sxs-lookup"><span data-stu-id="034b5-113">Delete the BotService By InputObject</span></span>

## <span data-ttu-id="034b5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="034b5-114">PARAMETERS</span></span>

### <span data-ttu-id="034b5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="034b5-115">-DefaultProfile</span></span>
<span data-ttu-id="034b5-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="034b5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="034b5-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="034b5-117">-InputObject</span></span>
<span data-ttu-id="034b5-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="034b5-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="034b5-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="034b5-119">-Name</span></span>
<span data-ttu-id="034b5-120">Nazwa zasobu bota.</span><span class="sxs-lookup"><span data-stu-id="034b5-120">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="034b5-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="034b5-121">-PassThru</span></span>
<span data-ttu-id="034b5-122">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="034b5-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="034b5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="034b5-123">-ResourceGroupName</span></span>
<span data-ttu-id="034b5-124">Nazwa grupy zasobów bota w subskrypcji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="034b5-124">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="034b5-125">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="034b5-125">-SubscriptionId</span></span>
<span data-ttu-id="034b5-126">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="034b5-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="034b5-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="034b5-127">-Confirm</span></span>
<span data-ttu-id="034b5-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="034b5-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="034b5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="034b5-129">-WhatIf</span></span>
<span data-ttu-id="034b5-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="034b5-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="034b5-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="034b5-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="034b5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="034b5-132">CommonParameters</span></span>
<span data-ttu-id="034b5-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="034b5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="034b5-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="034b5-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="034b5-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="034b5-135">INPUTS</span></span>

### <span data-ttu-id="034b5-136">Microsoft.Azure.PowerShell.cmdlet.BotService.Models.IBotServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="034b5-136">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span></span>

## <span data-ttu-id="034b5-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="034b5-137">OUTPUTS</span></span>

### <span data-ttu-id="034b5-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="034b5-138">System.Boolean</span></span>

## <span data-ttu-id="034b5-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="034b5-139">NOTES</span></span>

<span data-ttu-id="034b5-140">ALIASY</span><span class="sxs-lookup"><span data-stu-id="034b5-140">ALIASES</span></span>

<span data-ttu-id="034b5-141">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="034b5-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="034b5-142">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="034b5-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="034b5-143">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="034b5-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="034b5-144">INPUTOBJECT: <IBotServiceIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="034b5-144">INPUTOBJECT <IBotServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="034b5-145">`[ChannelName <ChannelName?>]`: nazwa zasobu Kanał.</span><span class="sxs-lookup"><span data-stu-id="034b5-145">`[ChannelName <ChannelName?>]`: The name of the Channel resource.</span></span>
  - <span data-ttu-id="034b5-146">`[ConnectionName <String>]`: nazwa zasobu ustawień połączenia usługi bota</span><span class="sxs-lookup"><span data-stu-id="034b5-146">`[ConnectionName <String>]`: The name of the Bot Service Connection Setting resource</span></span>
  - <span data-ttu-id="034b5-147">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="034b5-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="034b5-148">`[ResourceGroupName <String>]`: nazwa grupy zasobów bota w subskrypcji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="034b5-148">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="034b5-149">`[ResourceName <String>]`: nazwa zasobu bota.</span><span class="sxs-lookup"><span data-stu-id="034b5-149">`[ResourceName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="034b5-150">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="034b5-150">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="034b5-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="034b5-151">RELATED LINKS</span></span>

