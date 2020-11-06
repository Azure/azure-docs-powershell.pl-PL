---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopicAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopicAuthorizationRule.md
ms.openlocfilehash: 5694d46e44931d59f79a5ac7b86ceabf7632f945
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553108"
---
# <span data-ttu-id="f24cd-101">Remove-AzureRmServiceBusTopicAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f24cd-101">Remove-AzureRmServiceBusTopicAuthorizationRule</span></span>

## <span data-ttu-id="f24cd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f24cd-102">SYNOPSIS</span></span>
<span data-ttu-id="f24cd-103">Usuwa regułę autoryzacji tematu z określonego obszaru nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="f24cd-103">Removes the authorization rule of a topic from the specified Service Bus Namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f24cd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f24cd-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusTopicAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Topic <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f24cd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f24cd-105">DESCRIPTION</span></span>
<span data-ttu-id="f24cd-106">Polecenie cmdlet **Remove-AzureRmServiceBusTopicAuthorizationRule** usuwa regułę autoryzacji tematu z określonego obszaru nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="f24cd-106">The **Remove-AzureRmServiceBusTopicAuthorizationRule** cmdlet removes the authorization rule of a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="f24cd-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f24cd-107">EXAMPLES</span></span>

### <span data-ttu-id="f24cd-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f24cd-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusTopicAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1
```

<span data-ttu-id="f24cd-109">Usuwa regułę autoryzacji `SBTopicAuthoRule1` tematu `SB-Topic_exampl1` z obszaru nazw `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="f24cd-109">Removes the authorization rule `SBTopicAuthoRule1` of the topic `SB-Topic_exampl1` from the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="f24cd-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f24cd-110">PARAMETERS</span></span>

### <span data-ttu-id="f24cd-111">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="f24cd-111">-ResourceGroup</span></span>
<span data-ttu-id="f24cd-112">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f24cd-112">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f24cd-113">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f24cd-113">-Confirm</span></span>
<span data-ttu-id="f24cd-114">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f24cd-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f24cd-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f24cd-115">-WhatIf</span></span>
<span data-ttu-id="f24cd-116">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f24cd-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f24cd-117">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f24cd-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f24cd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f24cd-118">-DefaultProfile</span></span>
<span data-ttu-id="f24cd-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f24cd-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f24cd-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f24cd-120">-Name</span></span>
<span data-ttu-id="f24cd-121">Temat AuthorizationRule nazwa.</span><span class="sxs-lookup"><span data-stu-id="f24cd-121">Topic AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f24cd-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f24cd-122">-Namespace</span></span>
<span data-ttu-id="f24cd-123">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="f24cd-123">Namespace Name.</span></span>

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

### <span data-ttu-id="f24cd-124">— Temat</span><span class="sxs-lookup"><span data-stu-id="f24cd-124">-Topic</span></span>
<span data-ttu-id="f24cd-125">Nazwa tematu.</span><span class="sxs-lookup"><span data-stu-id="f24cd-125">Topic Name.</span></span>

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

### <span data-ttu-id="f24cd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f24cd-126">CommonParameters</span></span>
<span data-ttu-id="f24cd-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f24cd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f24cd-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f24cd-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f24cd-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f24cd-129">INPUTS</span></span>

### <span data-ttu-id="f24cd-130">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="f24cd-130">-ResourceGroup</span></span>
 <span data-ttu-id="f24cd-131">System. String</span><span class="sxs-lookup"><span data-stu-id="f24cd-131">System.String</span></span>

### <span data-ttu-id="f24cd-132">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="f24cd-132">-NamespaceName</span></span>
 <span data-ttu-id="f24cd-133">System. String</span><span class="sxs-lookup"><span data-stu-id="f24cd-133">System.String</span></span>

### <span data-ttu-id="f24cd-134">-Tematname</span><span class="sxs-lookup"><span data-stu-id="f24cd-134">-TopicName</span></span>
 <span data-ttu-id="f24cd-135">System. String</span><span class="sxs-lookup"><span data-stu-id="f24cd-135">System.String</span></span>

### <span data-ttu-id="f24cd-136">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="f24cd-136">-AuthorizationRuleName</span></span>
 <span data-ttu-id="f24cd-137">System. String</span><span class="sxs-lookup"><span data-stu-id="f24cd-137">System.String</span></span>

## <span data-ttu-id="f24cd-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f24cd-138">OUTPUTS</span></span>

### <span data-ttu-id="f24cd-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="f24cd-139">System.Object</span></span>

## <span data-ttu-id="f24cd-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f24cd-140">NOTES</span></span>

## <span data-ttu-id="f24cd-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f24cd-141">RELATED LINKS</span></span>

