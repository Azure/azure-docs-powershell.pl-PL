---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashareprovidersharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareProviderShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareProviderShareSubscription.md
ms.openlocfilehash: 5422b43019b7b667ba7ea787663e91e2b6beb118
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198794"
---
# <span data-ttu-id="dc805-101">Get-AzDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="dc805-101">Get-AzDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="dc805-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc805-102">SYNOPSIS</span></span>
<span data-ttu-id="dc805-103">Pobiera informacje o subskrypcjach udostępniania konsumenckiego po stronie dostawcy.</span><span class="sxs-lookup"><span data-stu-id="dc805-103">Gets information about consumer share subscriptions on provider side.</span></span>

## <span data-ttu-id="dc805-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="dc805-104">SYNTAX</span></span>

### <span data-ttu-id="dc805-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="dc805-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareProviderShareSubscription -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-ShareSubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc805-106">ByProviderShareSubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc805-106">ByProviderShareSubscriptionIdParameterSet</span></span>
```
Get-AzDataShareProviderShareSubscription [-ShareSubscriptionId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc805-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="dc805-107">DESCRIPTION</span></span>
<span data-ttu-id="dc805-108">Polecenie **cmdlet Get-AzDataShareProviderSubscription** pobiera informacje o subskrypcjach udziału konsumenckiego po stronie dostawcy.</span><span class="sxs-lookup"><span data-stu-id="dc805-108">The **Get-AzDataShareProviderSubscription** cmdlet gets information about consumer share subscriptions on provider side.</span></span> <span data-ttu-id="dc805-109">Jeśli określisz identyfikator podscrption udostępniania, to polecenie cmdlet pobiera informacje o subskrypcji udostępniania.</span><span class="sxs-lookup"><span data-stu-id="dc805-109">If you specify the share subscrption id, this cmdlet gets information about the share subscription.</span></span> <span data-ttu-id="dc805-110">Jeśli nie określisz identyfikatora subskrypcji udostępniania, to polecenie cmdlet pobiera informacje o wszystkich subskrypcjach udostępniania dla klientów domowych skojarzonych z tym udostępnianiem.</span><span class="sxs-lookup"><span data-stu-id="dc805-110">If you do not specify the share subscription id, this cmdlet gets information about all the consumer share subscriptions in associated with the share.</span></span>

## <span data-ttu-id="dc805-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="dc805-111">EXAMPLES</span></span>

### <span data-ttu-id="dc805-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="dc805-112">Example 1</span></span>
```
PS C:\> Get-AzDataShareProviderShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -ShareSubscriptionId "/subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/shareSubscriptions/505c3500-b2ff-46ab-96bf-50f5ec89d75a"

Company                   : ADS Test
CreatedAt                 : 6/30/2019 12:42:12 AM
CreatedBy                 : adstest@microsoft.com
SharedAt                  : 6/30/2019 12:41:37 AM
SharedBy                  : adsprovider@microsoft.com
ShareSubscriptionObjectId : 505c3500-b2ff-46ab-96bf-50f5ec89d75a
ShareSubscriptionStatus   : Active
Id                        : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/shareSubscriptions/505c3500-b2ff-46ab-96bf-50f5ec89d75a
Name                      : AdsShareSubscription
Type                      : Microsoft.DataShare/ShareSubscriptions
```

<span data-ttu-id="dc805-113">To polecenia zawierają informacje na temat subskrypcji udostępniania konsumenckiego skojarzonej z udostępnianiem AdsShare w dziel się danymi konta WikiAds.</span><span class="sxs-lookup"><span data-stu-id="dc805-113">This commands provides information about consumer share subscription associated with share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="dc805-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dc805-114">PARAMETERS</span></span>

### <span data-ttu-id="dc805-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="dc805-115">-AccountName</span></span>
<span data-ttu-id="dc805-116">Nazwa konta usługi Azure DataShare.</span><span class="sxs-lookup"><span data-stu-id="dc805-116">Azure DataShare Account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc805-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc805-117">-DefaultProfile</span></span>
<span data-ttu-id="dc805-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="dc805-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc805-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc805-119">-ResourceGroupName</span></span>
<span data-ttu-id="dc805-120">Grupa zasobów konta usługi Azure DataShare.</span><span class="sxs-lookup"><span data-stu-id="dc805-120">The resource group of the Azure DataShare Account.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc805-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc805-121">-ResourceId</span></span>
<span data-ttu-id="dc805-122">Identyfikator zasobu udziału</span><span class="sxs-lookup"><span data-stu-id="dc805-122">The resource id of the share</span></span>

```yaml
Type: System.String
Parameter Sets: ByProviderShareSubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc805-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="dc805-123">-ShareName</span></span>
<span data-ttu-id="dc805-124">Nazwa usługi Azure DataShare.</span><span class="sxs-lookup"><span data-stu-id="dc805-124">Azure DataShare name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc805-125">-ShareSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dc805-125">-ShareSubscriptionId</span></span>
<span data-ttu-id="dc805-126">Identyfikator subskrypcji udziału konsumenckiego</span><span class="sxs-lookup"><span data-stu-id="dc805-126">The id of consumer share subscription</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc805-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc805-127">CommonParameters</span></span>
<span data-ttu-id="dc805-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc805-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc805-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dc805-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc805-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dc805-130">INPUTS</span></span>

### <span data-ttu-id="dc805-131">System.String</span><span class="sxs-lookup"><span data-stu-id="dc805-131">System.String</span></span>

## <span data-ttu-id="dc805-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dc805-132">OUTPUTS</span></span>

### <span data-ttu-id="dc805-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="dc805-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="dc805-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="dc805-134">NOTES</span></span>

## <span data-ttu-id="dc805-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dc805-135">RELATED LINKS</span></span>
