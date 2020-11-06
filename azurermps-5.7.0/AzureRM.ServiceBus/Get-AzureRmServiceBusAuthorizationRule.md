---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: e5a4886eef132f0e48c146fa70889dfa283489b2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542292"
---
# <span data-ttu-id="be769-101">Get-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="be769-101">Get-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="be769-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="be769-102">SYNOPSIS</span></span>
<span data-ttu-id="be769-103">Pobiera opis określonej reguły autoryzacji dla określonego obszaru nazw lub kolejki lub tematu albo aliasu (GeoDR).</span><span class="sxs-lookup"><span data-stu-id="be769-103">Gets a description of the specified authorization rule for a given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span> 


[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be769-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="be769-104">SYNTAX</span></span>

### <span data-ttu-id="be769-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="be769-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be769-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="be769-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be769-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="be769-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be769-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="be769-108">AliasAuthoRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String>
 [-AliasName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be769-109">Opis</span><span class="sxs-lookup"><span data-stu-id="be769-109">DESCRIPTION</span></span>
<span data-ttu-id="be769-110">Polecenie cmdlet **Get-AzureRmServiceBusAuthorizationRule** Pobiera opis określonej reguły autoryzacji w danym obszarze nazw lub kolejce albo temacie lub aliasze (Konfiguracja GeoDR).</span><span class="sxs-lookup"><span data-stu-id="be769-110">The **Get-AzureRmServiceBusAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="be769-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="be769-111">EXAMPLES</span></span>

### <span data-ttu-id="be769-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="be769-112">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="be769-113">Zwraca opis określonej reguły autoryzacji dla określonego obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="be769-113">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="be769-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="be769-114">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="be769-115">Zwraca opis reguły autoryzacji określonej kolejki.</span><span class="sxs-lookup"><span data-stu-id="be769-115">Returns the specified authorization rule description for a specified queue.</span></span>

### <span data-ttu-id="be769-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="be769-116">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="be769-117">Zwraca opis reguły autoryzacji określonego tematu.</span><span class="sxs-lookup"><span data-stu-id="be769-117">Returns the specified authorization rule description for a specified topic.</span></span>

### <span data-ttu-id="be769-118">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="be769-118">Example 4</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="be769-119">Zwraca opis reguły autoryzacji określonego obszaru nazw i aliasu.</span><span class="sxs-lookup"><span data-stu-id="be769-119">Returns the specified authorization rule description for a specified namespace and alias.</span></span>

## <span data-ttu-id="be769-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="be769-120">PARAMETERS</span></span>

### <span data-ttu-id="be769-121">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="be769-121">-AliasName</span></span>
<span data-ttu-id="be769-122">Nazwa konfiguracji GeoDR</span><span class="sxs-lookup"><span data-stu-id="be769-122">GeoDR Configuration Name</span></span>

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

### <span data-ttu-id="be769-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be769-123">-DefaultProfile</span></span>
<span data-ttu-id="be769-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="be769-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be769-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="be769-125">-Name</span></span>
<span data-ttu-id="be769-126">Nazwa AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="be769-126">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="be769-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="be769-127">-Namespace</span></span>
<span data-ttu-id="be769-128">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="be769-128">Namespace Name</span></span>

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

### <span data-ttu-id="be769-129">-Queue</span><span class="sxs-lookup"><span data-stu-id="be769-129">-Queue</span></span>
<span data-ttu-id="be769-130">Nazwa kolejki</span><span class="sxs-lookup"><span data-stu-id="be769-130">Queue Name</span></span>

```yaml
Type: String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be769-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be769-131">-ResourceGroupName</span></span>
<span data-ttu-id="be769-132">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="be769-132">Resource Group Name</span></span>

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

### <span data-ttu-id="be769-133">— Temat</span><span class="sxs-lookup"><span data-stu-id="be769-133">-Topic</span></span>
<span data-ttu-id="be769-134">Nazwa tematu</span><span class="sxs-lookup"><span data-stu-id="be769-134">Topic Name</span></span>

```yaml
Type: String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be769-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be769-135">CommonParameters</span></span>
<span data-ttu-id="be769-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be769-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="be769-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be769-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be769-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="be769-138">INPUTS</span></span>

### <span data-ttu-id="be769-139">System. String</span><span class="sxs-lookup"><span data-stu-id="be769-139">System.String</span></span>


## <span data-ttu-id="be769-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="be769-140">OUTPUTS</span></span>

### <span data-ttu-id="be769-141">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. ServiceBus. MODELES. PSSharedAccessAuthorizationRuleAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="be769-141">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="be769-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="be769-142">NOTES</span></span>

## <span data-ttu-id="be769-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="be769-143">RELATED LINKS</span></span>
