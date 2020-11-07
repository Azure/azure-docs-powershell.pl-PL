---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/get-azurermeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicKey.md
ms.openlocfilehash: 741a888287ba7fcb4a9b54c1281a6a27be5fbb0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718500"
---
# <span data-ttu-id="00ea6-101">Get-AzureRmEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="00ea6-101">Get-AzureRmEventGridTopicKey</span></span>

## <span data-ttu-id="00ea6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="00ea6-102">SYNOPSIS</span></span>
<span data-ttu-id="00ea6-103">Pobiera klucze dostępu współużytkowanego używane do publikowania zdarzeń w temacie dotyczącym siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="00ea6-103">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00ea6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="00ea6-104">SYNTAX</span></span>

### <span data-ttu-id="00ea6-105">TopicNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="00ea6-105">TopicNameParameterSet (Default)</span></span>
```
Get-AzureRmEventGridTopicKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00ea6-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="00ea6-106">TopicInputObjectParameterSet</span></span>
```
Get-AzureRmEventGridTopicKey [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="00ea6-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="00ea6-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzureRmEventGridTopicKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="00ea6-108">Opis</span><span class="sxs-lookup"><span data-stu-id="00ea6-108">DESCRIPTION</span></span>
<span data-ttu-id="00ea6-109">Pobiera klucze dostępu współużytkowanego używane do publikowania zdarzeń w temacie dotyczącym siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="00ea6-109">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="00ea6-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="00ea6-110">EXAMPLES</span></span>

### <span data-ttu-id="00ea6-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="00ea6-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridTopicKey -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="00ea6-112">Pobiera klucze dostępu współużytkowanego tematu siatki zdarzeń \` Temat1 \` w MyResourceGroupName grupy \` zasobów \` .</span><span class="sxs-lookup"><span data-stu-id="00ea6-112">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="00ea6-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="00ea6-113">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | Get-AzureRmEventGridTopicKey
```

<span data-ttu-id="00ea6-114">Pobiera klucze dostępu współużytkowanego tematu siatki zdarzeń \` Temat1 \` w MyResourceGroupName grupy \` zasobów \` .</span><span class="sxs-lookup"><span data-stu-id="00ea6-114">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="00ea6-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="00ea6-115">PARAMETERS</span></span>

### <span data-ttu-id="00ea6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00ea6-116">-DefaultProfile</span></span>
<span data-ttu-id="00ea6-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="00ea6-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="00ea6-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="00ea6-118">-InputObject</span></span>
<span data-ttu-id="00ea6-119">Obiekt tematu EventGrid.</span><span class="sxs-lookup"><span data-stu-id="00ea6-119">EventGrid Topic object.</span></span>

```yaml
Type: PSTopic
Parameter Sets: TopicInputObjectParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00ea6-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="00ea6-120">-Name</span></span>
<span data-ttu-id="00ea6-121">Nazwa tematu EventGrid.</span><span class="sxs-lookup"><span data-stu-id="00ea6-121">EventGrid Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00ea6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00ea6-122">-ResourceGroupName</span></span>
<span data-ttu-id="00ea6-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="00ea6-123">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00ea6-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="00ea6-124">-ResourceId</span></span>
<span data-ttu-id="00ea6-125">Identyfikator zasobu reprezentujący temat siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="00ea6-125">Resource Identifier representing the Event Grid Topic.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00ea6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00ea6-126">CommonParameters</span></span>
<span data-ttu-id="00ea6-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00ea6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00ea6-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00ea6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00ea6-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="00ea6-129">INPUTS</span></span>

### <span data-ttu-id="00ea6-130">System. String</span><span class="sxs-lookup"><span data-stu-id="00ea6-130">System.String</span></span>

## <span data-ttu-id="00ea6-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="00ea6-131">OUTPUTS</span></span>

### <span data-ttu-id="00ea6-132">Microsoft. Azure. Management. EventGrid. MODELES. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="00ea6-132">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="00ea6-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="00ea6-133">NOTES</span></span>

## <span data-ttu-id="00ea6-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="00ea6-134">RELATED LINKS</span></span>

