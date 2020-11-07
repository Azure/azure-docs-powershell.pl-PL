---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
ms.openlocfilehash: 38a727c2e632173befe6b5b08756d558a9c9f177
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891438"
---
# <span data-ttu-id="b8fec-101">Remove-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="b8fec-101">Remove-AzEventHubNamespace</span></span>

## <span data-ttu-id="b8fec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b8fec-102">SYNOPSIS</span></span>
<span data-ttu-id="b8fec-103">Usuwa określoną przestrzeń nazw koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="b8fec-103">Removes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="b8fec-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b8fec-104">SYNTAX</span></span>

### <span data-ttu-id="b8fec-105">NamespaceParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b8fec-105">NamespaceParameterSet (Default)</span></span>
```
Remove-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8fec-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b8fec-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8fec-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8fec-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzEventHubNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8fec-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b8fec-108">DESCRIPTION</span></span>
<span data-ttu-id="b8fec-109">Polecenie cmdlet Remove-AzEventHubNamespace powoduje usunięcie i usunięcie określonego obszaru nazw koncentratora zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="b8fec-109">The Remove-AzEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="b8fec-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b8fec-110">EXAMPLES</span></span>

### <span data-ttu-id="b8fec-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b8fec-111">Example 1</span></span>
```
PS C:\> Remove-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="b8fec-112">Usuwa przestrzeń nazw Hub zdarzeń \` \` w MyResourceGroupName grupy zasobów \` \` .</span><span class="sxs-lookup"><span data-stu-id="b8fec-112">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="b8fec-113">Przykład 2,1-wejście-przy użyciu zmiennej:</span><span class="sxs-lookup"><span data-stu-id="b8fec-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputObject = Get-AzEventHubNamespace <params> 
PS C:\> Remove-AzEventHubNamespace -InputObject $inputObject
```

### <span data-ttu-id="b8fec-114">Przykład 2,1-Inputobject-przy użyciu instalacji rurowej:</span><span class="sxs-lookup"><span data-stu-id="b8fec-114">Example 2.1 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzEventHubNamespace <params> | Remove-AzEventHubNamespace
```

### <span data-ttu-id="b8fec-115">Przykład 3,1-ResourceId-używa zmiennej</span><span class="sxs-lookup"><span data-stu-id="b8fec-115">Example 3.1 - ResourceId - Using Variable</span></span>
```
PS C:\> $resourceid = Get-AzEventHubNamespace <params>
PS C:\> Remove-AzEventHubNamespace -ResourceId $resourceid.Id
```

### <span data-ttu-id="b8fec-116">Przykład 3,2-ResourceId — korzystanie z połączeń rurowych:</span><span class="sxs-lookup"><span data-stu-id="b8fec-116">Example 3.2 - ResourceId - Using Piping:</span></span>
```
PS C:\> Get-AzResource -ResourceType Microsoft.EventHub/Namespaces | Remove-AzEventHubNamespace
```

### <span data-ttu-id="b8fec-117">Przykład 3,3-ResourceId-przy użyciu ciągu:</span><span class="sxs-lookup"><span data-stu-id="b8fec-117">Example 3.3 - ResourceId - Using String:</span></span>
```
PS C:\> Remove-AzEventHubNamespace -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName"
```

## <span data-ttu-id="b8fec-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b8fec-118">PARAMETERS</span></span>

### <span data-ttu-id="b8fec-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8fec-119">-AsJob</span></span>
<span data-ttu-id="b8fec-120">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b8fec-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b8fec-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8fec-121">-DefaultProfile</span></span>
<span data-ttu-id="b8fec-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b8fec-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8fec-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b8fec-123">-InputObject</span></span>
<span data-ttu-id="b8fec-124">Obiekt przestrzeni nazw EventHubs</span><span class="sxs-lookup"><span data-stu-id="b8fec-124">EventHubs Namespace Object</span></span>

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

### <span data-ttu-id="b8fec-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b8fec-125">-Name</span></span>
<span data-ttu-id="b8fec-126">Nazwa obszaru nazw EventHub</span><span class="sxs-lookup"><span data-stu-id="b8fec-126">EventHub Namespace Name</span></span>

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

### <span data-ttu-id="b8fec-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b8fec-127">-PassThru</span></span>
<span data-ttu-id="b8fec-128">Określenie tej wartości zwróci wartość PRAWDA, jeśli polecenie zostało wykonane prawidłowo.</span><span class="sxs-lookup"><span data-stu-id="b8fec-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="b8fec-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8fec-129">-ResourceGroupName</span></span>
<span data-ttu-id="b8fec-130">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b8fec-130">Resource Group Name</span></span>

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

### <span data-ttu-id="b8fec-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8fec-131">-ResourceId</span></span>
<span data-ttu-id="b8fec-132">Identyfikator zasobu EventHubs Namespace</span><span class="sxs-lookup"><span data-stu-id="b8fec-132">EventHubs Namespace Resource Id</span></span>

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

### <span data-ttu-id="b8fec-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b8fec-133">-Confirm</span></span>
<span data-ttu-id="b8fec-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8fec-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8fec-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8fec-135">-WhatIf</span></span>
<span data-ttu-id="b8fec-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8fec-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8fec-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b8fec-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8fec-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8fec-138">CommonParameters</span></span>
<span data-ttu-id="b8fec-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8fec-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8fec-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8fec-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8fec-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b8fec-141">INPUTS</span></span>

### <span data-ttu-id="b8fec-142">System. String</span><span class="sxs-lookup"><span data-stu-id="b8fec-142">System.String</span></span>

### <span data-ttu-id="b8fec-143">Microsoft. Azure. Commands. EventHub. modele. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="b8fec-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="b8fec-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b8fec-144">OUTPUTS</span></span>

### <span data-ttu-id="b8fec-145">System. void</span><span class="sxs-lookup"><span data-stu-id="b8fec-145">System.Void</span></span>

## <span data-ttu-id="b8fec-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b8fec-146">NOTES</span></span>

## <span data-ttu-id="b8fec-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b8fec-147">RELATED LINKS</span></span>
