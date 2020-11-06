---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 3bd06ea2534298ba81cd546e8fa6e8de02fa5928
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553899"
---
# <span data-ttu-id="7a2d3-101">New-AzureRmEventHubKey</span><span class="sxs-lookup"><span data-stu-id="7a2d3-101">New-AzureRmEventHubKey</span></span>

## <span data-ttu-id="7a2d3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7a2d3-102">SYNOPSIS</span></span>
<span data-ttu-id="7a2d3-103">Tworzy nowy klucz podstawowy lub pomocniczy dla określonej reguły autoryzacji koncentratora zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="7a2d3-103">Creates a new primary or secondary key for the specified Event Hubs authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a2d3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7a2d3-104">SYNTAX</span></span>

### <span data-ttu-id="7a2d3-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7a2d3-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmEventHubKey -ResourceGroupName <String> -Namespace <String> -Name <String> -RegenerateKey <String>
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="7a2d3-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="7a2d3-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzureRmEventHubKey -ResourceGroupName <String> [-Namespace <String>] -EventHub <String> -Name <String>
 -RegenerateKey <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="7a2d3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7a2d3-107">DESCRIPTION</span></span>
<span data-ttu-id="7a2d3-108">Polecenie cmdlet New-AzureRmEventHubKey ponownie generuje podstawowy lub drugorzędny klucz SAS dla określonej reguły autoryzacji koncentratora zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="7a2d3-108">The New-AzureRmEventHubKey cmdlet regenerates the primary or secondary SAS key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="7a2d3-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7a2d3-109">EXAMPLES</span></span>

### <span data-ttu-id="7a2d3-110">Przykład 1,1</span><span class="sxs-lookup"><span data-stu-id="7a2d3-110">Example 1.1</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="7a2d3-111">Generuje ponownie klucz podstawowy reguły autoryzacji \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="7a2d3-111">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="7a2d3-112">Przykład 1,2</span><span class="sxs-lookup"><span data-stu-id="7a2d3-112">Example 1.2</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="7a2d3-113">Generuje ponownie klucz podstawowy reguły autoryzacji \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="7a2d3-113">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="7a2d3-114">Przykład 2,1</span><span class="sxs-lookup"><span data-stu-id="7a2d3-114">Example 2.1</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

### <span data-ttu-id="7a2d3-115">Przykład 2,2</span><span class="sxs-lookup"><span data-stu-id="7a2d3-115">Example 2.2</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

<span data-ttu-id="7a2d3-116">Generuje ponownie klucz pomocniczy reguły autoryzacji \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="7a2d3-116">Regenerates the secondary key for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="7a2d3-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7a2d3-117">PARAMETERS</span></span>

### <span data-ttu-id="7a2d3-118">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="7a2d3-118">-RegenerateKey</span></span>
<span data-ttu-id="7a2d3-119">Klawisz do ponownego generowania: \` PrimaryKey \` lub \` SecondaryKey \` .</span><span class="sxs-lookup"><span data-stu-id="7a2d3-119">Key to regenerate: \`PrimaryKey\` or \`SecondaryKey\`.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a2d3-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7a2d3-120">-Confirm</span></span>
<span data-ttu-id="7a2d3-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a2d3-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a2d3-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a2d3-122">-WhatIf</span></span>
<span data-ttu-id="7a2d3-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a2d3-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a2d3-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7a2d3-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a2d3-125">— EventHub</span><span class="sxs-lookup"><span data-stu-id="7a2d3-125">-EventHub</span></span>
<span data-ttu-id="7a2d3-126">Nazwa EventHub.</span><span class="sxs-lookup"><span data-stu-id="7a2d3-126">EventHub Name.</span></span>

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

### <span data-ttu-id="7a2d3-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7a2d3-127">-Name</span></span>
<span data-ttu-id="7a2d3-128">Nazwa AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="7a2d3-128">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="7a2d3-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7a2d3-129">-Namespace</span></span>
<span data-ttu-id="7a2d3-130">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="7a2d3-130">Namespace Name.</span></span>

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

### <span data-ttu-id="7a2d3-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a2d3-131">-ResourceGroupName</span></span>
<span data-ttu-id="7a2d3-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7a2d3-132">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="7a2d3-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a2d3-133">INPUTS</span></span>

### <span data-ttu-id="7a2d3-134">System. String</span><span class="sxs-lookup"><span data-stu-id="7a2d3-134">System.String</span></span>

## <span data-ttu-id="7a2d3-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7a2d3-135">OUTPUTS</span></span>

### <span data-ttu-id="7a2d3-136">Microsoft. Azure. Commands. EventHub. modele. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="7a2d3-136">Microsoft.Azure.Commands.EventHub.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="7a2d3-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7a2d3-137">NOTES</span></span>

## <span data-ttu-id="7a2d3-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7a2d3-138">RELATED LINKS</span></span>

