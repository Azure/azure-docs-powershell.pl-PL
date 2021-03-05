---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/get-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusRule.md
ms.openlocfilehash: 0dc9c54b3d2a080d7bb40c8560371b31f4ad3acf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993385"
---
# <span data-ttu-id="738e0-101">Get-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="738e0-101">Get-AzServiceBusRule</span></span>

## <span data-ttu-id="738e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="738e0-102">SYNOPSIS</span></span>
<span data-ttu-id="738e0-103">Pobiera definicję istniejącej reguły w danej subskrypcji tematu.</span><span class="sxs-lookup"><span data-stu-id="738e0-103">Retrieves the definition of an existing rule in a given Subscription of Topic.</span></span> 

## <span data-ttu-id="738e0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="738e0-104">SYNTAX</span></span>

```
Get-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="738e0-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="738e0-105">DESCRIPTION</span></span>
<span data-ttu-id="738e0-106">Polecenie **cmdlet Get-AzServiceBusRule** pobiera opis określonej reguły w danej subskrypcji tematu.</span><span class="sxs-lookup"><span data-stu-id="738e0-106">The **Get-AzServiceBusRule** cmdlet gets the description of the specified rule in the given subscription of topic.</span></span>

## <span data-ttu-id="738e0-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="738e0-107">EXAMPLES</span></span>

### <span data-ttu-id="738e0-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="738e0-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="738e0-109">Zwraca opis określonej reguły dla określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="738e0-109">Returns the specified rule description for a specified subscription.</span></span>

### <span data-ttu-id="738e0-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="738e0-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription
```

<span data-ttu-id="738e0-111">Zwraca listę opisów reguł dla określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="738e0-111">Returns list of rule descriptions for a specified subscription.</span></span>  <span data-ttu-id="738e0-112">Domyślnie zostanie zwrócona reguła 100, jeśli zostanie zwróconych więcej niż 100 reguł, użyj parametru -MaxCount.</span><span class="sxs-lookup"><span data-stu-id="738e0-112">By default 100 rule will be returned, if more than 100 rule to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="738e0-113">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="738e0-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -MaxCount 150
```

<span data-ttu-id="738e0-114">Zwraca listę pierwszych 150 opisów reguł dla określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="738e0-114">Returns list of first 150 rules descriptions for a specified subscription.</span></span>

## <span data-ttu-id="738e0-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="738e0-115">PARAMETERS</span></span>

### <span data-ttu-id="738e0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="738e0-116">-DefaultProfile</span></span>
<span data-ttu-id="738e0-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="738e0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="738e0-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="738e0-118">-MaxCount</span></span>
<span data-ttu-id="738e0-119">Określ maksymalną liczbę reguł do zwrócenia.</span><span class="sxs-lookup"><span data-stu-id="738e0-119">Determine the maximum number of Rules to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="738e0-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="738e0-120">-Name</span></span>
<span data-ttu-id="738e0-121">Nazwa reguły</span><span class="sxs-lookup"><span data-stu-id="738e0-121">Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="738e0-122">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="738e0-122">-Namespace</span></span>
<span data-ttu-id="738e0-123">Nazwa przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="738e0-123">Namespace Name</span></span>

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

### <span data-ttu-id="738e0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="738e0-124">-ResourceGroupName</span></span>
<span data-ttu-id="738e0-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="738e0-125">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="738e0-126">— Subskrypcja</span><span class="sxs-lookup"><span data-stu-id="738e0-126">-Subscription</span></span>
<span data-ttu-id="738e0-127">Nazwa subskrypcji</span><span class="sxs-lookup"><span data-stu-id="738e0-127">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="738e0-128">— Temat</span><span class="sxs-lookup"><span data-stu-id="738e0-128">-Topic</span></span>
<span data-ttu-id="738e0-129">Nazwa tematu</span><span class="sxs-lookup"><span data-stu-id="738e0-129">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="738e0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="738e0-130">CommonParameters</span></span>
<span data-ttu-id="738e0-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="738e0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="738e0-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="738e0-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="738e0-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="738e0-133">INPUTS</span></span>

### <span data-ttu-id="738e0-134">System.String</span><span class="sxs-lookup"><span data-stu-id="738e0-134">System.String</span></span>

## <span data-ttu-id="738e0-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="738e0-135">OUTPUTS</span></span>

### <span data-ttu-id="738e0-136">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="738e0-136">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="738e0-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="738e0-137">NOTES</span></span>

## <span data-ttu-id="738e0-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="738e0-138">RELATED LINKS</span></span>
