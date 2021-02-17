---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomainkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
ms.openlocfilehash: c080a5132d5ed31828fbf7a35385432d3c91a923
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243667"
---
# <span data-ttu-id="201b8-101">Get-AzEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="201b8-101">Get-AzEventGridDomainKey</span></span>

## <span data-ttu-id="201b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="201b8-102">SYNOPSIS</span></span>
<span data-ttu-id="201b8-103">Pobiera klucze dostępu udostępnionego używane do publikowania zdarzeń w domenie siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="201b8-103">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="201b8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="201b8-104">SYNTAX</span></span>

### <span data-ttu-id="201b8-105">DomainNameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="201b8-105">DomainNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomainKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="201b8-106">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="201b8-106">DomainInputObjectParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainObject] <PSDomain> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="201b8-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="201b8-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="201b8-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="201b8-108">DESCRIPTION</span></span>
<span data-ttu-id="201b8-109">Pobiera klucze dostępu udostępnionego używane do publikowania zdarzeń w domenie siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="201b8-109">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="201b8-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="201b8-110">EXAMPLES</span></span>

### <span data-ttu-id="201b8-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="201b8-111">Example 1</span></span>

<span data-ttu-id="201b8-112">Pobiera klucze dostępu udostępnionego domeny Siatki zdarzeń \` (Domain1) \` w grupie zasobów \` MyResourceGroupName (Nazwa_grupy \` zasobów).</span><span class="sxs-lookup"><span data-stu-id="201b8-112">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainKey -ResourceGroup MyResourceGroupName -Name Domain1

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

### <span data-ttu-id="201b8-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="201b8-113">Example 2</span></span>

<span data-ttu-id="201b8-114">Pobiera klucze dostępu udostępnionego domeny Siatki zdarzeń \` (Domain1) \` w grupie zasobów \` MyResourceGroupName (Nazwa_grupy \` zasobów).</span><span class="sxs-lookup"><span data-stu-id="201b8-114">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1 | Get-AzEventGridDomainKey

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

## <span data-ttu-id="201b8-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="201b8-115">PARAMETERS</span></span>

### <span data-ttu-id="201b8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="201b8-116">-DefaultProfile</span></span>
<span data-ttu-id="201b8-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="201b8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="201b8-118">-DomainObject</span><span class="sxs-lookup"><span data-stu-id="201b8-118">-DomainObject</span></span>
<span data-ttu-id="201b8-119">Obiekt Domeny EventGrid.</span><span class="sxs-lookup"><span data-stu-id="201b8-119">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="201b8-120">-DomainResourceId</span><span class="sxs-lookup"><span data-stu-id="201b8-120">-DomainResourceId</span></span>
<span data-ttu-id="201b8-121">Identyfikator zasobu reprezentujący domenę siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="201b8-121">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="201b8-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="201b8-122">-Name</span></span>
<span data-ttu-id="201b8-123">Nazwa domeny EventGrid.</span><span class="sxs-lookup"><span data-stu-id="201b8-123">EventGrid domain name.</span></span>

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

### <span data-ttu-id="201b8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="201b8-124">-ResourceGroupName</span></span>
<span data-ttu-id="201b8-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="201b8-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="201b8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="201b8-126">CommonParameters</span></span>
<span data-ttu-id="201b8-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="201b8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="201b8-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="201b8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="201b8-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="201b8-129">INPUTS</span></span>

### <span data-ttu-id="201b8-130">System.String</span><span class="sxs-lookup"><span data-stu-id="201b8-130">System.String</span></span>

### <span data-ttu-id="201b8-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="201b8-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="201b8-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="201b8-132">OUTPUTS</span></span>

### <span data-ttu-id="201b8-133">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="201b8-133">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span></span>

## <span data-ttu-id="201b8-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="201b8-134">NOTES</span></span>

## <span data-ttu-id="201b8-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="201b8-135">RELATED LINKS</span></span>
