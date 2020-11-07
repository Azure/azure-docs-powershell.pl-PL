---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
ms.openlocfilehash: 21bad7c36b39acbfbcc438603a57f504aaa1a106
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93896209"
---
# <span data-ttu-id="b6da2-101">New-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="b6da2-101">New-AzEventGridTopic</span></span>

## <span data-ttu-id="b6da2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b6da2-102">SYNOPSIS</span></span>
<span data-ttu-id="b6da2-103">Tworzy nowy temat siatki zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b6da2-103">Creates a new Azure Event Grid Topic.</span></span>

## <span data-ttu-id="b6da2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b6da2-104">SYNTAX</span></span>

```
New-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6da2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b6da2-105">DESCRIPTION</span></span>
<span data-ttu-id="b6da2-106">Tworzy nowy temat siatki zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b6da2-106">Creates a new Azure Event Grid Topic.</span></span> <span data-ttu-id="b6da2-107">Po utworzeniu tematu aplikacja może publikować zdarzenia w punkcie końcowym tematu.</span><span class="sxs-lookup"><span data-stu-id="b6da2-107">Once the topic is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="b6da2-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b6da2-108">EXAMPLES</span></span>

### <span data-ttu-id="b6da2-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b6da2-109">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2
```

<span data-ttu-id="b6da2-110">Tworzy temat \` Temat1 w siatce zdarzeń \` w podanej lokalizacji geograficznej \` westus2 \` , w MyResourceGroupName grup zasobów \` \` .</span><span class="sxs-lookup"><span data-stu-id="b6da2-110">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="b6da2-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b6da2-111">Example 2</span></span>
```powershell
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="b6da2-112">Tworzy temat \` Temat1 w siatce zdarzeń \` w określonej lokalizacji geograficznej \` westus2 \` , w MyResourceGroupName grup zasobów \` \` z określonymi znacznikami "Department" i "Environment".</span><span class="sxs-lookup"><span data-stu-id="b6da2-112">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="b6da2-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b6da2-113">PARAMETERS</span></span>

### <span data-ttu-id="b6da2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6da2-114">-DefaultProfile</span></span>
<span data-ttu-id="b6da2-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b6da2-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6da2-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b6da2-116">-Location</span></span>
<span data-ttu-id="b6da2-117">Lokalizacja tematu</span><span class="sxs-lookup"><span data-stu-id="b6da2-117">The location of the topic</span></span>

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

### <span data-ttu-id="b6da2-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b6da2-118">-Name</span></span>
<span data-ttu-id="b6da2-119">Nazwa tematu.</span><span class="sxs-lookup"><span data-stu-id="b6da2-119">The name of the topic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6da2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6da2-120">-ResourceGroupName</span></span>
<span data-ttu-id="b6da2-121">Grupa zasobów, w której ma zostać utworzony temat.</span><span class="sxs-lookup"><span data-stu-id="b6da2-121">The resource group in which the topic should be created.</span></span>

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

### <span data-ttu-id="b6da2-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="b6da2-122">-Tag</span></span>
<span data-ttu-id="b6da2-123">Hashtable, które reprezentują znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="b6da2-123">Hashtables which represents resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6da2-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b6da2-124">-Confirm</span></span>
<span data-ttu-id="b6da2-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6da2-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6da2-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6da2-126">-WhatIf</span></span>
<span data-ttu-id="b6da2-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6da2-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6da2-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b6da2-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6da2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6da2-129">CommonParameters</span></span>
<span data-ttu-id="b6da2-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6da2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6da2-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6da2-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6da2-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6da2-132">INPUTS</span></span>

### <span data-ttu-id="b6da2-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b6da2-133">System.String</span></span>

### <span data-ttu-id="b6da2-134">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b6da2-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b6da2-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b6da2-135">OUTPUTS</span></span>

### <span data-ttu-id="b6da2-136">Microsoft. Azure. Commands. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="b6da2-136">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="b6da2-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b6da2-137">NOTES</span></span>

## <span data-ttu-id="b6da2-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b6da2-138">RELATED LINKS</span></span>
