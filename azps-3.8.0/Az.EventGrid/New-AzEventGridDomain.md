---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomain.md
ms.openlocfilehash: 442a88c7fe64fd8913e86ba0ee6be013f226061e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895225"
---
# <span data-ttu-id="6592d-101">New-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="6592d-101">New-AzEventGridDomain</span></span>

## <span data-ttu-id="6592d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6592d-102">SYNOPSIS</span></span>
<span data-ttu-id="6592d-103">Tworzy nową domenę siatki zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6592d-103">Creates a new Azure Event Grid Domain.</span></span>

## <span data-ttu-id="6592d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6592d-104">SYNTAX</span></span>

```
New-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6592d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6592d-105">DESCRIPTION</span></span>
<span data-ttu-id="6592d-106">Tworzy nową domenę siatki zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6592d-106">Creates a new Azure Event Grid Domain.</span></span> <span data-ttu-id="6592d-107">Po utworzeniu domeny aplikacja może publikować zdarzenia w punkcie końcowym tematu.</span><span class="sxs-lookup"><span data-stu-id="6592d-107">Once the domain is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="6592d-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6592d-108">EXAMPLES</span></span>

### <span data-ttu-id="6592d-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6592d-109">Example 1</span></span>

<span data-ttu-id="6592d-110">Tworzy Domain1 domeny w siatce \` zdarzeń \` w podanej lokalizacji geograficznej \` westus2 \` , w MyResourceGroupName grup zasobów \` \` .</span><span class="sxs-lookup"><span data-stu-id="6592d-110">Creates an Event Grid domain \`Domain1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1 -Location westus2

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :
```

### <span data-ttu-id="6592d-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="6592d-111">Example 2</span></span>

<span data-ttu-id="6592d-112">Tworzy Domain1 domeny w siatce \` zdarzeń \` w określonej lokalizacji geograficznej \` westus2 \` , w MyResourceGroupName grup zasobów \` \` z określonymi znacznikami "Department" i "Environment".</span><span class="sxs-lookup"><span data-stu-id="6592d-112">Creates an Event Grid domain \`Domain1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

```powershell
PS C:\> New-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Department, Finance], [Environment, Test]}
```

## <span data-ttu-id="6592d-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6592d-113">PARAMETERS</span></span>

### <span data-ttu-id="6592d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6592d-114">-DefaultProfile</span></span>
<span data-ttu-id="6592d-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6592d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6592d-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="6592d-116">-Location</span></span>
<span data-ttu-id="6592d-117">Lokalizacja domeny.</span><span class="sxs-lookup"><span data-stu-id="6592d-117">The location of the domain.</span></span>

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

### <span data-ttu-id="6592d-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6592d-118">-Name</span></span>
<span data-ttu-id="6592d-119">EventGrid nazwa domeny.</span><span class="sxs-lookup"><span data-stu-id="6592d-119">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6592d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6592d-120">-ResourceGroupName</span></span>
<span data-ttu-id="6592d-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6592d-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="6592d-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="6592d-122">-Tag</span></span>
<span data-ttu-id="6592d-123">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="6592d-123">Hashtable which represents resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6592d-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6592d-124">-Confirm</span></span>
<span data-ttu-id="6592d-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6592d-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6592d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6592d-126">-WhatIf</span></span>
<span data-ttu-id="6592d-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6592d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6592d-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6592d-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6592d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6592d-129">CommonParameters</span></span>
<span data-ttu-id="6592d-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6592d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6592d-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6592d-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6592d-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6592d-132">INPUTS</span></span>

### <span data-ttu-id="6592d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="6592d-133">System.String</span></span>

### <span data-ttu-id="6592d-134">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6592d-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6592d-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6592d-135">OUTPUTS</span></span>

### <span data-ttu-id="6592d-136">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="6592d-136">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="6592d-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6592d-137">NOTES</span></span>

## <span data-ttu-id="6592d-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6592d-138">RELATED LINKS</span></span>
