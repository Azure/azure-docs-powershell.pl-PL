---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
ms.openlocfilehash: c15528befc90a0249101602fef9b178e7a63c0ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545751"
---
# <span data-ttu-id="ce20d-101">Remove-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ce20d-101">Remove-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="ce20d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ce20d-102">SYNOPSIS</span></span>
<span data-ttu-id="ce20d-103">Usuwa określoną regułę autoryzacji centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="ce20d-103">Removes the specified Event Hub authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce20d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ce20d-104">SYNTAX</span></span>

### <span data-ttu-id="ce20d-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ce20d-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce20d-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="ce20d-106">EventhubAuthorizationRuleSet</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String>
 [-EventHub] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce20d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ce20d-107">DESCRIPTION</span></span>
<span data-ttu-id="ce20d-108">Polecenie cmdlet Remove-AzureRmEventHubAuthorizationRule powoduje usunięcie i usunięcie określonej reguły autoryzacji z danego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="ce20d-108">The Remove-AzureRmEventHubAuthorizationRule cmdlet removes and deletes the specified authorization rule from the given Event Hub.</span></span>

## <span data-ttu-id="ce20d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ce20d-109">EXAMPLES</span></span>

### <span data-ttu-id="ce20d-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ce20d-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName
```

### <span data-ttu-id="ce20d-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ce20d-111">Example 2</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="ce20d-112">Usuwa regułę autoryzacji \` MyAuthRuleName \` z MyEventHubName centrum zdarzeń \` \` .</span><span class="sxs-lookup"><span data-stu-id="ce20d-112">Removes the authorization rule \`MyAuthRuleName\` from the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="ce20d-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ce20d-113">PARAMETERS</span></span>

### <span data-ttu-id="ce20d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce20d-114">-DefaultProfile</span></span>
<span data-ttu-id="ce20d-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ce20d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce20d-116">— EventHub</span><span class="sxs-lookup"><span data-stu-id="ce20d-116">-EventHub</span></span>
<span data-ttu-id="ce20d-117">Nazwa EventHub</span><span class="sxs-lookup"><span data-stu-id="ce20d-117">EventHub Name</span></span>

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

### <span data-ttu-id="ce20d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ce20d-118">-Force</span></span>
<span data-ttu-id="ce20d-119">Nie pytaj o potwierdzenie</span><span class="sxs-lookup"><span data-stu-id="ce20d-119">Do not ask for confirmation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce20d-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ce20d-120">-Name</span></span>
<span data-ttu-id="ce20d-121">Nazwa AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ce20d-121">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="ce20d-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ce20d-122">-Namespace</span></span>
<span data-ttu-id="ce20d-123">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="ce20d-123">Namespace Name</span></span>

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

### <span data-ttu-id="ce20d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ce20d-124">-PassThru</span></span>
<span data-ttu-id="ce20d-125">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="ce20d-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ce20d-126">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="ce20d-126">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce20d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce20d-127">-ResourceGroupName</span></span>
<span data-ttu-id="ce20d-128">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="ce20d-128">Resource Group Name</span></span>

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

### <span data-ttu-id="ce20d-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ce20d-129">-Confirm</span></span>
<span data-ttu-id="ce20d-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce20d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce20d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce20d-131">-WhatIf</span></span>
<span data-ttu-id="ce20d-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce20d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce20d-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ce20d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce20d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce20d-134">CommonParameters</span></span>
<span data-ttu-id="ce20d-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce20d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ce20d-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce20d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce20d-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ce20d-137">INPUTS</span></span>

### <span data-ttu-id="ce20d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ce20d-138">System.String</span></span>


## <span data-ttu-id="ce20d-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ce20d-139">OUTPUTS</span></span>

### <span data-ttu-id="ce20d-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ce20d-140">System.Boolean</span></span>


## <span data-ttu-id="ce20d-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ce20d-141">NOTES</span></span>

## <span data-ttu-id="ce20d-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ce20d-142">RELATED LINKS</span></span>
