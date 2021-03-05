---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/get-azeventgriddomainkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
ms.openlocfilehash: a211e3857cd81a5dd057795fb9e2956d60cbae17
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984670"
---
# <span data-ttu-id="58297-101">Get-AzEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="58297-101">Get-AzEventGridDomainKey</span></span>

## <span data-ttu-id="58297-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58297-102">SYNOPSIS</span></span>
<span data-ttu-id="58297-103">Pobiera klucze dostępu udostępnionego używane do publikowania zdarzeń w domenie siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="58297-103">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="58297-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="58297-104">SYNTAX</span></span>

### <span data-ttu-id="58297-105">DomainNameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="58297-105">DomainNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomainKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58297-106">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="58297-106">DomainInputObjectParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainObject] <PSDomain> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="58297-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="58297-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="58297-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="58297-108">DESCRIPTION</span></span>
<span data-ttu-id="58297-109">Pobiera klucze dostępu udostępnionego używane do publikowania zdarzeń w domenie siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="58297-109">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="58297-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="58297-110">EXAMPLES</span></span>

### <span data-ttu-id="58297-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="58297-111">Example 1</span></span>

<span data-ttu-id="58297-112">Pobiera klucze dostępu udostępnionego domeny Siatki zdarzeń \` (Domain1) \` w grupie zasobów \` MyResourceGroupName (Nazwa_grupy \` zasobów).</span><span class="sxs-lookup"><span data-stu-id="58297-112">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainKey -ResourceGroup MyResourceGroupName -Name Domain1

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

### <span data-ttu-id="58297-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="58297-113">Example 2</span></span>

<span data-ttu-id="58297-114">Pobiera klucze dostępu udostępnionego domeny Siatki zdarzeń \` (Domain1) \` w grupie zasobów \` MyResourceGroupName (Nazwa_grupy \` zasobów).</span><span class="sxs-lookup"><span data-stu-id="58297-114">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1 | Get-AzEventGridDomainKey

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

## <span data-ttu-id="58297-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58297-115">PARAMETERS</span></span>

### <span data-ttu-id="58297-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58297-116">-DefaultProfile</span></span>
<span data-ttu-id="58297-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="58297-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58297-118">-DomainObject</span><span class="sxs-lookup"><span data-stu-id="58297-118">-DomainObject</span></span>
<span data-ttu-id="58297-119">Obiekt Domeny EventGrid.</span><span class="sxs-lookup"><span data-stu-id="58297-119">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="58297-120">-DomainResourceId</span><span class="sxs-lookup"><span data-stu-id="58297-120">-DomainResourceId</span></span>
<span data-ttu-id="58297-121">Identyfikator zasobu reprezentujący domenę siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="58297-121">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="58297-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="58297-122">-Name</span></span>
<span data-ttu-id="58297-123">Nazwa domeny EventGrid.</span><span class="sxs-lookup"><span data-stu-id="58297-123">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58297-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58297-124">-ResourceGroupName</span></span>
<span data-ttu-id="58297-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="58297-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="58297-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58297-126">CommonParameters</span></span>
<span data-ttu-id="58297-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58297-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58297-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="58297-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58297-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="58297-129">INPUTS</span></span>

### <span data-ttu-id="58297-130">System.String</span><span class="sxs-lookup"><span data-stu-id="58297-130">System.String</span></span>

### <span data-ttu-id="58297-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="58297-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="58297-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="58297-132">OUTPUTS</span></span>

### <span data-ttu-id="58297-133">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="58297-133">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span></span>

## <span data-ttu-id="58297-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="58297-134">NOTES</span></span>

## <span data-ttu-id="58297-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="58297-135">RELATED LINKS</span></span>
