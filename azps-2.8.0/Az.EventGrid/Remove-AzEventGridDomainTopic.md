---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomainTopic.md
ms.openlocfilehash: 04bed413aca213a558ab1e0afaf5e6badcf238c2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705480"
---
# <span data-ttu-id="1ec09-101">Remove-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="1ec09-101">Remove-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="1ec09-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1ec09-102">SYNOPSIS</span></span>
<span data-ttu-id="1ec09-103">Usuwa temat domeny z siatką zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1ec09-103">Removes an Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="1ec09-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1ec09-104">SYNTAX</span></span>

### <span data-ttu-id="1ec09-105">DomainTopicNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1ec09-105">DomainTopicNameParameterSet (Default)</span></span>
```
Remove-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ec09-106">ResourceIdDomainTopicParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ec09-106">ResourceIdDomainTopicParameterSet</span></span>
```
Remove-AzEventGridDomainTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ec09-107">DomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ec09-107">DomainTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridDomainTopic [-InputObject] <PSDomainTopic> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ec09-108">Opis</span><span class="sxs-lookup"><span data-stu-id="1ec09-108">DESCRIPTION</span></span>
<span data-ttu-id="1ec09-109">Usuwa temat domeny z siatką zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1ec09-109">Removes an Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="1ec09-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1ec09-110">EXAMPLES</span></span>

### <span data-ttu-id="1ec09-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1ec09-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridDomainTopic -ResourceGroupName MyResourceGroupName -DomainName Domain1 -Name Topic1
```

<span data-ttu-id="1ec09-112">Usuwa temat domeny w siatce zdarzeń \` Temat1 w \` obszarze Domain \` Domain1 ( \` zasób Group \` MyResourceGroupName) \` .</span><span class="sxs-lookup"><span data-stu-id="1ec09-112">Removes the Event Grid Domain Topic \`Topic1\` under Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="1ec09-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="1ec09-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/Topic1" | Remove-AzEventGridDomainTopic
```

<span data-ttu-id="1ec09-114">Usuwa temat domeny w siatce zdarzeń \` Temat1 w \` obszarze Domain \` Domain1 ( \` zasób Group \` MyResourceGroupName) \` .</span><span class="sxs-lookup"><span data-stu-id="1ec09-114">Removes the Event Grid Domain Topic \`Topic1\` under Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="1ec09-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1ec09-115">PARAMETERS</span></span>

### <span data-ttu-id="1ec09-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ec09-116">-DefaultProfile</span></span>
<span data-ttu-id="1ec09-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1ec09-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ec09-118">-NazwaDomeny</span><span class="sxs-lookup"><span data-stu-id="1ec09-118">-DomainName</span></span>
<span data-ttu-id="1ec09-119">EventGrid nazwa domeny.</span><span class="sxs-lookup"><span data-stu-id="1ec09-119">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ec09-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1ec09-120">-InputObject</span></span>
<span data-ttu-id="1ec09-121">Obiekt tematu domeny EventGrid.</span><span class="sxs-lookup"><span data-stu-id="1ec09-121">EventGrid Domain Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic
Parameter Sets: DomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ec09-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1ec09-122">-Name</span></span>
<span data-ttu-id="1ec09-123">Nazwa tematu domeny EventGrid.</span><span class="sxs-lookup"><span data-stu-id="1ec09-123">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: DomainTopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ec09-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1ec09-124">-PassThru</span></span>
<span data-ttu-id="1ec09-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="1ec09-125">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ec09-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ec09-126">-ResourceGroupName</span></span>
<span data-ttu-id="1ec09-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1ec09-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ec09-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1ec09-128">-ResourceId</span></span>
<span data-ttu-id="1ec09-129">Identyfikator zasobu reprezentujący temat domeny siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="1ec09-129">Resource Identifier representing the Event Grid Domain Topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdDomainTopicParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ec09-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1ec09-130">-Confirm</span></span>
<span data-ttu-id="1ec09-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ec09-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ec09-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ec09-132">-WhatIf</span></span>
<span data-ttu-id="1ec09-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ec09-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ec09-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1ec09-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ec09-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ec09-135">CommonParameters</span></span>
<span data-ttu-id="1ec09-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ec09-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ec09-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ec09-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ec09-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1ec09-138">INPUTS</span></span>

### <span data-ttu-id="1ec09-139">System. String</span><span class="sxs-lookup"><span data-stu-id="1ec09-139">System.String</span></span>

### <span data-ttu-id="1ec09-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="1ec09-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="1ec09-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1ec09-141">OUTPUTS</span></span>

### <span data-ttu-id="1ec09-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1ec09-142">System.Boolean</span></span>

## <span data-ttu-id="1ec09-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1ec09-143">NOTES</span></span>

## <span data-ttu-id="1ec09-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1ec09-144">RELATED LINKS</span></span>