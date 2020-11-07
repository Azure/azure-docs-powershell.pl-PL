---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomain.md
ms.openlocfilehash: 2b69fed3c63edb503b2087cfb7b8ab142eb04473
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705493"
---
# <span data-ttu-id="c1873-101">New-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="c1873-101">New-AzEventGridDomain</span></span>

## <span data-ttu-id="c1873-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c1873-102">SYNOPSIS</span></span>
<span data-ttu-id="c1873-103">Tworzy nową domenę siatki zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c1873-103">Creates a new Azure Event Grid Domain.</span></span>

## <span data-ttu-id="c1873-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c1873-104">SYNTAX</span></span>

```
New-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1873-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c1873-105">DESCRIPTION</span></span>
<span data-ttu-id="c1873-106">Tworzy nową domenę siatki zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c1873-106">Creates a new Azure Event Grid Domain.</span></span> <span data-ttu-id="c1873-107">Po utworzeniu domeny aplikacja może publikować zdarzenia w punkcie końcowym tematu.</span><span class="sxs-lookup"><span data-stu-id="c1873-107">Once the domain is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="c1873-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c1873-108">EXAMPLES</span></span>

### <span data-ttu-id="c1873-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c1873-109">Example 1</span></span>

<span data-ttu-id="c1873-110">Tworzy Domain1 domeny w siatce \` zdarzeń \` w podanej lokalizacji geograficznej \` westus2 \` , w MyResourceGroupName grup zasobów \` \` .</span><span class="sxs-lookup"><span data-stu-id="c1873-110">Creates an Event Grid domain \`Domain1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

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

### <span data-ttu-id="c1873-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c1873-111">Example 2</span></span>

<span data-ttu-id="c1873-112">Tworzy Domain1 domeny w siatce \` zdarzeń \` w określonej lokalizacji geograficznej \` westus2 \` , w MyResourceGroupName grup zasobów \` \` z określonymi znacznikami "Department" i "Environment".</span><span class="sxs-lookup"><span data-stu-id="c1873-112">Creates an Event Grid domain \`Domain1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

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

## <span data-ttu-id="c1873-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c1873-113">PARAMETERS</span></span>

### <span data-ttu-id="c1873-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1873-114">-DefaultProfile</span></span>
<span data-ttu-id="c1873-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c1873-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1873-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="c1873-116">-Location</span></span>
<span data-ttu-id="c1873-117">Lokalizacja domeny.</span><span class="sxs-lookup"><span data-stu-id="c1873-117">The location of the domain.</span></span>

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

### <span data-ttu-id="c1873-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c1873-118">-Name</span></span>
<span data-ttu-id="c1873-119">EventGrid nazwa domeny.</span><span class="sxs-lookup"><span data-stu-id="c1873-119">EventGrid domain name.</span></span>

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

### <span data-ttu-id="c1873-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1873-120">-ResourceGroupName</span></span>
<span data-ttu-id="c1873-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c1873-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="c1873-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="c1873-122">-Tag</span></span>
<span data-ttu-id="c1873-123">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="c1873-123">Hashtable which represents resource Tags.</span></span>

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

### <span data-ttu-id="c1873-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c1873-124">-Confirm</span></span>
<span data-ttu-id="c1873-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1873-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1873-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1873-126">-WhatIf</span></span>
<span data-ttu-id="c1873-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1873-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1873-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c1873-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1873-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1873-129">CommonParameters</span></span>
<span data-ttu-id="c1873-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1873-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1873-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1873-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1873-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c1873-132">INPUTS</span></span>

### <span data-ttu-id="c1873-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c1873-133">System.String</span></span>

### <span data-ttu-id="c1873-134">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c1873-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c1873-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c1873-135">OUTPUTS</span></span>

### <span data-ttu-id="c1873-136">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="c1873-136">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="c1873-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c1873-137">NOTES</span></span>

## <span data-ttu-id="c1873-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c1873-138">RELATED LINKS</span></span>
