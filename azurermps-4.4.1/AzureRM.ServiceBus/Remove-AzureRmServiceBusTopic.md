---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopic.md
ms.openlocfilehash: 356140c964280634f469dd9b9955adaf62130090
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527274"
---
# <span data-ttu-id="3dacc-101">Remove-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="3dacc-101">Remove-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="3dacc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3dacc-102">SYNOPSIS</span></span>
<span data-ttu-id="3dacc-103">Usuwa temat z określonego obszaru nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="3dacc-103">Removes the topic from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3dacc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3dacc-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusTopic -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3dacc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3dacc-105">DESCRIPTION</span></span>
<span data-ttu-id="3dacc-106">Polecenie cmdlet **Remove-AzureRmServiceBusTopic** usuwa temat z określonego obszaru nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="3dacc-106">The **Remove-AzureRmServiceBusTopic** cmdlet removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="3dacc-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3dacc-107">EXAMPLES</span></span>

### <span data-ttu-id="3dacc-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3dacc-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="3dacc-109">Usuwa temat `SB-Topic_exampl1` z obszaru nazw `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="3dacc-109">Removes the topic `SB-Topic_exampl1` from the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="3dacc-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3dacc-110">PARAMETERS</span></span>

### <span data-ttu-id="3dacc-111">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3dacc-111">-Confirm</span></span>
<span data-ttu-id="3dacc-112">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3dacc-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dacc-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dacc-113">-WhatIf</span></span>
<span data-ttu-id="3dacc-114">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3dacc-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3dacc-115">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3dacc-115">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dacc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dacc-116">-DefaultProfile</span></span>
<span data-ttu-id="3dacc-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3dacc-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3dacc-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3dacc-118">-Name</span></span>
<span data-ttu-id="3dacc-119">Nazwa tematu.</span><span class="sxs-lookup"><span data-stu-id="3dacc-119">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dacc-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3dacc-120">-Namespace</span></span>
<span data-ttu-id="3dacc-121">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="3dacc-121">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dacc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3dacc-122">-ResourceGroupName</span></span>
<span data-ttu-id="3dacc-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="3dacc-123">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dacc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dacc-124">CommonParameters</span></span>
<span data-ttu-id="3dacc-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dacc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dacc-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3dacc-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dacc-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3dacc-127">INPUTS</span></span>

### <span data-ttu-id="3dacc-128">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="3dacc-128">-ResourceGroup</span></span>
 <span data-ttu-id="3dacc-129">System. String</span><span class="sxs-lookup"><span data-stu-id="3dacc-129">System.String</span></span>

### <span data-ttu-id="3dacc-130">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="3dacc-130">-NamespaceName</span></span>
 <span data-ttu-id="3dacc-131">System. String</span><span class="sxs-lookup"><span data-stu-id="3dacc-131">System.String</span></span>

### <span data-ttu-id="3dacc-132">-Tematname</span><span class="sxs-lookup"><span data-stu-id="3dacc-132">-TopicName</span></span>
 <span data-ttu-id="3dacc-133">System. String</span><span class="sxs-lookup"><span data-stu-id="3dacc-133">System.String</span></span>

## <span data-ttu-id="3dacc-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3dacc-134">OUTPUTS</span></span>

### <span data-ttu-id="3dacc-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="3dacc-135">System.Object</span></span>

## <span data-ttu-id="3dacc-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3dacc-136">NOTES</span></span>

## <span data-ttu-id="3dacc-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3dacc-137">RELATED LINKS</span></span>

