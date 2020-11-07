---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/get-azurermeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicKey.md
ms.openlocfilehash: 8bd28b3bbe043663a451b235abf46c3a42e235e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719132"
---
# <span data-ttu-id="2e50d-101">Get-AzureRmEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="2e50d-101">Get-AzureRmEventGridTopicKey</span></span>

## <span data-ttu-id="2e50d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2e50d-102">SYNOPSIS</span></span>
<span data-ttu-id="2e50d-103">Pobiera klucze dostępu współużytkowanego używane do publikowania zdarzeń w temacie dotyczącym siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="2e50d-103">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e50d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2e50d-104">SYNTAX</span></span>

### <span data-ttu-id="2e50d-105">TopicNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2e50d-105">TopicNameParameterSet (Default)</span></span>
```
Get-AzureRmEventGridTopicKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e50d-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e50d-106">TopicInputObjectParameterSet</span></span>
```
Get-AzureRmEventGridTopicKey [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2e50d-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e50d-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzureRmEventGridTopicKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2e50d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2e50d-108">DESCRIPTION</span></span>
<span data-ttu-id="2e50d-109">Pobiera klucze dostępu współużytkowanego używane do publikowania zdarzeń w temacie dotyczącym siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="2e50d-109">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="2e50d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2e50d-110">EXAMPLES</span></span>

### <span data-ttu-id="2e50d-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2e50d-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridTopicKey -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="2e50d-112">Pobiera klucze dostępu współużytkowanego tematu siatki zdarzeń \` Temat1 \` w MyResourceGroupName grupy \` zasobów \` .</span><span class="sxs-lookup"><span data-stu-id="2e50d-112">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="2e50d-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="2e50d-113">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | Get-AzureRmEventGridTopicKey
```

<span data-ttu-id="2e50d-114">Pobiera klucze dostępu współużytkowanego tematu siatki zdarzeń \` Temat1 \` w MyResourceGroupName grupy \` zasobów \` .</span><span class="sxs-lookup"><span data-stu-id="2e50d-114">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="2e50d-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2e50d-115">PARAMETERS</span></span>

### <span data-ttu-id="2e50d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e50d-116">-DefaultProfile</span></span>
<span data-ttu-id="2e50d-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="2e50d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2e50d-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2e50d-118">-InputObject</span></span>
<span data-ttu-id="2e50d-119">Obiekt tematu EventGrid.</span><span class="sxs-lookup"><span data-stu-id="2e50d-119">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e50d-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2e50d-120">-Name</span></span>
<span data-ttu-id="2e50d-121">Nazwa tematu EventGrid.</span><span class="sxs-lookup"><span data-stu-id="2e50d-121">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e50d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e50d-122">-ResourceGroupName</span></span>
<span data-ttu-id="2e50d-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2e50d-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e50d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e50d-124">-ResourceId</span></span>
<span data-ttu-id="2e50d-125">Identyfikator zasobu reprezentujący temat siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="2e50d-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="2e50d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e50d-126">CommonParameters</span></span>
<span data-ttu-id="2e50d-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e50d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e50d-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e50d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e50d-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2e50d-129">INPUTS</span></span>

### <span data-ttu-id="2e50d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2e50d-130">System.String</span></span>

### <span data-ttu-id="2e50d-131">Microsoft. Azure. Commands. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="2e50d-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>
<span data-ttu-id="2e50d-132">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2e50d-132">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="2e50d-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2e50d-133">OUTPUTS</span></span>

### <span data-ttu-id="2e50d-134">Microsoft. Azure. Management. EventGrid. MODELES. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="2e50d-134">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="2e50d-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2e50d-135">NOTES</span></span>

## <span data-ttu-id="2e50d-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2e50d-136">RELATED LINKS</span></span>
