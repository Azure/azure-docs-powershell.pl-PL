---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/test-azservicebusnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
ms.openlocfilehash: adaf7485b0af16821a1f4adec7919422bef07f90
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219825"
---
# <span data-ttu-id="d1c02-101">Test-AzServiceBusNameAvailability</span><span class="sxs-lookup"><span data-stu-id="d1c02-101">Test-AzServiceBusNameAvailability</span></span>

## <span data-ttu-id="d1c02-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d1c02-102">SYNOPSIS</span></span>
<span data-ttu-id="d1c02-103">Sprawdza dostępność danej kolejki lub nazwy tematu</span><span class="sxs-lookup"><span data-stu-id="d1c02-103">Checks the Availability of the given Queue or Topic name</span></span>

## <span data-ttu-id="d1c02-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d1c02-104">SYNTAX</span></span>

### <span data-ttu-id="d1c02-105">QueueCheckNameAvailabilitySet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d1c02-105">QueueCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Queue]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1c02-106">TopicCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d1c02-106">TopicCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Topic]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1c02-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d1c02-107">DESCRIPTION</span></span>
<span data-ttu-id="d1c02-108">Polecenie cmdlet **test-AzServiceBusNameAvailability** sprawdza dostępność podanej nazwy kolejki lub tematu.</span><span class="sxs-lookup"><span data-stu-id="d1c02-108">The **Test-AzServiceBusNameAvailability** Cmdlet Check Availability of the provided Name of Queue or Topic</span></span>

## <span data-ttu-id="d1c02-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d1c02-109">EXAMPLES</span></span>

### <span data-ttu-id="d1c02-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d1c02-110">Example 1</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameQueue -Queue
True
```

<span data-ttu-id="d1c02-111">Zwraca wartość PRAWDA, jeśli podana nazwa $nameQueue jest Availabile lub zwraca wartość FAŁSZ, jeśli podana nazwa $nameQueue jest niedostępna.</span><span class="sxs-lookup"><span data-stu-id="d1c02-111">Returns True if the Provided $nameQueue name is Availabile or returns False if Provided $nameQueue name in not available</span></span>

### <span data-ttu-id="d1c02-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d1c02-112">Example 2</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameTopic -Topic
True
```

<span data-ttu-id="d1c02-113">Zwraca wartość PRAWDA, jeśli podana nazwa $nameTopic jest Availabile lub zwraca wartość FAŁSZ, jeśli podana nazwa $nameTopic jest niedostępna.</span><span class="sxs-lookup"><span data-stu-id="d1c02-113">Returns True if the Provided $nameTopic name is Availabile or returns False if Provided $nameTopic name in not available</span></span>

## <span data-ttu-id="d1c02-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d1c02-114">PARAMETERS</span></span>

### <span data-ttu-id="d1c02-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1c02-115">-DefaultProfile</span></span>
<span data-ttu-id="d1c02-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d1c02-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1c02-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d1c02-117">-Name</span></span>
<span data-ttu-id="d1c02-118">Nazwa kolejki w celu sprawdzenia dostępności nazw</span><span class="sxs-lookup"><span data-stu-id="d1c02-118">Queue Name to check the Name Availability</span></span>

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

### <span data-ttu-id="d1c02-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d1c02-119">-Namespace</span></span>
<span data-ttu-id="d1c02-120">Nazwa przestrzeni nazw ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d1c02-120">Servicebus Namespace Name</span></span>

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

### <span data-ttu-id="d1c02-121">-Queue</span><span class="sxs-lookup"><span data-stu-id="d1c02-121">-Queue</span></span>
<span data-ttu-id="d1c02-122">Aby sprawdzić dostępność nazw dla kolejki</span><span class="sxs-lookup"><span data-stu-id="d1c02-122">To Check Name Availability for Queue Name</span></span>

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

### <span data-ttu-id="d1c02-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1c02-123">-ResourceGroupName</span></span>
<span data-ttu-id="d1c02-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="d1c02-124">Resource Group Name</span></span>

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

### <span data-ttu-id="d1c02-125">— Temat</span><span class="sxs-lookup"><span data-stu-id="d1c02-125">-Topic</span></span>
<span data-ttu-id="d1c02-126">Aby sprawdzić dostępność nazw dla nazwy tematu</span><span class="sxs-lookup"><span data-stu-id="d1c02-126">To Check Name Availability for Topic Name</span></span>

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

### <span data-ttu-id="d1c02-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1c02-127">CommonParameters</span></span>
<span data-ttu-id="d1c02-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1c02-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d1c02-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1c02-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1c02-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d1c02-130">INPUTS</span></span>

### <span data-ttu-id="d1c02-131">System. String</span><span class="sxs-lookup"><span data-stu-id="d1c02-131">System.String</span></span>

## <span data-ttu-id="d1c02-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d1c02-132">OUTPUTS</span></span>

### <span data-ttu-id="d1c02-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d1c02-133">System.Boolean</span></span>

## <span data-ttu-id="d1c02-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d1c02-134">NOTES</span></span>

## <span data-ttu-id="d1c02-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d1c02-135">RELATED LINKS</span></span>
