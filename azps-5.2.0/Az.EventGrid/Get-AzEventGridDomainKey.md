---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomainkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
ms.openlocfilehash: c080a5132d5ed31828fbf7a35385432d3c91a923
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346762"
---
# <span data-ttu-id="1dc36-101">Get-AzEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="1dc36-101">Get-AzEventGridDomainKey</span></span>

## <span data-ttu-id="1dc36-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1dc36-102">SYNOPSIS</span></span>
<span data-ttu-id="1dc36-103">Pobiera klucze dostępu współużytkowanego używane do publikowania zdarzeń w domenie siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="1dc36-103">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="1dc36-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1dc36-104">SYNTAX</span></span>

### <span data-ttu-id="1dc36-105">DomainNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1dc36-105">DomainNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomainKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1dc36-106">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1dc36-106">DomainInputObjectParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainObject] <PSDomain> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1dc36-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="1dc36-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1dc36-108">Opis</span><span class="sxs-lookup"><span data-stu-id="1dc36-108">DESCRIPTION</span></span>
<span data-ttu-id="1dc36-109">Pobiera klucze dostępu współużytkowanego używane do publikowania zdarzeń w domenie siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="1dc36-109">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="1dc36-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1dc36-110">EXAMPLES</span></span>

### <span data-ttu-id="1dc36-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1dc36-111">Example 1</span></span>

<span data-ttu-id="1dc36-112">Pobiera klucze dostępu współdzielonego do domeny \` Domain1 \` w grupie zasób \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="1dc36-112">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainKey -ResourceGroup MyResourceGroupName -Name Domain1

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

### <span data-ttu-id="1dc36-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="1dc36-113">Example 2</span></span>

<span data-ttu-id="1dc36-114">Pobiera klucze dostępu współdzielonego do domeny \` Domain1 \` w grupie zasób \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="1dc36-114">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1 | Get-AzEventGridDomainKey

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

## <span data-ttu-id="1dc36-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1dc36-115">PARAMETERS</span></span>

### <span data-ttu-id="1dc36-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dc36-116">-DefaultProfile</span></span>
<span data-ttu-id="1dc36-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1dc36-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1dc36-118">-Domainobject</span><span class="sxs-lookup"><span data-stu-id="1dc36-118">-DomainObject</span></span>
<span data-ttu-id="1dc36-119">Obiekt domeny EventGrid.</span><span class="sxs-lookup"><span data-stu-id="1dc36-119">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="1dc36-120">-DomainResourceId</span><span class="sxs-lookup"><span data-stu-id="1dc36-120">-DomainResourceId</span></span>
<span data-ttu-id="1dc36-121">Identyfikator zasobu reprezentujący domenę siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="1dc36-121">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="1dc36-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1dc36-122">-Name</span></span>
<span data-ttu-id="1dc36-123">EventGrid nazwa domeny.</span><span class="sxs-lookup"><span data-stu-id="1dc36-123">EventGrid domain name.</span></span>

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

### <span data-ttu-id="1dc36-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dc36-124">-ResourceGroupName</span></span>
<span data-ttu-id="1dc36-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1dc36-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="1dc36-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dc36-126">CommonParameters</span></span>
<span data-ttu-id="1dc36-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dc36-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dc36-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1dc36-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dc36-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1dc36-129">INPUTS</span></span>

### <span data-ttu-id="1dc36-130">System. String</span><span class="sxs-lookup"><span data-stu-id="1dc36-130">System.String</span></span>

### <span data-ttu-id="1dc36-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="1dc36-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="1dc36-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1dc36-132">OUTPUTS</span></span>

### <span data-ttu-id="1dc36-133">Microsoft. Azure. Management. EventGrid. MODELES. DomainSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="1dc36-133">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span></span>

## <span data-ttu-id="1dc36-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1dc36-134">NOTES</span></span>

## <span data-ttu-id="1dc36-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1dc36-135">RELATED LINKS</span></span>
