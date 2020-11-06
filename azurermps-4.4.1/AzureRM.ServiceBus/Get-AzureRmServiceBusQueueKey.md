---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueueKey.md
ms.openlocfilehash: 4faca15a0c348ee1011789db5acd227c06ee1b85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550760"
---
# <span data-ttu-id="bf169-101">Get-AzureRmServiceBusQueueKey</span><span class="sxs-lookup"><span data-stu-id="bf169-101">Get-AzureRmServiceBusQueueKey</span></span>

## <span data-ttu-id="bf169-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bf169-102">SYNOPSIS</span></span>
<span data-ttu-id="bf169-103">Pobiera podstawowe i pomocnicze parametry połączenia dla danej kolejki usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="bf169-103">Gets the primary and secondary connection strings for the given Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf169-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bf169-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusQueueKey [-ResourceGroup] <String> -Namespace <String> -Queue <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf169-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bf169-105">DESCRIPTION</span></span>
<span data-ttu-id="bf169-106">Polecenie cmdlet **Get-AzureRmServiceBusQueueKey** zwraca podstawowe i pomocnicze parametry połączenia dla danej kolejki usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="bf169-106">The **Get-AzureRmServiceBusQueueKey** cmdlet returns the primary and secondary connection strings for the given Service Bus queue.</span></span> 

## <span data-ttu-id="bf169-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bf169-107">EXAMPLES</span></span>

### <span data-ttu-id="bf169-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bf169-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusQueueKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1
```

<span data-ttu-id="bf169-109">Zwraca podstawowe i pomocnicze parametry połączenia dla określonej kolejki usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="bf169-109">Returns the primary and secondary connection strings for the specified Service Bus queue.</span></span>

## <span data-ttu-id="bf169-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bf169-110">PARAMETERS</span></span>

### <span data-ttu-id="bf169-111">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="bf169-111">-ResourceGroup</span></span>
<span data-ttu-id="bf169-112">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bf169-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="bf169-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf169-113">-DefaultProfile</span></span>
<span data-ttu-id="bf169-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bf169-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf169-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bf169-115">-Name</span></span>
<span data-ttu-id="bf169-116">Nazwa AuthorizationRule kolejki ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="bf169-116">ServiceBus Queue AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="bf169-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="bf169-117">-Namespace</span></span>
<span data-ttu-id="bf169-118">Nazwa przestrzeni nazw ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="bf169-118">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="bf169-119">-Queue</span><span class="sxs-lookup"><span data-stu-id="bf169-119">-Queue</span></span>
<span data-ttu-id="bf169-120">Nazwa kolejki ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="bf169-120">ServiceBus Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf169-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf169-121">CommonParameters</span></span>
<span data-ttu-id="bf169-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf169-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf169-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf169-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf169-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bf169-124">INPUTS</span></span>

### <span data-ttu-id="bf169-125">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="bf169-125">-ResourceGroup</span></span>
 <span data-ttu-id="bf169-126">System. String</span><span class="sxs-lookup"><span data-stu-id="bf169-126">System.String</span></span>
 

### <span data-ttu-id="bf169-127">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="bf169-127">-NamespaceName</span></span>
 <span data-ttu-id="bf169-128">System. String</span><span class="sxs-lookup"><span data-stu-id="bf169-128">System.String</span></span>
 

### <span data-ttu-id="bf169-129">-QueueName</span><span class="sxs-lookup"><span data-stu-id="bf169-129">-QueueName</span></span>
 <span data-ttu-id="bf169-130">System. String</span><span class="sxs-lookup"><span data-stu-id="bf169-130">System.String</span></span>
 

### <span data-ttu-id="bf169-131">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="bf169-131">-AuthorizationRuleName</span></span>
 <span data-ttu-id="bf169-132">System. String</span><span class="sxs-lookup"><span data-stu-id="bf169-132">System.String</span></span>

## <span data-ttu-id="bf169-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bf169-133">OUTPUTS</span></span>

### <span data-ttu-id="bf169-134">Microsoft. Azure. Commands. ServiceBus. models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="bf169-134">Microsoft.Azure.Commands.ServiceBus.Models.ListKeysAttributes</span></span>
<span data-ttu-id="bf169-135">PrimaryConnectionString: punkt końcowy = SB://SB-example1.ServiceBus.Windows.NET/; SharedAccessKeyName = SBAuthoRule1; SharedAccessKey = {SharedAccessKey-Value}; EntityPath = SB-Queue_e xampl1 SecondaryConnectionString: Endpoint = SB://SB-example1.ServiceBus.Windows.NET/; SharedAccessKeyName = SBAuthoRule1; SharedAccessKey = {SharedAccessKey-Value}; EntityPath = SB-Queue_e xampl1 PrimaryKey: {wartość PrimaryKey} SecondaryKey: {SecondaryKey wartość} NazwaKlucza: SBAuthoRule1</span><span class="sxs-lookup"><span data-stu-id="bf169-135">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Queue_e xampl1 SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Queue_e xampl1 PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : SBAuthoRule1</span></span>

## <span data-ttu-id="bf169-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bf169-136">NOTES</span></span>

## <span data-ttu-id="bf169-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bf169-137">RELATED LINKS</span></span>

