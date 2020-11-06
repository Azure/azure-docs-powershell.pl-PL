---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubKey.md
ms.openlocfilehash: c22bb41702bb4e338d0548be6c7544d597ef0230
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549376"
---
# <span data-ttu-id="1dc3d-101">Get-AzureRmEventHubKey</span><span class="sxs-lookup"><span data-stu-id="1dc3d-101">Get-AzureRmEventHubKey</span></span>

## <span data-ttu-id="1dc3d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1dc3d-102">SYNOPSIS</span></span>
<span data-ttu-id="1dc3d-103">Pobiera szczegóły klucza podstawowego określonej reguły autoryzacji koncentratora zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="1dc3d-103">Gets the primary key details of the specified Event Hubs authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1dc3d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1dc3d-104">SYNTAX</span></span>

### <span data-ttu-id="1dc3d-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1dc3d-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1dc3d-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="1dc3d-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1dc3d-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="1dc3d-107">AliasAuthoRuleSet</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1dc3d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="1dc3d-108">DESCRIPTION</span></span>
<span data-ttu-id="1dc3d-109">Polecenie cmdlet Get-AzureRmEventHubKey zwraca podstawowe i pomocnicze connectionStrings i klucze dotyczące określonej reguły autoryzacji węzłów i obszarów nazw/zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="1dc3d-109">The Get-AzureRmEventHubKey cmdlet returns Primary and Secondary connectionstrings and keys details of the specified NameSpace/Event Hubs/Alias authorization rule.</span></span>

## <span data-ttu-id="1dc3d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1dc3d-110">EXAMPLES</span></span>

### <span data-ttu-id="1dc3d-111">Przykład 1-obszar nazw</span><span class="sxs-lookup"><span data-stu-id="1dc3d-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzureRmEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

### <span data-ttu-id="1dc3d-112">Przykład 2 – EventHub</span><span class="sxs-lookup"><span data-stu-id="1dc3d-112">Example 2 - EventHub</span></span>
```
PS C:\> Get-AzureRmEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="1dc3d-113">Pobiera szczegóły podstawowego i pomocniczego connectionStrings oraz kluczy dla reguły autoryzacji \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="1dc3d-113">Gets details of Primary and Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="1dc3d-114">Przykład 3-alias (Konfiguracja geoawaryjna)</span><span class="sxs-lookup"><span data-stu-id="1dc3d-114">Example 3 - Alias (GeoRecovery Configuration)</span></span>
```
PS C:\> Get-AzureRmEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AliasName MyAliasName -Name MyAuthRuleName
```

<span data-ttu-id="1dc3d-115">Pobiera szczegółowe informacje dotyczące connectionStrings podstawowych, pomocniczych, AliasPrimary oraz AliasSecondary i kluczy reguły autoryzacji \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="1dc3d-115">Gets details of Primary, Secondary, AliasPrimary and AliasSecondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="1dc3d-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1dc3d-116">PARAMETERS</span></span>

### <span data-ttu-id="1dc3d-117">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="1dc3d-117">-AliasName</span></span>
<span data-ttu-id="1dc3d-118">Nazwa aliasu</span><span class="sxs-lookup"><span data-stu-id="1dc3d-118">Alias Name</span></span>

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

### <span data-ttu-id="1dc3d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dc3d-119">-DefaultProfile</span></span>
<span data-ttu-id="1dc3d-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1dc3d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1dc3d-121">— EventHub</span><span class="sxs-lookup"><span data-stu-id="1dc3d-121">-EventHub</span></span>
<span data-ttu-id="1dc3d-122">Nazwa EventHub</span><span class="sxs-lookup"><span data-stu-id="1dc3d-122">EventHub Name</span></span>

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

### <span data-ttu-id="1dc3d-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1dc3d-123">-Name</span></span>
<span data-ttu-id="1dc3d-124">Nazwa AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1dc3d-124">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="1dc3d-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1dc3d-125">-Namespace</span></span>
<span data-ttu-id="1dc3d-126">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="1dc3d-126">Namespace Name</span></span>

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

### <span data-ttu-id="1dc3d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dc3d-127">-ResourceGroupName</span></span>
<span data-ttu-id="1dc3d-128">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="1dc3d-128">Resource Group Name</span></span>

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

### <span data-ttu-id="1dc3d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dc3d-129">CommonParameters</span></span>
<span data-ttu-id="1dc3d-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dc3d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dc3d-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dc3d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dc3d-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1dc3d-132">INPUTS</span></span>

### <span data-ttu-id="1dc3d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="1dc3d-133">System.String</span></span>

## <span data-ttu-id="1dc3d-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1dc3d-134">OUTPUTS</span></span>

### <span data-ttu-id="1dc3d-135">Microsoft. Azure. Commands. EventHub. modele. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="1dc3d-135">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="1dc3d-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1dc3d-136">NOTES</span></span>

## <span data-ttu-id="1dc3d-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1dc3d-137">RELATED LINKS</span></span>
