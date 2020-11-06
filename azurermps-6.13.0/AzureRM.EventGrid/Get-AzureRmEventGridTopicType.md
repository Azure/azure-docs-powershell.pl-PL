---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/get-azurermeventgridtopictype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicType.md
ms.openlocfilehash: cd3182a2a00f488dabd70a97d06693362068768c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552092"
---
# <span data-ttu-id="9a515-101">Get-AzureRmEventGridTopicType</span><span class="sxs-lookup"><span data-stu-id="9a515-101">Get-AzureRmEventGridTopicType</span></span>

## <span data-ttu-id="9a515-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9a515-102">SYNOPSIS</span></span>
<span data-ttu-id="9a515-103">Pobiera szczegóły dotyczące typów tematów obsługiwanych przez siatkę zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9a515-103">Gets the details about the topic types supported by Azure Event Grid.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a515-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9a515-104">SYNTAX</span></span>

```
Get-AzureRmEventGridTopicType [[-Name] <String>] [-IncludeEventTypeData]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a515-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9a515-105">DESCRIPTION</span></span>
<span data-ttu-id="9a515-106">Pobiera szczegóły typów tematów obsługiwanych przez siatkę zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9a515-106">Gets the details of topic types supported by Azure Event Grid.</span></span>
<span data-ttu-id="9a515-107">Jeśli podano nazwę typu tematu, zostaną zwrócone szczegóły dotyczące tego typu tematu.</span><span class="sxs-lookup"><span data-stu-id="9a515-107">If a topic type name is specified, details about that topic type are returned.</span></span>
<span data-ttu-id="9a515-108">Jeśli nie podano nazwy typu tematu, zwracane są szczegóły dotyczące wszystkich typów tematów.</span><span class="sxs-lookup"><span data-stu-id="9a515-108">If a topic type name is not specified, details about all topic types are returned.</span></span>
<span data-ttu-id="9a515-109">Jeśli IncludeEventTypes jest określony, w odpowiedzi jest uwzględniana informacja o typach zdarzeń obsługiwanych przez poszczególne typy tematów.</span><span class="sxs-lookup"><span data-stu-id="9a515-109">If IncludeEventTypes is specified, information about event types supported by each topic type is included in the response.</span></span>

## <span data-ttu-id="9a515-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9a515-110">EXAMPLES</span></span>

### <span data-ttu-id="9a515-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9a515-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridTopicType
```

<span data-ttu-id="9a515-112">Pobiera listę typów tematów.</span><span class="sxs-lookup"><span data-stu-id="9a515-112">Gets a list of the topic types.</span></span>

### <span data-ttu-id="9a515-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="9a515-113">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopicType -Name "Microsoft.Storage.StorageAccounts"
```

<span data-ttu-id="9a515-114">Pobiera informacje o typie tematu StorageAccounts.</span><span class="sxs-lookup"><span data-stu-id="9a515-114">Gets information about the StorageAccounts topic type.</span></span>

### <span data-ttu-id="9a515-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="9a515-115">Example 3</span></span>
```
PS C:\> Get-AzureRmEventGridTopicType -Name "Microsoft.Storage.StorageAccounts" -IncludeEventTypeData
```

<span data-ttu-id="9a515-116">Pobiera informacje o typie tematu StorageAccounts, w tym o typach zdarzeń obsługiwanych przez StorageAccounts.</span><span class="sxs-lookup"><span data-stu-id="9a515-116">Gets information about the StorageAccounts topic type, including the event types supported by StorageAccounts.</span></span>

## <span data-ttu-id="9a515-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9a515-117">PARAMETERS</span></span>

### <span data-ttu-id="9a515-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a515-118">-DefaultProfile</span></span>
<span data-ttu-id="9a515-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="9a515-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a515-120">-IncludeEventTypeData</span><span class="sxs-lookup"><span data-stu-id="9a515-120">-IncludeEventTypeData</span></span>
<span data-ttu-id="9a515-121">Jeśli ta wartość jest określona, odpowiedź będzie zawierać typy zdarzeń obsługiwane przez typ tematu.</span><span class="sxs-lookup"><span data-stu-id="9a515-121">If specified, the response will include the event types supported by a topic type.</span></span>

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

### <span data-ttu-id="9a515-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9a515-122">-Name</span></span>
<span data-ttu-id="9a515-123">Nazwa typu tematu EventGrid.</span><span class="sxs-lookup"><span data-stu-id="9a515-123">EventGrid Topic Type Name.</span></span>

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

### <span data-ttu-id="9a515-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a515-124">CommonParameters</span></span>
<span data-ttu-id="9a515-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a515-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a515-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a515-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a515-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9a515-127">INPUTS</span></span>

### <span data-ttu-id="9a515-128">System. String</span><span class="sxs-lookup"><span data-stu-id="9a515-128">System.String</span></span>

## <span data-ttu-id="9a515-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9a515-129">OUTPUTS</span></span>

### <span data-ttu-id="9a515-130">Microsoft. Azure. Commands. EventGrid. models. PSTopicTypeInfoListInstance</span><span class="sxs-lookup"><span data-stu-id="9a515-130">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfoListInstance</span></span>

### <span data-ttu-id="9a515-131">Microsoft. Azure. Commands. EventGrid. models. PSTopicTypeInfo</span><span class="sxs-lookup"><span data-stu-id="9a515-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfo</span></span>

## <span data-ttu-id="9a515-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9a515-132">NOTES</span></span>

## <span data-ttu-id="9a515-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9a515-133">RELATED LINKS</span></span>
