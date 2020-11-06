---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 510b6bfcaf49d406a7be2f6e4f53b2227469566d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542967"
---
# <span data-ttu-id="83e1c-101">Remove-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="83e1c-101">Remove-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="83e1c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="83e1c-102">SYNOPSIS</span></span>
<span data-ttu-id="83e1c-103">Usuwa obszar nazw z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="83e1c-103">Removes the namespace from the specified resource group.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83e1c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="83e1c-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusNamespace [-ResourceGroup] <String> [-NamespaceName] <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="83e1c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="83e1c-105">DESCRIPTION</span></span>
<span data-ttu-id="83e1c-106">Polecenie cmdlet **Remove-AzureRmServiceBusNamespace** usuwa obszar nazw z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="83e1c-106">The **Remove-AzureRmServiceBusNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="83e1c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="83e1c-107">EXAMPLES</span></span>

### <span data-ttu-id="83e1c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="83e1c-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="83e1c-109">Usuwa obszar nazw usługi Service Bus `SB-Example1` z określonej grupy zasobów `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="83e1c-109">Removes the Service Bus namespace `SB-Example1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="83e1c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="83e1c-110">PARAMETERS</span></span>

### <span data-ttu-id="83e1c-111">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="83e1c-111">-NamespaceName</span></span>
<span data-ttu-id="83e1c-112">Nazwa obszaru nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="83e1c-112">The Service Bus namespace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83e1c-113">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="83e1c-113">-ResourceGroup</span></span>
<span data-ttu-id="83e1c-114">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="83e1c-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="83e1c-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="83e1c-115">-Confirm</span></span>
<span data-ttu-id="83e1c-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83e1c-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83e1c-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83e1c-117">-WhatIf</span></span>
<span data-ttu-id="83e1c-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83e1c-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83e1c-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="83e1c-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83e1c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83e1c-120">CommonParameters</span></span>
<span data-ttu-id="83e1c-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83e1c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83e1c-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83e1c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83e1c-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="83e1c-123">INPUTS</span></span>

### <span data-ttu-id="83e1c-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="83e1c-124">-ResourceGroup</span></span>
 <span data-ttu-id="83e1c-125">System. String</span><span class="sxs-lookup"><span data-stu-id="83e1c-125">System.String</span></span>

### <span data-ttu-id="83e1c-126">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="83e1c-126">-NamespaceName</span></span>
 <span data-ttu-id="83e1c-127">System. String</span><span class="sxs-lookup"><span data-stu-id="83e1c-127">System.String</span></span>

## <span data-ttu-id="83e1c-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="83e1c-128">OUTPUTS</span></span>

### <span data-ttu-id="83e1c-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="83e1c-129">System.Object</span></span>

## <span data-ttu-id="83e1c-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="83e1c-130">NOTES</span></span>

## <span data-ttu-id="83e1c-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="83e1c-131">RELATED LINKS</span></span>

