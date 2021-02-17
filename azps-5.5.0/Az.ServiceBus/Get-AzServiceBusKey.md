---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusKey.md
ms.openlocfilehash: ffe220510f3046ea10b6374eb48c3c74730e4bc2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183531"
---
# <span data-ttu-id="2e100-101">Get-AzServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="2e100-101">Get-AzServiceBusKey</span></span>

## <span data-ttu-id="2e100-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e100-102">SYNOPSIS</span></span>
<span data-ttu-id="2e100-103">Pobiera podstawowe i pomocnicze parametry połączenia dla danej przestrzeni nazw lub konfiguracji kolejki, tematu lub aliasu (GeoDR).</span><span class="sxs-lookup"><span data-stu-id="2e100-103">Gets the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="2e100-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2e100-104">SYNTAX</span></span>

### <span data-ttu-id="2e100-105">NamespaceAuthorizationRuleSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="2e100-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e100-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="2e100-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e100-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="2e100-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e100-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="2e100-108">AliasAuthoRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e100-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="2e100-109">DESCRIPTION</span></span>
<span data-ttu-id="2e100-110">Polecenie **cmdlet Get-AzServiceBusKey** zwraca podstawowe i pomocnicze parametry połączenia dla danej przestrzeni nazw lub kolejki, tematu lub aliasu (konfiguracje GeoDR).</span><span class="sxs-lookup"><span data-stu-id="2e100-110">The **Get-AzServiceBusKey** cmdlet returns the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="2e100-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2e100-111">EXAMPLES</span></span>

### <span data-ttu-id="2e100-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2e100-112">Example 1</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="2e100-113">Podstawowe i pomocnicze ciągi połączenia do określonej przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="2e100-113">Primary and secondary connection string to the specified namespace.</span></span>

### <span data-ttu-id="2e100-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="2e100-114">Example 2</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="2e100-115">Podstawowe i pomocnicze ciągi połączeń do określonej kolejki.</span><span class="sxs-lookup"><span data-stu-id="2e100-115">Primary and secondary connection string to the specified queue.</span></span>

### <span data-ttu-id="2e100-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="2e100-116">Example 3</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="2e100-117">Podstawowe i pomocnicze parametrów połączenia z określonym tematem.</span><span class="sxs-lookup"><span data-stu-id="2e100-117">Primary and secondary connection string to the specified topic.</span></span>

### <span data-ttu-id="2e100-118">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="2e100-118">Example 4</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="2e100-119">Podstawowe i pomocnicze ciągi połączenia do określonej przestrzeni nazw i aliasu.</span><span class="sxs-lookup"><span data-stu-id="2e100-119">Primary and secondary connection string to the specified namespace and alias.</span></span>

## <span data-ttu-id="2e100-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e100-120">PARAMETERS</span></span>

### <span data-ttu-id="2e100-121">-AliasName</span><span class="sxs-lookup"><span data-stu-id="2e100-121">-AliasName</span></span>
<span data-ttu-id="2e100-122">Nazwa aliasu</span><span class="sxs-lookup"><span data-stu-id="2e100-122">Alias Name</span></span>

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

### <span data-ttu-id="2e100-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e100-123">-DefaultProfile</span></span>
<span data-ttu-id="2e100-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2e100-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e100-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="2e100-125">-Name</span></span>
<span data-ttu-id="2e100-126">Nazwa podmiotu autoryzacji</span><span class="sxs-lookup"><span data-stu-id="2e100-126">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="2e100-127">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="2e100-127">-Namespace</span></span>
<span data-ttu-id="2e100-128">Nazwa przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="2e100-128">Namespace Name</span></span>

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

### <span data-ttu-id="2e100-129">— Kolejka</span><span class="sxs-lookup"><span data-stu-id="2e100-129">-Queue</span></span>
<span data-ttu-id="2e100-130">Nazwa kolejki</span><span class="sxs-lookup"><span data-stu-id="2e100-130">Queue Name</span></span>

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

### <span data-ttu-id="2e100-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e100-131">-ResourceGroupName</span></span>
<span data-ttu-id="2e100-132">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="2e100-132">Resource Group Name</span></span>

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

### <span data-ttu-id="2e100-133">— Temat</span><span class="sxs-lookup"><span data-stu-id="2e100-133">-Topic</span></span>
<span data-ttu-id="2e100-134">Nazwa tematu</span><span class="sxs-lookup"><span data-stu-id="2e100-134">Topic Name</span></span>

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

### <span data-ttu-id="2e100-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e100-135">CommonParameters</span></span>
<span data-ttu-id="2e100-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e100-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e100-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e100-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e100-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2e100-138">INPUTS</span></span>

### <span data-ttu-id="2e100-139">System.String</span><span class="sxs-lookup"><span data-stu-id="2e100-139">System.String</span></span>

## <span data-ttu-id="2e100-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2e100-140">OUTPUTS</span></span>

### <span data-ttu-id="2e100-141">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="2e100-141">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="2e100-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2e100-142">NOTES</span></span>

## <span data-ttu-id="2e100-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2e100-143">RELATED LINKS</span></span>
