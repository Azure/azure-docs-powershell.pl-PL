---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: f4f28ee3f07127803e6187f00565ee8d4caf3084
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553909"
---
# <span data-ttu-id="8c6da-101">Get-AzureRmEventHubKey</span><span class="sxs-lookup"><span data-stu-id="8c6da-101">Get-AzureRmEventHubKey</span></span>

## <span data-ttu-id="8c6da-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8c6da-102">SYNOPSIS</span></span>
<span data-ttu-id="8c6da-103">Pobiera szczegóły klucza podstawowego określonej reguły autoryzacji koncentratora zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="8c6da-103">Gets the primary key details of the specified Event Hubs authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c6da-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8c6da-104">SYNTAX</span></span>

### <span data-ttu-id="8c6da-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8c6da-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> -Namespace <String> -Name <String>
```

### <span data-ttu-id="8c6da-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="8c6da-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace <String>] -EventHub <String> -Name <String>
```

## <span data-ttu-id="8c6da-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8c6da-107">DESCRIPTION</span></span>
<span data-ttu-id="8c6da-108">Polecenie cmdlet Get-AzureRmEventHubKey zwraca podstawowe i pomocnicze connectionStrings i klucze dotyczące określonej reguły autoryzacji koncentratora zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="8c6da-108">The Get-AzureRmEventHubKey cmdlet returns Primary and Secondary connectionstrings and keys details of the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="8c6da-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8c6da-109">EXAMPLES</span></span>

### <span data-ttu-id="8c6da-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8c6da-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="8c6da-111">Pobiera szczegóły podstawowego i pomocniczego connectionStrings oraz kluczy dla reguły autoryzacji \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="8c6da-111">Gets details of Primary and Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="8c6da-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8c6da-112">PARAMETERS</span></span>

### <span data-ttu-id="8c6da-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c6da-113">-ResourceGroupName</span></span>
<span data-ttu-id="8c6da-114">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8c6da-114">Resource group name.</span></span>

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

### <span data-ttu-id="8c6da-115">— EventHub</span><span class="sxs-lookup"><span data-stu-id="8c6da-115">-EventHub</span></span>
<span data-ttu-id="8c6da-116">Nazwa EventHub.</span><span class="sxs-lookup"><span data-stu-id="8c6da-116">EventHub Name.</span></span>

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c6da-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8c6da-117">-Name</span></span>
<span data-ttu-id="8c6da-118">Nazwa AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="8c6da-118">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c6da-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8c6da-119">-Namespace</span></span>
<span data-ttu-id="8c6da-120">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="8c6da-120">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: NamespaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="8c6da-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8c6da-121">INPUTS</span></span>

### <span data-ttu-id="8c6da-122">System. String</span><span class="sxs-lookup"><span data-stu-id="8c6da-122">System.String</span></span>

## <span data-ttu-id="8c6da-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8c6da-123">OUTPUTS</span></span>

### <span data-ttu-id="8c6da-124">Microsoft. Azure. Commands. EventHub. modele. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="8c6da-124">Microsoft.Azure.Commands.EventHub.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="8c6da-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8c6da-125">NOTES</span></span>

## <span data-ttu-id="8c6da-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8c6da-126">RELATED LINKS</span></span>

