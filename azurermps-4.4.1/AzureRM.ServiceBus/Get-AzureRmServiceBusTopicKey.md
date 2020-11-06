---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopicKey.md
ms.openlocfilehash: 24041c299f2f242126f265ad232db3e0c5d526b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552356"
---
# <span data-ttu-id="4de18-101">Get-AzureRmServiceBusTopicKey</span><span class="sxs-lookup"><span data-stu-id="4de18-101">Get-AzureRmServiceBusTopicKey</span></span>

## <span data-ttu-id="4de18-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4de18-102">SYNOPSIS</span></span>
<span data-ttu-id="4de18-103">Pobiera podstawowe i pomocnicze ciągi połączeń dla tematu Magistrala usług.</span><span class="sxs-lookup"><span data-stu-id="4de18-103">Gets the primary and secondary connection strings for the Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4de18-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4de18-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusTopicKey [-ResourceGroup] <String> -Namespace <String> -Topic <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4de18-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4de18-105">DESCRIPTION</span></span>
<span data-ttu-id="4de18-106">Polecenie cmdlet **Get-AzureRmServiceBusTopicKey** zwraca podstawowe i pomocnicze parametry połączenia dla danego tematu magistrali usług.</span><span class="sxs-lookup"><span data-stu-id="4de18-106">The **Get-AzureRmServiceBusTopicKey** cmdlet returns the primary and secondary connection strings for the given Service Bus topic.</span></span>

## <span data-ttu-id="4de18-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4de18-107">EXAMPLES</span></span>

### <span data-ttu-id="4de18-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4de18-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusTopicKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1
```

<span data-ttu-id="4de18-109">Zwraca podstawowe i pomocnicze parametry połączenia dla określonego tematu magistrali usług.</span><span class="sxs-lookup"><span data-stu-id="4de18-109">Returns the primary and secondary connection strings for the specified Service Bus topic.</span></span>

## <span data-ttu-id="4de18-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4de18-110">PARAMETERS</span></span>

### <span data-ttu-id="4de18-111">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="4de18-111">-ResourceGroup</span></span>
<span data-ttu-id="4de18-112">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4de18-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="4de18-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4de18-113">-DefaultProfile</span></span>
<span data-ttu-id="4de18-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4de18-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4de18-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4de18-115">-Name</span></span>
<span data-ttu-id="4de18-116">Temat AuthorizationRule nazwa.</span><span class="sxs-lookup"><span data-stu-id="4de18-116">Topic AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4de18-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4de18-117">-Namespace</span></span>
<span data-ttu-id="4de18-118">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="4de18-118">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4de18-119">— Temat</span><span class="sxs-lookup"><span data-stu-id="4de18-119">-Topic</span></span>
<span data-ttu-id="4de18-120">Nazwa tematu.</span><span class="sxs-lookup"><span data-stu-id="4de18-120">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4de18-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4de18-121">CommonParameters</span></span>
<span data-ttu-id="4de18-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4de18-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4de18-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4de18-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4de18-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4de18-124">INPUTS</span></span>

### <span data-ttu-id="4de18-125">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="4de18-125">-ResourceGroup</span></span>
 <span data-ttu-id="4de18-126">System. String</span><span class="sxs-lookup"><span data-stu-id="4de18-126">System.String</span></span>
 

### <span data-ttu-id="4de18-127">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="4de18-127">-NamespaceName</span></span>
 <span data-ttu-id="4de18-128">System. String</span><span class="sxs-lookup"><span data-stu-id="4de18-128">System.String</span></span>
 

### <span data-ttu-id="4de18-129">-Tematname</span><span class="sxs-lookup"><span data-stu-id="4de18-129">-TopicName</span></span>
 <span data-ttu-id="4de18-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4de18-130">System.String</span></span>
 

### <span data-ttu-id="4de18-131">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="4de18-131">-AuthorizationRuleName</span></span>
 <span data-ttu-id="4de18-132">System. String</span><span class="sxs-lookup"><span data-stu-id="4de18-132">System.String</span></span>

## <span data-ttu-id="4de18-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4de18-133">OUTPUTS</span></span>

### <span data-ttu-id="4de18-134">Microsoft. Azure. Commands. ServiceBus. models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="4de18-134">Microsoft.Azure.Commands.ServiceBus.Models.ListKeysAttributes</span></span>
<span data-ttu-id="4de18-135">PrimaryConnectionString: punkt końcowy = SB://SB-example1.ServiceBus.Windows.NET/; SharedAccessKeyName = SBTopicAuthoRule1; SharedAccessKey = {SharedAccessKey-Value}; EntityPath = SB-to pic_exampl1 SecondaryConnectionString: Endpoint = SB://SB-example1.ServiceBus.Windows.NET/; SharedAccessKeyName = SBTopicAuthoRule1; SharedAccessKey = {SharedAccessKey-Value}; EntityPath = SB-to pic_exampl1 PrimaryKey: {wartość PrimaryKey} SecondaryKey: {SecondaryKey Value} NazwaKlucza: SBTopicAuthoRule1</span><span class="sxs-lookup"><span data-stu-id="4de18-135">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBTopicAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-To pic_exampl1 SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBTopicAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-To pic_exampl1 PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : SBTopicAuthoRule1</span></span>

## <span data-ttu-id="4de18-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4de18-136">NOTES</span></span>

## <span data-ttu-id="4de18-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4de18-137">RELATED LINKS</span></span>

