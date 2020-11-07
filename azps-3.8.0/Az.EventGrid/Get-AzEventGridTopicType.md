---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopictype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
ms.openlocfilehash: 23392f77c9315cee2bf8b1b8369febbc2281c6ff
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895234"
---
# <span data-ttu-id="272d4-101">Get-AzEventGridTopicType</span><span class="sxs-lookup"><span data-stu-id="272d4-101">Get-AzEventGridTopicType</span></span>

## <span data-ttu-id="272d4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="272d4-102">SYNOPSIS</span></span>
<span data-ttu-id="272d4-103">Pobiera szczegóły dotyczące typów tematów obsługiwanych przez siatkę zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="272d4-103">Gets the details about the topic types supported by Azure Event Grid.</span></span>

## <span data-ttu-id="272d4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="272d4-104">SYNTAX</span></span>

```
Get-AzEventGridTopicType [[-Name] <String>] [-IncludeEventTypeData] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="272d4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="272d4-105">DESCRIPTION</span></span>
<span data-ttu-id="272d4-106">Pobiera szczegóły typów tematów obsługiwanych przez siatkę zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="272d4-106">Gets the details of topic types supported by Azure Event Grid.</span></span>
<span data-ttu-id="272d4-107">Jeśli podano nazwę typu tematu, zostaną zwrócone szczegóły dotyczące tego typu tematu.</span><span class="sxs-lookup"><span data-stu-id="272d4-107">If a topic type name is specified, details about that topic type are returned.</span></span>
<span data-ttu-id="272d4-108">Jeśli nie podano nazwy typu tematu, zwracane są szczegóły dotyczące wszystkich typów tematów.</span><span class="sxs-lookup"><span data-stu-id="272d4-108">If a topic type name is not specified, details about all topic types are returned.</span></span>
<span data-ttu-id="272d4-109">Jeśli IncludeEventTypes jest określony, w odpowiedzi jest uwzględniana informacja o typach zdarzeń obsługiwanych przez poszczególne typy tematów.</span><span class="sxs-lookup"><span data-stu-id="272d4-109">If IncludeEventTypes is specified, information about event types supported by each topic type is included in the response.</span></span>

## <span data-ttu-id="272d4-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="272d4-110">EXAMPLES</span></span>

### <span data-ttu-id="272d4-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="272d4-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType
```

<span data-ttu-id="272d4-112">Pobiera listę typów tematów.</span><span class="sxs-lookup"><span data-stu-id="272d4-112">Gets a list of the topic types.</span></span>

### <span data-ttu-id="272d4-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="272d4-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts"
```

<span data-ttu-id="272d4-114">Pobiera informacje o typie tematu StorageAccounts.</span><span class="sxs-lookup"><span data-stu-id="272d4-114">Gets information about the StorageAccounts topic type.</span></span>

### <span data-ttu-id="272d4-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="272d4-115">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts" -IncludeEventTypeData
```

<span data-ttu-id="272d4-116">Pobiera informacje o typie tematu StorageAccounts, w tym o typach zdarzeń obsługiwanych przez StorageAccounts.</span><span class="sxs-lookup"><span data-stu-id="272d4-116">Gets information about the StorageAccounts topic type, including the event types supported by StorageAccounts.</span></span>

## <span data-ttu-id="272d4-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="272d4-117">PARAMETERS</span></span>

### <span data-ttu-id="272d4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="272d4-118">-DefaultProfile</span></span>
<span data-ttu-id="272d4-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="272d4-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="272d4-120">-IncludeEventTypeData</span><span class="sxs-lookup"><span data-stu-id="272d4-120">-IncludeEventTypeData</span></span>
<span data-ttu-id="272d4-121">Jeśli ta wartość jest określona, odpowiedź będzie zawierać typy zdarzeń obsługiwane przez typ tematu.</span><span class="sxs-lookup"><span data-stu-id="272d4-121">If specified, the response will include the event types supported by a topic type.</span></span>

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

### <span data-ttu-id="272d4-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="272d4-122">-Name</span></span>
<span data-ttu-id="272d4-123">Nazwa typu tematu EventGrid.</span><span class="sxs-lookup"><span data-stu-id="272d4-123">EventGrid Topic Type Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="272d4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="272d4-124">CommonParameters</span></span>
<span data-ttu-id="272d4-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="272d4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="272d4-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="272d4-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="272d4-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="272d4-127">INPUTS</span></span>

### <span data-ttu-id="272d4-128">System. String</span><span class="sxs-lookup"><span data-stu-id="272d4-128">System.String</span></span>

## <span data-ttu-id="272d4-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="272d4-129">OUTPUTS</span></span>

### <span data-ttu-id="272d4-130">Microsoft. Azure. Commands. EventGrid. models. PSTopicTypeInfoListInstance</span><span class="sxs-lookup"><span data-stu-id="272d4-130">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfoListInstance</span></span>

### <span data-ttu-id="272d4-131">Microsoft. Azure. Commands. EventGrid. models. PSTopicTypeInfo</span><span class="sxs-lookup"><span data-stu-id="272d4-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfo</span></span>

## <span data-ttu-id="272d4-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="272d4-132">NOTES</span></span>

## <span data-ttu-id="272d4-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="272d4-133">RELATED LINKS</span></span>
