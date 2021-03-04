---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/get-azeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubKey.md
ms.openlocfilehash: f9f4eb7f60683524eccec8b3d35926b86fa52bbe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957242"
---
# <span data-ttu-id="b300d-101">Get-AzEventHubKey</span><span class="sxs-lookup"><span data-stu-id="b300d-101">Get-AzEventHubKey</span></span>

## <span data-ttu-id="b300d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b300d-102">SYNOPSIS</span></span>
<span data-ttu-id="b300d-103">Pobiera szczegóły klucza podstawowego określonej reguły autoryzacji centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="b300d-103">Gets the primary key details of the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="b300d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b300d-104">SYNTAX</span></span>

### <span data-ttu-id="b300d-105">NamespaceAuthorizationRuleSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="b300d-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b300d-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="b300d-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b300d-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="b300d-107">AliasAuthoRuleSet</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b300d-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="b300d-108">DESCRIPTION</span></span>
<span data-ttu-id="b300d-109">Polecenie Get-AzEventHubKey zwraca podstawowe i pomocnicze connectionstrings oraz klucze szczegółów określonej reguły autoryzacji NameSpace/Event Hubs/Alias.</span><span class="sxs-lookup"><span data-stu-id="b300d-109">The Get-AzEventHubKey cmdlet returns Primary and Secondary connectionstrings and keys details of the specified NameSpace/Event Hubs/Alias authorization rule.</span></span>

## <span data-ttu-id="b300d-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b300d-110">EXAMPLES</span></span>

### <span data-ttu-id="b300d-111">Przykład 1. Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="b300d-111">Example 1: Namespace</span></span>
```powershell
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

### <span data-ttu-id="b300d-112">Przykład 2. Serwis EventHub</span><span class="sxs-lookup"><span data-stu-id="b300d-112">Example 2: EventHub</span></span>
```powershell
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="b300d-113">Pobiera szczegóły podstawowych i pomocniczych połączeń oraz kluczy reguły autoryzacji \` MyAuthRuleName. \`</span><span class="sxs-lookup"><span data-stu-id="b300d-113">Gets details of Primary and Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="b300d-114">Przykład 3. Alias (Konfiguracja funkcji geoodzysowania)</span><span class="sxs-lookup"><span data-stu-id="b300d-114">Example 3: Alias (GeoRecovery Configuration)</span></span>
```powershell
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AliasName MyAliasName -Name MyAuthRuleName
```

<span data-ttu-id="b300d-115">Pobiera szczegóły podstawowych, pomocniczych, aliasów AliasPrimary i aliassecondary połączeń oraz kluczy reguły autoryzacji \` MyAuthRuleName. \`</span><span class="sxs-lookup"><span data-stu-id="b300d-115">Gets details of Primary, Secondary, AliasPrimary and AliasSecondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="b300d-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b300d-116">PARAMETERS</span></span>

### <span data-ttu-id="b300d-117">-AliasName</span><span class="sxs-lookup"><span data-stu-id="b300d-117">-AliasName</span></span>
<span data-ttu-id="b300d-118">Nazwa aliasu</span><span class="sxs-lookup"><span data-stu-id="b300d-118">Alias Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b300d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b300d-119">-DefaultProfile</span></span>
<span data-ttu-id="b300d-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b300d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b300d-121">-EventHub</span><span class="sxs-lookup"><span data-stu-id="b300d-121">-EventHub</span></span>
<span data-ttu-id="b300d-122">Nazwa aplikacji EventHub</span><span class="sxs-lookup"><span data-stu-id="b300d-122">EventHub Name</span></span>

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

### <span data-ttu-id="b300d-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b300d-123">-Name</span></span>
<span data-ttu-id="b300d-124">Nazwa podmiotu autoryzacji</span><span class="sxs-lookup"><span data-stu-id="b300d-124">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="b300d-125">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="b300d-125">-Namespace</span></span>
<span data-ttu-id="b300d-126">Nazwa przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="b300d-126">Namespace Name</span></span>

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

### <span data-ttu-id="b300d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b300d-127">-ResourceGroupName</span></span>
<span data-ttu-id="b300d-128">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b300d-128">Resource Group Name</span></span>

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

### <span data-ttu-id="b300d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b300d-129">CommonParameters</span></span>
<span data-ttu-id="b300d-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b300d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b300d-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b300d-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b300d-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b300d-132">INPUTS</span></span>

### <span data-ttu-id="b300d-133">System.String</span><span class="sxs-lookup"><span data-stu-id="b300d-133">System.String</span></span>

## <span data-ttu-id="b300d-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b300d-134">OUTPUTS</span></span>

### <span data-ttu-id="b300d-135">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="b300d-135">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="b300d-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b300d-136">NOTES</span></span>

## <span data-ttu-id="b300d-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b300d-137">RELATED LINKS</span></span>
