---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: bad0e86061a5ffaa937209d778d5eaa83e29879d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719326"
---
# <span data-ttu-id="b37f9-101">Get-AzureRmEventHubNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b37f9-101">Get-AzureRmEventHubNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="b37f9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b37f9-102">SYNOPSIS</span></span>
<span data-ttu-id="b37f9-103">Pobiera szczegóły reguły autoryzacji obszaru nazw Eventubs lub pobiera listę reguł autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="b37f9-103">Gets the details of an Eventubs namespace authorization rule, or gets a list of authorization rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b37f9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b37f9-104">SYNTAX</span></span>

```
Get-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [[-AuthorizationRuleName] <String>]
```

## <span data-ttu-id="b37f9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b37f9-105">DESCRIPTION</span></span>
<span data-ttu-id="b37f9-106">Polecenie cmdlet Get-AzureRmEventHubNamespaceAuthorizationRule pobiera szczegóły dotyczące określonej reguły autoryzacji obszaru nazw koncentratora zdarzeń lub listę reguł autoryzacji obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="b37f9-106">The Get-AzureRmEventHubNamespaceAuthorizationRule cmdlet gets either the details of a specified Event Hubs namespace authorization rule, or a list of namespace authorization rules.</span></span>
<span data-ttu-id="b37f9-107">Jeśli jest podana nazwa reguły autoryzacji, zostanie zwrócona wartość szczegółów jednej reguły autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="b37f9-107">If the authorization rule name is provided, the details of a single authorization rule is returned.</span></span>
<span data-ttu-id="b37f9-108">Jeśli nie podano nazwy reguły autoryzacji, zostanie zwrócona lista wszystkich reguł autoryzacji w obszarze nazw.</span><span class="sxs-lookup"><span data-stu-id="b37f9-108">If an authorization rule name is not provided, a list of all authorization rules in the namespace is returned.</span></span>

## <span data-ttu-id="b37f9-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b37f9-109">EXAMPLES</span></span>

### <span data-ttu-id="b37f9-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b37f9-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="b37f9-111">Zwraca regułę autoryzacji \` MyAuthRuleName \` w obszarze nazw Hub zdarzeń obszar_nazwname \` \` o MyResourceGroupName grupy zasobów \` \` .</span><span class="sxs-lookup"><span data-stu-id="b37f9-111">Returns the authorization rule \`MyAuthRuleName\` in the Event Hubs namespace \`MyNamespaceName\`, with the resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="b37f9-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b37f9-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName RootManageSharedAccessKey
```

<span data-ttu-id="b37f9-113">Zwraca domyślną regułę autoryzacji \` RootManageSharedAccessKey \` w obszarze nazw Hubs nazwy obszar_nazwname \` \` z grupą zasobów \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="b37f9-113">Returns the default authorization rule \`RootManageSharedAccessKey\` in the Event Hubs namespace \`MyNamespaceName\`, with the resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="b37f9-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="b37f9-114">Example 3</span></span>
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="b37f9-115">Zwraca wszystkie reguły autoryzacji w przestrzeni nazw Hub zdarzeń \` \` o adresie NamespaceName z grupą \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="b37f9-115">Returns all authorization rules in the Event Hubs namespace \`MyNamespaceName\`, with the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="b37f9-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b37f9-116">PARAMETERS</span></span>

### <span data-ttu-id="b37f9-117">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="b37f9-117">-AuthorizationRuleName</span></span>
<span data-ttu-id="b37f9-118">Nazwa reguły autoryzacji obszaru nazw koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="b37f9-118">The Event Hubs namespace authorization rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b37f9-119">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="b37f9-119">-NamespaceName</span></span>
<span data-ttu-id="b37f9-120">Nazwa obszaru nazw koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="b37f9-120">The Event Hubs namespace name.</span></span>

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

### <span data-ttu-id="b37f9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b37f9-121">-ResourceGroupName</span></span>
<span data-ttu-id="b37f9-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b37f9-122">Resource group name.</span></span>

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

## <span data-ttu-id="b37f9-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b37f9-123">INPUTS</span></span>

### <span data-ttu-id="b37f9-124">System. String</span><span class="sxs-lookup"><span data-stu-id="b37f9-124">System.String</span></span>

## <span data-ttu-id="b37f9-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b37f9-125">OUTPUTS</span></span>

### <span data-ttu-id="b37f9-126">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. EventHub. modele. SharedAccessAuthorizationRuleAttributes, Microsoft. Azure. Commands. EventHub, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="b37f9-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.EventHub, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="b37f9-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b37f9-127">NOTES</span></span>

## <span data-ttu-id="b37f9-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b37f9-128">RELATED LINKS</span></span>

