---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
ms.openlocfilehash: cec41bda56da33f22def6c44752effb3d705b935
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717116"
---
# <span data-ttu-id="92a0f-101">Remove-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="92a0f-101">Remove-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="92a0f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="92a0f-102">SYNOPSIS</span></span>
<span data-ttu-id="92a0f-103">Usuwa określoną przestrzeń nazw koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="92a0f-103">Removes the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92a0f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="92a0f-104">SYNTAX</span></span>

```
Remove-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92a0f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="92a0f-105">DESCRIPTION</span></span>
<span data-ttu-id="92a0f-106">Polecenie cmdlet Remove-AzureRmEventHubNamespace powoduje usunięcie i usunięcie określonego obszaru nazw koncentratora zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="92a0f-106">The Remove-AzureRmEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="92a0f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="92a0f-107">EXAMPLES</span></span>

### <span data-ttu-id="92a0f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="92a0f-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="92a0f-109">Usuwa przestrzeń nazw Hub zdarzeń \` \` w MyResourceGroupName grupy zasobów \` \` .</span><span class="sxs-lookup"><span data-stu-id="92a0f-109">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="92a0f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="92a0f-110">PARAMETERS</span></span>

### <span data-ttu-id="92a0f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92a0f-111">-DefaultProfile</span></span>
<span data-ttu-id="92a0f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="92a0f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92a0f-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="92a0f-113">-Name</span></span>
<span data-ttu-id="92a0f-114">Nazwa obszaru nazw EventHub</span><span class="sxs-lookup"><span data-stu-id="92a0f-114">EventHub Namespace Name</span></span>

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

### <span data-ttu-id="92a0f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92a0f-115">-ResourceGroupName</span></span>
<span data-ttu-id="92a0f-116">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="92a0f-116">Resource Group Name</span></span>

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

### <span data-ttu-id="92a0f-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="92a0f-117">-Confirm</span></span>
<span data-ttu-id="92a0f-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92a0f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92a0f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92a0f-119">-WhatIf</span></span>
<span data-ttu-id="92a0f-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92a0f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92a0f-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="92a0f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92a0f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92a0f-122">CommonParameters</span></span>
<span data-ttu-id="92a0f-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92a0f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="92a0f-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92a0f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92a0f-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="92a0f-125">INPUTS</span></span>

### <span data-ttu-id="92a0f-126">System. String</span><span class="sxs-lookup"><span data-stu-id="92a0f-126">System.String</span></span>


## <span data-ttu-id="92a0f-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="92a0f-127">OUTPUTS</span></span>

### <span data-ttu-id="92a0f-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="92a0f-128">System.Object</span></span>

## <span data-ttu-id="92a0f-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="92a0f-129">NOTES</span></span>

## <span data-ttu-id="92a0f-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="92a0f-130">RELATED LINKS</span></span>
