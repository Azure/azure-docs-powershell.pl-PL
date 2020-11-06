---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: e91b7edacc575ac98eb78ae44c88be4f6873f34c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553904"
---
# <span data-ttu-id="c282e-101">Get-AzureRmEventHubNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="c282e-101">Get-AzureRmEventHubNamespaceKey</span></span>

## <span data-ttu-id="c282e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c282e-102">SYNOPSIS</span></span>
<span data-ttu-id="c282e-103">Pobiera szczegóły podstawowego, pomocniczego connectionStrings oraz kluczy reguły autoryzacji określonej reguły autoryzacji obszaru nazw koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="c282e-103">Gets details of Primary, Secondary connectionstrings and keys for the authorization rule of the specified Event Hubs namespace authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c282e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c282e-104">SYNTAX</span></span>

```
Get-AzureRmEventHubNamespaceKey [-ResourceGroupName] <String> [-NamespaceName] <String>
 [-AuthorizationRuleName] <String>
```

## <span data-ttu-id="c282e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c282e-105">DESCRIPTION</span></span>
<span data-ttu-id="c282e-106">Polecenie cmdlet Get-AzureRmEventHubNamespaceKey zwraca podstawowe i pomocnicze connectionStrings oraz klucze dotyczące określonej reguły autoryzacji w danym obszarze nazw koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="c282e-106">The Get-AzureRmEventHubNamespaceKey cmdlet returns the Primary and Secondary connectionstrings and keys details of the specified authorization rule in the given Event Hubs namespace.</span></span>

## <span data-ttu-id="c282e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c282e-107">EXAMPLES</span></span>

### <span data-ttu-id="c282e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c282e-108">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubNamespaceKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="c282e-109">Pobiera szczegóły podstawowego, pomocniczego connectionStrings oraz kluczy dla reguły autoryzacji \` MyAuthRuleName w \` obszarze nazw Hub zdarzeń w obszarze nazw \` \` \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="c282e-109">Gets details of Primary, Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\` on the Event Hubs namespace \`MyNamespaceName\` in the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="c282e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c282e-110">PARAMETERS</span></span>

### <span data-ttu-id="c282e-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="c282e-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="c282e-112">Nazwa reguły autoryzacji w obszarze nazw koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="c282e-112">The name of the authorization rule on the Event Hubs namespace.</span></span>

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

### <span data-ttu-id="c282e-113">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="c282e-113">-NamespaceName</span></span>
<span data-ttu-id="c282e-114">Nazwa obszaru nazw koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="c282e-114">The Event Hubs namespace name.</span></span>

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

### <span data-ttu-id="c282e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c282e-115">-ResourceGroupName</span></span>
<span data-ttu-id="c282e-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c282e-116">Resource group name.</span></span>

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

## <span data-ttu-id="c282e-117">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c282e-117">INPUTS</span></span>

### <span data-ttu-id="c282e-118">System. String</span><span class="sxs-lookup"><span data-stu-id="c282e-118">System.String</span></span>

## <span data-ttu-id="c282e-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c282e-119">OUTPUTS</span></span>

### <span data-ttu-id="c282e-120">Microsoft. Azure. Commands. EventHub. modele. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="c282e-120">Microsoft.Azure.Commands.EventHub.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="c282e-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c282e-121">NOTES</span></span>

## <span data-ttu-id="c282e-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c282e-122">RELATED LINKS</span></span>

