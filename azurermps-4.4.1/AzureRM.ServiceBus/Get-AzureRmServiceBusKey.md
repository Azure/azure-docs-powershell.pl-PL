---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusKey.md
ms.openlocfilehash: 28abf3ff725f5a1b124f99c96b46d03458b42f8e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527301"
---
# <span data-ttu-id="914f1-101">Get-AzureRmServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="914f1-101">Get-AzureRmServiceBusKey</span></span>

## <span data-ttu-id="914f1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="914f1-102">SYNOPSIS</span></span>
<span data-ttu-id="914f1-103">Pobiera podstawowe i pomocnicze ciągi połączeń dla danej przestrzeni nazw lub kolejki lub tematu.</span><span class="sxs-lookup"><span data-stu-id="914f1-103">Gets the primary and secondary connection strings for the given Namespace or Queue or Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="914f1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="914f1-104">SYNTAX</span></span>

### <span data-ttu-id="914f1-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="914f1-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="914f1-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="914f1-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="914f1-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="914f1-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="914f1-108">Opis</span><span class="sxs-lookup"><span data-stu-id="914f1-108">DESCRIPTION</span></span>
<span data-ttu-id="914f1-109">Polecenie cmdlet **Get-AzureRmServiceBusKey** zwraca podstawowe i pomocnicze ciągi połączeń dla danej przestrzeni nazw lub kolejki lub tematu.</span><span class="sxs-lookup"><span data-stu-id="914f1-109">The **Get-AzureRmServiceBusKey** cmdlet returns the primary and secondary connection strings for the given Namespace or Queue or Topic.</span></span> 

## <span data-ttu-id="914f1-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="914f1-110">EXAMPLES</span></span>

### <span data-ttu-id="914f1-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="914f1-111">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="914f1-112">Podstawowy i pomocniczy ciąg połączenia z określoną przestrzenią nazw.</span><span class="sxs-lookup"><span data-stu-id="914f1-112">Primary and secondary connection string to the specified namespace.</span></span>

### <span data-ttu-id="914f1-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="914f1-113">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="914f1-114">Podstawowy i pomocniczy ciąg połączenia z określoną kolejką.</span><span class="sxs-lookup"><span data-stu-id="914f1-114">Primary and secondary connection string to the specified queue.</span></span>

### <span data-ttu-id="914f1-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="914f1-115">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="914f1-116">Podstawowy i pomocniczy ciąg połączenia z określonym tematem.</span><span class="sxs-lookup"><span data-stu-id="914f1-116">Primary and secondary connection string to the specified topic.</span></span>

## <span data-ttu-id="914f1-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="914f1-117">PARAMETERS</span></span>

### <span data-ttu-id="914f1-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="914f1-118">-Name</span></span>
<span data-ttu-id="914f1-119">Nazwa AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="914f1-119">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="914f1-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="914f1-120">-Namespace</span></span>
<span data-ttu-id="914f1-121">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="914f1-121">Namespace Name.</span></span>

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

### <span data-ttu-id="914f1-122">-Queue</span><span class="sxs-lookup"><span data-stu-id="914f1-122">-Queue</span></span>
<span data-ttu-id="914f1-123">Nazwa kolejki.</span><span class="sxs-lookup"><span data-stu-id="914f1-123">Queue Name.</span></span>

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

### <span data-ttu-id="914f1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="914f1-124">-ResourceGroupName</span></span>
<span data-ttu-id="914f1-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="914f1-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="914f1-126">— Temat</span><span class="sxs-lookup"><span data-stu-id="914f1-126">-Topic</span></span>
<span data-ttu-id="914f1-127">Nazwa tematu.</span><span class="sxs-lookup"><span data-stu-id="914f1-127">Topic Name.</span></span>

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

### <span data-ttu-id="914f1-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="914f1-128">-DefaultProfile</span></span>
<span data-ttu-id="914f1-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="914f1-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="914f1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="914f1-130">CommonParameters</span></span>
<span data-ttu-id="914f1-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="914f1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="914f1-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="914f1-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="914f1-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="914f1-133">INPUTS</span></span>

### <span data-ttu-id="914f1-134">System. String</span><span class="sxs-lookup"><span data-stu-id="914f1-134">System.String</span></span>

## <span data-ttu-id="914f1-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="914f1-135">OUTPUTS</span></span>

### <span data-ttu-id="914f1-136">Microsoft. Azure. Commands. ServiceBus. models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="914f1-136">Microsoft.Azure.Commands.ServiceBus.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="914f1-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="914f1-137">NOTES</span></span>

## <span data-ttu-id="914f1-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="914f1-138">RELATED LINKS</span></span>

