---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespaceAuthorizationRule.md
ms.openlocfilehash: 08f7f33138ddf9d5226cfc93f263fdec65de3388
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542971"
---
# <span data-ttu-id="89f89-101">Remove-AzureRmServiceBusNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="89f89-101">Remove-AzureRmServiceBusNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="89f89-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="89f89-102">SYNOPSIS</span></span>
<span data-ttu-id="89f89-103">Usuwa regułę autoryzacji obszaru nazw magistrali usług z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="89f89-103">Removes the authorization rule of a Service Bus namespace from the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89f89-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="89f89-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroupName <String> -Namespace <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89f89-105">Opis</span><span class="sxs-lookup"><span data-stu-id="89f89-105">DESCRIPTION</span></span>
<span data-ttu-id="89f89-106">Polecenie cmdlet **Remove-AzureRmServiceBusNamespaceAuthorizationRule** usuwa regułę autoryzacji obszaru nazw magistrali usług dla określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="89f89-106">The **Remove-AzureRmServiceBusNamespaceAuthorizationRule** cmdlet removes the authorization rule of a Service Bus namespace for the specified resource group.</span></span>

## <span data-ttu-id="89f89-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="89f89-107">EXAMPLES</span></span>

### <span data-ttu-id="89f89-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="89f89-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1
```

<span data-ttu-id="89f89-109">Usuwa regułę autoryzacji `SBAuthoRule1` obszaru nazw `SB-Example1` z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="89f89-109">Removes the authorization rule `SBAuthoRule1` of namespace `SB-Example1` from the specified resource group.</span></span>

## <span data-ttu-id="89f89-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="89f89-110">PARAMETERS</span></span>

### <span data-ttu-id="89f89-111">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="89f89-111">-Confirm</span></span>
<span data-ttu-id="89f89-112">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89f89-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89f89-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89f89-113">-WhatIf</span></span>
<span data-ttu-id="89f89-114">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89f89-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89f89-115">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="89f89-115">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89f89-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89f89-116">-DefaultProfile</span></span>
<span data-ttu-id="89f89-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="89f89-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89f89-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="89f89-118">-Name</span></span>
<span data-ttu-id="89f89-119">Nazwa AuthorizationRule obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="89f89-119">Namespace AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="89f89-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="89f89-120">-Namespace</span></span>
<span data-ttu-id="89f89-121">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="89f89-121">Namespace Name.</span></span>

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

### <span data-ttu-id="89f89-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89f89-122">-ResourceGroupName</span></span>
<span data-ttu-id="89f89-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="89f89-123">The name of the resource group</span></span>

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

### <span data-ttu-id="89f89-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89f89-124">CommonParameters</span></span>
<span data-ttu-id="89f89-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89f89-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89f89-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89f89-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89f89-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="89f89-127">INPUTS</span></span>

### <span data-ttu-id="89f89-128">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="89f89-128">-ResourceGroup</span></span>
 <span data-ttu-id="89f89-129">System. String</span><span class="sxs-lookup"><span data-stu-id="89f89-129">System.String</span></span>

### <span data-ttu-id="89f89-130">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="89f89-130">-NamespaceName</span></span>
 <span data-ttu-id="89f89-131">System. String</span><span class="sxs-lookup"><span data-stu-id="89f89-131">System.String</span></span>

### <span data-ttu-id="89f89-132">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="89f89-132">-AuthorizationRuleName</span></span>
 <span data-ttu-id="89f89-133">System. String</span><span class="sxs-lookup"><span data-stu-id="89f89-133">System.String</span></span>

## <span data-ttu-id="89f89-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="89f89-134">OUTPUTS</span></span>

### <span data-ttu-id="89f89-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="89f89-135">System.Boolean</span></span>

## <span data-ttu-id="89f89-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="89f89-136">NOTES</span></span>

## <span data-ttu-id="89f89-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="89f89-137">RELATED LINKS</span></span>

