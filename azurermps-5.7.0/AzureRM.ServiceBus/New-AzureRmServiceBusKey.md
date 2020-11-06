---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusKey.md
ms.openlocfilehash: 0dc0e2ebf22d995577abd37e2eef2b16b0ea4001
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549563"
---
# <span data-ttu-id="e7489-101">New-AzureRmServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="e7489-101">New-AzureRmServiceBusKey</span></span>

## <span data-ttu-id="e7489-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e7489-102">SYNOPSIS</span></span>
<span data-ttu-id="e7489-103">Generuje podstawowe lub pomocnicze ciągi połączeń dla obszaru nazw lub kolejki usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="e7489-103">Regenerates the primary or secondary connection strings for the Service Bus namespace or queue or topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7489-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e7489-104">SYNTAX</span></span>

### <span data-ttu-id="e7489-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e7489-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7489-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="e7489-106">QueueAuthorizationRuleSet</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7489-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="e7489-107">TopicAuthorizationRuleSet</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7489-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e7489-108">DESCRIPTION</span></span>
<span data-ttu-id="e7489-109">Polecenie cmdlet **New-AzureRmServiceBusKey** generuje nowe podstawowe lub pomocnicze ciągi połączeń dla określonego obszaru nazw, kolejki lub tematu oraz reguły autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="e7489-109">The **New-AzureRmServiceBusKey** cmdlet generates new primary or secondary connection strings for the specified namespace or queue or topic and authorization rule.</span></span>

## <span data-ttu-id="e7489-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e7489-110">EXAMPLES</span></span>

### <span data-ttu-id="e7489-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e7489-111">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="e7489-112">Regeneruje podstawowy lub pomocniczy ciąg połączenia dla obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="e7489-112">Regenerates the primary or secondary connection strings for the namespace.</span></span>

### <span data-ttu-id="e7489-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e7489-113">Example 2</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="e7489-114">Regeneruje podstawowy lub pomocniczy ciąg połączenia dla kolejki.</span><span class="sxs-lookup"><span data-stu-id="e7489-114">Regenerates the primary or secondary connection strings for the queue.</span></span>

### <span data-ttu-id="e7489-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="e7489-115">Example 3</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="e7489-116">Regeneruje podstawowy lub pomocniczy ciąg połączenia dla tematu.</span><span class="sxs-lookup"><span data-stu-id="e7489-116">Regenerates the primary or secondary connection strings for the topic.</span></span>

## <span data-ttu-id="e7489-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e7489-117">PARAMETERS</span></span>

### <span data-ttu-id="e7489-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7489-118">-DefaultProfile</span></span>
<span data-ttu-id="e7489-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e7489-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7489-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e7489-120">-Name</span></span>
<span data-ttu-id="e7489-121">Nazwa AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="e7489-121">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7489-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e7489-122">-Namespace</span></span>
<span data-ttu-id="e7489-123">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="e7489-123">Namespace Name</span></span>

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

### <span data-ttu-id="e7489-124">-Queue</span><span class="sxs-lookup"><span data-stu-id="e7489-124">-Queue</span></span>
<span data-ttu-id="e7489-125">Nazwa kolejki</span><span class="sxs-lookup"><span data-stu-id="e7489-125">Queue Name</span></span>

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

### <span data-ttu-id="e7489-126">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="e7489-126">-RegenerateKey</span></span>
<span data-ttu-id="e7489-127">Ponowne generowanie kluczy — "Primarykea"/"SecondaryKey".</span><span class="sxs-lookup"><span data-stu-id="e7489-127">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7489-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7489-128">-ResourceGroupName</span></span>
<span data-ttu-id="e7489-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="e7489-129">Resource Group Name</span></span>

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

### <span data-ttu-id="e7489-130">— Temat</span><span class="sxs-lookup"><span data-stu-id="e7489-130">-Topic</span></span>
<span data-ttu-id="e7489-131">Nazwa tematu</span><span class="sxs-lookup"><span data-stu-id="e7489-131">Topic Name</span></span>

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

### <span data-ttu-id="e7489-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e7489-132">-Confirm</span></span>
<span data-ttu-id="e7489-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7489-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7489-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7489-134">-WhatIf</span></span>
<span data-ttu-id="e7489-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7489-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7489-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e7489-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7489-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7489-137">CommonParameters</span></span>
<span data-ttu-id="e7489-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7489-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e7489-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7489-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7489-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7489-140">INPUTS</span></span>

### <span data-ttu-id="e7489-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e7489-141">System.String</span></span>


## <span data-ttu-id="e7489-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e7489-142">OUTPUTS</span></span>

### <span data-ttu-id="e7489-143">Microsoft. Azure. Commands. ServiceBus. models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="e7489-143">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>


## <span data-ttu-id="e7489-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e7489-144">NOTES</span></span>

## <span data-ttu-id="e7489-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e7489-145">RELATED LINKS</span></span>
