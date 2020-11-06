---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 10c3d087bcde2a88fd33ff3118a40e44af918ea4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549200"
---
# <span data-ttu-id="6bd34-101">Remove-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="6bd34-101">Remove-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="6bd34-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6bd34-102">SYNOPSIS</span></span>
<span data-ttu-id="6bd34-103">Usuwa określoną przestrzeń nazw koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="6bd34-103">Removes the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6bd34-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6bd34-104">SYNTAX</span></span>

```
Remove-AzureRmEventHubNamespace [-ResourceGroupName] <String> -Name <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="6bd34-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6bd34-105">DESCRIPTION</span></span>
<span data-ttu-id="6bd34-106">Polecenie cmdlet Remove-AzureRmEventHubNamespace powoduje usunięcie i usunięcie określonego obszaru nazw koncentratora zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="6bd34-106">The Remove-AzureRmEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="6bd34-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6bd34-107">EXAMPLES</span></span>

### <span data-ttu-id="6bd34-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6bd34-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="6bd34-109">Usuwa przestrzeń nazw Hub zdarzeń \` \` w MyResourceGroupName grupy zasobów \` \` .</span><span class="sxs-lookup"><span data-stu-id="6bd34-109">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="6bd34-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6bd34-110">PARAMETERS</span></span>

### <span data-ttu-id="6bd34-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bd34-111">-ResourceGroupName</span></span>
<span data-ttu-id="6bd34-112">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6bd34-112">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bd34-113">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6bd34-113">-Confirm</span></span>
<span data-ttu-id="6bd34-114">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6bd34-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bd34-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bd34-115">-WhatIf</span></span>
<span data-ttu-id="6bd34-116">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6bd34-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bd34-117">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6bd34-117">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bd34-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6bd34-118">-Name</span></span>
<span data-ttu-id="6bd34-119">Nazwa obszaru nazw EventHub.</span><span class="sxs-lookup"><span data-stu-id="6bd34-119">EventHub Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="6bd34-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6bd34-120">INPUTS</span></span>

### <span data-ttu-id="6bd34-121">System. String</span><span class="sxs-lookup"><span data-stu-id="6bd34-121">System.String</span></span>

## <span data-ttu-id="6bd34-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6bd34-122">OUTPUTS</span></span>

### <span data-ttu-id="6bd34-123">System. Object</span><span class="sxs-lookup"><span data-stu-id="6bd34-123">System.Object</span></span>

## <span data-ttu-id="6bd34-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6bd34-124">NOTES</span></span>

## <span data-ttu-id="6bd34-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6bd34-125">RELATED LINKS</span></span>

