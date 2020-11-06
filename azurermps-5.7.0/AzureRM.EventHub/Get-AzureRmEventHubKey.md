---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubKey.md
ms.openlocfilehash: f8a9f074398df5ce9d8464adf3c22a65d14784b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551736"
---
# <span data-ttu-id="7669c-101">Get-AzureRmEventHubKey</span><span class="sxs-lookup"><span data-stu-id="7669c-101">Get-AzureRmEventHubKey</span></span>

## <span data-ttu-id="7669c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7669c-102">SYNOPSIS</span></span>
<span data-ttu-id="7669c-103">Pobiera szczegóły klucza podstawowego określonej reguły autoryzacji koncentratora zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="7669c-103">Gets the primary key details of the specified Event Hubs authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7669c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7669c-104">SYNTAX</span></span>

### <span data-ttu-id="7669c-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7669c-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7669c-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="7669c-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7669c-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="7669c-107">AliasAuthoRuleSet</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7669c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7669c-108">DESCRIPTION</span></span>
<span data-ttu-id="7669c-109">Polecenie cmdlet Get-AzureRmEventHubKey zwraca podstawowe i pomocnicze connectionStrings i klucze dotyczące określonej reguły autoryzacji węzłów i obszarów nazw/zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="7669c-109">The Get-AzureRmEventHubKey cmdlet returns Primary and Secondary connectionstrings and keys details of the specified NameSpace/Event Hubs/Alias authorization rule.</span></span>

## <span data-ttu-id="7669c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7669c-110">EXAMPLES</span></span>

### <span data-ttu-id="7669c-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7669c-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="7669c-112">Pobiera szczegóły podstawowego i pomocniczego connectionStrings oraz kluczy dla reguły autoryzacji \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="7669c-112">Gets details of Primary and Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="7669c-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7669c-113">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AliasName MyAliasName -Name MyAuthRuleName
```

<span data-ttu-id="7669c-114">Pobiera szczegółowe informacje dotyczące connectionStrings podstawowych, pomocniczych, AliasPrimary oraz AliasSecondary i kluczy reguły autoryzacji \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="7669c-114">Gets details of Primary, Secondary, AliasPrimary and AliasSecondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="7669c-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7669c-115">PARAMETERS</span></span>

### <span data-ttu-id="7669c-116">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="7669c-116">-AliasName</span></span>
<span data-ttu-id="7669c-117">Nazwa aliasu</span><span class="sxs-lookup"><span data-stu-id="7669c-117">Alias Name</span></span>

```yaml
Type: String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7669c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7669c-118">-DefaultProfile</span></span>
<span data-ttu-id="7669c-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7669c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7669c-120">— EventHub</span><span class="sxs-lookup"><span data-stu-id="7669c-120">-EventHub</span></span>
<span data-ttu-id="7669c-121">Nazwa EventHub</span><span class="sxs-lookup"><span data-stu-id="7669c-121">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7669c-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7669c-122">-Name</span></span>
<span data-ttu-id="7669c-123">Nazwa AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7669c-123">AuthorizationRule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7669c-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7669c-124">-Namespace</span></span>
<span data-ttu-id="7669c-125">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="7669c-125">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7669c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7669c-126">-ResourceGroupName</span></span>
<span data-ttu-id="7669c-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="7669c-127">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7669c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7669c-128">CommonParameters</span></span>
<span data-ttu-id="7669c-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7669c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="7669c-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7669c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7669c-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7669c-131">INPUTS</span></span>

### <span data-ttu-id="7669c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="7669c-132">System.String</span></span>


## <span data-ttu-id="7669c-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7669c-133">OUTPUTS</span></span>

### <span data-ttu-id="7669c-134">Microsoft. Azure. Commands. EventHub. modele. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="7669c-134">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>


## <span data-ttu-id="7669c-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7669c-135">NOTES</span></span>

## <span data-ttu-id="7669c-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7669c-136">RELATED LINKS</span></span>
