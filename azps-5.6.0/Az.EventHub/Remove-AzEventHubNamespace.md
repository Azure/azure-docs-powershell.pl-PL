---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/remove-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
ms.openlocfilehash: dca9094ac66e889b5a00899f6d48d6317279c1fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955921"
---
# <span data-ttu-id="a758b-101">Remove-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="a758b-101">Remove-AzEventHubNamespace</span></span>

## <span data-ttu-id="a758b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a758b-102">SYNOPSIS</span></span>
<span data-ttu-id="a758b-103">Usuwa określoną przestrzeń nazw centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="a758b-103">Removes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="a758b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a758b-104">SYNTAX</span></span>

### <span data-ttu-id="a758b-105">NamespaceParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="a758b-105">NamespaceParameterSet (Default)</span></span>
```
Remove-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a758b-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a758b-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a758b-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a758b-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzEventHubNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a758b-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="a758b-108">DESCRIPTION</span></span>
<span data-ttu-id="a758b-109">To Remove-AzEventHubNamespace cmdlet usuwa określoną przestrzeń nazw centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="a758b-109">The Remove-AzEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="a758b-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a758b-110">EXAMPLES</span></span>

### <span data-ttu-id="a758b-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a758b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="a758b-112">Usuwa przestrzeń nazw MyNamespaceName (Nazwa_domeny) centrum zdarzeń w \` \` grupie zasobów \` MyResourceGroupName (Nazwa_grupy \` zasobów).</span><span class="sxs-lookup"><span data-stu-id="a758b-112">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a758b-113">Przykład 2. InputObject — używanie zmiennej:</span><span class="sxs-lookup"><span data-stu-id="a758b-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputObject = Get-AzEventHubNamespace <params> 
PS C:\> Remove-AzEventHubNamespace -InputObject $inputObject
```

### <span data-ttu-id="a758b-114">Przykład 3. InputObject — używanie funkcji rurowych:</span><span class="sxs-lookup"><span data-stu-id="a758b-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\> Get-AzEventHubNamespace <params> | Remove-AzEventHubNamespace
```

### <span data-ttu-id="a758b-115">Przykład 4. ResourceId — używanie zmiennej</span><span class="sxs-lookup"><span data-stu-id="a758b-115">Example 4: ResourceId - Using Variable</span></span>
```powershell
PS C:\> $resourceid = Get-AzEventHubNamespace <params>
PS C:\> Remove-AzEventHubNamespace -ResourceId $resourceid.Id
```

### <span data-ttu-id="a758b-116">Przykład 5. ZasóbId — używanie funkcji rurowych:</span><span class="sxs-lookup"><span data-stu-id="a758b-116">Example 5: ResourceId - Using Piping:</span></span>
```powershell
PS C:\> Get-AzResource -ResourceType Microsoft.EventHub/Namespaces | Remove-AzEventHubNamespace
```

### <span data-ttu-id="a758b-117">Przykład 6. Wartość ResourceId — używanie ciągu:</span><span class="sxs-lookup"><span data-stu-id="a758b-117">Example 6: ResourceId - Using String:</span></span>
```powershell
PS C:\> Remove-AzEventHubNamespace -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName"
```

## <span data-ttu-id="a758b-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a758b-118">PARAMETERS</span></span>

### <span data-ttu-id="a758b-119">— AsJob</span><span class="sxs-lookup"><span data-stu-id="a758b-119">-AsJob</span></span>
<span data-ttu-id="a758b-120">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a758b-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a758b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a758b-121">-DefaultProfile</span></span>
<span data-ttu-id="a758b-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a758b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a758b-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a758b-123">-InputObject</span></span>
<span data-ttu-id="a758b-124">Obiekt przestrzeni nazw w usłudze EventHubs</span><span class="sxs-lookup"><span data-stu-id="a758b-124">EventHubs Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a758b-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a758b-125">-Name</span></span>
<span data-ttu-id="a758b-126">Nazwa przestrzeni nazw aplikacji EventHub</span><span class="sxs-lookup"><span data-stu-id="a758b-126">EventHub Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceParameterSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a758b-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a758b-127">-PassThru</span></span>
<span data-ttu-id="a758b-128">Określenie tej wartości spowoduje zwrócenie wartości prawda, jeśli polecenie zostało pomyślnie określone.</span><span class="sxs-lookup"><span data-stu-id="a758b-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="a758b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a758b-129">-ResourceGroupName</span></span>
<span data-ttu-id="a758b-130">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a758b-130">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a758b-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a758b-131">-ResourceId</span></span>
<span data-ttu-id="a758b-132">Identyfikator zasobu przestrzeni nazw aplikacji EventHubs</span><span class="sxs-lookup"><span data-stu-id="a758b-132">EventHubs Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a758b-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a758b-133">-Confirm</span></span>
<span data-ttu-id="a758b-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a758b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a758b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a758b-135">-WhatIf</span></span>
<span data-ttu-id="a758b-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a758b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a758b-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a758b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a758b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a758b-138">CommonParameters</span></span>
<span data-ttu-id="a758b-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a758b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a758b-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a758b-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a758b-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a758b-141">INPUTS</span></span>

### <span data-ttu-id="a758b-142">System.String</span><span class="sxs-lookup"><span data-stu-id="a758b-142">System.String</span></span>

### <span data-ttu-id="a758b-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="a758b-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="a758b-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a758b-144">OUTPUTS</span></span>

### <span data-ttu-id="a758b-145">System.Void</span><span class="sxs-lookup"><span data-stu-id="a758b-145">System.Void</span></span>

## <span data-ttu-id="a758b-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a758b-146">NOTES</span></span>

## <span data-ttu-id="a758b-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a758b-147">RELATED LINKS</span></span>
