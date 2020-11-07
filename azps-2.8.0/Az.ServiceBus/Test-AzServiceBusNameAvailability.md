---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/test-azservicebusnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
ms.openlocfilehash: 396a328de8c075b49ae4dda181158c33518eaa8a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871555"
---
# <span data-ttu-id="ffceb-101">Test-AzServiceBusNameAvailability</span><span class="sxs-lookup"><span data-stu-id="ffceb-101">Test-AzServiceBusNameAvailability</span></span>

## <span data-ttu-id="ffceb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ffceb-102">SYNOPSIS</span></span>
<span data-ttu-id="ffceb-103">Sprawdza dostępność danej kolejki lub nazwy tematu</span><span class="sxs-lookup"><span data-stu-id="ffceb-103">Checks the Availability of the given Queue or Topic name</span></span>

## <span data-ttu-id="ffceb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ffceb-104">SYNTAX</span></span>

### <span data-ttu-id="ffceb-105">QueueCheckNameAvailabilitySet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ffceb-105">QueueCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Queue]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ffceb-106">TopicCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ffceb-106">TopicCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Topic]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ffceb-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ffceb-107">DESCRIPTION</span></span>
<span data-ttu-id="ffceb-108">Polecenie cmdlet **test-AzServiceBusNameAvailability** sprawdza dostępność podanej nazwy kolejki lub tematu.</span><span class="sxs-lookup"><span data-stu-id="ffceb-108">The **Test-AzServiceBusNameAvailability** Cmdlet Check Availability of the provided Name of Queue or Topic</span></span>

## <span data-ttu-id="ffceb-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ffceb-109">EXAMPLES</span></span>

### <span data-ttu-id="ffceb-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ffceb-110">Example 1</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameQueue -Queue
True
```

<span data-ttu-id="ffceb-111">Zwraca wartość PRAWDA, jeśli podana nazwa $nameQueue jest Availabile lub zwraca wartość FAŁSZ, jeśli podana nazwa $nameQueue jest niedostępna.</span><span class="sxs-lookup"><span data-stu-id="ffceb-111">Returns True if the Provided $nameQueue name is Availabile or returns False if Provided $nameQueue name in not available</span></span>

### <span data-ttu-id="ffceb-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ffceb-112">Example 2</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameTopic -Topic
True
```

<span data-ttu-id="ffceb-113">Zwraca wartość PRAWDA, jeśli podana nazwa $nameTopic jest Availabile lub zwraca wartość FAŁSZ, jeśli podana nazwa $nameTopic jest niedostępna.</span><span class="sxs-lookup"><span data-stu-id="ffceb-113">Returns True if the Provided $nameTopic name is Availabile or returns False if Provided $nameTopic name in not available</span></span>

## <span data-ttu-id="ffceb-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ffceb-114">PARAMETERS</span></span>

### <span data-ttu-id="ffceb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffceb-115">-DefaultProfile</span></span>
<span data-ttu-id="ffceb-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ffceb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffceb-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ffceb-117">-Name</span></span>
<span data-ttu-id="ffceb-118">Nazwa kolejki w celu sprawdzenia dostępności nazw</span><span class="sxs-lookup"><span data-stu-id="ffceb-118">Queue Name to check the Name Availability</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffceb-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ffceb-119">-Namespace</span></span>
<span data-ttu-id="ffceb-120">Nazwa przestrzeni nazw ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ffceb-120">Servicebus Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffceb-121">-Queue</span><span class="sxs-lookup"><span data-stu-id="ffceb-121">-Queue</span></span>
<span data-ttu-id="ffceb-122">Aby sprawdzić dostępność nazw dla kolejki</span><span class="sxs-lookup"><span data-stu-id="ffceb-122">To Check Name Availability for Queue Name</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: QueueCheckNameAvailabilitySet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffceb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffceb-123">-ResourceGroupName</span></span>
<span data-ttu-id="ffceb-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="ffceb-124">Resource Group Name</span></span>

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

### <span data-ttu-id="ffceb-125">— Temat</span><span class="sxs-lookup"><span data-stu-id="ffceb-125">-Topic</span></span>
<span data-ttu-id="ffceb-126">Aby sprawdzić dostępność nazw dla nazwy tematu</span><span class="sxs-lookup"><span data-stu-id="ffceb-126">To Check Name Availability for Topic Name</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: TopicCheckNameAvailabilitySet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffceb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffceb-127">CommonParameters</span></span>
<span data-ttu-id="ffceb-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffceb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ffceb-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffceb-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffceb-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ffceb-130">INPUTS</span></span>

### <span data-ttu-id="ffceb-131">System. String</span><span class="sxs-lookup"><span data-stu-id="ffceb-131">System.String</span></span>

## <span data-ttu-id="ffceb-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ffceb-132">OUTPUTS</span></span>

### <span data-ttu-id="ffceb-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ffceb-133">System.Boolean</span></span>

## <span data-ttu-id="ffceb-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ffceb-134">NOTES</span></span>

## <span data-ttu-id="ffceb-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ffceb-135">RELATED LINKS</span></span>
