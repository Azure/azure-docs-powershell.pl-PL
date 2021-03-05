---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/new-azeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubKey.md
ms.openlocfilehash: c03a3ef7151c360bbcf81e249090fe39e3c144b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980426"
---
# <span data-ttu-id="087ea-101">New-AzEventHubKey</span><span class="sxs-lookup"><span data-stu-id="087ea-101">New-AzEventHubKey</span></span>

## <span data-ttu-id="087ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="087ea-102">SYNOPSIS</span></span>
<span data-ttu-id="087ea-103">Tworzy nowy klucz podstawowy lub pomocniczy dla określonej reguły autoryzacji centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="087ea-103">Creates a new primary or secondary key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="087ea-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="087ea-104">SYNTAX</span></span>

### <span data-ttu-id="087ea-105">NamespaceAuthorizationRuleSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="087ea-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RegenerateKey] <String> [[-KeyValue] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="087ea-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="087ea-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String> [-Name] <String>
 [-RegenerateKey] <String> [[-KeyValue] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="087ea-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="087ea-107">DESCRIPTION</span></span>
<span data-ttu-id="087ea-108">Polecenie New-AzEventHubKey ponownie generuje podstawowy lub pomocniczy klucz SAS dla określonej reguły autoryzacji centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="087ea-108">The New-AzEventHubKey cmdlet regenerates the primary or secondary SAS key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="087ea-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="087ea-109">EXAMPLES</span></span>

### <span data-ttu-id="087ea-110">Przykład 1. Przestrzeń nazw — AuthorizationRule PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="087ea-110">Example 1: Namespace - AuthorizationRule PrimaryKey</span></span>
```powershell
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="087ea-111">Ponownie generuje klucz podstawowy reguły autoryzacji \` MyAuthRuleName. \`</span><span class="sxs-lookup"><span data-stu-id="087ea-111">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="087ea-112">Przykład 2. Serwis EventHub — AuthorizationRule PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="087ea-112">Example 2: EventHub - AuthorizationRule PrimaryKey</span></span>
```powershell
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="087ea-113">Ponownie generuje klucz podstawowy reguły autoryzacji \` MyAuthRuleName. \`</span><span class="sxs-lookup"><span data-stu-id="087ea-113">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="087ea-114">Przykład 3. Przestrzeń nazw — AuthorizationRule SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="087ea-114">Example 3: - Namespace - AuthorizationRule SecondaryKey</span></span>
```powershell
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

### <span data-ttu-id="087ea-115">Przykład 4. EventHub — AuthorizationRule SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="087ea-115">Example 4: EventHub - AuthorizationRule SecondaryKey</span></span>
```powershell
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

<span data-ttu-id="087ea-116">Ponownie generuje klucz pomocniczy reguły autoryzacji \` MyAuthRuleName. \`</span><span class="sxs-lookup"><span data-stu-id="087ea-116">Regenerates the secondary key for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="087ea-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="087ea-117">PARAMETERS</span></span>

### <span data-ttu-id="087ea-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="087ea-118">-DefaultProfile</span></span>
<span data-ttu-id="087ea-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="087ea-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="087ea-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="087ea-120">-EventHub</span></span>
<span data-ttu-id="087ea-121">Nazwa aplikacji EventHub</span><span class="sxs-lookup"><span data-stu-id="087ea-121">EventHub Name</span></span>

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

### <span data-ttu-id="087ea-122">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="087ea-122">-KeyValue</span></span>
<span data-ttu-id="087ea-123">Zakodowany w bazie danych klucz 256-bitowy do podpisywania i sprawdzania poprawności tokenu SAS.</span><span class="sxs-lookup"><span data-stu-id="087ea-123">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

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

### <span data-ttu-id="087ea-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="087ea-124">-Name</span></span>
<span data-ttu-id="087ea-125">Nazwa podmiotu autoryzacji</span><span class="sxs-lookup"><span data-stu-id="087ea-125">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="087ea-126">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="087ea-126">-Namespace</span></span>
<span data-ttu-id="087ea-127">Nazwa przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="087ea-127">Namespace Name</span></span>

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

### <span data-ttu-id="087ea-128">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="087ea-128">-RegenerateKey</span></span>
<span data-ttu-id="087ea-129">Generuj ponownie klucze — "KluczPodstawowy"/"Klucz Pomocniczy"</span><span class="sxs-lookup"><span data-stu-id="087ea-129">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'</span></span>

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

### <span data-ttu-id="087ea-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="087ea-130">-ResourceGroupName</span></span>
<span data-ttu-id="087ea-131">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="087ea-131">Resource Group Name</span></span>

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

### <span data-ttu-id="087ea-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="087ea-132">-Confirm</span></span>
<span data-ttu-id="087ea-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="087ea-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="087ea-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="087ea-134">-WhatIf</span></span>
<span data-ttu-id="087ea-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="087ea-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="087ea-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="087ea-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="087ea-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="087ea-137">CommonParameters</span></span>
<span data-ttu-id="087ea-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="087ea-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="087ea-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="087ea-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="087ea-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="087ea-140">INPUTS</span></span>

### <span data-ttu-id="087ea-141">System.String</span><span class="sxs-lookup"><span data-stu-id="087ea-141">System.String</span></span>

## <span data-ttu-id="087ea-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="087ea-142">OUTPUTS</span></span>

### <span data-ttu-id="087ea-143">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="087ea-143">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="087ea-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="087ea-144">NOTES</span></span>

## <span data-ttu-id="087ea-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="087ea-145">RELATED LINKS</span></span>
