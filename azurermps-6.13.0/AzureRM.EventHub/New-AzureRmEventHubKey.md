---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubKey.md
ms.openlocfilehash: 891e72945e3557ad1047b007504572a981449cd9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718600"
---
# <span data-ttu-id="89c21-101">New-AzureRmEventHubKey</span><span class="sxs-lookup"><span data-stu-id="89c21-101">New-AzureRmEventHubKey</span></span>

## <span data-ttu-id="89c21-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="89c21-102">SYNOPSIS</span></span>
<span data-ttu-id="89c21-103">Tworzy nowy klucz podstawowy lub pomocniczy dla określonej reguły autoryzacji koncentratora zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="89c21-103">Creates a new primary or secondary key for the specified Event Hubs authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89c21-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="89c21-104">SYNTAX</span></span>

### <span data-ttu-id="89c21-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="89c21-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RegenerateKey] <String> [[-KeyValue] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89c21-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="89c21-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-RegenerateKey] <String> [[-KeyValue] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89c21-107">Opis</span><span class="sxs-lookup"><span data-stu-id="89c21-107">DESCRIPTION</span></span>
<span data-ttu-id="89c21-108">Polecenie cmdlet New-AzureRmEventHubKey ponownie generuje podstawowy lub drugorzędny klucz SAS dla określonej reguły autoryzacji koncentratora zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="89c21-108">The New-AzureRmEventHubKey cmdlet regenerates the primary or secondary SAS key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="89c21-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="89c21-109">EXAMPLES</span></span>

### <span data-ttu-id="89c21-110">Przykład 1,1-Namespace-AuthorizationRule PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="89c21-110">Example 1.1 - Namespace - AuthorizationRule PrimaryKey</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="89c21-111">Generuje ponownie klucz podstawowy reguły autoryzacji \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="89c21-111">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="89c21-112">Przykład 1,2-EventHub-AuthorizationRule PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="89c21-112">Example 1.2 - EventHub - AuthorizationRule PrimaryKey</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="89c21-113">Generuje ponownie klucz podstawowy reguły autoryzacji \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="89c21-113">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="89c21-114">Przykład 2,1-Namespace-AuthorizationRule SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="89c21-114">Example 2.1  - Namespace - AuthorizationRule SecondaryKey</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

### <span data-ttu-id="89c21-115">Przykład 2,2-EventHub-AuthorizationRule SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="89c21-115">Example 2.2 - EventHub - AuthorizationRule SecondaryKey</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

<span data-ttu-id="89c21-116">Generuje ponownie klucz pomocniczy reguły autoryzacji \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="89c21-116">Regenerates the secondary key for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="89c21-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="89c21-117">PARAMETERS</span></span>

### <span data-ttu-id="89c21-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89c21-118">-DefaultProfile</span></span>
<span data-ttu-id="89c21-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="89c21-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89c21-120">— EventHub</span><span class="sxs-lookup"><span data-stu-id="89c21-120">-EventHub</span></span>
<span data-ttu-id="89c21-121">Nazwa EventHub</span><span class="sxs-lookup"><span data-stu-id="89c21-121">EventHub Name</span></span>

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

### <span data-ttu-id="89c21-122">-Wartość parametru</span><span class="sxs-lookup"><span data-stu-id="89c21-122">-KeyValue</span></span>
<span data-ttu-id="89c21-123">Zakodowany algorytm Base64 256-bitowy klucz do podpisywania i sprawdzania poprawności tokenu SAS.</span><span class="sxs-lookup"><span data-stu-id="89c21-123">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

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

### <span data-ttu-id="89c21-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="89c21-124">-Name</span></span>
<span data-ttu-id="89c21-125">Nazwa AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="89c21-125">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="89c21-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="89c21-126">-Namespace</span></span>
<span data-ttu-id="89c21-127">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="89c21-127">Namespace Name</span></span>

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

### <span data-ttu-id="89c21-128">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="89c21-128">-RegenerateKey</span></span>
<span data-ttu-id="89c21-129">Ponowne generowanie kluczy — "Primarykea"/"SecondaryKey"</span><span class="sxs-lookup"><span data-stu-id="89c21-129">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'</span></span>

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

### <span data-ttu-id="89c21-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89c21-130">-ResourceGroupName</span></span>
<span data-ttu-id="89c21-131">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="89c21-131">Resource Group Name</span></span>

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

### <span data-ttu-id="89c21-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="89c21-132">-Confirm</span></span>
<span data-ttu-id="89c21-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89c21-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89c21-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89c21-134">-WhatIf</span></span>
<span data-ttu-id="89c21-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89c21-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89c21-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="89c21-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89c21-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89c21-137">CommonParameters</span></span>
<span data-ttu-id="89c21-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89c21-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89c21-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89c21-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89c21-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="89c21-140">INPUTS</span></span>

### <span data-ttu-id="89c21-141">System. String</span><span class="sxs-lookup"><span data-stu-id="89c21-141">System.String</span></span>

## <span data-ttu-id="89c21-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="89c21-142">OUTPUTS</span></span>

### <span data-ttu-id="89c21-143">Microsoft. Azure. Commands. EventHub. modele. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="89c21-143">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="89c21-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="89c21-144">NOTES</span></span>

## <span data-ttu-id="89c21-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="89c21-145">RELATED LINKS</span></span>
