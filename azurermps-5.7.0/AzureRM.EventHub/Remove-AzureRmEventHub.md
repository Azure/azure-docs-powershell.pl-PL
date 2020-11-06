---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
ms.openlocfilehash: b546c4f610bb6bc8021547fa5f7f0516ffbc2371
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554156"
---
# <span data-ttu-id="2531d-101">Remove-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="2531d-101">Remove-AzureRmEventHub</span></span>

## <span data-ttu-id="2531d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2531d-102">SYNOPSIS</span></span>
<span data-ttu-id="2531d-103">Umożliwia usunięcie określonego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="2531d-103">Removes the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2531d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2531d-104">SYNTAX</span></span>

```
Remove-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2531d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2531d-105">DESCRIPTION</span></span>
<span data-ttu-id="2531d-106">Polecenie cmdlet Remove-AzureRmEventHub powoduje usunięcie i usunięcie określonego centrum zdarzeń z danego obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="2531d-106">The Remove-AzureRmEventHub cmdlet removes and deletes the specified Event Hub from the given namespace.</span></span>

## <span data-ttu-id="2531d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2531d-107">EXAMPLES</span></span>

### <span data-ttu-id="2531d-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2531d-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="2531d-109">Usuwa MyEventHubName centrum zdarzeń \` \` .</span><span class="sxs-lookup"><span data-stu-id="2531d-109">Removes the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="2531d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2531d-110">PARAMETERS</span></span>

### <span data-ttu-id="2531d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2531d-111">-DefaultProfile</span></span>
<span data-ttu-id="2531d-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2531d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2531d-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2531d-113">-Name</span></span>
<span data-ttu-id="2531d-114">Nazwa EventHub</span><span class="sxs-lookup"><span data-stu-id="2531d-114">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2531d-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2531d-115">-Namespace</span></span>
<span data-ttu-id="2531d-116">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="2531d-116">Namespace Name</span></span>

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

### <span data-ttu-id="2531d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2531d-117">-ResourceGroupName</span></span>
<span data-ttu-id="2531d-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="2531d-118">Resource Group Name</span></span>

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

### <span data-ttu-id="2531d-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2531d-119">-Confirm</span></span>
<span data-ttu-id="2531d-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2531d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2531d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2531d-121">-WhatIf</span></span>
<span data-ttu-id="2531d-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2531d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2531d-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2531d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2531d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2531d-124">CommonParameters</span></span>
<span data-ttu-id="2531d-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2531d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2531d-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2531d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2531d-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2531d-127">INPUTS</span></span>

### <span data-ttu-id="2531d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="2531d-128">System.String</span></span>


## <span data-ttu-id="2531d-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2531d-129">OUTPUTS</span></span>

### <span data-ttu-id="2531d-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="2531d-130">System.Object</span></span>

## <span data-ttu-id="2531d-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2531d-131">NOTES</span></span>

## <span data-ttu-id="2531d-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2531d-132">RELATED LINKS</span></span>
