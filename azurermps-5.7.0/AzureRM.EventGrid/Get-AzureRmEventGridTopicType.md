---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/get-azurermeventgridtopictype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicType.md
ms.openlocfilehash: bc272648920e29ed2e735ca08b9fa78563a9f9d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717532"
---
# <span data-ttu-id="1d55a-101">Get-AzureRmEventGridTopicType</span><span class="sxs-lookup"><span data-stu-id="1d55a-101">Get-AzureRmEventGridTopicType</span></span>

## <span data-ttu-id="1d55a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1d55a-102">SYNOPSIS</span></span>
<span data-ttu-id="1d55a-103">Pobiera szczegóły dotyczące typów tematów obsługiwanych przez siatkę zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1d55a-103">Gets the details about the topic types supported by Azure Event Grid.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d55a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1d55a-104">SYNTAX</span></span>

```
Get-AzureRmEventGridTopicType [[-Name] <String>] [-IncludeEventTypeData]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d55a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1d55a-105">DESCRIPTION</span></span>
<span data-ttu-id="1d55a-106">Pobiera szczegóły typów tematów obsługiwanych przez siatkę zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1d55a-106">Gets the details of topic types supported by Azure Event Grid.</span></span>
<span data-ttu-id="1d55a-107">Jeśli podano nazwę typu tematu, zostaną zwrócone szczegóły dotyczące tego typu tematu.</span><span class="sxs-lookup"><span data-stu-id="1d55a-107">If a topic type name is specified, details about that topic type are returned.</span></span>
<span data-ttu-id="1d55a-108">Jeśli nie podano nazwy typu tematu, zwracane są szczegóły dotyczące wszystkich typów tematów.</span><span class="sxs-lookup"><span data-stu-id="1d55a-108">If a topic type name is not specified, details about all topic types are returned.</span></span>
<span data-ttu-id="1d55a-109">Jeśli IncludeEventTypes jest określony, w odpowiedzi jest uwzględniana informacja o typach zdarzeń obsługiwanych przez poszczególne typy tematów.</span><span class="sxs-lookup"><span data-stu-id="1d55a-109">If IncludeEventTypes is specified, information about event types supported by each topic type is included in the response.</span></span>

## <span data-ttu-id="1d55a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1d55a-110">EXAMPLES</span></span>

### <span data-ttu-id="1d55a-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1d55a-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridTopicType
```

<span data-ttu-id="1d55a-112">Pobiera listę typów tematów.</span><span class="sxs-lookup"><span data-stu-id="1d55a-112">Gets a list of the topic types.</span></span>

### <span data-ttu-id="1d55a-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="1d55a-113">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopicType -Name "Microsoft.Storage.StorageAccounts"
```

<span data-ttu-id="1d55a-114">Pobiera informacje o typie tematu StorageAccounts.</span><span class="sxs-lookup"><span data-stu-id="1d55a-114">Gets information about the StorageAccounts topic type.</span></span>

### <span data-ttu-id="1d55a-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="1d55a-115">Example 3</span></span>
```
PS C:\> Get-AzureRmEventGridTopicType -Name "Microsoft.Storage.StorageAccounts" -IncludeEventTypeData
```

<span data-ttu-id="1d55a-116">Pobiera informacje o typie tematu StorageAccounts, w tym o typach zdarzeń obsługiwanych przez StorageAccounts.</span><span class="sxs-lookup"><span data-stu-id="1d55a-116">Gets information about the StorageAccounts topic type, including the event types supported by StorageAccounts.</span></span>

## <span data-ttu-id="1d55a-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1d55a-117">PARAMETERS</span></span>

### <span data-ttu-id="1d55a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d55a-118">-DefaultProfile</span></span>
<span data-ttu-id="1d55a-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="1d55a-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d55a-120">-IncludeEventTypeData</span><span class="sxs-lookup"><span data-stu-id="1d55a-120">-IncludeEventTypeData</span></span>
<span data-ttu-id="1d55a-121">Jeśli ta wartość jest określona, odpowiedź będzie zawierać typy zdarzeń obsługiwane przez typ tematu.</span><span class="sxs-lookup"><span data-stu-id="1d55a-121">If specified, the response will include the event types supported by a topic type.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d55a-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1d55a-122">-Name</span></span>
<span data-ttu-id="1d55a-123">Nazwa typu tematu EventGrid.</span><span class="sxs-lookup"><span data-stu-id="1d55a-123">EventGrid Topic Type Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d55a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d55a-124">CommonParameters</span></span>
<span data-ttu-id="1d55a-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d55a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d55a-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d55a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d55a-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1d55a-127">INPUTS</span></span>

### <span data-ttu-id="1d55a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="1d55a-128">System.String</span></span>
<span data-ttu-id="1d55a-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1d55a-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1d55a-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1d55a-130">OUTPUTS</span></span>

### <span data-ttu-id="1d55a-131">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. EventGrid. MODELES. PSTopicTypeInfoListInstance, Microsoft. Azure. Commands. EventGrid, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="1d55a-131">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfoListInstance, Microsoft.Azure.Commands.EventGrid, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="1d55a-132">Microsoft. Azure. Commands. EventGrid. models. PSTopicTypeInfo</span><span class="sxs-lookup"><span data-stu-id="1d55a-132">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfo</span></span>

## <span data-ttu-id="1d55a-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1d55a-133">NOTES</span></span>

## <span data-ttu-id="1d55a-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1d55a-134">RELATED LINKS</span></span>

