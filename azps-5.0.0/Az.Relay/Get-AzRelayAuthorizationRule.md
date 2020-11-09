---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayAuthorizationRule.md
ms.openlocfilehash: af83820d33b9f36d93cc7623001d22a6cb5e0212
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317826"
---
# <span data-ttu-id="b30fa-101">Get-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b30fa-101">Get-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="b30fa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b30fa-102">SYNOPSIS</span></span>
<span data-ttu-id="b30fa-103">Pobiera opis określonej reguły autoryzacji dla określonych jednostek przekazujących (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="b30fa-103">Gets the description of a specified authorization rule for a given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="b30fa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b30fa-104">SYNTAX</span></span>

### <span data-ttu-id="b30fa-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b30fa-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b30fa-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="b30fa-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b30fa-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="b30fa-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b30fa-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b30fa-108">DESCRIPTION</span></span>
<span data-ttu-id="b30fa-109">Polecenie cmdlet **Get-AzRelayAuthorizationRule** Pobiera opis określonej reguły autoryzacji w określonych jednostkach przekazujących (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="b30fa-109">The **Get-AzRelayAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="b30fa-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b30fa-110">EXAMPLES</span></span>

### <span data-ttu-id="b30fa-111">Przykład 1: przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="b30fa-111">Example 1: Namespace</span></span>
```powershell
PS C:\> Get-AzRelayNamespaceAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/Aut
         hoRule1
```

<span data-ttu-id="b30fa-112">Zwraca opis określonej reguły autoryzacji dla określonego obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="b30fa-112">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="b30fa-113">Przykład 2: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="b30fa-113">Example 2: WcfRelay</span></span>
```powershell
PS C:\>Get-AzWcfRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay
         1/authorizationRules/AuthoRule1
```

<span data-ttu-id="b30fa-114">Zwraca określony opis reguły autoryzacji dla danego WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="b30fa-114">Returns the specified authorization rule description for a given WcfRelay.</span></span>

### <span data-ttu-id="b30fa-115">Przykład 3: HybridConnection</span><span class="sxs-lookup"><span data-stu-id="b30fa-115">Example 3: HybridConnection</span></span>
```powershell
PS C:\> Get-AzRelayHybridConnectionAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnections TestHybridConnection -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/Test
         HybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="b30fa-116">Zwraca określony opis reguły autoryzacji dla danego HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="b30fa-116">Returns the specified authorization rule description for a given HybridConnection.</span></span>

## <span data-ttu-id="b30fa-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b30fa-117">PARAMETERS</span></span>

### <span data-ttu-id="b30fa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b30fa-118">-DefaultProfile</span></span>
<span data-ttu-id="b30fa-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b30fa-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b30fa-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="b30fa-120">-HybridConnection</span></span>
<span data-ttu-id="b30fa-121">Nazwa HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="b30fa-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="b30fa-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b30fa-122">-Name</span></span>
<span data-ttu-id="b30fa-123">Nazwa AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="b30fa-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="b30fa-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b30fa-124">-Namespace</span></span>
<span data-ttu-id="b30fa-125">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="b30fa-125">Namespace Name.</span></span>

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

### <span data-ttu-id="b30fa-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b30fa-126">-ResourceGroupName</span></span>
<span data-ttu-id="b30fa-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b30fa-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="b30fa-128">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="b30fa-128">-WcfRelay</span></span>
<span data-ttu-id="b30fa-129">Nazwa WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="b30fa-129">WcfRelay Name.</span></span>

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

### <span data-ttu-id="b30fa-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b30fa-130">CommonParameters</span></span>
<span data-ttu-id="b30fa-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b30fa-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b30fa-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b30fa-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b30fa-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b30fa-133">INPUTS</span></span>

### <span data-ttu-id="b30fa-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b30fa-134">System.String</span></span>

## <span data-ttu-id="b30fa-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b30fa-135">OUTPUTS</span></span>

### <span data-ttu-id="b30fa-136">Microsoft. Azure. Commands. Relay. modele. PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="b30fa-136">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="b30fa-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b30fa-137">NOTES</span></span>

## <span data-ttu-id="b30fa-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b30fa-138">RELATED LINKS</span></span>
