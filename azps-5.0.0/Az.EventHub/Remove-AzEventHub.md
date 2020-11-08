---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHub.md
ms.openlocfilehash: daa63859c9649d9467f750f77d5b0e466d03ff56
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224426"
---
# <span data-ttu-id="614f6-101">Remove-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="614f6-101">Remove-AzEventHub</span></span>

## <span data-ttu-id="614f6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="614f6-102">SYNOPSIS</span></span>
<span data-ttu-id="614f6-103">Umożliwia usunięcie określonego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="614f6-103">Removes the specified Event Hub.</span></span>

## <span data-ttu-id="614f6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="614f6-104">SYNTAX</span></span>

### <span data-ttu-id="614f6-105">EventhubDefaultSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="614f6-105">EventhubDefaultSet (Default)</span></span>
```
Remove-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="614f6-106">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="614f6-106">EventhubInputObjectSet</span></span>
```
Remove-AzEventHub [-InputObject] <PSEventHubAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="614f6-107">EventhubResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="614f6-107">EventhubResourceIdParameterSet</span></span>
```
Remove-AzEventHub [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="614f6-108">Opis</span><span class="sxs-lookup"><span data-stu-id="614f6-108">DESCRIPTION</span></span>
<span data-ttu-id="614f6-109">Polecenie cmdlet Remove-AzEventHub powoduje usunięcie i usunięcie określonego centrum zdarzeń z danego obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="614f6-109">The Remove-AzEventHub cmdlet removes and deletes the specified Event Hub from the given namespace.</span></span>

## <span data-ttu-id="614f6-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="614f6-110">EXAMPLES</span></span>

### <span data-ttu-id="614f6-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="614f6-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="614f6-112">Usuwa MyEventHubName centrum zdarzeń \` \` .</span><span class="sxs-lookup"><span data-stu-id="614f6-112">Removes the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="614f6-113">Przykład 2: wejście-przy użyciu zmiennej:</span><span class="sxs-lookup"><span data-stu-id="614f6-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzEventHub <params>
PS C:\> Remove-AzEventHub -InputObject $inputobject
```

### <span data-ttu-id="614f6-114">Przykład 3: wejście przy użyciu połączeń rurowych:</span><span class="sxs-lookup"><span data-stu-id="614f6-114">Example 3: InputObject Using Piping:</span></span>
```powershell
PS C:\> Get-AzEventHub <params> | Remove-AzEventHub
```

### <span data-ttu-id="614f6-115">Przykład 4: Identyfikator ResourceId używający zmiennej:</span><span class="sxs-lookup"><span data-stu-id="614f6-115">Example 4: ResourceId - Using Variable:</span></span>
```powershell
PS C:\> $resourceid = Get-AzEventHub <params>
PS C:\> Remove-AzEventHub -ResourceId $resourceid.Id
```

### <span data-ttu-id="614f6-116">Przykład 5: ResourceId — używanie ciągu:</span><span class="sxs-lookup"><span data-stu-id="614f6-116">Example 5: ResourceId - Using string:</span></span>
```powershell
PS C:\> Remove-AzEventHub -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName"
```

## <span data-ttu-id="614f6-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="614f6-117">PARAMETERS</span></span>

### <span data-ttu-id="614f6-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="614f6-118">-AsJob</span></span>
<span data-ttu-id="614f6-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="614f6-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="614f6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="614f6-120">-DefaultProfile</span></span>
<span data-ttu-id="614f6-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="614f6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="614f6-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="614f6-122">-InputObject</span></span>
<span data-ttu-id="614f6-123">Obiekt Eventhub</span><span class="sxs-lookup"><span data-stu-id="614f6-123">Eventhub Object</span></span>

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

### <span data-ttu-id="614f6-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="614f6-124">-Name</span></span>
<span data-ttu-id="614f6-125">Nazwa EventHub</span><span class="sxs-lookup"><span data-stu-id="614f6-125">EventHub Name</span></span>

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

### <span data-ttu-id="614f6-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="614f6-126">-Namespace</span></span>
<span data-ttu-id="614f6-127">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="614f6-127">Namespace Name</span></span>

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

### <span data-ttu-id="614f6-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="614f6-128">-PassThru</span></span>
<span data-ttu-id="614f6-129">Określenie tej wartości zwróci wartość PRAWDA, jeśli polecenie zostało wykonane prawidłowo.</span><span class="sxs-lookup"><span data-stu-id="614f6-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="614f6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="614f6-130">-ResourceGroupName</span></span>
<span data-ttu-id="614f6-131">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="614f6-131">Resource Group Name</span></span>

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

### <span data-ttu-id="614f6-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="614f6-132">-ResourceId</span></span>
<span data-ttu-id="614f6-133">Identyfikator zasobu Eventhub</span><span class="sxs-lookup"><span data-stu-id="614f6-133">Eventhub Resource Id</span></span>

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

### <span data-ttu-id="614f6-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="614f6-134">-Confirm</span></span>
<span data-ttu-id="614f6-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="614f6-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="614f6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="614f6-136">-WhatIf</span></span>
<span data-ttu-id="614f6-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="614f6-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="614f6-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="614f6-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="614f6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="614f6-139">CommonParameters</span></span>
<span data-ttu-id="614f6-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="614f6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="614f6-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="614f6-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="614f6-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="614f6-142">INPUTS</span></span>

### <span data-ttu-id="614f6-143">System. String</span><span class="sxs-lookup"><span data-stu-id="614f6-143">System.String</span></span>

### <span data-ttu-id="614f6-144">Microsoft. Azure. Commands. EventHub. modele. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="614f6-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="614f6-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="614f6-145">OUTPUTS</span></span>

### <span data-ttu-id="614f6-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="614f6-146">System.Boolean</span></span>

## <span data-ttu-id="614f6-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="614f6-147">NOTES</span></span>

## <span data-ttu-id="614f6-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="614f6-148">RELATED LINKS</span></span>
