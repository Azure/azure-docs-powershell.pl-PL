---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespaceKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 1a96916d0e3bed080e078226a14304b6ee6cecc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553898"
---
# <span data-ttu-id="81281-101">New-AzureRmEventHubNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="81281-101">New-AzureRmEventHubNamespaceKey</span></span>

## <span data-ttu-id="81281-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="81281-102">SYNOPSIS</span></span>
<span data-ttu-id="81281-103">Tworzy nowy podstawowy lub pomocniczy klucz reguły autoryzacji w określonym obszarze nazw koncentratora zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="81281-103">Creates a new primary or secondary key for the authorization rule on the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81281-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="81281-104">SYNTAX</span></span>

```
New-AzureRmEventHubNamespaceKey [-ResourceGroup] <String> [-NamespaceName] <String>
 [-AuthorizationRuleName] <String> [-RegenerateKeys] <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="81281-105">Opis</span><span class="sxs-lookup"><span data-stu-id="81281-105">DESCRIPTION</span></span>
<span data-ttu-id="81281-106">Polecenie cmdlet New-AzureRmEventHubNamespaceKey ponownie generuje podstawowy lub pomocniczy klucz dla danej reguły autoryzacji w określonym obszarze nazw koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="81281-106">The New-AzureRmEventHubNamespaceKey cmdlet regenerates the primary or secondary key for the for the given authorization rule on the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="81281-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="81281-107">EXAMPLES</span></span>

### <span data-ttu-id="81281-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="81281-108">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubNameSpaceKey -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName  -AuthorizationRuleName MyAuthRuleName -RegenerateKeys PrimaryKey
```

<span data-ttu-id="81281-109">Generuje ponownie klucz podstawowy reguły autoryzacji \` MyAuthRuleName \` w obszarze nazw Hubs zdarzenia obszar_nazwname \` \` , z grupą zasobów \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="81281-109">Regenerates the primary key for the authorization rule \`MyAuthRuleName\` in the Event Hubs namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="81281-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="81281-110">PARAMETERS</span></span>

### <span data-ttu-id="81281-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="81281-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="81281-112">Nazwa reguły autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="81281-112">Authorization rule name.</span></span>

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

### <span data-ttu-id="81281-113">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="81281-113">-NamespaceName</span></span>
<span data-ttu-id="81281-114">Nazwa obszaru nazw koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="81281-114">The Event Hubs namespace name.</span></span>

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

### <span data-ttu-id="81281-115">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="81281-115">-RegenerateKeys</span></span>
<span data-ttu-id="81281-116">Klawisz do ponownego generowania: \` PrimaryKey \` lub \` SecondaryKey \` .</span><span class="sxs-lookup"><span data-stu-id="81281-116">Key to regenerate: \`PrimaryKey\` or \`SecondaryKey\`.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81281-117">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="81281-117">-ResourceGroup</span></span>
<span data-ttu-id="81281-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="81281-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="81281-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="81281-119">-Confirm</span></span>
<span data-ttu-id="81281-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81281-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81281-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81281-121">-WhatIf</span></span>
<span data-ttu-id="81281-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81281-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81281-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="81281-123">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="81281-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="81281-124">INPUTS</span></span>

### <span data-ttu-id="81281-125">System. String</span><span class="sxs-lookup"><span data-stu-id="81281-125">System.String</span></span>

## <span data-ttu-id="81281-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="81281-126">OUTPUTS</span></span>

### <span data-ttu-id="81281-127">Microsoft. Azure. Commands. EventHub. modele. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="81281-127">Microsoft.Azure.Commands.EventHub.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="81281-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="81281-128">NOTES</span></span>

## <span data-ttu-id="81281-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="81281-129">RELATED LINKS</span></span>

