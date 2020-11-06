---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
ms.openlocfilehash: 2d944b629a72a8b97bf1bd639ced79d9bd1eab02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549007"
---
# <span data-ttu-id="06bf5-101">New-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="06bf5-101">New-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="06bf5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="06bf5-102">SYNOPSIS</span></span>
<span data-ttu-id="06bf5-103">Tworzy obszar nazw koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="06bf5-103">Creates an Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06bf5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="06bf5-104">SYNTAX</span></span>

### <span data-ttu-id="06bf5-105">NamespaceParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="06bf5-105">NamespaceParameterSet (Default)</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06bf5-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="06bf5-106">AutoInflateParameterSet</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="06bf5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="06bf5-107">DESCRIPTION</span></span>
<span data-ttu-id="06bf5-108">Polecenie cmdlet New-AzureRmEventHubNamespace tworzy nowy obszar nazw dla koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="06bf5-108">The New-AzureRmEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="06bf5-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="06bf5-109">EXAMPLES</span></span>

### <span data-ttu-id="06bf5-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="06bf5-110">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation
```

<span data-ttu-id="06bf5-111">Tworzy obszar nazw koncentratorów zdarzeń \` \` w określonej lokalizacji geograficznej moja \` Lokalizacja \` w obszarze MyResourceGroupName grupy zasobów \` \` .</span><span class="sxs-lookup"><span data-stu-id="06bf5-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="06bf5-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="06bf5-112">Example 2</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="06bf5-113">Tworzy obszar nazw koncentratorów zdarzeń \` \` w określonej lokalizacji geograficznej moja \` Lokalizacja \` , w grupie zasoby \` MyResourceGroupName \` i funkcja autorozdęcie jest włączona z MaximumThroughputUnits 10.</span><span class="sxs-lookup"><span data-stu-id="06bf5-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

## <span data-ttu-id="06bf5-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="06bf5-114">PARAMETERS</span></span>

### <span data-ttu-id="06bf5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06bf5-115">-DefaultProfile</span></span>
<span data-ttu-id="06bf5-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="06bf5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06bf5-117">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="06bf5-117">-EnableAutoInflate</span></span>
<span data-ttu-id="06bf5-118">Wskazuje, czy funkcja autorozdęcie jest włączona</span><span class="sxs-lookup"><span data-stu-id="06bf5-118">Indicates whether AutoInflate is enabled</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06bf5-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="06bf5-119">-Location</span></span>
<span data-ttu-id="06bf5-120">Lokalizacja obszaru nazw EventHub.</span><span class="sxs-lookup"><span data-stu-id="06bf5-120">EventHub Namespace Location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06bf5-121">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="06bf5-121">-MaximumThroughputUnits</span></span>
<span data-ttu-id="06bf5-122">Górny limit jednostek przepływności, gdy funkcja podwyższanie jest włączona, wartość powinna należeć do zakresu od 0 do 20 jednostek przepływności.</span><span class="sxs-lookup"><span data-stu-id="06bf5-122">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

```yaml
Type: Int32
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06bf5-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="06bf5-123">-Name</span></span>
<span data-ttu-id="06bf5-124">Nazwa obszaru nazw EventHub.</span><span class="sxs-lookup"><span data-stu-id="06bf5-124">EventHub Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06bf5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06bf5-125">-ResourceGroupName</span></span>
<span data-ttu-id="06bf5-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="06bf5-126">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06bf5-127">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="06bf5-127">-SkuCapacity</span></span>
<span data-ttu-id="06bf5-128">Jednostki przepływności eventhub.</span><span class="sxs-lookup"><span data-stu-id="06bf5-128">The eventhub throughput units.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06bf5-129">-SkuName</span><span class="sxs-lookup"><span data-stu-id="06bf5-129">-SkuName</span></span>
<span data-ttu-id="06bf5-130">Nazwa SKU obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="06bf5-130">Namespace Sku Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06bf5-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="06bf5-131">-Tag</span></span>
<span data-ttu-id="06bf5-132">Hashtable, które reprezentują znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="06bf5-132">Hashtables which represents resource Tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06bf5-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="06bf5-133">-Confirm</span></span>
<span data-ttu-id="06bf5-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06bf5-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06bf5-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06bf5-135">-WhatIf</span></span>
<span data-ttu-id="06bf5-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06bf5-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06bf5-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="06bf5-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06bf5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06bf5-138">CommonParameters</span></span>
<span data-ttu-id="06bf5-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06bf5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="06bf5-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06bf5-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06bf5-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="06bf5-141">INPUTS</span></span>

### <span data-ttu-id="06bf5-142">System. String</span><span class="sxs-lookup"><span data-stu-id="06bf5-142">System.String</span></span>
<span data-ttu-id="06bf5-143">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]] system. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="06bf5-143">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.Collections.Hashtable</span></span>


## <span data-ttu-id="06bf5-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="06bf5-144">OUTPUTS</span></span>

### <span data-ttu-id="06bf5-145">Microsoft. Azure. Commands. EventHub. modele. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="06bf5-145">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>


## <span data-ttu-id="06bf5-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="06bf5-146">NOTES</span></span>

## <span data-ttu-id="06bf5-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="06bf5-147">RELATED LINKS</span></span>
