---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/get-azeventgridtopictype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
ms.openlocfilehash: 3a715e0c4c2540a0905035afabc15ef46caa32bc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991299"
---
# <span data-ttu-id="71add-101">Get-AzEventGridTopicType</span><span class="sxs-lookup"><span data-stu-id="71add-101">Get-AzEventGridTopicType</span></span>

## <span data-ttu-id="71add-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71add-102">SYNOPSIS</span></span>
<span data-ttu-id="71add-103">Pobiera szczegółowe informacje na temat typów tematów obsługiwanych przez usługę Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="71add-103">Gets the details about the topic types supported by Azure Event Grid.</span></span>

## <span data-ttu-id="71add-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="71add-104">SYNTAX</span></span>

```
Get-AzEventGridTopicType [-Name <String>] [-IncludeEventTypeData] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="71add-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="71add-105">DESCRIPTION</span></span>
<span data-ttu-id="71add-106">Pobiera szczegółowe informacje o typach tematów obsługiwanych w usłudze Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="71add-106">Gets the details of topic types supported by Azure Event Grid.</span></span>
<span data-ttu-id="71add-107">Jeśli określono nazwę typu tematu, zostaną zwrócone szczegóły dotyczące tego typu tematu.</span><span class="sxs-lookup"><span data-stu-id="71add-107">If a topic type name is specified, details about that topic type are returned.</span></span>
<span data-ttu-id="71add-108">Jeśli nazwa typu tematu nie zostanie określona, zostaną zwrócone szczegółowe informacje o wszystkich typach tematów.</span><span class="sxs-lookup"><span data-stu-id="71add-108">If a topic type name is not specified, details about all topic types are returned.</span></span>
<span data-ttu-id="71add-109">Jeśli określono typy zdarzeń IncludeEventTypes, informacje o typach zdarzeń obsługiwanych przez poszczególne typy tematów są uwzględniane w odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="71add-109">If IncludeEventTypes is specified, information about event types supported by each topic type is included in the response.</span></span>

## <span data-ttu-id="71add-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="71add-110">EXAMPLES</span></span>

### <span data-ttu-id="71add-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="71add-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType
```

<span data-ttu-id="71add-112">Pobiera listę typów tematów.</span><span class="sxs-lookup"><span data-stu-id="71add-112">Gets a list of the topic types.</span></span>

### <span data-ttu-id="71add-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="71add-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts"
```

<span data-ttu-id="71add-114">Informacje o typie tematu StorageAccounts.</span><span class="sxs-lookup"><span data-stu-id="71add-114">Gets information about the StorageAccounts topic type.</span></span>

### <span data-ttu-id="71add-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="71add-115">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts" -IncludeEventTypeData
```

<span data-ttu-id="71add-116">Pobiera informacje o typie tematu StorageAccounts, w tym o typach zdarzeń obsługiwanych przez konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="71add-116">Gets information about the StorageAccounts topic type, including the event types supported by StorageAccounts.</span></span>

## <span data-ttu-id="71add-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71add-117">PARAMETERS</span></span>

### <span data-ttu-id="71add-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71add-118">-DefaultProfile</span></span>
<span data-ttu-id="71add-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="71add-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="71add-120">-IncludeEventTypeData</span><span class="sxs-lookup"><span data-stu-id="71add-120">-IncludeEventTypeData</span></span>
<span data-ttu-id="71add-121">Jeśli zostanie określona, odpowiedź będzie zawierać typy zdarzeń obsługiwane przez typ tematu.</span><span class="sxs-lookup"><span data-stu-id="71add-121">If specified, the response will include the event types supported by a topic type.</span></span>

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

### <span data-ttu-id="71add-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="71add-122">-Name</span></span>
<span data-ttu-id="71add-123">Nazwa typu tematu w aplikacji EventGrid.</span><span class="sxs-lookup"><span data-stu-id="71add-123">EventGrid Topic Type Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71add-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71add-124">CommonParameters</span></span>
<span data-ttu-id="71add-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71add-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71add-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="71add-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71add-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="71add-127">INPUTS</span></span>

### <span data-ttu-id="71add-128">System.String</span><span class="sxs-lookup"><span data-stu-id="71add-128">System.String</span></span>

## <span data-ttu-id="71add-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="71add-129">OUTPUTS</span></span>

### <span data-ttu-id="71add-130">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfoListInstance</span><span class="sxs-lookup"><span data-stu-id="71add-130">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfoListInstance</span></span>

### <span data-ttu-id="71add-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfo</span><span class="sxs-lookup"><span data-stu-id="71add-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfo</span></span>

## <span data-ttu-id="71add-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="71add-132">NOTES</span></span>

## <span data-ttu-id="71add-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="71add-133">RELATED LINKS</span></span>
