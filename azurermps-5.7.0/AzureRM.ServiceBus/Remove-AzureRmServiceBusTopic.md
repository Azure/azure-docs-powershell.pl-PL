---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopic.md
ms.openlocfilehash: f2d295d31b0112a2adf73e2e4be064164df8fbb5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551572"
---
# <span data-ttu-id="77da1-101">Remove-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="77da1-101">Remove-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="77da1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="77da1-102">SYNOPSIS</span></span>
<span data-ttu-id="77da1-103">Usuwa temat z określonego obszaru nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="77da1-103">Removes the topic from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77da1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="77da1-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77da1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="77da1-105">DESCRIPTION</span></span>
<span data-ttu-id="77da1-106">Polecenie cmdlet **Remove-AzureRmServiceBusTopic** usuwa temat z określonego obszaru nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="77da1-106">The **Remove-AzureRmServiceBusTopic** cmdlet removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="77da1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="77da1-107">EXAMPLES</span></span>

### <span data-ttu-id="77da1-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="77da1-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="77da1-109">Usuwa temat `SB-Topic_exampl1` z obszaru nazw `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="77da1-109">Removes the topic `SB-Topic_exampl1` from the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="77da1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="77da1-110">PARAMETERS</span></span>

### <span data-ttu-id="77da1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77da1-111">-DefaultProfile</span></span>
<span data-ttu-id="77da1-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="77da1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77da1-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="77da1-113">-Name</span></span>
<span data-ttu-id="77da1-114">Nazwa tematu.</span><span class="sxs-lookup"><span data-stu-id="77da1-114">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77da1-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="77da1-115">-Namespace</span></span>
<span data-ttu-id="77da1-116">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="77da1-116">Namespace Name.</span></span>

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

### <span data-ttu-id="77da1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77da1-117">-ResourceGroupName</span></span>
<span data-ttu-id="77da1-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="77da1-118">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77da1-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="77da1-119">-Confirm</span></span>
<span data-ttu-id="77da1-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77da1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77da1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77da1-121">-WhatIf</span></span>
<span data-ttu-id="77da1-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77da1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77da1-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="77da1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77da1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77da1-124">CommonParameters</span></span>
<span data-ttu-id="77da1-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77da1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77da1-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77da1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77da1-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="77da1-127">INPUTS</span></span>

### <span data-ttu-id="77da1-128">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="77da1-128">-ResourceGroup</span></span>
 <span data-ttu-id="77da1-129">System. String</span><span class="sxs-lookup"><span data-stu-id="77da1-129">System.String</span></span>

### <span data-ttu-id="77da1-130">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="77da1-130">-NamespaceName</span></span>
 <span data-ttu-id="77da1-131">System. String</span><span class="sxs-lookup"><span data-stu-id="77da1-131">System.String</span></span>

### <span data-ttu-id="77da1-132">-Tematname</span><span class="sxs-lookup"><span data-stu-id="77da1-132">-TopicName</span></span>
 <span data-ttu-id="77da1-133">System. String</span><span class="sxs-lookup"><span data-stu-id="77da1-133">System.String</span></span>

## <span data-ttu-id="77da1-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="77da1-134">OUTPUTS</span></span>

### <span data-ttu-id="77da1-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="77da1-135">System.Object</span></span>

## <span data-ttu-id="77da1-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="77da1-136">NOTES</span></span>

## <span data-ttu-id="77da1-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="77da1-137">RELATED LINKS</span></span>

