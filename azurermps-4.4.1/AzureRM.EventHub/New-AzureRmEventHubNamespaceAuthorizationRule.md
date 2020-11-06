---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: dc384ca6056ef13d5517241d550bacddf2e7d0d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553900"
---
# <span data-ttu-id="cb105-101">New-AzureRmEventHubNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="cb105-101">New-AzureRmEventHubNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="cb105-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cb105-102">SYNOPSIS</span></span>
<span data-ttu-id="cb105-103">Tworzy nową regułę autoryzacji w określonym obszarze nazw.</span><span class="sxs-lookup"><span data-stu-id="cb105-103">Creates a new authorization rule on the specified namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb105-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cb105-104">SYNTAX</span></span>

```
New-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [-AuthorizationRuleName] <String> [-Rights] <String[]> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="cb105-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cb105-105">DESCRIPTION</span></span>
<span data-ttu-id="cb105-106">Polecenie cmdlet New-AzureRmEventHubNamespaceAuthorizationRule powoduje utworzenie nowej reguły autoryzacji w określonym obszarze nazw koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="cb105-106">The New-AzureRmEventHubNamespaceAuthorizationRule cmdlet creates a new authorization rule on the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="cb105-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cb105-107">EXAMPLES</span></span>

### <span data-ttu-id="cb105-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cb105-108">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="cb105-109">Umożliwia utworzenie reguły autoryzacji \` MyAuthRuleName \` z prawami do nasłuchiwania i wysyłania, dla obszaru nazw Hub \* obszar_nazwname \` \` , w grupie zasób \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="cb105-109">Creates the authorization rule \`MyAuthRuleName\` with Listen and Send rights, for Event Hubs namespace \`MyNamespaceName\`, in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="cb105-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cb105-110">PARAMETERS</span></span>

### <span data-ttu-id="cb105-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="cb105-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="cb105-112">Nazwa reguły autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="cb105-112">Authorization rule name.</span></span>

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

### <span data-ttu-id="cb105-113">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="cb105-113">-NamespaceName</span></span>
<span data-ttu-id="cb105-114">Nazwa obszaru nazw koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="cb105-114">The Event Hubs namespace name.</span></span>

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

### <span data-ttu-id="cb105-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb105-115">-ResourceGroupName</span></span>
<span data-ttu-id="cb105-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cb105-116">Resource group name.</span></span>

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

### <span data-ttu-id="cb105-117">-Prawa</span><span class="sxs-lookup"><span data-stu-id="cb105-117">-Rights</span></span>
<span data-ttu-id="cb105-118">Prawa, na przykład @ ("nasłuchuj", "Wyślij", "Zarządzaj")</span><span class="sxs-lookup"><span data-stu-id="cb105-118">Rights;for example,  @("Listen","Send","Manage")</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb105-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cb105-119">-Confirm</span></span>
<span data-ttu-id="cb105-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb105-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb105-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb105-121">-WhatIf</span></span>
<span data-ttu-id="cb105-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb105-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb105-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cb105-123">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="cb105-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cb105-124">INPUTS</span></span>

### <span data-ttu-id="cb105-125">System. String</span><span class="sxs-lookup"><span data-stu-id="cb105-125">System.String</span></span>

## <span data-ttu-id="cb105-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cb105-126">OUTPUTS</span></span>

### <span data-ttu-id="cb105-127">Microsoft. Azure. Commands. EventHub. modele. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="cb105-127">Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="cb105-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cb105-128">NOTES</span></span>

## <span data-ttu-id="cb105-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cb105-129">RELATED LINKS</span></span>

