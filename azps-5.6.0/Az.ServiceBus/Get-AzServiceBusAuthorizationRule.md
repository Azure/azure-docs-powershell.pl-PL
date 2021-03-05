---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/get-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: 39f43af6685f754cacfd1340560fd4c3429f792d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961681"
---
# <span data-ttu-id="6079e-101">Get-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6079e-101">Get-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="6079e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6079e-102">SYNOPSIS</span></span>
<span data-ttu-id="6079e-103">Pobiera opis określonej reguły autoryzacji dla danej przestrzeni nazw, kolejki, tematu lub aliasu (konfiguracje GeoDR).</span><span class="sxs-lookup"><span data-stu-id="6079e-103">Gets a description of the specified authorization rule for a given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span> 

## <span data-ttu-id="6079e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6079e-104">SYNTAX</span></span>

### <span data-ttu-id="6079e-105">NamespaceAuthorizationRuleSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="6079e-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6079e-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="6079e-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6079e-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="6079e-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6079e-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="6079e-108">AliasAuthoRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6079e-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="6079e-109">DESCRIPTION</span></span>
<span data-ttu-id="6079e-110">Polecenie **cmdlet Get-AzServiceBusAuthorizationRule** pobiera opis określonej reguły autoryzacji w danej przestrzeni nazw, kolejce, temacie lub aliasie (konfiguracjach geodr).</span><span class="sxs-lookup"><span data-stu-id="6079e-110">The **Get-AzServiceBusAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="6079e-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6079e-111">EXAMPLES</span></span>

### <span data-ttu-id="6079e-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6079e-112">Example 1</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="6079e-113">Zwraca opis określonej reguły autoryzacji dla określonej przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="6079e-113">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="6079e-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="6079e-114">Example 2</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="6079e-115">Zwraca opis określonej reguły autoryzacji dla określonej kolejki.</span><span class="sxs-lookup"><span data-stu-id="6079e-115">Returns the specified authorization rule description for a specified queue.</span></span>

### <span data-ttu-id="6079e-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="6079e-116">Example 3</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="6079e-117">Zwraca opis określonej reguły autoryzacji dla określonego tematu.</span><span class="sxs-lookup"><span data-stu-id="6079e-117">Returns the specified authorization rule description for a specified topic.</span></span>

### <span data-ttu-id="6079e-118">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="6079e-118">Example 4</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="6079e-119">Zwraca opis określonej reguły autoryzacji dla określonej przestrzeni nazw i aliasu.</span><span class="sxs-lookup"><span data-stu-id="6079e-119">Returns the specified authorization rule description for a specified namespace and alias.</span></span>

## <span data-ttu-id="6079e-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6079e-120">PARAMETERS</span></span>

### <span data-ttu-id="6079e-121">-AliasName</span><span class="sxs-lookup"><span data-stu-id="6079e-121">-AliasName</span></span>
<span data-ttu-id="6079e-122">Nazwa konfiguracji geodr</span><span class="sxs-lookup"><span data-stu-id="6079e-122">GeoDR Configuration Name</span></span>

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

### <span data-ttu-id="6079e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6079e-123">-DefaultProfile</span></span>
<span data-ttu-id="6079e-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6079e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6079e-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6079e-125">-Name</span></span>
<span data-ttu-id="6079e-126">Nazwa podmiotu autoryzacji</span><span class="sxs-lookup"><span data-stu-id="6079e-126">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="6079e-127">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="6079e-127">-Namespace</span></span>
<span data-ttu-id="6079e-128">Nazwa przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="6079e-128">Namespace Name</span></span>

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

### <span data-ttu-id="6079e-129">— Kolejka</span><span class="sxs-lookup"><span data-stu-id="6079e-129">-Queue</span></span>
<span data-ttu-id="6079e-130">Nazwa kolejki</span><span class="sxs-lookup"><span data-stu-id="6079e-130">Queue Name</span></span>

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

### <span data-ttu-id="6079e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6079e-131">-ResourceGroupName</span></span>
<span data-ttu-id="6079e-132">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="6079e-132">Resource Group Name</span></span>

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

### <span data-ttu-id="6079e-133">— Temat</span><span class="sxs-lookup"><span data-stu-id="6079e-133">-Topic</span></span>
<span data-ttu-id="6079e-134">Nazwa tematu</span><span class="sxs-lookup"><span data-stu-id="6079e-134">Topic Name</span></span>

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

### <span data-ttu-id="6079e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6079e-135">CommonParameters</span></span>
<span data-ttu-id="6079e-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6079e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6079e-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6079e-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6079e-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6079e-138">INPUTS</span></span>

### <span data-ttu-id="6079e-139">System.String</span><span class="sxs-lookup"><span data-stu-id="6079e-139">System.String</span></span>

## <span data-ttu-id="6079e-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6079e-140">OUTPUTS</span></span>

### <span data-ttu-id="6079e-141">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="6079e-141">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="6079e-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6079e-142">NOTES</span></span>

## <span data-ttu-id="6079e-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6079e-143">RELATED LINKS</span></span>
