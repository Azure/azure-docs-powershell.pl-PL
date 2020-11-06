---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubAuthorizationRule.md
ms.openlocfilehash: 4d162122b82f592472fb31f1087db29faedf08cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551744"
---
# <span data-ttu-id="26da3-101">Get-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="26da3-101">Get-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="26da3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="26da3-102">SYNOPSIS</span></span>
<span data-ttu-id="26da3-103">Pobiera szczegóły reguły autoryzacji lub pobiera listę reguł autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="26da3-103">Gets the details of an authorization rule, or gets a list of authorization rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26da3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="26da3-104">SYNTAX</span></span>

### <span data-ttu-id="26da3-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="26da3-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26da3-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="26da3-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Eventhub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26da3-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="26da3-107">AliasAuthoRuleSet</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26da3-108">Opis</span><span class="sxs-lookup"><span data-stu-id="26da3-108">DESCRIPTION</span></span>
<span data-ttu-id="26da3-109">Polecenie cmdlet Get-AzureRmEventHubAuthorizationRule pobiera szczegóły reguły autoryzacji lub listę wszystkich reguł autoryzacji określonego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="26da3-109">The Get-AzureRmEventHubAuthorizationRule cmdlet gets either the details of an authorization rule, or a list of all authorization rules for a specified Event Hub.</span></span>
<span data-ttu-id="26da3-110">Jeśli jest podana nazwa reguły autoryzacji, zostaną zwrócone szczegóły dotyczące jednej reguły autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="26da3-110">If the name of an authorization rule is provided, the details of that single authorization rule are returned.</span></span>
<span data-ttu-id="26da3-111">Jeśli nie podano nazwy reguły autoryzacji, zostanie zwrócona lista wszystkich reguł autoryzacji określonego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="26da3-111">If the name of an authorization rule is not provided, a list of all authorization rules for the specified Event Hub is returned.</span></span>
<span data-ttu-id="26da3-112">Jeśli zostanie podana nazwa aliasu (odzyskiwanie po awarii), zostanie zwrócona wartość szczegółów reguły autoryzacji obszaru nazw skonfigurowanego dla aliasu.</span><span class="sxs-lookup"><span data-stu-id="26da3-112">If (Disaster Recovery) Alias name provided, the details of authorization rule of the Namespace for Alias configured is returned.</span></span> 

## <span data-ttu-id="26da3-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="26da3-113">EXAMPLES</span></span>

### <span data-ttu-id="26da3-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="26da3-114">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRule MyAuthRuleName
```

<span data-ttu-id="26da3-115">Pobiera regułę autoryzacji \` MyAuthRuleName \` w MyEventHubName centrum zdarzeń \` \` , która jest zakresem obszaru nazw \` \` obszar_nazwname.</span><span class="sxs-lookup"><span data-stu-id="26da3-115">Gets the authorization rule \`MyAuthRuleName\` in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="26da3-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="26da3-116">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="26da3-117">Pobiera listę wszystkich reguł autoryzacji w MyEventHubName centrum zdarzeń \` \` , które są objęte zakresem przestrzeni nazw obszar_nazwname \` \` .</span><span class="sxs-lookup"><span data-stu-id="26da3-117">Gets a list of all authorization rules in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="26da3-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="26da3-118">Example 3</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName -Name MyAuthRuleName
```

<span data-ttu-id="26da3-119">Pobiera regułę autoryzacji \` MyAuthRuleName \` w obszarze nazw obszar_nazwname \` \` .</span><span class="sxs-lookup"><span data-stu-id="26da3-119">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="26da3-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="26da3-120">PARAMETERS</span></span>

### <span data-ttu-id="26da3-121">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="26da3-121">-AliasName</span></span>
<span data-ttu-id="26da3-122">Nazwa aliasu</span><span class="sxs-lookup"><span data-stu-id="26da3-122">Alias Name</span></span>

```yaml
Type: String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26da3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26da3-123">-DefaultProfile</span></span>
<span data-ttu-id="26da3-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="26da3-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26da3-125">— Eventhub</span><span class="sxs-lookup"><span data-stu-id="26da3-125">-Eventhub</span></span>
<span data-ttu-id="26da3-126">Nazwa Eventhub</span><span class="sxs-lookup"><span data-stu-id="26da3-126">Eventhub Name</span></span>

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

### <span data-ttu-id="26da3-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="26da3-127">-Name</span></span>
<span data-ttu-id="26da3-128">Nazwa AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="26da3-128">AuthorizationRule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26da3-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="26da3-129">-Namespace</span></span>
<span data-ttu-id="26da3-130">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="26da3-130">Namespace Name</span></span>

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

### <span data-ttu-id="26da3-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26da3-131">-ResourceGroupName</span></span>
<span data-ttu-id="26da3-132">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="26da3-132">Resource Group Name</span></span>

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

### <span data-ttu-id="26da3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26da3-133">CommonParameters</span></span>
<span data-ttu-id="26da3-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26da3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="26da3-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26da3-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26da3-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="26da3-136">INPUTS</span></span>

### <span data-ttu-id="26da3-137">System. String</span><span class="sxs-lookup"><span data-stu-id="26da3-137">System.String</span></span>


## <span data-ttu-id="26da3-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="26da3-138">OUTPUTS</span></span>

### <span data-ttu-id="26da3-139">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. EventHub. modele. PSSharedAccessAuthorizationRuleAttributes, Microsoft. Azure. Commands. EventHub, Version = 0.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="26da3-139">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.EventHub, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="26da3-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="26da3-140">NOTES</span></span>

## <span data-ttu-id="26da3-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="26da3-141">RELATED LINKS</span></span>
