---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/new-azurermeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopic.md
ms.openlocfilehash: a20262e1414b8f747e638f22283aed26b5483896
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546635"
---
# <span data-ttu-id="2e72e-101">New-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="2e72e-101">New-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="2e72e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2e72e-102">SYNOPSIS</span></span>
<span data-ttu-id="2e72e-103">Tworzy nowy temat siatki zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2e72e-103">Creates a new Azure Event Grid Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e72e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2e72e-104">SYNTAX</span></span>

```
New-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e72e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2e72e-105">DESCRIPTION</span></span>
<span data-ttu-id="2e72e-106">Tworzy nowy temat siatki zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2e72e-106">Creates a new Azure Event Grid Topic.</span></span> <span data-ttu-id="2e72e-107">Po utworzeniu tematu aplikacja może publikować zdarzenia w punkcie końcowym tematu.</span><span class="sxs-lookup"><span data-stu-id="2e72e-107">Once the topic is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="2e72e-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2e72e-108">EXAMPLES</span></span>

### <span data-ttu-id="2e72e-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2e72e-109">Example 1</span></span>
```
PS C:\> New-AzureRmEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2
```

<span data-ttu-id="2e72e-110">Tworzy temat \` Temat1 w siatce zdarzeń \` w podanej lokalizacji geograficznej \` westus2 \` , w MyResourceGroupName grup zasobów \` \` .</span><span class="sxs-lookup"><span data-stu-id="2e72e-110">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="2e72e-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="2e72e-111">Example 2</span></span>
```
PS C:\> New-AzureRmEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="2e72e-112">Tworzy temat \` Temat1 w siatce zdarzeń \` w określonej lokalizacji geograficznej \` westus2 \` , w MyResourceGroupName grup zasobów \` \` z określonymi znacznikami "Department" i "Environment".</span><span class="sxs-lookup"><span data-stu-id="2e72e-112">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="2e72e-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2e72e-113">PARAMETERS</span></span>

### <span data-ttu-id="2e72e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e72e-114">-DefaultProfile</span></span>
<span data-ttu-id="2e72e-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="2e72e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2e72e-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="2e72e-116">-Location</span></span>
<span data-ttu-id="2e72e-117">Lokalizacja tematu</span><span class="sxs-lookup"><span data-stu-id="2e72e-117">The location of the topic</span></span>

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

### <span data-ttu-id="2e72e-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2e72e-118">-Name</span></span>
<span data-ttu-id="2e72e-119">Nazwa tematu.</span><span class="sxs-lookup"><span data-stu-id="2e72e-119">The name of the topic.</span></span>

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

### <span data-ttu-id="2e72e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e72e-120">-ResourceGroupName</span></span>
<span data-ttu-id="2e72e-121">Grupa zasobów, w której ma zostać utworzony temat.</span><span class="sxs-lookup"><span data-stu-id="2e72e-121">The resource group in which the topic should be created.</span></span>

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

### <span data-ttu-id="2e72e-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="2e72e-122">-Tag</span></span>
<span data-ttu-id="2e72e-123">Hashtable, które reprezentują znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="2e72e-123">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="2e72e-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2e72e-124">-Confirm</span></span>
<span data-ttu-id="2e72e-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e72e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e72e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e72e-126">-WhatIf</span></span>
<span data-ttu-id="2e72e-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e72e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e72e-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2e72e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e72e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e72e-129">CommonParameters</span></span>
<span data-ttu-id="2e72e-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e72e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e72e-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e72e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e72e-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2e72e-132">INPUTS</span></span>

### <span data-ttu-id="2e72e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="2e72e-133">System.String</span></span>

### <span data-ttu-id="2e72e-134">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2e72e-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2e72e-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2e72e-135">OUTPUTS</span></span>

### <span data-ttu-id="2e72e-136">Microsoft. Azure. Commands. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="2e72e-136">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="2e72e-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2e72e-137">NOTES</span></span>

## <span data-ttu-id="2e72e-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2e72e-138">RELATED LINKS</span></span>
