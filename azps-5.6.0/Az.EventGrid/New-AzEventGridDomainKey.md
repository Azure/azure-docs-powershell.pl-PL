---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/new-azeventgriddomainkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainKey.md
ms.openlocfilehash: 297abcdf06d1efbe5cf7e39e310d2c2d422a6324
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991271"
---
# <span data-ttu-id="ddc24-101">New-AzEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="ddc24-101">New-AzEventGridDomainKey</span></span>

## <span data-ttu-id="ddc24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddc24-102">SYNOPSIS</span></span>
<span data-ttu-id="ddc24-103">Ponownie generuje klucz dostępu udostępnionego dla domeny siatki zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ddc24-103">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="ddc24-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ddc24-104">SYNTAX</span></span>

### <span data-ttu-id="ddc24-105">DomainNameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="ddc24-105">DomainNameParameterSet (Default)</span></span>
```
New-AzEventGridDomainKey [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddc24-106">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ddc24-106">DomainInputObjectParameterSet</span></span>
```
New-AzEventGridDomainKey [-Name] <String> [-DomainInputObject] <PSDomain>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddc24-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="ddc24-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridDomainKey [-Name] <String> [-DomainResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddc24-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="ddc24-108">DESCRIPTION</span></span>
<span data-ttu-id="ddc24-109">Ponownie generuje klucz dostępu udostępnionego dla domeny siatki zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ddc24-109">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="ddc24-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ddc24-110">EXAMPLES</span></span>

### <span data-ttu-id="ddc24-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ddc24-111">Example 1</span></span>

<span data-ttu-id="ddc24-112">Ponownie generuj klucz odpowiadający kluczowi key1'\ domeny siatki zdarzeń (Domain1) w grupie zasobów \' \` \` \` MyResourceGroupName (Nazwa_grupy \` zasobów).</span><span class="sxs-lookup"><span data-stu-id="ddc24-112">Regenerate the key corresponding to key \'key1'\ of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomainKey -ResourceGroup MyResourceGroupName -DomainName Domain1 -Name key1

Key1                                         Key2
----                                         ----
<New Value for Key1>                        <Old Value for Key2>
```

### <span data-ttu-id="ddc24-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ddc24-113">Example 2</span></span>

<span data-ttu-id="ddc24-114">Ponownie generuj klucz odpowiadający kluczowi key1'\ domeny siatki zdarzeń (Domain1) w grupie zasobów \' \` \` \` MyResourceGroupName (Nazwa_grupy \` zasobów).</span><span class="sxs-lookup"><span data-stu-id="ddc24-114">Regenerate the key corresponding to key \'key1'\ of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1 | New-AzEventGridTopicKey -KeyName "key1"

Key1                                         Key2
----                                         ----
<New Value for Key1>                        <Old Value for Key2>
```

### <span data-ttu-id="ddc24-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="ddc24-115">Example 3</span></span>

<span data-ttu-id="ddc24-116">Ponownie wygeneruj klucz odpowiadający kluczowi key2'\ domeny siatki zdarzeń (Domena1) w grupie zasobów \' \` \` \` MyResourceGroupName przy użyciu \` pełnego identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="ddc24-116">Regenerate the key corresponding to key \'key2'\ of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using its full resource Id.</span></span>

```powershell
PS C:\> New-AzEventGridDomainKey -ResourceId /subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1 -KeyName Key2

Key1                                         Key2
----                                         ----
<Old Value for Key1>                        <New Value for Key2>
```

## <span data-ttu-id="ddc24-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ddc24-117">PARAMETERS</span></span>

### <span data-ttu-id="ddc24-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddc24-118">-DefaultProfile</span></span>
<span data-ttu-id="ddc24-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ddc24-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddc24-120">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="ddc24-120">-DomainInputObject</span></span>
<span data-ttu-id="ddc24-121">Obiekt Domeny EventGrid.</span><span class="sxs-lookup"><span data-stu-id="ddc24-121">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="ddc24-122">-DomainName</span><span class="sxs-lookup"><span data-stu-id="ddc24-122">-DomainName</span></span>
<span data-ttu-id="ddc24-123">Nazwa domeny EventGrid.</span><span class="sxs-lookup"><span data-stu-id="ddc24-123">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddc24-124">-DomainResourceId</span><span class="sxs-lookup"><span data-stu-id="ddc24-124">-DomainResourceId</span></span>
<span data-ttu-id="ddc24-125">Identyfikator zasobu reprezentujący domenę siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="ddc24-125">Resource Identifier representing the Event Grid Domain.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddc24-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ddc24-126">-Name</span></span>
<span data-ttu-id="ddc24-127">Nazwa klucza, który wymaga ponownego wygenerowania</span><span class="sxs-lookup"><span data-stu-id="ddc24-127">The name of the key that needs to be regenerated</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddc24-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddc24-128">-ResourceGroupName</span></span>
<span data-ttu-id="ddc24-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ddc24-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddc24-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ddc24-130">-Confirm</span></span>
<span data-ttu-id="ddc24-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ddc24-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddc24-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddc24-132">-WhatIf</span></span>
<span data-ttu-id="ddc24-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ddc24-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddc24-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ddc24-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddc24-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddc24-135">CommonParameters</span></span>
<span data-ttu-id="ddc24-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddc24-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddc24-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ddc24-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddc24-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ddc24-138">INPUTS</span></span>

### <span data-ttu-id="ddc24-139">System.String</span><span class="sxs-lookup"><span data-stu-id="ddc24-139">System.String</span></span>

### <span data-ttu-id="ddc24-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="ddc24-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="ddc24-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ddc24-141">OUTPUTS</span></span>

### <span data-ttu-id="ddc24-142">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="ddc24-142">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span></span>

## <span data-ttu-id="ddc24-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ddc24-143">NOTES</span></span>

## <span data-ttu-id="ddc24-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ddc24-144">RELATED LINKS</span></span>
