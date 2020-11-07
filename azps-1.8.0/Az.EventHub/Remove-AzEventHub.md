---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHub.md
ms.openlocfilehash: 1e53e1a1eb1070a9f13c9e67ea4a838358012a13
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868443"
---
# <span data-ttu-id="dd68a-101">Remove-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="dd68a-101">Remove-AzEventHub</span></span>

## <span data-ttu-id="dd68a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dd68a-102">SYNOPSIS</span></span>
<span data-ttu-id="dd68a-103">Umożliwia usunięcie określonego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="dd68a-103">Removes the specified Event Hub.</span></span>

## <span data-ttu-id="dd68a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dd68a-104">SYNTAX</span></span>

### <span data-ttu-id="dd68a-105">EventhubDefaultSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="dd68a-105">EventhubDefaultSet (Default)</span></span>
```
Remove-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd68a-106">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="dd68a-106">EventhubInputObjectSet</span></span>
```
Remove-AzEventHub [-InputObject] <PSEventHubAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd68a-107">EventhubResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd68a-107">EventhubResourceIdParameterSet</span></span>
```
Remove-AzEventHub [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd68a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="dd68a-108">DESCRIPTION</span></span>
<span data-ttu-id="dd68a-109">Polecenie cmdlet Remove-AzEventHub powoduje usunięcie i usunięcie określonego centrum zdarzeń z danego obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="dd68a-109">The Remove-AzEventHub cmdlet removes and deletes the specified Event Hub from the given namespace.</span></span>

## <span data-ttu-id="dd68a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dd68a-110">EXAMPLES</span></span>

### <span data-ttu-id="dd68a-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="dd68a-111">Example 1</span></span>
```
PS C:\> Remove-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="dd68a-112">Usuwa MyEventHubName centrum zdarzeń \` \` .</span><span class="sxs-lookup"><span data-stu-id="dd68a-112">Removes the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="dd68a-113">Przykład 2,1-wejście-przy użyciu zmiennej:</span><span class="sxs-lookup"><span data-stu-id="dd68a-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputobject = Get-AzEventHub <params>
PS C:\> Remove-AzEventHub -InputObject $inputobject
```

### <span data-ttu-id="dd68a-114">Przykład 2,2-Inputobject przy użyciu połączeń rurowych:</span><span class="sxs-lookup"><span data-stu-id="dd68a-114">Example 2.2 - InputObject Using Piping:</span></span>
```
PS C:\> Get-AzEventHub <params> | Remove-AzEventHub
```

### <span data-ttu-id="dd68a-115">Przykład 3,1-ResourceId-używa zmiennej:</span><span class="sxs-lookup"><span data-stu-id="dd68a-115">Example 3.1 - ResourceId - Using Variable:</span></span>
```
PS C:\> $resourceid = Get-AzEventHub <params>
PS C:\> Remove-AzEventHub -ResourceId $resourceid.Id
```

### <span data-ttu-id="dd68a-116">Przykład 3,1-ResourceId-przy użyciu ciągu:</span><span class="sxs-lookup"><span data-stu-id="dd68a-116">Example 3.1 - ResourceId - Using string:</span></span>
```
PS C:\> Remove-AzEventHub -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName"
```

## <span data-ttu-id="dd68a-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dd68a-117">PARAMETERS</span></span>

### <span data-ttu-id="dd68a-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd68a-118">-AsJob</span></span>
<span data-ttu-id="dd68a-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="dd68a-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dd68a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd68a-120">-DefaultProfile</span></span>
<span data-ttu-id="dd68a-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dd68a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd68a-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="dd68a-122">-InputObject</span></span>
<span data-ttu-id="dd68a-123">Obiekt Eventhub</span><span class="sxs-lookup"><span data-stu-id="dd68a-123">Eventhub Object</span></span>

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

### <span data-ttu-id="dd68a-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dd68a-124">-Name</span></span>
<span data-ttu-id="dd68a-125">Nazwa EventHub</span><span class="sxs-lookup"><span data-stu-id="dd68a-125">EventHub Name</span></span>

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

### <span data-ttu-id="dd68a-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="dd68a-126">-Namespace</span></span>
<span data-ttu-id="dd68a-127">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="dd68a-127">Namespace Name</span></span>

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

### <span data-ttu-id="dd68a-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd68a-128">-PassThru</span></span>
<span data-ttu-id="dd68a-129">Określenie tej wartości zwróci wartość PRAWDA, jeśli polecenie zostało wykonane prawidłowo.</span><span class="sxs-lookup"><span data-stu-id="dd68a-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="dd68a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd68a-130">-ResourceGroupName</span></span>
<span data-ttu-id="dd68a-131">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="dd68a-131">Resource Group Name</span></span>

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

### <span data-ttu-id="dd68a-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd68a-132">-ResourceId</span></span>
<span data-ttu-id="dd68a-133">Identyfikator zasobu Eventhub</span><span class="sxs-lookup"><span data-stu-id="dd68a-133">Eventhub Resource Id</span></span>

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

### <span data-ttu-id="dd68a-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dd68a-134">-Confirm</span></span>
<span data-ttu-id="dd68a-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd68a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd68a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd68a-136">-WhatIf</span></span>
<span data-ttu-id="dd68a-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd68a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd68a-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="dd68a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd68a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd68a-139">CommonParameters</span></span>
<span data-ttu-id="dd68a-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd68a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd68a-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd68a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd68a-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dd68a-142">INPUTS</span></span>

### <span data-ttu-id="dd68a-143">System. String</span><span class="sxs-lookup"><span data-stu-id="dd68a-143">System.String</span></span>

### <span data-ttu-id="dd68a-144">Microsoft. Azure. Commands. EventHub. modele. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="dd68a-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="dd68a-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dd68a-145">OUTPUTS</span></span>

### <span data-ttu-id="dd68a-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dd68a-146">System.Boolean</span></span>

## <span data-ttu-id="dd68a-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dd68a-147">NOTES</span></span>

## <span data-ttu-id="dd68a-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dd68a-148">RELATED LINKS</span></span>
