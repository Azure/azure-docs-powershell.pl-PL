---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusRule.md
ms.openlocfilehash: 08f3fb2654d4c0b64900a4f15bbb7816e6d44c6f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547964"
---
# <span data-ttu-id="3c1e2-101">Remove-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="3c1e2-101">Remove-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="3c1e2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3c1e2-102">SYNOPSIS</span></span>
<span data-ttu-id="3c1e2-103">Usuwa regułę speficied danej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="3c1e2-103">Removes the speficied rule of a given subscription .</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c1e2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3c1e2-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c1e2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3c1e2-105">DESCRIPTION</span></span>
<span data-ttu-id="3c1e2-106">Polecenie cmdlet **Remove-AzureRmServiceBusRule** usuwa regułę abonamentu danego tematu.</span><span class="sxs-lookup"><span data-stu-id="3c1e2-106">The **Remove-AzureRmServiceBusRule** cmdlet removes the rule of a subscription of given topic.</span></span>

## <span data-ttu-id="3c1e2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3c1e2-107">EXAMPLES</span></span>

### <span data-ttu-id="3c1e2-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3c1e2-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="3c1e2-109">Usuwa regułę `SBRule` abonamentu `SBSubscription` określonego tematu `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="3c1e2-109">Removes the rule `SBRule` of subscription `SBSubscription` of specified topic `SBTopic`.</span></span>

## <span data-ttu-id="3c1e2-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3c1e2-110">PARAMETERS</span></span>

### <span data-ttu-id="3c1e2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c1e2-111">-DefaultProfile</span></span>
<span data-ttu-id="3c1e2-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3c1e2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c1e2-113">-Force</span><span class="sxs-lookup"><span data-stu-id="3c1e2-113">-Force</span></span>
<span data-ttu-id="3c1e2-114">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3c1e2-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="3c1e2-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3c1e2-115">-Name</span></span>
<span data-ttu-id="3c1e2-116">Nazwa reguły.</span><span class="sxs-lookup"><span data-stu-id="3c1e2-116">Rule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c1e2-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3c1e2-117">-Namespace</span></span>
<span data-ttu-id="3c1e2-118">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="3c1e2-118">Namespace Name.</span></span>

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

### <span data-ttu-id="3c1e2-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3c1e2-119">-PassThru</span></span>
<span data-ttu-id="3c1e2-120">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="3c1e2-120">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="3c1e2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c1e2-121">-ResourceGroupName</span></span>
<span data-ttu-id="3c1e2-122">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="3c1e2-122">The name of the resource group</span></span>

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

### <span data-ttu-id="3c1e2-123">-Subscription</span><span class="sxs-lookup"><span data-stu-id="3c1e2-123">-Subscription</span></span>
<span data-ttu-id="3c1e2-124">Nazwa subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="3c1e2-124">Subscription Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c1e2-125">— Temat</span><span class="sxs-lookup"><span data-stu-id="3c1e2-125">-Topic</span></span>
<span data-ttu-id="3c1e2-126">Nazwa tematu.</span><span class="sxs-lookup"><span data-stu-id="3c1e2-126">Topic Name.</span></span>

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

### <span data-ttu-id="3c1e2-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3c1e2-127">-Confirm</span></span>
<span data-ttu-id="3c1e2-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c1e2-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c1e2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c1e2-129">-WhatIf</span></span>
<span data-ttu-id="3c1e2-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c1e2-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c1e2-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3c1e2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c1e2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c1e2-132">CommonParameters</span></span>
<span data-ttu-id="3c1e2-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c1e2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c1e2-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c1e2-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c1e2-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3c1e2-135">INPUTS</span></span>

### <span data-ttu-id="3c1e2-136">System. String</span><span class="sxs-lookup"><span data-stu-id="3c1e2-136">System.String</span></span>

## <span data-ttu-id="3c1e2-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3c1e2-137">OUTPUTS</span></span>

### <span data-ttu-id="3c1e2-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3c1e2-138">System.Boolean</span></span>

## <span data-ttu-id="3c1e2-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3c1e2-139">NOTES</span></span>

## <span data-ttu-id="3c1e2-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3c1e2-140">RELATED LINKS</span></span>

