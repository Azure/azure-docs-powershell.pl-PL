---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
ms.openlocfilehash: 6df8d5539bf340df5e00ad69ac557bc2cbb8ccaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545359"
---
# <span data-ttu-id="30596-101">Remove-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="30596-101">Remove-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="30596-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="30596-102">SYNOPSIS</span></span>
<span data-ttu-id="30596-103">Usuwa określoną przestrzeń nazw koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="30596-103">Removes the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30596-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="30596-104">SYNTAX</span></span>

### <span data-ttu-id="30596-105">NamespaceParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="30596-105">NamespaceParameterSet (Default)</span></span>
```
Remove-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30596-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="30596-106">NamespaceInputObjectSet</span></span>
```
Remove-AzureRmEventHubNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30596-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="30596-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzureRmEventHubNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30596-108">Opis</span><span class="sxs-lookup"><span data-stu-id="30596-108">DESCRIPTION</span></span>
<span data-ttu-id="30596-109">Polecenie cmdlet Remove-AzureRmEventHubNamespace powoduje usunięcie i usunięcie określonego obszaru nazw koncentratora zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="30596-109">The Remove-AzureRmEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="30596-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="30596-110">EXAMPLES</span></span>

### <span data-ttu-id="30596-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="30596-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="30596-112">Usuwa przestrzeń nazw Hub zdarzeń \` \` w MyResourceGroupName grupy zasobów \` \` .</span><span class="sxs-lookup"><span data-stu-id="30596-112">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="30596-113">Przykład 2,1-wejście-przy użyciu zmiennej:</span><span class="sxs-lookup"><span data-stu-id="30596-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputObject = Get-AzureRmEventHubNamespace <params> 
PS C:\> Remove-AzureRmEventHubNamespace -InputObject $inputObject
```

### <span data-ttu-id="30596-114">Przykład 2,1-Inputobject-przy użyciu instalacji rurowej:</span><span class="sxs-lookup"><span data-stu-id="30596-114">Example 2.1 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzureRmEventHubNamespace <params> | Remove-AzureRmEventHubNamespace
```

### <span data-ttu-id="30596-115">Przykład 3,1-ResourceId-używa zmiennej</span><span class="sxs-lookup"><span data-stu-id="30596-115">Example 3.1 - ResourceId - Using Variable</span></span>
```
PS C:\> $resourceid = Get-AzureRmEventHubNamespace <params>
PS C:\> Remove-AzureRmEventHubNamespace -ResourceId $resourceid.Id
```

### <span data-ttu-id="30596-116">Przykład 3,2-ResourceId — korzystanie z połączeń rurowych:</span><span class="sxs-lookup"><span data-stu-id="30596-116">Example 3.2 - ResourceId - Using Piping:</span></span>
```
PS C:\> Get-AzureRmResource -ResourceType Microsoft.EventHub/Namespaces | Remove-AzureRmEventHubNamespace
```

### <span data-ttu-id="30596-117">Przykład 3,3-ResourceId-przy użyciu ciągu:</span><span class="sxs-lookup"><span data-stu-id="30596-117">Example 3.3 - ResourceId - Using String:</span></span>
```
PS C:\> Remove-AzureRmEventHubNamespace -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName"
```

## <span data-ttu-id="30596-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="30596-118">PARAMETERS</span></span>

### <span data-ttu-id="30596-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="30596-119">-AsJob</span></span>
<span data-ttu-id="30596-120">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="30596-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="30596-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30596-121">-DefaultProfile</span></span>
<span data-ttu-id="30596-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="30596-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30596-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="30596-123">-InputObject</span></span>
<span data-ttu-id="30596-124">Obiekt przestrzeni nazw EventHubs</span><span class="sxs-lookup"><span data-stu-id="30596-124">EventHubs Namespace Object</span></span>

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

### <span data-ttu-id="30596-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="30596-125">-Name</span></span>
<span data-ttu-id="30596-126">Nazwa obszaru nazw EventHub</span><span class="sxs-lookup"><span data-stu-id="30596-126">EventHub Namespace Name</span></span>

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

### <span data-ttu-id="30596-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="30596-127">-PassThru</span></span>
<span data-ttu-id="30596-128">Określenie tej wartości zwróci wartość PRAWDA, jeśli polecenie zostało wykonane prawidłowo.</span><span class="sxs-lookup"><span data-stu-id="30596-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="30596-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30596-129">-ResourceGroupName</span></span>
<span data-ttu-id="30596-130">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="30596-130">Resource Group Name</span></span>

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

### <span data-ttu-id="30596-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="30596-131">-ResourceId</span></span>
<span data-ttu-id="30596-132">Identyfikator zasobu EventHubs Namespace</span><span class="sxs-lookup"><span data-stu-id="30596-132">EventHubs Namespace Resource Id</span></span>

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

### <span data-ttu-id="30596-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="30596-133">-Confirm</span></span>
<span data-ttu-id="30596-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30596-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30596-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30596-135">-WhatIf</span></span>
<span data-ttu-id="30596-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30596-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30596-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="30596-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30596-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30596-138">CommonParameters</span></span>
<span data-ttu-id="30596-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30596-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30596-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30596-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30596-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="30596-141">INPUTS</span></span>

### <span data-ttu-id="30596-142">System. String</span><span class="sxs-lookup"><span data-stu-id="30596-142">System.String</span></span>

### <span data-ttu-id="30596-143">Microsoft. Azure. Commands. EventHub. modele. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="30596-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="30596-144">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="30596-144">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="30596-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="30596-145">OUTPUTS</span></span>

### <span data-ttu-id="30596-146">System. void</span><span class="sxs-lookup"><span data-stu-id="30596-146">System.Void</span></span>

## <span data-ttu-id="30596-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="30596-147">NOTES</span></span>

## <span data-ttu-id="30596-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="30596-148">RELATED LINKS</span></span>
