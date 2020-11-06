---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespaceAuthorizationRule.md
ms.openlocfilehash: 70b58b53b8e1ef88c59983b9da134a0fb935bcd2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546015"
---
# <span data-ttu-id="f2954-101">Get-AzureRmServiceBusNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f2954-101">Get-AzureRmServiceBusNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="f2954-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f2954-102">SYNOPSIS</span></span>
<span data-ttu-id="f2954-103">Pobiera opis określonej reguły autoryzacji dla danego obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="f2954-103">Gets a description of the specified authorization rule for a given namespace.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2954-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f2954-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusNamespaceAuthorizationRule [-ResourceGroup] <String> -Namespace <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2954-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f2954-105">DESCRIPTION</span></span>
<span data-ttu-id="f2954-106">Polecenie cmdlet **Get-AzureRmServiceBusNamespaceAuthorizationRule** Pobiera opis określonej reguły autoryzacji w danym obszarze nazw.</span><span class="sxs-lookup"><span data-stu-id="f2954-106">The **Get-AzureRmServiceBusNamespaceAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given namespace.</span></span>

## <span data-ttu-id="f2954-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f2954-107">EXAMPLES</span></span>

### <span data-ttu-id="f2954-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f2954-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1
```

<span data-ttu-id="f2954-109">Zwraca opis określonej reguły autoryzacji dla określonego obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="f2954-109">Returns the specified authorization rule description for a specified namespace.</span></span>

## <span data-ttu-id="f2954-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f2954-110">PARAMETERS</span></span>

### <span data-ttu-id="f2954-111">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="f2954-111">-ResourceGroup</span></span>
<span data-ttu-id="f2954-112">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f2954-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="f2954-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2954-113">-DefaultProfile</span></span>
<span data-ttu-id="f2954-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f2954-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2954-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f2954-115">-Name</span></span>
<span data-ttu-id="f2954-116">ServiceBus przestrzeń nazw AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="f2954-116">ServiceBus Namespace AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="f2954-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f2954-117">-Namespace</span></span>
<span data-ttu-id="f2954-118">Nazwa przestrzeni nazw ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="f2954-118">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="f2954-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2954-119">CommonParameters</span></span>
<span data-ttu-id="f2954-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2954-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2954-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2954-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2954-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f2954-122">INPUTS</span></span>

### <span data-ttu-id="f2954-123">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="f2954-123">-ResourceGroup</span></span>
 <span data-ttu-id="f2954-124">System. String</span><span class="sxs-lookup"><span data-stu-id="f2954-124">System.String</span></span>
 

### <span data-ttu-id="f2954-125">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="f2954-125">-NamespaceName</span></span>
 <span data-ttu-id="f2954-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f2954-126">System.String</span></span>
 

### <span data-ttu-id="f2954-127">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="f2954-127">-AuthorizationRuleName</span></span>
 <span data-ttu-id="f2954-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f2954-128">System.String</span></span>

## <span data-ttu-id="f2954-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f2954-129">OUTPUTS</span></span>

### <span data-ttu-id="f2954-130">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. ServiceBus. MODELES. SharedAccessAuthorizationRuleAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="f2954-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="f2954-131">Identyfikator:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 typ: Microsoft. ServiceBus/AuthorizationRules Name: AuthoRule1 lokalizacja: Znaczniki: prawa: {Listen, Send}</span><span class="sxs-lookup"><span data-stu-id="f2954-131">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : AuthoRule1 Location : Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="f2954-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f2954-132">NOTES</span></span>

## <span data-ttu-id="f2954-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f2954-133">RELATED LINKS</span></span>

