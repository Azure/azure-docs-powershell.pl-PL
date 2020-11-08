---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: e0f6c8c2b07c0d9ab788504bb8eae3eb4615a7e0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052723"
---
# <span data-ttu-id="cdff0-101">Get-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="cdff0-101">Get-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="cdff0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cdff0-102">SYNOPSIS</span></span>
<span data-ttu-id="cdff0-103">Pobiera opis określonej reguły autoryzacji dla określonego obszaru nazw lub kolejki lub tematu albo aliasu (GeoDR).</span><span class="sxs-lookup"><span data-stu-id="cdff0-103">Gets a description of the specified authorization rule for a given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span> 

## <span data-ttu-id="cdff0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cdff0-104">SYNTAX</span></span>

### <span data-ttu-id="cdff0-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cdff0-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cdff0-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="cdff0-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cdff0-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="cdff0-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cdff0-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="cdff0-108">AliasAuthoRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cdff0-109">Opis</span><span class="sxs-lookup"><span data-stu-id="cdff0-109">DESCRIPTION</span></span>
<span data-ttu-id="cdff0-110">Polecenie cmdlet **Get-AzServiceBusAuthorizationRule** Pobiera opis określonej reguły autoryzacji w danym obszarze nazw lub kolejce albo temacie lub aliasze (Konfiguracja GeoDR).</span><span class="sxs-lookup"><span data-stu-id="cdff0-110">The **Get-AzServiceBusAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="cdff0-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cdff0-111">EXAMPLES</span></span>

### <span data-ttu-id="cdff0-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cdff0-112">Example 1</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="cdff0-113">Zwraca opis określonej reguły autoryzacji dla określonego obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="cdff0-113">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="cdff0-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="cdff0-114">Example 2</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="cdff0-115">Zwraca opis reguły autoryzacji określonej kolejki.</span><span class="sxs-lookup"><span data-stu-id="cdff0-115">Returns the specified authorization rule description for a specified queue.</span></span>

### <span data-ttu-id="cdff0-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="cdff0-116">Example 3</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="cdff0-117">Zwraca opis reguły autoryzacji określonego tematu.</span><span class="sxs-lookup"><span data-stu-id="cdff0-117">Returns the specified authorization rule description for a specified topic.</span></span>

### <span data-ttu-id="cdff0-118">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="cdff0-118">Example 4</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="cdff0-119">Zwraca opis reguły autoryzacji określonego obszaru nazw i aliasu.</span><span class="sxs-lookup"><span data-stu-id="cdff0-119">Returns the specified authorization rule description for a specified namespace and alias.</span></span>

## <span data-ttu-id="cdff0-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cdff0-120">PARAMETERS</span></span>

### <span data-ttu-id="cdff0-121">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="cdff0-121">-AliasName</span></span>
<span data-ttu-id="cdff0-122">Nazwa konfiguracji GeoDR</span><span class="sxs-lookup"><span data-stu-id="cdff0-122">GeoDR Configuration Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdff0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdff0-123">-DefaultProfile</span></span>
<span data-ttu-id="cdff0-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cdff0-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdff0-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cdff0-125">-Name</span></span>
<span data-ttu-id="cdff0-126">Nazwa AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="cdff0-126">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdff0-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="cdff0-127">-Namespace</span></span>
<span data-ttu-id="cdff0-128">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="cdff0-128">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdff0-129">-Queue</span><span class="sxs-lookup"><span data-stu-id="cdff0-129">-Queue</span></span>
<span data-ttu-id="cdff0-130">Nazwa kolejki</span><span class="sxs-lookup"><span data-stu-id="cdff0-130">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdff0-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdff0-131">-ResourceGroupName</span></span>
<span data-ttu-id="cdff0-132">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="cdff0-132">Resource Group Name</span></span>

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

### <span data-ttu-id="cdff0-133">— Temat</span><span class="sxs-lookup"><span data-stu-id="cdff0-133">-Topic</span></span>
<span data-ttu-id="cdff0-134">Nazwa tematu</span><span class="sxs-lookup"><span data-stu-id="cdff0-134">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdff0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdff0-135">CommonParameters</span></span>
<span data-ttu-id="cdff0-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdff0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdff0-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdff0-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdff0-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cdff0-138">INPUTS</span></span>

### <span data-ttu-id="cdff0-139">System. String</span><span class="sxs-lookup"><span data-stu-id="cdff0-139">System.String</span></span>

## <span data-ttu-id="cdff0-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cdff0-140">OUTPUTS</span></span>

### <span data-ttu-id="cdff0-141">Microsoft. Azure. Commands. ServiceBus. models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="cdff0-141">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="cdff0-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cdff0-142">NOTES</span></span>

## <span data-ttu-id="cdff0-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cdff0-143">RELATED LINKS</span></span>
