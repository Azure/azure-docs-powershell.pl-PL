---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Get-AzEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Get-AzEventHubKey.md
ms.openlocfilehash: 27be06fb85cc4bd1dc38dd7a123205d3ba7ff4d3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891502"
---
# <span data-ttu-id="68638-101">Get-AzEventHubKey</span><span class="sxs-lookup"><span data-stu-id="68638-101">Get-AzEventHubKey</span></span>

## <span data-ttu-id="68638-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="68638-102">SYNOPSIS</span></span>
<span data-ttu-id="68638-103">Pobiera szczegóły klucza podstawowego określonej reguły autoryzacji koncentratora zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="68638-103">Gets the primary key details of the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="68638-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="68638-104">SYNTAX</span></span>

### <span data-ttu-id="68638-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="68638-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68638-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="68638-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68638-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="68638-107">AliasAuthoRuleSet</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68638-108">Opis</span><span class="sxs-lookup"><span data-stu-id="68638-108">DESCRIPTION</span></span>
<span data-ttu-id="68638-109">Polecenie cmdlet Get-AzEventHubKey zwraca podstawowe i pomocnicze connectionStrings i klucze dotyczące określonej reguły autoryzacji węzłów i obszarów nazw/zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="68638-109">The Get-AzEventHubKey cmdlet returns Primary and Secondary connectionstrings and keys details of the specified NameSpace/Event Hubs/Alias authorization rule.</span></span>

## <span data-ttu-id="68638-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="68638-110">EXAMPLES</span></span>

### <span data-ttu-id="68638-111">Przykład 1-obszar nazw</span><span class="sxs-lookup"><span data-stu-id="68638-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

### <span data-ttu-id="68638-112">Przykład 2 – EventHub</span><span class="sxs-lookup"><span data-stu-id="68638-112">Example 2 - EventHub</span></span>
```
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="68638-113">Pobiera szczegóły podstawowego i pomocniczego connectionStrings oraz kluczy dla reguły autoryzacji \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="68638-113">Gets details of Primary and Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="68638-114">Przykład 3-alias (Konfiguracja geoawaryjna)</span><span class="sxs-lookup"><span data-stu-id="68638-114">Example 3 - Alias (GeoRecovery Configuration)</span></span>
```
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AliasName MyAliasName -Name MyAuthRuleName
```

<span data-ttu-id="68638-115">Pobiera szczegółowe informacje dotyczące connectionStrings podstawowych, pomocniczych, AliasPrimary oraz AliasSecondary i kluczy reguły autoryzacji \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="68638-115">Gets details of Primary, Secondary, AliasPrimary and AliasSecondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="68638-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="68638-116">PARAMETERS</span></span>

### <span data-ttu-id="68638-117">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="68638-117">-AliasName</span></span>
<span data-ttu-id="68638-118">Nazwa aliasu</span><span class="sxs-lookup"><span data-stu-id="68638-118">Alias Name</span></span>

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

### <span data-ttu-id="68638-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68638-119">-DefaultProfile</span></span>
<span data-ttu-id="68638-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="68638-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68638-121">— EventHub</span><span class="sxs-lookup"><span data-stu-id="68638-121">-EventHub</span></span>
<span data-ttu-id="68638-122">Nazwa EventHub</span><span class="sxs-lookup"><span data-stu-id="68638-122">EventHub Name</span></span>

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

### <span data-ttu-id="68638-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="68638-123">-Name</span></span>
<span data-ttu-id="68638-124">Nazwa AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="68638-124">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="68638-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="68638-125">-Namespace</span></span>
<span data-ttu-id="68638-126">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="68638-126">Namespace Name</span></span>

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

### <span data-ttu-id="68638-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68638-127">-ResourceGroupName</span></span>
<span data-ttu-id="68638-128">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="68638-128">Resource Group Name</span></span>

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

### <span data-ttu-id="68638-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68638-129">CommonParameters</span></span>
<span data-ttu-id="68638-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68638-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68638-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68638-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68638-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="68638-132">INPUTS</span></span>

### <span data-ttu-id="68638-133">System. String</span><span class="sxs-lookup"><span data-stu-id="68638-133">System.String</span></span>

## <span data-ttu-id="68638-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="68638-134">OUTPUTS</span></span>

### <span data-ttu-id="68638-135">Microsoft. Azure. Commands. EventHub. modele. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="68638-135">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="68638-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="68638-136">NOTES</span></span>

## <span data-ttu-id="68638-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="68638-137">RELATED LINKS</span></span>
