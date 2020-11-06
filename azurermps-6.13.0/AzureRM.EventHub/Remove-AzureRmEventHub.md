---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
ms.openlocfilehash: 31ed4d8765599fcc99f58870b347a14cdaf00162
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548664"
---
# <span data-ttu-id="92950-101">Remove-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="92950-101">Remove-AzureRmEventHub</span></span>

## <span data-ttu-id="92950-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="92950-102">SYNOPSIS</span></span>
<span data-ttu-id="92950-103">Umożliwia usunięcie określonego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="92950-103">Removes the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92950-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="92950-104">SYNTAX</span></span>

### <span data-ttu-id="92950-105">EventhubDefaultSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="92950-105">EventhubDefaultSet (Default)</span></span>
```
Remove-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92950-106">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="92950-106">EventhubInputObjectSet</span></span>
```
Remove-AzureRmEventHub [-InputObject] <PSEventHubAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92950-107">EventhubResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="92950-107">EventhubResourceIdParameterSet</span></span>
```
Remove-AzureRmEventHub [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92950-108">Opis</span><span class="sxs-lookup"><span data-stu-id="92950-108">DESCRIPTION</span></span>
<span data-ttu-id="92950-109">Polecenie cmdlet Remove-AzureRmEventHub powoduje usunięcie i usunięcie określonego centrum zdarzeń z danego obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="92950-109">The Remove-AzureRmEventHub cmdlet removes and deletes the specified Event Hub from the given namespace.</span></span>

## <span data-ttu-id="92950-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="92950-110">EXAMPLES</span></span>

### <span data-ttu-id="92950-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="92950-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="92950-112">Usuwa MyEventHubName centrum zdarzeń \` \` .</span><span class="sxs-lookup"><span data-stu-id="92950-112">Removes the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="92950-113">Przykład 2,1-wejście-przy użyciu zmiennej:</span><span class="sxs-lookup"><span data-stu-id="92950-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputobject = Get-AzureRmEventHub <params>
PS C:\> Remove-AzureRmEventHub -InputObject $inputobject
```

### <span data-ttu-id="92950-114">Przykład 2,2-Inputobject przy użyciu połączeń rurowych:</span><span class="sxs-lookup"><span data-stu-id="92950-114">Example 2.2 - InputObject Using Piping:</span></span>
```
PS C:\> Get-AzureRmEventHub <params> | Remove-AzureRmEventHub
```

### <span data-ttu-id="92950-115">Przykład 3,1-ResourceId-używa zmiennej:</span><span class="sxs-lookup"><span data-stu-id="92950-115">Example 3.1 - ResourceId - Using Variable:</span></span>
```
PS C:\> $resourceid = Get-AzureRmEventHub <params>
PS C:\> Remove-AzureRmEventHub -ResourceId $resourceid.Id
```

### <span data-ttu-id="92950-116">Przykład 3,1-ResourceId-przy użyciu ciągu:</span><span class="sxs-lookup"><span data-stu-id="92950-116">Example 3.1 - ResourceId - Using string:</span></span>
```
PS C:\> Remove-AzureRmEventHub -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName"
```

## <span data-ttu-id="92950-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="92950-117">PARAMETERS</span></span>

### <span data-ttu-id="92950-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="92950-118">-AsJob</span></span>
<span data-ttu-id="92950-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="92950-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="92950-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92950-120">-DefaultProfile</span></span>
<span data-ttu-id="92950-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="92950-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92950-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="92950-122">-InputObject</span></span>
<span data-ttu-id="92950-123">Obiekt Eventhub</span><span class="sxs-lookup"><span data-stu-id="92950-123">Eventhub Object</span></span>

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

### <span data-ttu-id="92950-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="92950-124">-Name</span></span>
<span data-ttu-id="92950-125">Nazwa EventHub</span><span class="sxs-lookup"><span data-stu-id="92950-125">EventHub Name</span></span>

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

### <span data-ttu-id="92950-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="92950-126">-Namespace</span></span>
<span data-ttu-id="92950-127">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="92950-127">Namespace Name</span></span>

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

### <span data-ttu-id="92950-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92950-128">-PassThru</span></span>
<span data-ttu-id="92950-129">Określenie tej wartości zwróci wartość PRAWDA, jeśli polecenie zostało wykonane prawidłowo.</span><span class="sxs-lookup"><span data-stu-id="92950-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="92950-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92950-130">-ResourceGroupName</span></span>
<span data-ttu-id="92950-131">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="92950-131">Resource Group Name</span></span>

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

### <span data-ttu-id="92950-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="92950-132">-ResourceId</span></span>
<span data-ttu-id="92950-133">Identyfikator zasobu Eventhub</span><span class="sxs-lookup"><span data-stu-id="92950-133">Eventhub Resource Id</span></span>

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

### <span data-ttu-id="92950-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="92950-134">-Confirm</span></span>
<span data-ttu-id="92950-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92950-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92950-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92950-136">-WhatIf</span></span>
<span data-ttu-id="92950-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92950-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92950-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="92950-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92950-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92950-139">CommonParameters</span></span>
<span data-ttu-id="92950-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92950-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92950-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92950-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92950-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="92950-142">INPUTS</span></span>

### <span data-ttu-id="92950-143">System. String</span><span class="sxs-lookup"><span data-stu-id="92950-143">System.String</span></span>

### <span data-ttu-id="92950-144">Microsoft. Azure. Commands. EventHub. modele. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="92950-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>
<span data-ttu-id="92950-145">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="92950-145">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="92950-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="92950-146">OUTPUTS</span></span>

### <span data-ttu-id="92950-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="92950-147">System.Boolean</span></span>

## <span data-ttu-id="92950-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="92950-148">NOTES</span></span>

## <span data-ttu-id="92950-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="92950-149">RELATED LINKS</span></span>
