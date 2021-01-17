---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainTopic.md
ms.openlocfilehash: 2923f05bc954c0570c49886c3a036ef78848a1e7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329518"
---
# <span data-ttu-id="77b7f-101">New-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="77b7f-101">New-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="77b7f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="77b7f-102">SYNOPSIS</span></span>
<span data-ttu-id="77b7f-103">Tworzy nową domenę siatki zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="77b7f-103">Creates a new Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="77b7f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="77b7f-104">SYNTAX</span></span>

```
New-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77b7f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="77b7f-105">DESCRIPTION</span></span>
<span data-ttu-id="77b7f-106">Tworzy nową domenę siatki zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="77b7f-106">Creates a new Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="77b7f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="77b7f-107">EXAMPLES</span></span>

### <span data-ttu-id="77b7f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="77b7f-108">Example 1</span></span>

<span data-ttu-id="77b7f-109">Tworzy temat domeny w siatce zdarzeń \` Temat1 \` w Domain1 domeny w \` \` obszarze MyResourceGroupName grupy zasobów \` \` .</span><span class="sxs-lookup"><span data-stu-id="77b7f-109">Creates an Event Grid Domain Topic \`Topic1\` in Domain \`Domain1\` under resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomainTopic -ResourceGroupName MyResourceGroupName -DomainName Domain1 -Name Topic1

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : topic1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/topic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

## <span data-ttu-id="77b7f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="77b7f-110">PARAMETERS</span></span>

### <span data-ttu-id="77b7f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77b7f-111">-DefaultProfile</span></span>
<span data-ttu-id="77b7f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="77b7f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77b7f-113">-NazwaDomeny</span><span class="sxs-lookup"><span data-stu-id="77b7f-113">-DomainName</span></span>
<span data-ttu-id="77b7f-114">EventGrid nazwa domeny.</span><span class="sxs-lookup"><span data-stu-id="77b7f-114">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Domain

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77b7f-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="77b7f-115">-Name</span></span>
<span data-ttu-id="77b7f-116">Nazwa tematu domeny EventGrid.</span><span class="sxs-lookup"><span data-stu-id="77b7f-116">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DomainTopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77b7f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77b7f-117">-ResourceGroupName</span></span>
<span data-ttu-id="77b7f-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="77b7f-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="77b7f-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="77b7f-119">-Confirm</span></span>
<span data-ttu-id="77b7f-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77b7f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77b7f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77b7f-121">-WhatIf</span></span>
<span data-ttu-id="77b7f-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77b7f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77b7f-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="77b7f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77b7f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77b7f-124">CommonParameters</span></span>
<span data-ttu-id="77b7f-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77b7f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77b7f-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77b7f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77b7f-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="77b7f-127">INPUTS</span></span>

### <span data-ttu-id="77b7f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="77b7f-128">System.String</span></span>

## <span data-ttu-id="77b7f-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="77b7f-129">OUTPUTS</span></span>

### <span data-ttu-id="77b7f-130">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="77b7f-130">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="77b7f-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="77b7f-131">NOTES</span></span>

## <span data-ttu-id="77b7f-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="77b7f-132">RELATED LINKS</span></span>
