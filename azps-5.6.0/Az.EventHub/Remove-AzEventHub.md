---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/remove-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHub.md
ms.openlocfilehash: 2d3f2ee9a4dc55dd709be3113770df402434c911
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992783"
---
# <span data-ttu-id="7f05d-101">Remove-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="7f05d-101">Remove-AzEventHub</span></span>

## <span data-ttu-id="7f05d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f05d-102">SYNOPSIS</span></span>
<span data-ttu-id="7f05d-103">Usuwa określone centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="7f05d-103">Removes the specified Event Hub.</span></span>

## <span data-ttu-id="7f05d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7f05d-104">SYNTAX</span></span>

### <span data-ttu-id="7f05d-105">EventhubDefaultSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="7f05d-105">EventhubDefaultSet (Default)</span></span>
```
Remove-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f05d-106">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7f05d-106">EventhubInputObjectSet</span></span>
```
Remove-AzEventHub [-InputObject] <PSEventHubAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f05d-107">EventhubResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f05d-107">EventhubResourceIdParameterSet</span></span>
```
Remove-AzEventHub [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f05d-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="7f05d-108">DESCRIPTION</span></span>
<span data-ttu-id="7f05d-109">Polecenie Remove-AzEventHub cmdlet usuwa określone centrum zdarzeń z danej przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="7f05d-109">The Remove-AzEventHub cmdlet removes and deletes the specified Event Hub from the given namespace.</span></span>

## <span data-ttu-id="7f05d-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7f05d-110">EXAMPLES</span></span>

### <span data-ttu-id="7f05d-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7f05d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="7f05d-112">Usuwa nazwę \` MyEventHubName centrum \` zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="7f05d-112">Removes the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="7f05d-113">Przykład 2. InputObject — używanie zmiennej:</span><span class="sxs-lookup"><span data-stu-id="7f05d-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzEventHub <params>
PS C:\> Remove-AzEventHub -InputObject $inputobject
```

### <span data-ttu-id="7f05d-114">Przykład 3. InputObject using Piping:</span><span class="sxs-lookup"><span data-stu-id="7f05d-114">Example 3: InputObject Using Piping:</span></span>
```powershell
PS C:\> Get-AzEventHub <params> | Remove-AzEventHub
```

### <span data-ttu-id="7f05d-115">Przykład 4. ResourceId — używanie zmiennej:</span><span class="sxs-lookup"><span data-stu-id="7f05d-115">Example 4: ResourceId - Using Variable:</span></span>
```powershell
PS C:\> $resourceid = Get-AzEventHub <params>
PS C:\> Remove-AzEventHub -ResourceId $resourceid.Id
```

### <span data-ttu-id="7f05d-116">Przykład 5. ResourceId — używanie ciągu:</span><span class="sxs-lookup"><span data-stu-id="7f05d-116">Example 5: ResourceId - Using string:</span></span>
```powershell
PS C:\> Remove-AzEventHub -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName"
```

## <span data-ttu-id="7f05d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f05d-117">PARAMETERS</span></span>

### <span data-ttu-id="7f05d-118">— AsJob</span><span class="sxs-lookup"><span data-stu-id="7f05d-118">-AsJob</span></span>
<span data-ttu-id="7f05d-119">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="7f05d-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7f05d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f05d-120">-DefaultProfile</span></span>
<span data-ttu-id="7f05d-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7f05d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f05d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7f05d-122">-InputObject</span></span>
<span data-ttu-id="7f05d-123">Obiekt Eventhub</span><span class="sxs-lookup"><span data-stu-id="7f05d-123">Eventhub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes
Parameter Sets: EventhubInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f05d-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7f05d-124">-Name</span></span>
<span data-ttu-id="7f05d-125">Nazwa aplikacji EventHub</span><span class="sxs-lookup"><span data-stu-id="7f05d-125">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubDefaultSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f05d-126">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="7f05d-126">-Namespace</span></span>
<span data-ttu-id="7f05d-127">Nazwa przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="7f05d-127">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubDefaultSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f05d-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7f05d-128">-PassThru</span></span>
<span data-ttu-id="7f05d-129">Określenie tej wartości spowoduje zwrócenie wartości prawda, jeśli polecenie zostało pomyślnie określone.</span><span class="sxs-lookup"><span data-stu-id="7f05d-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="7f05d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f05d-130">-ResourceGroupName</span></span>
<span data-ttu-id="7f05d-131">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="7f05d-131">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubDefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f05d-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f05d-132">-ResourceId</span></span>
<span data-ttu-id="7f05d-133">Identyfikator zasobu aplikacji Eventhub</span><span class="sxs-lookup"><span data-stu-id="7f05d-133">Eventhub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f05d-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7f05d-134">-Confirm</span></span>
<span data-ttu-id="7f05d-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7f05d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f05d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f05d-136">-WhatIf</span></span>
<span data-ttu-id="7f05d-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f05d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f05d-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7f05d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f05d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f05d-139">CommonParameters</span></span>
<span data-ttu-id="7f05d-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f05d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f05d-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f05d-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f05d-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7f05d-142">INPUTS</span></span>

### <span data-ttu-id="7f05d-143">System.String</span><span class="sxs-lookup"><span data-stu-id="7f05d-143">System.String</span></span>

### <span data-ttu-id="7f05d-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="7f05d-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="7f05d-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7f05d-145">OUTPUTS</span></span>

### <span data-ttu-id="7f05d-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7f05d-146">System.Boolean</span></span>

## <span data-ttu-id="7f05d-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7f05d-147">NOTES</span></span>

## <span data-ttu-id="7f05d-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7f05d-148">RELATED LINKS</span></span>
