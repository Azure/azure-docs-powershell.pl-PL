---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopic.md
ms.openlocfilehash: fdd15de19f921781e89d7e24b57e1d82632e4735
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553920"
---
# <span data-ttu-id="9209e-101">New-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="9209e-101">New-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="9209e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9209e-102">SYNOPSIS</span></span>
<span data-ttu-id="9209e-103">Tworzy nowy temat siatki zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9209e-103">Creates a new Azure Event Grid Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9209e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9209e-104">SYNTAX</span></span>

```
New-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9209e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9209e-105">DESCRIPTION</span></span>
<span data-ttu-id="9209e-106">Tworzy nowy temat siatki zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9209e-106">Creates a new Azure Event Grid Topic.</span></span> <span data-ttu-id="9209e-107">Po utworzeniu tematu aplikacja może publikować zdarzenia w punkcie końcowym tematu.</span><span class="sxs-lookup"><span data-stu-id="9209e-107">Once the topic is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="9209e-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9209e-108">EXAMPLES</span></span>

### <span data-ttu-id="9209e-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9209e-109">Example 1</span></span>
```
PS C:\> New-AzureRmEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2
```

<span data-ttu-id="9209e-110">Tworzy temat \` Temat1 w siatce zdarzeń \` w podanej lokalizacji geograficznej \` westus2 \` , w MyResourceGroupName grup zasobów \` \` .</span><span class="sxs-lookup"><span data-stu-id="9209e-110">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="9209e-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="9209e-111">Example 2</span></span>
```
PS C:\> New-AzureRmEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="9209e-112">Tworzy temat \` Temat1 w siatce zdarzeń \` w określonej lokalizacji geograficznej \` westus2 \` , w MyResourceGroupName grup zasobów \` \` z określonymi znacznikami "Department" i "Environment".</span><span class="sxs-lookup"><span data-stu-id="9209e-112">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="9209e-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9209e-113">PARAMETERS</span></span>

### <span data-ttu-id="9209e-114">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="9209e-114">-Location</span></span>
<span data-ttu-id="9209e-115">Lokalizacja tematu</span><span class="sxs-lookup"><span data-stu-id="9209e-115">The location of the topic</span></span>

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

### <span data-ttu-id="9209e-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9209e-116">-Name</span></span>
<span data-ttu-id="9209e-117">Nazwa tematu.</span><span class="sxs-lookup"><span data-stu-id="9209e-117">The name of the topic.</span></span>

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

### <span data-ttu-id="9209e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9209e-118">-ResourceGroupName</span></span>
<span data-ttu-id="9209e-119">Grupa zasobów, w której ma zostać utworzony temat.</span><span class="sxs-lookup"><span data-stu-id="9209e-119">The resource group in which the topic should be created.</span></span>

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

### <span data-ttu-id="9209e-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="9209e-120">-Tag</span></span>
<span data-ttu-id="9209e-121">Hashtable, które reprezentują znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="9209e-121">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="9209e-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9209e-122">-Confirm</span></span>
<span data-ttu-id="9209e-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9209e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9209e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9209e-124">-WhatIf</span></span>
<span data-ttu-id="9209e-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9209e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9209e-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9209e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9209e-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9209e-127">-DefaultProfile</span></span>
<span data-ttu-id="9209e-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9209e-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9209e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9209e-129">CommonParameters</span></span>
<span data-ttu-id="9209e-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9209e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9209e-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9209e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9209e-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9209e-132">INPUTS</span></span>

### <span data-ttu-id="9209e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="9209e-133">System.String</span></span>
<span data-ttu-id="9209e-134">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9209e-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9209e-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9209e-135">OUTPUTS</span></span>

### <span data-ttu-id="9209e-136">Microsoft. Azure. Commands. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="9209e-136">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="9209e-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9209e-137">NOTES</span></span>

## <span data-ttu-id="9209e-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9209e-138">RELATED LINKS</span></span>

