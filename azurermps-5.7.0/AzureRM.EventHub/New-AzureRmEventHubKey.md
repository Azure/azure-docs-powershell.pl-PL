---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubKey.md
ms.openlocfilehash: 8be39cb4b4b173d3b87efbf0b7ecea72ae233061
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717526"
---
# <span data-ttu-id="f5167-101">New-AzureRmEventHubKey</span><span class="sxs-lookup"><span data-stu-id="f5167-101">New-AzureRmEventHubKey</span></span>

## <span data-ttu-id="f5167-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f5167-102">SYNOPSIS</span></span>
<span data-ttu-id="f5167-103">Tworzy nowy klucz podstawowy lub pomocniczy dla określonej reguły autoryzacji koncentratora zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="f5167-103">Creates a new primary or secondary key for the specified Event Hubs authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5167-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f5167-104">SYNTAX</span></span>

### <span data-ttu-id="f5167-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f5167-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RegenerateKey] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5167-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f5167-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-RegenerateKey] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f5167-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f5167-107">DESCRIPTION</span></span>
<span data-ttu-id="f5167-108">Polecenie cmdlet New-AzureRmEventHubKey ponownie generuje podstawowy lub drugorzędny klucz SAS dla określonej reguły autoryzacji koncentratora zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="f5167-108">The New-AzureRmEventHubKey cmdlet regenerates the primary or secondary SAS key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="f5167-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f5167-109">EXAMPLES</span></span>

### <span data-ttu-id="f5167-110">Przykład 1,1</span><span class="sxs-lookup"><span data-stu-id="f5167-110">Example 1.1</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="f5167-111">Generuje ponownie klucz podstawowy reguły autoryzacji \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="f5167-111">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="f5167-112">Przykład 1,2</span><span class="sxs-lookup"><span data-stu-id="f5167-112">Example 1.2</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="f5167-113">Generuje ponownie klucz podstawowy reguły autoryzacji \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="f5167-113">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="f5167-114">Przykład 2,1</span><span class="sxs-lookup"><span data-stu-id="f5167-114">Example 2.1</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

### <span data-ttu-id="f5167-115">Przykład 2,2</span><span class="sxs-lookup"><span data-stu-id="f5167-115">Example 2.2</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

<span data-ttu-id="f5167-116">Generuje ponownie klucz pomocniczy reguły autoryzacji \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="f5167-116">Regenerates the secondary key for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="f5167-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f5167-117">PARAMETERS</span></span>

### <span data-ttu-id="f5167-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5167-118">-DefaultProfile</span></span>
<span data-ttu-id="f5167-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f5167-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5167-120">— EventHub</span><span class="sxs-lookup"><span data-stu-id="f5167-120">-EventHub</span></span>
<span data-ttu-id="f5167-121">Nazwa EventHub</span><span class="sxs-lookup"><span data-stu-id="f5167-121">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5167-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f5167-122">-Name</span></span>
<span data-ttu-id="f5167-123">Nazwa AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f5167-123">AuthorizationRule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5167-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f5167-124">-Namespace</span></span>
<span data-ttu-id="f5167-125">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="f5167-125">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5167-126">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="f5167-126">-RegenerateKey</span></span>
<span data-ttu-id="f5167-127">Ponowne generowanie kluczy — "Primarykea"/"SecondaryKey"</span><span class="sxs-lookup"><span data-stu-id="f5167-127">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5167-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5167-128">-ResourceGroupName</span></span>
<span data-ttu-id="f5167-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="f5167-129">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5167-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f5167-130">-Confirm</span></span>
<span data-ttu-id="f5167-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5167-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5167-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5167-132">-WhatIf</span></span>
<span data-ttu-id="f5167-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5167-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5167-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f5167-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5167-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5167-135">CommonParameters</span></span>
<span data-ttu-id="f5167-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5167-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f5167-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5167-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5167-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f5167-138">INPUTS</span></span>

### <span data-ttu-id="f5167-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f5167-139">System.String</span></span>


## <span data-ttu-id="f5167-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f5167-140">OUTPUTS</span></span>

### <span data-ttu-id="f5167-141">Microsoft. Azure. Commands. EventHub. modele. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="f5167-141">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>


## <span data-ttu-id="f5167-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f5167-142">NOTES</span></span>

## <span data-ttu-id="f5167-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f5167-143">RELATED LINKS</span></span>
