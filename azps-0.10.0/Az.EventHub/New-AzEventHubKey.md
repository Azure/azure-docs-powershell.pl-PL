---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/New-AzEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/New-AzEventHubKey.md
ms.openlocfilehash: 50ec39882a510393e304efae4c7cbc9469d14d91
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891469"
---
# <span data-ttu-id="eddf3-101">New-AzEventHubKey</span><span class="sxs-lookup"><span data-stu-id="eddf3-101">New-AzEventHubKey</span></span>

## <span data-ttu-id="eddf3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eddf3-102">SYNOPSIS</span></span>
<span data-ttu-id="eddf3-103">Tworzy nowy klucz podstawowy lub pomocniczy dla określonej reguły autoryzacji koncentratora zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="eddf3-103">Creates a new primary or secondary key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="eddf3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eddf3-104">SYNTAX</span></span>

### <span data-ttu-id="eddf3-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="eddf3-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RegenerateKey] <String> [[-KeyValue] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eddf3-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="eddf3-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String> [-Name] <String>
 [-RegenerateKey] <String> [[-KeyValue] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eddf3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="eddf3-107">DESCRIPTION</span></span>
<span data-ttu-id="eddf3-108">Polecenie cmdlet New-AzEventHubKey ponownie generuje podstawowy lub drugorzędny klucz SAS dla określonej reguły autoryzacji koncentratora zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="eddf3-108">The New-AzEventHubKey cmdlet regenerates the primary or secondary SAS key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="eddf3-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eddf3-109">EXAMPLES</span></span>

### <span data-ttu-id="eddf3-110">Przykład 1,1-Namespace-AuthorizationRule PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="eddf3-110">Example 1.1 - Namespace - AuthorizationRule PrimaryKey</span></span>
```
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="eddf3-111">Generuje ponownie klucz podstawowy reguły autoryzacji \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="eddf3-111">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="eddf3-112">Przykład 1,2-EventHub-AuthorizationRule PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="eddf3-112">Example 1.2 - EventHub - AuthorizationRule PrimaryKey</span></span>
```
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="eddf3-113">Generuje ponownie klucz podstawowy reguły autoryzacji \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="eddf3-113">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="eddf3-114">Przykład 2,1-Namespace-AuthorizationRule SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="eddf3-114">Example 2.1  - Namespace - AuthorizationRule SecondaryKey</span></span>
```
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

### <span data-ttu-id="eddf3-115">Przykład 2,2-EventHub-AuthorizationRule SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="eddf3-115">Example 2.2 - EventHub - AuthorizationRule SecondaryKey</span></span>
```
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

<span data-ttu-id="eddf3-116">Generuje ponownie klucz pomocniczy reguły autoryzacji \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="eddf3-116">Regenerates the secondary key for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="eddf3-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eddf3-117">PARAMETERS</span></span>

### <span data-ttu-id="eddf3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eddf3-118">-DefaultProfile</span></span>
<span data-ttu-id="eddf3-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="eddf3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eddf3-120">— EventHub</span><span class="sxs-lookup"><span data-stu-id="eddf3-120">-EventHub</span></span>
<span data-ttu-id="eddf3-121">Nazwa EventHub</span><span class="sxs-lookup"><span data-stu-id="eddf3-121">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eddf3-122">-Wartość parametru</span><span class="sxs-lookup"><span data-stu-id="eddf3-122">-KeyValue</span></span>
<span data-ttu-id="eddf3-123">Zakodowany algorytm Base64 256-bitowy klucz do podpisywania i sprawdzania poprawności tokenu SAS.</span><span class="sxs-lookup"><span data-stu-id="eddf3-123">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eddf3-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="eddf3-124">-Name</span></span>
<span data-ttu-id="eddf3-125">Nazwa AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="eddf3-125">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eddf3-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="eddf3-126">-Namespace</span></span>
<span data-ttu-id="eddf3-127">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="eddf3-127">Namespace Name</span></span>

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

### <span data-ttu-id="eddf3-128">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="eddf3-128">-RegenerateKey</span></span>
<span data-ttu-id="eddf3-129">Ponowne generowanie kluczy — "Primarykea"/"SecondaryKey"</span><span class="sxs-lookup"><span data-stu-id="eddf3-129">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eddf3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eddf3-130">-ResourceGroupName</span></span>
<span data-ttu-id="eddf3-131">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="eddf3-131">Resource Group Name</span></span>

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

### <span data-ttu-id="eddf3-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="eddf3-132">-Confirm</span></span>
<span data-ttu-id="eddf3-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eddf3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eddf3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eddf3-134">-WhatIf</span></span>
<span data-ttu-id="eddf3-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eddf3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eddf3-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="eddf3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eddf3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eddf3-137">CommonParameters</span></span>
<span data-ttu-id="eddf3-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eddf3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eddf3-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eddf3-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eddf3-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eddf3-140">INPUTS</span></span>

### <span data-ttu-id="eddf3-141">System. String</span><span class="sxs-lookup"><span data-stu-id="eddf3-141">System.String</span></span>

## <span data-ttu-id="eddf3-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eddf3-142">OUTPUTS</span></span>

### <span data-ttu-id="eddf3-143">Microsoft. Azure. Commands. EventHub. modele. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="eddf3-143">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="eddf3-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eddf3-144">NOTES</span></span>

## <span data-ttu-id="eddf3-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eddf3-145">RELATED LINKS</span></span>
