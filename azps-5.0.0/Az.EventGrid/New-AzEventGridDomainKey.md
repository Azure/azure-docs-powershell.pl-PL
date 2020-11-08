---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgriddomainkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainKey.md
ms.openlocfilehash: 6afb01ef46ba4f9c627f20a1c49ab58c2a79f252
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233178"
---
# <span data-ttu-id="b16ca-101">New-AzEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="b16ca-101">New-AzEventGridDomainKey</span></span>

## <span data-ttu-id="b16ca-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b16ca-102">SYNOPSIS</span></span>
<span data-ttu-id="b16ca-103">Generuje ponownie klucz dostępu współużytkowanego dla domeny z siatką zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b16ca-103">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="b16ca-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b16ca-104">SYNTAX</span></span>

### <span data-ttu-id="b16ca-105">DomainNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b16ca-105">DomainNameParameterSet (Default)</span></span>
```
New-AzEventGridDomainKey [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b16ca-106">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b16ca-106">DomainInputObjectParameterSet</span></span>
```
New-AzEventGridDomainKey [-Name] <String> [-DomainInputObject] <PSDomain>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b16ca-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="b16ca-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridDomainKey [-Name] <String> [-DomainResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b16ca-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b16ca-108">DESCRIPTION</span></span>
<span data-ttu-id="b16ca-109">Generuje ponownie klucz dostępu współużytkowanego dla domeny z siatką zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b16ca-109">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="b16ca-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b16ca-110">EXAMPLES</span></span>

### <span data-ttu-id="b16ca-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b16ca-111">Example 1</span></span>

<span data-ttu-id="b16ca-112">Ponownie wygenerowano klucz odpowiadający kluczowi \' KEY1 ' \ z domeny \` Domain1 \` w grupie zasobów \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="b16ca-112">Regenerate the key corresponding to key \'key1'\ of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomainKey -ResourceGroup MyResourceGroupName -DomainName Domain1 -Name key1

Key1                                         Key2
----                                         ----
<New Value for Key1>                        <Old Value for Key2>
```

### <span data-ttu-id="b16ca-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b16ca-113">Example 2</span></span>

<span data-ttu-id="b16ca-114">Ponownie wygenerowano klucz odpowiadający kluczowi \' KEY1 ' \ z domeny \` Domain1 \` w grupie zasobów \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="b16ca-114">Regenerate the key corresponding to key \'key1'\ of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1 | New-AzEventGridTopicKey -KeyName "key1"

Key1                                         Key2
----                                         ----
<New Value for Key1>                        <Old Value for Key2>
```

### <span data-ttu-id="b16ca-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="b16ca-115">Example 3</span></span>

<span data-ttu-id="b16ca-116">Ponownie wygenerowano klucz odpowiadający kluczowi \' key2 ' \ z domeny \` Domain1 \` w grupie zasobów \` MyResourceGroupName \` przy użyciu pełnego identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="b16ca-116">Regenerate the key corresponding to key \'key2'\ of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using its full resource Id.</span></span>

```powershell
PS C:\> New-AzEventGridDomainKey -ResourceId /subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1 -KeyName Key2

Key1                                         Key2
----                                         ----
<Old Value for Key1>                        <New Value for Key2>
```

## <span data-ttu-id="b16ca-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b16ca-117">PARAMETERS</span></span>

### <span data-ttu-id="b16ca-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b16ca-118">-DefaultProfile</span></span>
<span data-ttu-id="b16ca-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b16ca-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b16ca-120">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="b16ca-120">-DomainInputObject</span></span>
<span data-ttu-id="b16ca-121">Obiekt domeny EventGrid.</span><span class="sxs-lookup"><span data-stu-id="b16ca-121">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="b16ca-122">-NazwaDomeny</span><span class="sxs-lookup"><span data-stu-id="b16ca-122">-DomainName</span></span>
<span data-ttu-id="b16ca-123">EventGrid nazwa domeny.</span><span class="sxs-lookup"><span data-stu-id="b16ca-123">EventGrid domain name.</span></span>

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

### <span data-ttu-id="b16ca-124">-DomainResourceId</span><span class="sxs-lookup"><span data-stu-id="b16ca-124">-DomainResourceId</span></span>
<span data-ttu-id="b16ca-125">Identyfikator zasobu reprezentujący domenę siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="b16ca-125">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="b16ca-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b16ca-126">-Name</span></span>
<span data-ttu-id="b16ca-127">Nazwa klucza, który należy ponownie wygenerować</span><span class="sxs-lookup"><span data-stu-id="b16ca-127">The name of the key that needs to be regenerated</span></span>

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

### <span data-ttu-id="b16ca-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b16ca-128">-ResourceGroupName</span></span>
<span data-ttu-id="b16ca-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b16ca-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="b16ca-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b16ca-130">-Confirm</span></span>
<span data-ttu-id="b16ca-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b16ca-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b16ca-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b16ca-132">-WhatIf</span></span>
<span data-ttu-id="b16ca-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b16ca-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b16ca-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b16ca-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b16ca-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b16ca-135">CommonParameters</span></span>
<span data-ttu-id="b16ca-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b16ca-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b16ca-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b16ca-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b16ca-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b16ca-138">INPUTS</span></span>

### <span data-ttu-id="b16ca-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b16ca-139">System.String</span></span>

### <span data-ttu-id="b16ca-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="b16ca-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="b16ca-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b16ca-141">OUTPUTS</span></span>

### <span data-ttu-id="b16ca-142">Microsoft. Azure. Management. EventGrid. MODELES. DomainSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="b16ca-142">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span></span>

## <span data-ttu-id="b16ca-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b16ca-143">NOTES</span></span>

## <span data-ttu-id="b16ca-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b16ca-144">RELATED LINKS</span></span>
