---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatashareprovidersharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareProviderShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareProviderShareSubscription.md
ms.openlocfilehash: b28182a5593454b110b2fe4036b022a8d74c33d0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012225"
---
# <span data-ttu-id="8e609-101">Get-AzDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="8e609-101">Get-AzDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="8e609-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e609-102">SYNOPSIS</span></span>
<span data-ttu-id="8e609-103">Pobiera informacje o subskrypcjach udostępniania konsumenckiego po stronie dostawcy.</span><span class="sxs-lookup"><span data-stu-id="8e609-103">Gets information about consumer share subscriptions on provider side.</span></span>

## <span data-ttu-id="8e609-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8e609-104">SYNTAX</span></span>

### <span data-ttu-id="8e609-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="8e609-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareProviderShareSubscription -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-ShareSubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e609-106">ByProviderShareSubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e609-106">ByProviderShareSubscriptionIdParameterSet</span></span>
```
Get-AzDataShareProviderShareSubscription [-ShareSubscriptionId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e609-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="8e609-107">DESCRIPTION</span></span>
<span data-ttu-id="8e609-108">Polecenie **cmdlet Get-AzDataShareProviderSubscription** pobiera informacje o subskrypcjach udziału konsumenckiego po stronie dostawcy.</span><span class="sxs-lookup"><span data-stu-id="8e609-108">The **Get-AzDataShareProviderSubscription** cmdlet gets information about consumer share subscriptions on provider side.</span></span> <span data-ttu-id="8e609-109">Jeśli określisz identyfikator podscrption udostępniania, to polecenie cmdlet pobiera informacje o subskrypcji udostępniania.</span><span class="sxs-lookup"><span data-stu-id="8e609-109">If you specify the share subscrption id, this cmdlet gets information about the share subscription.</span></span> <span data-ttu-id="8e609-110">Jeśli nie określisz identyfikatora subskrypcji udostępniania, to polecenie cmdlet pobiera informacje o wszystkich subskrypcjach udziału konsumenckiego skojarzonych z tym udostępnianiem.</span><span class="sxs-lookup"><span data-stu-id="8e609-110">If you do not specify the share subscription id, this cmdlet gets information about all the consumer share subscriptions in associated with the share.</span></span>

## <span data-ttu-id="8e609-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8e609-111">EXAMPLES</span></span>

### <span data-ttu-id="8e609-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8e609-112">Example 1</span></span>
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

<span data-ttu-id="8e609-113">To polecenia zawierają informacje na temat subskrypcji udostępniania konsumenckiego skojarzonej z udostępnianiem AdsShare w dziel się danymi konta WikiAds.</span><span class="sxs-lookup"><span data-stu-id="8e609-113">This commands provides information about consumer share subscription associated with share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="8e609-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e609-114">PARAMETERS</span></span>

### <span data-ttu-id="8e609-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8e609-115">-AccountName</span></span>
<span data-ttu-id="8e609-116">Nazwa konta usługi Azure DataShare.</span><span class="sxs-lookup"><span data-stu-id="8e609-116">Azure DataShare Account name.</span></span>

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

### <span data-ttu-id="8e609-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e609-117">-DefaultProfile</span></span>
<span data-ttu-id="8e609-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8e609-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e609-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e609-119">-ResourceGroupName</span></span>
<span data-ttu-id="8e609-120">Grupa zasobów konta usługi Azure DataShare.</span><span class="sxs-lookup"><span data-stu-id="8e609-120">The resource group of the Azure DataShare Account.</span></span>

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

### <span data-ttu-id="8e609-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e609-121">-ResourceId</span></span>
<span data-ttu-id="8e609-122">Identyfikator zasobu udziału</span><span class="sxs-lookup"><span data-stu-id="8e609-122">The resource id of the share</span></span>

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

### <span data-ttu-id="8e609-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="8e609-123">-ShareName</span></span>
<span data-ttu-id="8e609-124">Nazwa usługi Azure DataShare.</span><span class="sxs-lookup"><span data-stu-id="8e609-124">Azure DataShare name.</span></span>

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

### <span data-ttu-id="8e609-125">-ShareSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8e609-125">-ShareSubscriptionId</span></span>
<span data-ttu-id="8e609-126">Identyfikator subskrypcji udziału konsumenckiego</span><span class="sxs-lookup"><span data-stu-id="8e609-126">The id of consumer share subscription</span></span>

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

### <span data-ttu-id="8e609-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e609-127">CommonParameters</span></span>
<span data-ttu-id="8e609-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e609-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e609-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e609-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e609-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8e609-130">INPUTS</span></span>

### <span data-ttu-id="8e609-131">System.String</span><span class="sxs-lookup"><span data-stu-id="8e609-131">System.String</span></span>

## <span data-ttu-id="8e609-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8e609-132">OUTPUTS</span></span>

### <span data-ttu-id="8e609-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="8e609-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="8e609-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8e609-134">NOTES</span></span>

## <span data-ttu-id="8e609-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8e609-135">RELATED LINKS</span></span>
