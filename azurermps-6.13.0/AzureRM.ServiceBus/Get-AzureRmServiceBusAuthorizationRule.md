---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: 8c69ab59f539180c3146f01c7a5fce9907b40c8a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716560"
---
# <span data-ttu-id="67234-101">Get-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="67234-101">Get-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="67234-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="67234-102">SYNOPSIS</span></span>
<span data-ttu-id="67234-103">Pobiera opis określonej reguły autoryzacji dla określonego obszaru nazw lub kolejki lub tematu albo aliasu (GeoDR).</span><span class="sxs-lookup"><span data-stu-id="67234-103">Gets a description of the specified authorization rule for a given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67234-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="67234-104">SYNTAX</span></span>

### <span data-ttu-id="67234-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="67234-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67234-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="67234-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67234-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="67234-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67234-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="67234-108">AliasAuthoRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String>
 [-AliasName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67234-109">Opis</span><span class="sxs-lookup"><span data-stu-id="67234-109">DESCRIPTION</span></span>
<span data-ttu-id="67234-110">Polecenie cmdlet **Get-AzureRmServiceBusAuthorizationRule** Pobiera opis określonej reguły autoryzacji w danym obszarze nazw lub kolejce albo temacie lub aliasze (Konfiguracja GeoDR).</span><span class="sxs-lookup"><span data-stu-id="67234-110">The **Get-AzureRmServiceBusAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="67234-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="67234-111">EXAMPLES</span></span>

### <span data-ttu-id="67234-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="67234-112">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="67234-113">Zwraca opis określonej reguły autoryzacji dla określonego obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="67234-113">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="67234-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="67234-114">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="67234-115">Zwraca opis reguły autoryzacji określonej kolejki.</span><span class="sxs-lookup"><span data-stu-id="67234-115">Returns the specified authorization rule description for a specified queue.</span></span>

### <span data-ttu-id="67234-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="67234-116">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="67234-117">Zwraca opis reguły autoryzacji określonego tematu.</span><span class="sxs-lookup"><span data-stu-id="67234-117">Returns the specified authorization rule description for a specified topic.</span></span>

### <span data-ttu-id="67234-118">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="67234-118">Example 4</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="67234-119">Zwraca opis reguły autoryzacji określonego obszaru nazw i aliasu.</span><span class="sxs-lookup"><span data-stu-id="67234-119">Returns the specified authorization rule description for a specified namespace and alias.</span></span>

## <span data-ttu-id="67234-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="67234-120">PARAMETERS</span></span>

### <span data-ttu-id="67234-121">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="67234-121">-AliasName</span></span>
<span data-ttu-id="67234-122">Nazwa konfiguracji GeoDR</span><span class="sxs-lookup"><span data-stu-id="67234-122">GeoDR Configuration Name</span></span>

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

### <span data-ttu-id="67234-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67234-123">-DefaultProfile</span></span>
<span data-ttu-id="67234-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="67234-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67234-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="67234-125">-Name</span></span>
<span data-ttu-id="67234-126">Nazwa AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="67234-126">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="67234-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="67234-127">-Namespace</span></span>
<span data-ttu-id="67234-128">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="67234-128">Namespace Name</span></span>

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

### <span data-ttu-id="67234-129">-Queue</span><span class="sxs-lookup"><span data-stu-id="67234-129">-Queue</span></span>
<span data-ttu-id="67234-130">Nazwa kolejki</span><span class="sxs-lookup"><span data-stu-id="67234-130">Queue Name</span></span>

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

### <span data-ttu-id="67234-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67234-131">-ResourceGroupName</span></span>
<span data-ttu-id="67234-132">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="67234-132">Resource Group Name</span></span>

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

### <span data-ttu-id="67234-133">— Temat</span><span class="sxs-lookup"><span data-stu-id="67234-133">-Topic</span></span>
<span data-ttu-id="67234-134">Nazwa tematu</span><span class="sxs-lookup"><span data-stu-id="67234-134">Topic Name</span></span>

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

### <span data-ttu-id="67234-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67234-135">CommonParameters</span></span>
<span data-ttu-id="67234-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67234-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67234-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67234-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67234-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="67234-138">INPUTS</span></span>

### <span data-ttu-id="67234-139">System. String</span><span class="sxs-lookup"><span data-stu-id="67234-139">System.String</span></span>

## <span data-ttu-id="67234-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="67234-140">OUTPUTS</span></span>

### <span data-ttu-id="67234-141">Microsoft. Azure. Commands. ServiceBus. models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="67234-141">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="67234-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="67234-142">NOTES</span></span>

## <span data-ttu-id="67234-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="67234-143">RELATED LINKS</span></span>
