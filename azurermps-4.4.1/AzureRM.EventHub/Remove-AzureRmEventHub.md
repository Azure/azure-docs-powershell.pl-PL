---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 22904260488c716ffb702f47442dc8f4678ebe12
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553896"
---
# <span data-ttu-id="7b8c3-101">Remove-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="7b8c3-101">Remove-AzureRmEventHub</span></span>

## <span data-ttu-id="7b8c3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7b8c3-102">SYNOPSIS</span></span>
<span data-ttu-id="7b8c3-103">Umożliwia usunięcie określonego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="7b8c3-103">Removes the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b8c3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7b8c3-104">SYNTAX</span></span>

```
Remove-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> -Name <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="7b8c3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7b8c3-105">DESCRIPTION</span></span>
<span data-ttu-id="7b8c3-106">Polecenie cmdlet Remove-AzureRmEventHub powoduje usunięcie i usunięcie określonego centrum zdarzeń z danego obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="7b8c3-106">The Remove-AzureRmEventHub cmdlet removes and deletes the specified Event Hub from the given namespace.</span></span>

## <span data-ttu-id="7b8c3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7b8c3-107">EXAMPLES</span></span>

### <span data-ttu-id="7b8c3-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7b8c3-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="7b8c3-109">Usuwa MyEventHubName centrum zdarzeń \` \` .</span><span class="sxs-lookup"><span data-stu-id="7b8c3-109">Removes the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="7b8c3-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7b8c3-110">PARAMETERS</span></span>

### <span data-ttu-id="7b8c3-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b8c3-111">-ResourceGroupName</span></span>
<span data-ttu-id="7b8c3-112">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7b8c3-112">Resource group name.</span></span>

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

### <span data-ttu-id="7b8c3-113">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7b8c3-113">-Confirm</span></span>
<span data-ttu-id="7b8c3-114">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b8c3-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b8c3-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b8c3-115">-WhatIf</span></span>
<span data-ttu-id="7b8c3-116">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b8c3-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b8c3-117">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7b8c3-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b8c3-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7b8c3-118">-Name</span></span>
<span data-ttu-id="7b8c3-119">Nazwa EventHub.</span><span class="sxs-lookup"><span data-stu-id="7b8c3-119">EventHub Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b8c3-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7b8c3-120">-Namespace</span></span>
<span data-ttu-id="7b8c3-121">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="7b8c3-121">Namespace Name.</span></span>

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

## <span data-ttu-id="7b8c3-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7b8c3-122">INPUTS</span></span>

### <span data-ttu-id="7b8c3-123">System. String</span><span class="sxs-lookup"><span data-stu-id="7b8c3-123">System.String</span></span>

## <span data-ttu-id="7b8c3-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7b8c3-124">OUTPUTS</span></span>

### <span data-ttu-id="7b8c3-125">System. Object</span><span class="sxs-lookup"><span data-stu-id="7b8c3-125">System.Object</span></span>

## <span data-ttu-id="7b8c3-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7b8c3-126">NOTES</span></span>

## <span data-ttu-id="7b8c3-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7b8c3-127">RELATED LINKS</span></span>

