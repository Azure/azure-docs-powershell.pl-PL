---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/test-azservicebusnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
ms.openlocfilehash: adaf7485b0af16821a1f4adec7919422bef07f90
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198667"
---
# <span data-ttu-id="33e46-101">Test-AzServiceBusNameAvailability</span><span class="sxs-lookup"><span data-stu-id="33e46-101">Test-AzServiceBusNameAvailability</span></span>

## <span data-ttu-id="33e46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33e46-102">SYNOPSIS</span></span>
<span data-ttu-id="33e46-103">Sprawdza dostępność danej kolejki lub nazwy tematu.</span><span class="sxs-lookup"><span data-stu-id="33e46-103">Checks the Availability of the given Queue or Topic name</span></span>

## <span data-ttu-id="33e46-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="33e46-104">SYNTAX</span></span>

### <span data-ttu-id="33e46-105">QueueCheckNameAvailabilitySet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="33e46-105">QueueCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Queue]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33e46-106">TopicCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="33e46-106">TopicCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Topic]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33e46-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="33e46-107">DESCRIPTION</span></span>
<span data-ttu-id="33e46-108">Polecenie **cmdlet Test-AzServiceBusNameAvailability** sprawdza dostępność podanej nazwy kolejki lub tematu</span><span class="sxs-lookup"><span data-stu-id="33e46-108">The **Test-AzServiceBusNameAvailability** Cmdlet Check Availability of the provided Name of Queue or Topic</span></span>

## <span data-ttu-id="33e46-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="33e46-109">EXAMPLES</span></span>

### <span data-ttu-id="33e46-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="33e46-110">Example 1</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameQueue -Queue
True
```

<span data-ttu-id="33e46-111">Zwraca wartość Prawda, jeśli $nameQueue nazwa adresowa dostępności lub zwraca wartość Fałsz, $nameQueue nazwa w stanie niedostępnym.</span><span class="sxs-lookup"><span data-stu-id="33e46-111">Returns True if the Provided $nameQueue name is Availabile or returns False if Provided $nameQueue name in not available</span></span>

### <span data-ttu-id="33e46-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="33e46-112">Example 2</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameTopic -Topic
True
```

<span data-ttu-id="33e46-113">Zwraca wartość Prawda, jeśli $nameTopic nazwa adresowa dostępności lub zwraca wartość Fałsz, $nameTopic nazwa nie jest dostępna.</span><span class="sxs-lookup"><span data-stu-id="33e46-113">Returns True if the Provided $nameTopic name is Availabile or returns False if Provided $nameTopic name in not available</span></span>

## <span data-ttu-id="33e46-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="33e46-114">PARAMETERS</span></span>

### <span data-ttu-id="33e46-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33e46-115">-DefaultProfile</span></span>
<span data-ttu-id="33e46-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="33e46-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33e46-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="33e46-117">-Name</span></span>
<span data-ttu-id="33e46-118">Nazwa kolejki w celu sprawdzenia dostępności nazwy</span><span class="sxs-lookup"><span data-stu-id="33e46-118">Queue Name to check the Name Availability</span></span>

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

### <span data-ttu-id="33e46-119">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="33e46-119">-Namespace</span></span>
<span data-ttu-id="33e46-120">Nazwa przestrzeni nazw usługi Servicebus</span><span class="sxs-lookup"><span data-stu-id="33e46-120">Servicebus Namespace Name</span></span>

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

### <span data-ttu-id="33e46-121">— Kolejka</span><span class="sxs-lookup"><span data-stu-id="33e46-121">-Queue</span></span>
<span data-ttu-id="33e46-122">Aby sprawdzić dostępność nazwy dla nazwy kolejki</span><span class="sxs-lookup"><span data-stu-id="33e46-122">To Check Name Availability for Queue Name</span></span>

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

### <span data-ttu-id="33e46-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33e46-123">-ResourceGroupName</span></span>
<span data-ttu-id="33e46-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="33e46-124">Resource Group Name</span></span>

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

### <span data-ttu-id="33e46-125">— Temat</span><span class="sxs-lookup"><span data-stu-id="33e46-125">-Topic</span></span>
<span data-ttu-id="33e46-126">Aby sprawdzić dostępność nazwy tematu</span><span class="sxs-lookup"><span data-stu-id="33e46-126">To Check Name Availability for Topic Name</span></span>

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

### <span data-ttu-id="33e46-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33e46-127">CommonParameters</span></span>
<span data-ttu-id="33e46-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33e46-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="33e46-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33e46-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33e46-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="33e46-130">INPUTS</span></span>

### <span data-ttu-id="33e46-131">System.String</span><span class="sxs-lookup"><span data-stu-id="33e46-131">System.String</span></span>

## <span data-ttu-id="33e46-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="33e46-132">OUTPUTS</span></span>

### <span data-ttu-id="33e46-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="33e46-133">System.Boolean</span></span>

## <span data-ttu-id="33e46-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="33e46-134">NOTES</span></span>

## <span data-ttu-id="33e46-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="33e46-135">RELATED LINKS</span></span>
