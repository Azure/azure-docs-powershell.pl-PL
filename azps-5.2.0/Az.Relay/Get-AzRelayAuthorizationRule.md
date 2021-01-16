---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayAuthorizationRule.md
ms.openlocfilehash: af83820d33b9f36d93cc7623001d22a6cb5e0212
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357189"
---
# <span data-ttu-id="a4a58-101">Get-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a4a58-101">Get-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="a4a58-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a4a58-102">SYNOPSIS</span></span>
<span data-ttu-id="a4a58-103">Pobiera opis określonej reguły autoryzacji dla określonych jednostek przekazujących (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="a4a58-103">Gets the description of a specified authorization rule for a given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="a4a58-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a4a58-104">SYNTAX</span></span>

### <span data-ttu-id="a4a58-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a4a58-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4a58-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="a4a58-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4a58-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="a4a58-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4a58-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a4a58-108">DESCRIPTION</span></span>
<span data-ttu-id="a4a58-109">Polecenie cmdlet **Get-AzRelayAuthorizationRule** Pobiera opis określonej reguły autoryzacji w określonych jednostkach przekazujących (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="a4a58-109">The **Get-AzRelayAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="a4a58-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a4a58-110">EXAMPLES</span></span>

### <span data-ttu-id="a4a58-111">Przykład 1: przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="a4a58-111">Example 1: Namespace</span></span>
```powershell
PS C:\> Get-AzRelayNamespaceAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/Aut
         hoRule1
```

<span data-ttu-id="a4a58-112">Zwraca opis określonej reguły autoryzacji dla określonego obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="a4a58-112">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="a4a58-113">Przykład 2: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="a4a58-113">Example 2: WcfRelay</span></span>
```powershell
PS C:\>Get-AzWcfRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay
         1/authorizationRules/AuthoRule1
```

<span data-ttu-id="a4a58-114">Zwraca określony opis reguły autoryzacji dla danego WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="a4a58-114">Returns the specified authorization rule description for a given WcfRelay.</span></span>

### <span data-ttu-id="a4a58-115">Przykład 3: HybridConnection</span><span class="sxs-lookup"><span data-stu-id="a4a58-115">Example 3: HybridConnection</span></span>
```powershell
PS C:\> Get-AzRelayHybridConnectionAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnections TestHybridConnection -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/Test
         HybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="a4a58-116">Zwraca określony opis reguły autoryzacji dla danego HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="a4a58-116">Returns the specified authorization rule description for a given HybridConnection.</span></span>

## <span data-ttu-id="a4a58-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a4a58-117">PARAMETERS</span></span>

### <span data-ttu-id="a4a58-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4a58-118">-DefaultProfile</span></span>
<span data-ttu-id="a4a58-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a4a58-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4a58-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="a4a58-120">-HybridConnection</span></span>
<span data-ttu-id="a4a58-121">Nazwa HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="a4a58-121">HybridConnection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4a58-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a4a58-122">-Name</span></span>
<span data-ttu-id="a4a58-123">Nazwa AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="a4a58-123">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4a58-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a4a58-124">-Namespace</span></span>
<span data-ttu-id="a4a58-125">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="a4a58-125">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4a58-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4a58-126">-ResourceGroupName</span></span>
<span data-ttu-id="a4a58-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a4a58-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4a58-128">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="a4a58-128">-WcfRelay</span></span>
<span data-ttu-id="a4a58-129">Nazwa WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="a4a58-129">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4a58-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4a58-130">CommonParameters</span></span>
<span data-ttu-id="a4a58-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4a58-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4a58-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4a58-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4a58-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a4a58-133">INPUTS</span></span>

### <span data-ttu-id="a4a58-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a4a58-134">System.String</span></span>

## <span data-ttu-id="a4a58-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a4a58-135">OUTPUTS</span></span>

### <span data-ttu-id="a4a58-136">Microsoft. Azure. Commands. Relay. modele. PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="a4a58-136">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="a4a58-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a4a58-137">NOTES</span></span>

## <span data-ttu-id="a4a58-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a4a58-138">RELATED LINKS</span></span>
