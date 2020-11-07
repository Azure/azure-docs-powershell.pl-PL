---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 4a980edd1833b37b358f86d2e3ccb6a9efc8d836
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717590"
---
# <span data-ttu-id="72dbb-101">Remove-AzureRmEventHubNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="72dbb-101">Remove-AzureRmEventHubNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="72dbb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="72dbb-102">SYNOPSIS</span></span>
<span data-ttu-id="72dbb-103">Usuwa określoną regułę autoryzacji w obszarze nazw koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="72dbb-103">Deletes the specified authorization rule on the given Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72dbb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="72dbb-104">SYNTAX</span></span>

```
Remove-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [-AuthorizationRuleName] <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="72dbb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="72dbb-105">DESCRIPTION</span></span>
<span data-ttu-id="72dbb-106">Polecenie cmdlet Remove-AzureRmEventHubNamespaceAuthorizationRule powoduje usunięcie i usunięcie określonej reguły autoryzacji w danym obszarze nazw koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="72dbb-106">The Remove-AzureRmEventHubNamespaceAuthorizationRule cmdlet removes and deletes the specified authorization rule on the given Event Hubs namespace.</span></span>

## <span data-ttu-id="72dbb-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="72dbb-107">EXAMPLES</span></span>

### <span data-ttu-id="72dbb-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="72dbb-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="72dbb-109">Usuwa regułę autoryzacji \` MyAuthRuleName \` z obszaru nazw obszar_nazwname \` \` .</span><span class="sxs-lookup"><span data-stu-id="72dbb-109">Removes the authorization rule \`MyAuthRuleName\` from the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="72dbb-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="72dbb-110">PARAMETERS</span></span>

### <span data-ttu-id="72dbb-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="72dbb-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="72dbb-112">Nazwa reguły autoryzacji obszaru nazw koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="72dbb-112">The Event Hubs namespace authorization rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72dbb-113">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="72dbb-113">-NamespaceName</span></span>
<span data-ttu-id="72dbb-114">Nazwa obszaru nazw koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="72dbb-114">The Event Hubs namespace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72dbb-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72dbb-115">-ResourceGroupName</span></span>
<span data-ttu-id="72dbb-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="72dbb-116">Resource group name.</span></span>

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

### <span data-ttu-id="72dbb-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="72dbb-117">-Confirm</span></span>
<span data-ttu-id="72dbb-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72dbb-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72dbb-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72dbb-119">-WhatIf</span></span>
<span data-ttu-id="72dbb-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72dbb-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72dbb-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="72dbb-121">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="72dbb-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="72dbb-122">INPUTS</span></span>

### <span data-ttu-id="72dbb-123">System. String</span><span class="sxs-lookup"><span data-stu-id="72dbb-123">System.String</span></span>

## <span data-ttu-id="72dbb-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="72dbb-124">OUTPUTS</span></span>

### <span data-ttu-id="72dbb-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="72dbb-125">System.Boolean</span></span>

## <span data-ttu-id="72dbb-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="72dbb-126">NOTES</span></span>

## <span data-ttu-id="72dbb-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="72dbb-127">RELATED LINKS</span></span>

