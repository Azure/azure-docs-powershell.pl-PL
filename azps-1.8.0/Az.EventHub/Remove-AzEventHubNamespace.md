---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
ms.openlocfilehash: 4d5ddbc4dff2922b90bc6d1117ff32473afd9042
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709794"
---
# <span data-ttu-id="11220-101">Remove-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="11220-101">Remove-AzEventHubNamespace</span></span>

## <span data-ttu-id="11220-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="11220-102">SYNOPSIS</span></span>
<span data-ttu-id="11220-103">Usuwa określoną przestrzeń nazw koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="11220-103">Removes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="11220-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="11220-104">SYNTAX</span></span>

### <span data-ttu-id="11220-105">NamespaceParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="11220-105">NamespaceParameterSet (Default)</span></span>
```
Remove-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11220-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="11220-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11220-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="11220-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzEventHubNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11220-108">Opis</span><span class="sxs-lookup"><span data-stu-id="11220-108">DESCRIPTION</span></span>
<span data-ttu-id="11220-109">Polecenie cmdlet Remove-AzEventHubNamespace powoduje usunięcie i usunięcie określonego obszaru nazw koncentratora zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="11220-109">The Remove-AzEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="11220-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="11220-110">EXAMPLES</span></span>

### <span data-ttu-id="11220-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="11220-111">Example 1</span></span>
```
PS C:\> Remove-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="11220-112">Usuwa przestrzeń nazw Hub zdarzeń \` \` w MyResourceGroupName grupy zasobów \` \` .</span><span class="sxs-lookup"><span data-stu-id="11220-112">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="11220-113">Przykład 2,1-wejście-przy użyciu zmiennej:</span><span class="sxs-lookup"><span data-stu-id="11220-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputObject = Get-AzEventHubNamespace <params> 
PS C:\> Remove-AzEventHubNamespace -InputObject $inputObject
```

### <span data-ttu-id="11220-114">Przykład 2,1-Inputobject-przy użyciu instalacji rurowej:</span><span class="sxs-lookup"><span data-stu-id="11220-114">Example 2.1 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzEventHubNamespace <params> | Remove-AzEventHubNamespace
```

### <span data-ttu-id="11220-115">Przykład 3,1-ResourceId-używa zmiennej</span><span class="sxs-lookup"><span data-stu-id="11220-115">Example 3.1 - ResourceId - Using Variable</span></span>
```
PS C:\> $resourceid = Get-AzEventHubNamespace <params>
PS C:\> Remove-AzEventHubNamespace -ResourceId $resourceid.Id
```

### <span data-ttu-id="11220-116">Przykład 3,2-ResourceId — korzystanie z połączeń rurowych:</span><span class="sxs-lookup"><span data-stu-id="11220-116">Example 3.2 - ResourceId - Using Piping:</span></span>
```
PS C:\> Get-AzResource -ResourceType Microsoft.EventHub/Namespaces | Remove-AzEventHubNamespace
```

### <span data-ttu-id="11220-117">Przykład 3,3-ResourceId-przy użyciu ciągu:</span><span class="sxs-lookup"><span data-stu-id="11220-117">Example 3.3 - ResourceId - Using String:</span></span>
```
PS C:\> Remove-AzEventHubNamespace -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName"
```

## <span data-ttu-id="11220-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="11220-118">PARAMETERS</span></span>

### <span data-ttu-id="11220-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11220-119">-AsJob</span></span>
<span data-ttu-id="11220-120">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="11220-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="11220-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11220-121">-DefaultProfile</span></span>
<span data-ttu-id="11220-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="11220-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11220-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="11220-123">-InputObject</span></span>
<span data-ttu-id="11220-124">Obiekt przestrzeni nazw EventHubs</span><span class="sxs-lookup"><span data-stu-id="11220-124">EventHubs Namespace Object</span></span>

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

### <span data-ttu-id="11220-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="11220-125">-Name</span></span>
<span data-ttu-id="11220-126">Nazwa obszaru nazw EventHub</span><span class="sxs-lookup"><span data-stu-id="11220-126">EventHub Namespace Name</span></span>

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

### <span data-ttu-id="11220-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="11220-127">-PassThru</span></span>
<span data-ttu-id="11220-128">Określenie tej wartości zwróci wartość PRAWDA, jeśli polecenie zostało wykonane prawidłowo.</span><span class="sxs-lookup"><span data-stu-id="11220-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="11220-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11220-129">-ResourceGroupName</span></span>
<span data-ttu-id="11220-130">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="11220-130">Resource Group Name</span></span>

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

### <span data-ttu-id="11220-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11220-131">-ResourceId</span></span>
<span data-ttu-id="11220-132">Identyfikator zasobu EventHubs Namespace</span><span class="sxs-lookup"><span data-stu-id="11220-132">EventHubs Namespace Resource Id</span></span>

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

### <span data-ttu-id="11220-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="11220-133">-Confirm</span></span>
<span data-ttu-id="11220-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11220-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11220-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11220-135">-WhatIf</span></span>
<span data-ttu-id="11220-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11220-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11220-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="11220-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11220-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11220-138">CommonParameters</span></span>
<span data-ttu-id="11220-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11220-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11220-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11220-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11220-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11220-141">INPUTS</span></span>

### <span data-ttu-id="11220-142">System. String</span><span class="sxs-lookup"><span data-stu-id="11220-142">System.String</span></span>

### <span data-ttu-id="11220-143">Microsoft. Azure. Commands. EventHub. modele. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="11220-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="11220-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="11220-144">OUTPUTS</span></span>

### <span data-ttu-id="11220-145">System. void</span><span class="sxs-lookup"><span data-stu-id="11220-145">System.Void</span></span>

## <span data-ttu-id="11220-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="11220-146">NOTES</span></span>

## <span data-ttu-id="11220-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="11220-147">RELATED LINKS</span></span>