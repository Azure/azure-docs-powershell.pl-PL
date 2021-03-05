---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/get-azservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusKey.md
ms.openlocfilehash: 28ecd68167a7db2f41ee64a38a4616548707096c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979265"
---
# <span data-ttu-id="df7a1-101">Get-AzServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="df7a1-101">Get-AzServiceBusKey</span></span>

## <span data-ttu-id="df7a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df7a1-102">SYNOPSIS</span></span>
<span data-ttu-id="df7a1-103">Pobiera podstawowe i pomocnicze parametry połączenia dla danej przestrzeni nazw lub konfiguracji kolejki, tematu lub aliasu (GeoDR).</span><span class="sxs-lookup"><span data-stu-id="df7a1-103">Gets the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="df7a1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="df7a1-104">SYNTAX</span></span>

### <span data-ttu-id="df7a1-105">NamespaceAuthorizationRuleSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="df7a1-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df7a1-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="df7a1-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df7a1-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="df7a1-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df7a1-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="df7a1-108">AliasAuthoRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df7a1-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="df7a1-109">DESCRIPTION</span></span>
<span data-ttu-id="df7a1-110">Polecenie **cmdlet Get-AzServiceBusKey** zwraca podstawowe i pomocnicze ciągi połączenia dla danej przestrzeni nazw lub kolejki, tematu lub aliasu (konfiguracji GeoDR).</span><span class="sxs-lookup"><span data-stu-id="df7a1-110">The **Get-AzServiceBusKey** cmdlet returns the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="df7a1-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="df7a1-111">EXAMPLES</span></span>

### <span data-ttu-id="df7a1-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="df7a1-112">Example 1</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="df7a1-113">Podstawowe i pomocnicze ciągi połączenia do określonej przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="df7a1-113">Primary and secondary connection string to the specified namespace.</span></span>

### <span data-ttu-id="df7a1-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="df7a1-114">Example 2</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="df7a1-115">Podstawowe i pomocnicze ciągi połączeń do określonej kolejki.</span><span class="sxs-lookup"><span data-stu-id="df7a1-115">Primary and secondary connection string to the specified queue.</span></span>

### <span data-ttu-id="df7a1-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="df7a1-116">Example 3</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="df7a1-117">Podstawowe i pomocnicze parametrów połączenia z określonym tematem.</span><span class="sxs-lookup"><span data-stu-id="df7a1-117">Primary and secondary connection string to the specified topic.</span></span>

### <span data-ttu-id="df7a1-118">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="df7a1-118">Example 4</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="df7a1-119">Podstawowe i pomocnicze ciągi połączenia do określonej przestrzeni nazw i aliasu.</span><span class="sxs-lookup"><span data-stu-id="df7a1-119">Primary and secondary connection string to the specified namespace and alias.</span></span>

## <span data-ttu-id="df7a1-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df7a1-120">PARAMETERS</span></span>

### <span data-ttu-id="df7a1-121">-AliasName</span><span class="sxs-lookup"><span data-stu-id="df7a1-121">-AliasName</span></span>
<span data-ttu-id="df7a1-122">Nazwa aliasu</span><span class="sxs-lookup"><span data-stu-id="df7a1-122">Alias Name</span></span>

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

### <span data-ttu-id="df7a1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df7a1-123">-DefaultProfile</span></span>
<span data-ttu-id="df7a1-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="df7a1-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df7a1-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="df7a1-125">-Name</span></span>
<span data-ttu-id="df7a1-126">Nazwa podmiotu autoryzacji</span><span class="sxs-lookup"><span data-stu-id="df7a1-126">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df7a1-127">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="df7a1-127">-Namespace</span></span>
<span data-ttu-id="df7a1-128">Nazwa przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="df7a1-128">Namespace Name</span></span>

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

### <span data-ttu-id="df7a1-129">— Kolejka</span><span class="sxs-lookup"><span data-stu-id="df7a1-129">-Queue</span></span>
<span data-ttu-id="df7a1-130">Nazwa kolejki</span><span class="sxs-lookup"><span data-stu-id="df7a1-130">Queue Name</span></span>

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

### <span data-ttu-id="df7a1-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df7a1-131">-ResourceGroupName</span></span>
<span data-ttu-id="df7a1-132">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="df7a1-132">Resource Group Name</span></span>

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

### <span data-ttu-id="df7a1-133">— Temat</span><span class="sxs-lookup"><span data-stu-id="df7a1-133">-Topic</span></span>
<span data-ttu-id="df7a1-134">Nazwa tematu</span><span class="sxs-lookup"><span data-stu-id="df7a1-134">Topic Name</span></span>

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

### <span data-ttu-id="df7a1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df7a1-135">CommonParameters</span></span>
<span data-ttu-id="df7a1-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df7a1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df7a1-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df7a1-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df7a1-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="df7a1-138">INPUTS</span></span>

### <span data-ttu-id="df7a1-139">System.String</span><span class="sxs-lookup"><span data-stu-id="df7a1-139">System.String</span></span>

## <span data-ttu-id="df7a1-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="df7a1-140">OUTPUTS</span></span>

### <span data-ttu-id="df7a1-141">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="df7a1-141">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="df7a1-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="df7a1-142">NOTES</span></span>

## <span data-ttu-id="df7a1-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="df7a1-143">RELATED LINKS</span></span>
