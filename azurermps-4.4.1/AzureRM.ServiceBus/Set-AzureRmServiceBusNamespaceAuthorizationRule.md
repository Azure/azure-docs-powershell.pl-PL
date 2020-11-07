---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespaceAuthorizationRule.md
ms.openlocfilehash: a56f9b27e19868d22eed94fbcf7717fbe1c68b39
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718986"
---
# <span data-ttu-id="a4401-101">Set-AzureRmServiceBusNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a4401-101">Set-AzureRmServiceBusNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="a4401-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a4401-102">SYNOPSIS</span></span>
<span data-ttu-id="a4401-103">Umożliwia zaktualizowanie określonego opisu reguły autoryzacji dla danego obszaru nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="a4401-103">Updates the specified authorization rule description for the given Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4401-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a4401-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusNamespaceAuthorizationRule [-ResourceGroup] <String> -Namespace <String>
 -InputObj <SharedAccessAuthorizationRuleAttributes> [-Name <String>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4401-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a4401-105">DESCRIPTION</span></span>
<span data-ttu-id="a4401-106">Polecenie cmdlet **Set-AzureRmServiceBusNamespaceAuthorizationRule** aktualizuje opis określonej reguły autoryzacji w danym obszarze nazw magistrali usług.</span><span class="sxs-lookup"><span data-stu-id="a4401-106">The **Set-AzureRmServiceBusNamespaceAuthorizationRule** cmdlet updates the description for the specified authorization rule in the given Service Bus namespace.</span></span>

## <span data-ttu-id="a4401-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a4401-107">EXAMPLES</span></span>

### <span data-ttu-id="a4401-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a4401-108">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthRuleObj $authRuleObj
```

<span data-ttu-id="a4401-109">Usuwa **Zarządzanie** z poziomu praw dostępu reguły autoryzacji `AuthoRule1` w obszarze nazw `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="a4401-109">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in namespace `SB-Example1`.</span></span>

## <span data-ttu-id="a4401-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a4401-110">PARAMETERS</span></span>

### <span data-ttu-id="a4401-111">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="a4401-111">-ResourceGroup</span></span>
<span data-ttu-id="a4401-112">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a4401-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="a4401-113">-Prawa</span><span class="sxs-lookup"><span data-stu-id="a4401-113">-Rights</span></span>
<span data-ttu-id="a4401-114">Intelektualn na przykład @ ("nasłuchuj", "Wyślij", "Zarządzaj").</span><span class="sxs-lookup"><span data-stu-id="a4401-114">Rights; for example @("Listen","Send","Manage").</span></span> <span data-ttu-id="a4401-115">Wymagany, jeśli nie podano **AuthruleObj** .</span><span class="sxs-lookup"><span data-stu-id="a4401-115">Required if **AuthruleObj** is not specified.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4401-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a4401-116">-Confirm</span></span>
<span data-ttu-id="a4401-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4401-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4401-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4401-118">-WhatIf</span></span>
<span data-ttu-id="a4401-119">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4401-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4401-120">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a4401-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4401-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4401-121">-DefaultProfile</span></span>
<span data-ttu-id="a4401-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a4401-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4401-123">-InputObj</span><span class="sxs-lookup"><span data-stu-id="a4401-123">-InputObj</span></span>
<span data-ttu-id="a4401-124">Obiekt AuthorizationRule ServiceBus NameSpace.</span><span class="sxs-lookup"><span data-stu-id="a4401-124">ServiceBus NameSpace AuthorizationRule Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: AuthRuleObj

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4401-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a4401-125">-Name</span></span>
<span data-ttu-id="a4401-126">AuthorizationRule nazwa — wymagane, jeśli nie podano parametru "AuthruleObj".</span><span class="sxs-lookup"><span data-stu-id="a4401-126">AuthorizationRule Name - Required if 'AuthruleObj' not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4401-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a4401-127">-Namespace</span></span>
<span data-ttu-id="a4401-128">Nazwa przestrzeni nazw ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="a4401-128">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="a4401-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4401-129">CommonParameters</span></span>
<span data-ttu-id="a4401-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4401-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4401-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4401-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4401-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a4401-132">INPUTS</span></span>

### <span data-ttu-id="a4401-133">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="a4401-133">-ResourceGroup</span></span>
 <span data-ttu-id="a4401-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a4401-134">System.String</span></span>

### <span data-ttu-id="a4401-135">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="a4401-135">-NamespaceName</span></span>
 <span data-ttu-id="a4401-136">System. String</span><span class="sxs-lookup"><span data-stu-id="a4401-136">System.String</span></span>

### <span data-ttu-id="a4401-137">-AuthRuleObj</span><span class="sxs-lookup"><span data-stu-id="a4401-137">-AuthRuleObj</span></span>
 <span data-ttu-id="a4401-138">Microsoft. Azure. Commands. ServiceBus. models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="a4401-138">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="a4401-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a4401-139">OUTPUTS</span></span>

### <span data-ttu-id="a4401-140">Microsoft. Azure. Commands. ServiceBus. models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="a4401-140">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="a4401-141">Identyfikator:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 typ: Microsoft. ServiceBus/AuthorizationRules Name: AuthoRule1 lokalizacja: Znaczniki: prawa: {Listen, Send}</span><span class="sxs-lookup"><span data-stu-id="a4401-141">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : AuthoRule1 Location : Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="a4401-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a4401-142">NOTES</span></span>

## <span data-ttu-id="a4401-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a4401-143">RELATED LINKS</span></span>

