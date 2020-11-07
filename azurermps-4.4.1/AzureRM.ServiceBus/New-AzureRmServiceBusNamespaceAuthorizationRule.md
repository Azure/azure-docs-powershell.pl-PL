---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespaceAuthorizationRule.md
ms.openlocfilehash: 6e20ceb2a6809e1e6010263563006468753cd41c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718698"
---
# <span data-ttu-id="0400a-101">New-AzureRmServiceBusNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="0400a-101">New-AzureRmServiceBusNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="0400a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0400a-102">SYNOPSIS</span></span>
<span data-ttu-id="0400a-103">Tworzy nową regułę autoryzacji dla określonego obszaru nazw magistrali usług.</span><span class="sxs-lookup"><span data-stu-id="0400a-103">Creates a new authorization rule for the specified Service Bus namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0400a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0400a-104">SYNTAX</span></span>

```
New-AzureRmServiceBusNamespaceAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Name <String>
 [-Rights] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0400a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0400a-105">DESCRIPTION</span></span>
<span data-ttu-id="0400a-106">Polecenie cmdlet **New-AzureRmServiceBusNamespaceAuthorizationRule** tworzy nową regułę autoryzacji dla określonego obszaru nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="0400a-106">The **New-AzureRmServiceBusNamespaceAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus namespace.</span></span>

## <span data-ttu-id="0400a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0400a-107">EXAMPLES</span></span>

### <span data-ttu-id="0400a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0400a-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="0400a-109">Tworzy `AuthoRule1` za pomocą **odsłuchiwania** i **wysyłania** praw do obszaru nazw `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="0400a-109">Creates `AuthoRule1` with **Listen** and **Send** rights for the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="0400a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0400a-110">PARAMETERS</span></span>

### <span data-ttu-id="0400a-111">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="0400a-111">-ResourceGroup</span></span>
<span data-ttu-id="0400a-112">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0400a-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="0400a-113">-Prawa</span><span class="sxs-lookup"><span data-stu-id="0400a-113">-Rights</span></span>
<span data-ttu-id="0400a-114">Prawa; na przykład @ ("nasłuchuj"; "Wyślij"; "Zarządzaj")</span><span class="sxs-lookup"><span data-stu-id="0400a-114">The Rights; for example, @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0400a-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0400a-115">-Confirm</span></span>
<span data-ttu-id="0400a-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0400a-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0400a-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0400a-117">-WhatIf</span></span>
<span data-ttu-id="0400a-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0400a-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0400a-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0400a-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0400a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0400a-120">-DefaultProfile</span></span>
<span data-ttu-id="0400a-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0400a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0400a-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0400a-122">-Name</span></span>
<span data-ttu-id="0400a-123">Nazwa AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="0400a-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="0400a-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0400a-124">-Namespace</span></span>
<span data-ttu-id="0400a-125">Nazwa przestrzeni nazw ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="0400a-125">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="0400a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0400a-126">CommonParameters</span></span>
<span data-ttu-id="0400a-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0400a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0400a-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0400a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0400a-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0400a-129">INPUTS</span></span>

### <span data-ttu-id="0400a-130">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="0400a-130">-ResourceGroup</span></span>
 <span data-ttu-id="0400a-131">System. String</span><span class="sxs-lookup"><span data-stu-id="0400a-131">System.String</span></span>
 

### <span data-ttu-id="0400a-132">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="0400a-132">-NamespaceName</span></span>
 <span data-ttu-id="0400a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0400a-133">System.String</span></span>
 

### <span data-ttu-id="0400a-134">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="0400a-134">-AuthorizationRuleName</span></span>
 <span data-ttu-id="0400a-135">System. String</span><span class="sxs-lookup"><span data-stu-id="0400a-135">System.String</span></span>
 

### <span data-ttu-id="0400a-136">-Prawa</span><span class="sxs-lookup"><span data-stu-id="0400a-136">-Rights</span></span>
 <span data-ttu-id="0400a-137">System. String []</span><span class="sxs-lookup"><span data-stu-id="0400a-137">System.String []</span></span>

## <span data-ttu-id="0400a-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0400a-138">OUTPUTS</span></span>

### <span data-ttu-id="0400a-139">Microsoft. Azure. Commands. ServiceBus. models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="0400a-139">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="0400a-140">Identyfikator:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 typ: Microsoft. ServiceBus/AuthorizationRules Name: AuthoRule1 lokalizacja: Znaczniki: prawa: {Listen, Send}</span><span class="sxs-lookup"><span data-stu-id="0400a-140">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : AuthoRule1 Location : Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="0400a-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0400a-141">NOTES</span></span>

## <span data-ttu-id="0400a-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0400a-142">RELATED LINKS</span></span>

