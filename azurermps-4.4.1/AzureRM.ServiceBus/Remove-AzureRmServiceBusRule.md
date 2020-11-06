---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusRule.md
ms.openlocfilehash: 287a0b82c9236841b613ac52a7a07ccf8adb4811
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542952"
---
# <span data-ttu-id="037c6-101">Remove-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="037c6-101">Remove-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="037c6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="037c6-102">SYNOPSIS</span></span>
<span data-ttu-id="037c6-103">Usuwa regułę speficied danej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="037c6-103">Removes the speficied rule of a given subscription .</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="037c6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="037c6-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="037c6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="037c6-105">DESCRIPTION</span></span>
<span data-ttu-id="037c6-106">Polecenie cmdlet **Remove-AzureRmServiceBusRule** usuwa regułę abonamentu danego tematu.</span><span class="sxs-lookup"><span data-stu-id="037c6-106">The **Remove-AzureRmServiceBusRule** cmdlet removes the rule of a subscription of given topic.</span></span>

## <span data-ttu-id="037c6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="037c6-107">EXAMPLES</span></span>

### <span data-ttu-id="037c6-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="037c6-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="037c6-109">Usuwa regułę `SBRule` abonamentu `SBSubscription` określonego tematu `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="037c6-109">Removes the rule `SBRule` of subscription `SBSubscription` of specified topic `SBTopic`.</span></span>

## <span data-ttu-id="037c6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="037c6-110">PARAMETERS</span></span>

### <span data-ttu-id="037c6-111">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="037c6-111">-Confirm</span></span>
<span data-ttu-id="037c6-112">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="037c6-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="037c6-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="037c6-113">-Name</span></span>
<span data-ttu-id="037c6-114">Nazwa reguły.</span><span class="sxs-lookup"><span data-stu-id="037c6-114">Rule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="037c6-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="037c6-115">-Namespace</span></span>
<span data-ttu-id="037c6-116">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="037c6-116">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="037c6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="037c6-117">-ResourceGroupName</span></span>
<span data-ttu-id="037c6-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="037c6-118">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="037c6-119">-Subscription</span><span class="sxs-lookup"><span data-stu-id="037c6-119">-Subscription</span></span>
<span data-ttu-id="037c6-120">Nazwa subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="037c6-120">Subscription Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="037c6-121">— Temat</span><span class="sxs-lookup"><span data-stu-id="037c6-121">-Topic</span></span>
<span data-ttu-id="037c6-122">Nazwa tematu.</span><span class="sxs-lookup"><span data-stu-id="037c6-122">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="037c6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="037c6-123">-WhatIf</span></span>
<span data-ttu-id="037c6-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="037c6-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="037c6-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="037c6-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="037c6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="037c6-126">-DefaultProfile</span></span>
<span data-ttu-id="037c6-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="037c6-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="037c6-128">-Force</span><span class="sxs-lookup"><span data-stu-id="037c6-128">-Force</span></span>
<span data-ttu-id="037c6-129">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="037c6-129">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="037c6-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="037c6-130">-PassThru</span></span>
<span data-ttu-id="037c6-131">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="037c6-131">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="037c6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="037c6-132">CommonParameters</span></span>
<span data-ttu-id="037c6-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="037c6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="037c6-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="037c6-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="037c6-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="037c6-135">INPUTS</span></span>

### <span data-ttu-id="037c6-136">System. String</span><span class="sxs-lookup"><span data-stu-id="037c6-136">System.String</span></span>

## <span data-ttu-id="037c6-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="037c6-137">OUTPUTS</span></span>

### <span data-ttu-id="037c6-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="037c6-138">System.Boolean</span></span>

## <span data-ttu-id="037c6-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="037c6-139">NOTES</span></span>

## <span data-ttu-id="037c6-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="037c6-140">RELATED LINKS</span></span>

