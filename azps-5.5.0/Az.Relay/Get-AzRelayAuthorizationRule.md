---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayAuthorizationRule.md
ms.openlocfilehash: af83820d33b9f36d93cc7623001d22a6cb5e0212
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240163"
---
# <span data-ttu-id="29599-101">Get-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="29599-101">Get-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="29599-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29599-102">SYNOPSIS</span></span>
<span data-ttu-id="29599-103">Pobiera opis określonej reguły autoryzacji dla określonej jednostki przekazywania (Przestrzeń nazw/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="29599-103">Gets the description of a specified authorization rule for a given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="29599-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="29599-104">SYNTAX</span></span>

### <span data-ttu-id="29599-105">NamespaceAuthorizationRuleSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="29599-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29599-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="29599-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29599-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="29599-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29599-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="29599-108">DESCRIPTION</span></span>
<span data-ttu-id="29599-109">Polecenie **cmdlet Get-AzRelayAuthorizationRule** pobiera opis określonej reguły autoryzacji w podanych jednostkach przekazywania (Przestrzeń nazw/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="29599-109">The **Get-AzRelayAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="29599-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="29599-110">EXAMPLES</span></span>

### <span data-ttu-id="29599-111">Przykład 1. Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="29599-111">Example 1: Namespace</span></span>
```powershell
PS C:\> Get-AzRelayNamespaceAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/Aut
         hoRule1
```

<span data-ttu-id="29599-112">Zwraca opis określonej reguły autoryzacji dla określonej przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="29599-112">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="29599-113">Przykład 2. WcfRelay</span><span class="sxs-lookup"><span data-stu-id="29599-113">Example 2: WcfRelay</span></span>
```powershell
PS C:\>Get-AzWcfRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay
         1/authorizationRules/AuthoRule1
```

<span data-ttu-id="29599-114">Zwraca opis określonej reguły autoryzacji dla danej aplikacji WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="29599-114">Returns the specified authorization rule description for a given WcfRelay.</span></span>

### <span data-ttu-id="29599-115">Przykład 3. HybridConnection</span><span class="sxs-lookup"><span data-stu-id="29599-115">Example 3: HybridConnection</span></span>
```powershell
PS C:\> Get-AzRelayHybridConnectionAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnections TestHybridConnection -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/Test
         HybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="29599-116">Zwraca określony opis reguły autoryzacji dla danego połączenia hybrydowego.</span><span class="sxs-lookup"><span data-stu-id="29599-116">Returns the specified authorization rule description for a given HybridConnection.</span></span>

## <span data-ttu-id="29599-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29599-117">PARAMETERS</span></span>

### <span data-ttu-id="29599-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29599-118">-DefaultProfile</span></span>
<span data-ttu-id="29599-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="29599-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29599-120">- HybridConnection</span><span class="sxs-lookup"><span data-stu-id="29599-120">-HybridConnection</span></span>
<span data-ttu-id="29599-121">Nazwa połączenia hybrydowego.</span><span class="sxs-lookup"><span data-stu-id="29599-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="29599-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="29599-122">-Name</span></span>
<span data-ttu-id="29599-123">Nazwa podmiotu autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="29599-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="29599-124">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="29599-124">-Namespace</span></span>
<span data-ttu-id="29599-125">Nazwa przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="29599-125">Namespace Name.</span></span>

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

### <span data-ttu-id="29599-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29599-126">-ResourceGroupName</span></span>
<span data-ttu-id="29599-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="29599-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="29599-128">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="29599-128">-WcfRelay</span></span>
<span data-ttu-id="29599-129">Nazwa aplikacji WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="29599-129">WcfRelay Name.</span></span>

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

### <span data-ttu-id="29599-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29599-130">CommonParameters</span></span>
<span data-ttu-id="29599-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29599-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29599-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29599-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29599-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="29599-133">INPUTS</span></span>

### <span data-ttu-id="29599-134">System.String</span><span class="sxs-lookup"><span data-stu-id="29599-134">System.String</span></span>

## <span data-ttu-id="29599-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="29599-135">OUTPUTS</span></span>

### <span data-ttu-id="29599-136">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="29599-136">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="29599-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="29599-137">NOTES</span></span>

## <span data-ttu-id="29599-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="29599-138">RELATED LINKS</span></span>
