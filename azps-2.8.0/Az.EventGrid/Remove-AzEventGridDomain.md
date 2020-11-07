---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
ms.openlocfilehash: b46c9be4c8731fa6b9082a8076dd9ae175e62422
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705482"
---
# <span data-ttu-id="1cfff-101">Remove-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="1cfff-101">Remove-AzEventGridDomain</span></span>

## <span data-ttu-id="1cfff-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1cfff-102">SYNOPSIS</span></span>
<span data-ttu-id="1cfff-103">Usuwa domenę siatki zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1cfff-103">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="1cfff-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1cfff-104">SYNTAX</span></span>

### <span data-ttu-id="1cfff-105">DomainNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1cfff-105">DomainNameParameterSet (Default)</span></span>
```
Remove-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cfff-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cfff-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridDomain [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cfff-107">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cfff-107">DomainInputObjectParameterSet</span></span>
```
Remove-AzEventGridDomain [-InputObject] <PSDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1cfff-108">Opis</span><span class="sxs-lookup"><span data-stu-id="1cfff-108">DESCRIPTION</span></span>
<span data-ttu-id="1cfff-109">Usuwa domenę siatki zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1cfff-109">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="1cfff-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1cfff-110">EXAMPLES</span></span>

### <span data-ttu-id="1cfff-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1cfff-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1
```

<span data-ttu-id="1cfff-112">Usuwa Domain1 domeny w siatce \` zdarzeń \` w MyResourceGroupName grupy \` zasobów \` .</span><span class="sxs-lookup"><span data-stu-id="1cfff-112">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="1cfff-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="1cfff-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/Domains/Domain1" | Remove-AzEventGridDomain
```

<span data-ttu-id="1cfff-114">Usuwa Domain1 domeny w siatce \` zdarzeń \` w MyResourceGroupName grupy \` zasobów \` .</span><span class="sxs-lookup"><span data-stu-id="1cfff-114">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="1cfff-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1cfff-115">PARAMETERS</span></span>

### <span data-ttu-id="1cfff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cfff-116">-DefaultProfile</span></span>
<span data-ttu-id="1cfff-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1cfff-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1cfff-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1cfff-118">-InputObject</span></span>
<span data-ttu-id="1cfff-119">Obiekt domeny EventGrid.</span><span class="sxs-lookup"><span data-stu-id="1cfff-119">EventGrid Domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomain
Parameter Sets: DomainInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1cfff-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1cfff-120">-Name</span></span>
<span data-ttu-id="1cfff-121">EventGrid nazwa domeny.</span><span class="sxs-lookup"><span data-stu-id="1cfff-121">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cfff-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1cfff-122">-PassThru</span></span>
<span data-ttu-id="1cfff-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="1cfff-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="1cfff-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cfff-124">-ResourceGroupName</span></span>
<span data-ttu-id="1cfff-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1cfff-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cfff-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1cfff-126">-ResourceId</span></span>
<span data-ttu-id="1cfff-127">Identyfikator zasobu reprezentujący domenę siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="1cfff-127">Resource Identifier representing the Event Grid Domain.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cfff-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1cfff-128">-Confirm</span></span>
<span data-ttu-id="1cfff-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1cfff-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cfff-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cfff-130">-WhatIf</span></span>
<span data-ttu-id="1cfff-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1cfff-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1cfff-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1cfff-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cfff-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cfff-133">CommonParameters</span></span>
<span data-ttu-id="1cfff-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cfff-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cfff-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cfff-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cfff-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1cfff-136">INPUTS</span></span>

### <span data-ttu-id="1cfff-137">System. String</span><span class="sxs-lookup"><span data-stu-id="1cfff-137">System.String</span></span>

### <span data-ttu-id="1cfff-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="1cfff-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="1cfff-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1cfff-139">OUTPUTS</span></span>

### <span data-ttu-id="1cfff-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1cfff-140">System.Boolean</span></span>

## <span data-ttu-id="1cfff-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1cfff-141">NOTES</span></span>

## <span data-ttu-id="1cfff-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1cfff-142">RELATED LINKS</span></span>
