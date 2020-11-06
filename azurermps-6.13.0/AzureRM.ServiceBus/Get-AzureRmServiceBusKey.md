---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusKey.md
ms.openlocfilehash: 96b95a4a6641e3bcfc2c1a18653da4231bee5c42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526034"
---
# <span data-ttu-id="db690-101">Get-AzureRmServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="db690-101">Get-AzureRmServiceBusKey</span></span>

## <span data-ttu-id="db690-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="db690-102">SYNOPSIS</span></span>
<span data-ttu-id="db690-103">Pobiera podstawowe i pomocnicze ciągi połączeń dla danego obszaru nazw lub kolejki lub tematu albo aliasu (GeoDR konfiguracje).</span><span class="sxs-lookup"><span data-stu-id="db690-103">Gets the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db690-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="db690-104">SYNTAX</span></span>

### <span data-ttu-id="db690-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="db690-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db690-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="db690-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db690-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="db690-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db690-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="db690-108">AliasAuthoRuleSet</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db690-109">Opis</span><span class="sxs-lookup"><span data-stu-id="db690-109">DESCRIPTION</span></span>
<span data-ttu-id="db690-110">Polecenie cmdlet **Get-AzureRmServiceBusKey** zwraca podstawowe i pomocnicze ciągi połączeń dla danego obszaru nazw lub kolejki lub tematu albo aliasu (GeoDR konfiguracje).</span><span class="sxs-lookup"><span data-stu-id="db690-110">The **Get-AzureRmServiceBusKey** cmdlet returns the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="db690-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="db690-111">EXAMPLES</span></span>

### <span data-ttu-id="db690-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="db690-112">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="db690-113">Podstawowy i pomocniczy ciąg połączenia z określoną przestrzenią nazw.</span><span class="sxs-lookup"><span data-stu-id="db690-113">Primary and secondary connection string to the specified namespace.</span></span>

### <span data-ttu-id="db690-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="db690-114">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="db690-115">Podstawowy i pomocniczy ciąg połączenia z określoną kolejką.</span><span class="sxs-lookup"><span data-stu-id="db690-115">Primary and secondary connection string to the specified queue.</span></span>

### <span data-ttu-id="db690-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="db690-116">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="db690-117">Podstawowy i pomocniczy ciąg połączenia z określonym tematem.</span><span class="sxs-lookup"><span data-stu-id="db690-117">Primary and secondary connection string to the specified topic.</span></span>

### <span data-ttu-id="db690-118">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="db690-118">Example 4</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="db690-119">Podstawowy i pomocniczy ciąg połączenia z określoną przestrzenią nazw i aliasem.</span><span class="sxs-lookup"><span data-stu-id="db690-119">Primary and secondary connection string to the specified namespace and alias.</span></span>

## <span data-ttu-id="db690-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="db690-120">PARAMETERS</span></span>

### <span data-ttu-id="db690-121">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="db690-121">-AliasName</span></span>
<span data-ttu-id="db690-122">Nazwa aliasu</span><span class="sxs-lookup"><span data-stu-id="db690-122">Alias Name</span></span>

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

### <span data-ttu-id="db690-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db690-123">-DefaultProfile</span></span>
<span data-ttu-id="db690-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="db690-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db690-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="db690-125">-Name</span></span>
<span data-ttu-id="db690-126">Nazwa AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="db690-126">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="db690-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="db690-127">-Namespace</span></span>
<span data-ttu-id="db690-128">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="db690-128">Namespace Name</span></span>

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

### <span data-ttu-id="db690-129">-Queue</span><span class="sxs-lookup"><span data-stu-id="db690-129">-Queue</span></span>
<span data-ttu-id="db690-130">Nazwa kolejki</span><span class="sxs-lookup"><span data-stu-id="db690-130">Queue Name</span></span>

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

### <span data-ttu-id="db690-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db690-131">-ResourceGroupName</span></span>
<span data-ttu-id="db690-132">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="db690-132">Resource Group Name</span></span>

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

### <span data-ttu-id="db690-133">— Temat</span><span class="sxs-lookup"><span data-stu-id="db690-133">-Topic</span></span>
<span data-ttu-id="db690-134">Nazwa tematu</span><span class="sxs-lookup"><span data-stu-id="db690-134">Topic Name</span></span>

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

### <span data-ttu-id="db690-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db690-135">CommonParameters</span></span>
<span data-ttu-id="db690-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db690-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db690-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db690-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db690-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="db690-138">INPUTS</span></span>

### <span data-ttu-id="db690-139">System. String</span><span class="sxs-lookup"><span data-stu-id="db690-139">System.String</span></span>

## <span data-ttu-id="db690-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="db690-140">OUTPUTS</span></span>

### <span data-ttu-id="db690-141">Microsoft. Azure. Commands. ServiceBus. models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="db690-141">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="db690-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="db690-142">NOTES</span></span>

## <span data-ttu-id="db690-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="db690-143">RELATED LINKS</span></span>
