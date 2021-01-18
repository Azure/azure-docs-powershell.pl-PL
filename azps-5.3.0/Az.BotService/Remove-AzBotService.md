---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/remove-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Remove-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Remove-AzBotService.md
ms.openlocfilehash: ef75ec3e48a68bffce7c5b281f542bd2e3dba9d9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502034"
---
# <span data-ttu-id="cf891-101">Remove-AzBotService</span><span class="sxs-lookup"><span data-stu-id="cf891-101">Remove-AzBotService</span></span>

## <span data-ttu-id="cf891-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cf891-102">SYNOPSIS</span></span>
<span data-ttu-id="cf891-103">Usuwa usługę bota z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cf891-103">Deletes a Bot Service from the resource group.</span></span>

## <span data-ttu-id="cf891-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cf891-104">SYNTAX</span></span>

### <span data-ttu-id="cf891-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="cf891-105">Delete (Default)</span></span>
```
Remove-AzBotService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cf891-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cf891-106">DeleteViaIdentity</span></span>
```
Remove-AzBotService -InputObject <IBotServiceIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cf891-107">Opis</span><span class="sxs-lookup"><span data-stu-id="cf891-107">DESCRIPTION</span></span>
<span data-ttu-id="cf891-108">Usuwa usługę bota z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cf891-108">Deletes a Bot Service from the resource group.</span></span>

## <span data-ttu-id="cf891-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cf891-109">EXAMPLES</span></span>

### <span data-ttu-id="cf891-110">Przykład 1. Usuń BotService za pomocą nazwy i ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf891-110">Example 1: Delete the BotService By Name and ResourceGroupName</span></span>
```powershell
PS C:\> Remove-AzBotService -Name youri-bot -ResourceGroupName youriBotTest

```

<span data-ttu-id="cf891-111">Usuń BotService według nazwy i ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf891-111">Delete the BotService By Name and ResourceGroupName</span></span>

### <span data-ttu-id="cf891-112">Przykład 2: usuwanie BotService za pomocą narzędzia Inputobject</span><span class="sxs-lookup"><span data-stu-id="cf891-112">Example 2: Delete the BotService By InputObject</span></span>
```powershell
PS C:\> $getservice = Get-AzBotService -Name youriechobottest -ResourceGroupName youriBotTest
Remove-AzBotService -InputObject $getservice

```

<span data-ttu-id="cf891-113">Usuwanie BotService przez wejście</span><span class="sxs-lookup"><span data-stu-id="cf891-113">Delete the BotService By InputObject</span></span>

## <span data-ttu-id="cf891-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cf891-114">PARAMETERS</span></span>

### <span data-ttu-id="cf891-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf891-115">-DefaultProfile</span></span>
<span data-ttu-id="cf891-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cf891-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf891-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cf891-117">-InputObject</span></span>
<span data-ttu-id="cf891-118">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="cf891-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cf891-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cf891-119">-Name</span></span>
<span data-ttu-id="cf891-120">Nazwa zasobu bota.</span><span class="sxs-lookup"><span data-stu-id="cf891-120">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="cf891-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cf891-121">-PassThru</span></span>
<span data-ttu-id="cf891-122">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="cf891-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="cf891-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf891-123">-ResourceGroupName</span></span>
<span data-ttu-id="cf891-124">Nazwa grupy zasobów bota w subskrypcji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="cf891-124">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="cf891-125">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="cf891-125">-SubscriptionId</span></span>
<span data-ttu-id="cf891-126">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cf891-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="cf891-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cf891-127">-Confirm</span></span>
<span data-ttu-id="cf891-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf891-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf891-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf891-129">-WhatIf</span></span>
<span data-ttu-id="cf891-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf891-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf891-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cf891-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf891-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf891-132">CommonParameters</span></span>
<span data-ttu-id="cf891-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf891-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf891-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cf891-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf891-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cf891-135">INPUTS</span></span>

### <span data-ttu-id="cf891-136">Microsoft. Azure. PowerShell. polecenia. BotService. models. IBotServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="cf891-136">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span></span>

## <span data-ttu-id="cf891-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cf891-137">OUTPUTS</span></span>

### <span data-ttu-id="cf891-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cf891-138">System.Boolean</span></span>

## <span data-ttu-id="cf891-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cf891-139">NOTES</span></span>

<span data-ttu-id="cf891-140">PISUJE</span><span class="sxs-lookup"><span data-stu-id="cf891-140">ALIASES</span></span>

<span data-ttu-id="cf891-141">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cf891-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cf891-142">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="cf891-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cf891-143">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cf891-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cf891-144">INPUTobject <IBotServiceIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="cf891-144">INPUTOBJECT <IBotServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cf891-145">`[ChannelName <ChannelName?>]`: Nazwa zasobu kanału.</span><span class="sxs-lookup"><span data-stu-id="cf891-145">`[ChannelName <ChannelName?>]`: The name of the Channel resource.</span></span>
  - <span data-ttu-id="cf891-146">`[ConnectionName <String>]`: Nazwa zasobu Ustawienia połączenia z usługą bota</span><span class="sxs-lookup"><span data-stu-id="cf891-146">`[ConnectionName <String>]`: The name of the Bot Service Connection Setting resource</span></span>
  - <span data-ttu-id="cf891-147">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="cf891-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cf891-148">`[ResourceGroupName <String>]`: Nazwa grupy zasobów bota w subskrypcji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="cf891-148">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="cf891-149">`[ResourceName <String>]`: Nazwa zasobu bota.</span><span class="sxs-lookup"><span data-stu-id="cf891-149">`[ResourceName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="cf891-150">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cf891-150">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="cf891-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cf891-151">RELATED LINKS</span></span>

