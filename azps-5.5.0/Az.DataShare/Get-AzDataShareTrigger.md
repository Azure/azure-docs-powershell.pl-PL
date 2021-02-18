---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareTrigger.md
ms.openlocfilehash: 23554c4de23062fa44a690843232dbc6337e3c9e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200539"
---
# <span data-ttu-id="ba9b7-101">Get-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="ba9b7-101">Get-AzDataShareTrigger</span></span>

## <span data-ttu-id="ba9b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba9b7-102">SYNOPSIS</span></span>
<span data-ttu-id="ba9b7-103">Pobiera informacje o wyzwalaczu w subskrypcji udostępniania.</span><span class="sxs-lookup"><span data-stu-id="ba9b7-103">Gets information about a trigger in share subscription.</span></span>

## <span data-ttu-id="ba9b7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ba9b7-104">SYNTAX</span></span>

### <span data-ttu-id="ba9b7-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="ba9b7-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba9b7-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba9b7-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba9b7-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="ba9b7-107">DESCRIPTION</span></span>
<span data-ttu-id="ba9b7-108">Polecenie **cmdlet Get-AzDataShareTrigger** pobiera informacje o wyzwalaczu udostępniania subskrypcji w ramach konta udostępniania danych.</span><span class="sxs-lookup"><span data-stu-id="ba9b7-108">The **Get-AzDataShareTrigger** cmdlet gets information about trigger for share subscription under data share account.</span></span>

## <span data-ttu-id="ba9b7-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ba9b7-109">EXAMPLES</span></span>

### <span data-ttu-id="ba9b7-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ba9b7-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareTrigger -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsTrigger"

CreatedAt           : 7/10/2019 12:16:34 AM
CreatedBy           : Ads test
ProvisioningState   : Succeeded
RecurrenceInterval  : Day
SynchronizationMode : Incremental
SynchronizationTime : 7/9/2019 9:00:00 AM
TriggerStatus       : Active
Id                  : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription/triggers/AdsTrigger
Name                : AdsTrigger
Type                : Microsoft.DataShare/Triggers
```

<span data-ttu-id="ba9b7-111">To polecenie pobiera informacje o wyzwalaczu AdsTrigger dla udostępniania subskrypcji AdsShareSubscription w obszarze wikiAds konta udostępniania danych.</span><span class="sxs-lookup"><span data-stu-id="ba9b7-111">This command gets information about trigger AdsTrigger for share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="ba9b7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba9b7-112">PARAMETERS</span></span>

### <span data-ttu-id="ba9b7-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ba9b7-113">-AccountName</span></span>
<span data-ttu-id="ba9b7-114">Nazwa konta współużytkowego danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="ba9b7-114">Azure data share account name</span></span>

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

### <span data-ttu-id="ba9b7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba9b7-115">-DefaultProfile</span></span>
<span data-ttu-id="ba9b7-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ba9b7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba9b7-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ba9b7-117">-Name</span></span>
<span data-ttu-id="ba9b7-118">Nazwa wyzwalacza udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="ba9b7-118">Azure data share trigger name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba9b7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba9b7-119">-ResourceGroupName</span></span>
<span data-ttu-id="ba9b7-120">Nazwa grupy zasobów konta udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="ba9b7-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="ba9b7-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba9b7-121">-ResourceId</span></span>
<span data-ttu-id="ba9b7-122">Identyfikator zasobu wyzwalacza</span><span class="sxs-lookup"><span data-stu-id="ba9b7-122">The resource id of the trigger</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba9b7-123">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="ba9b7-123">-ShareSubscriptionName</span></span>
<span data-ttu-id="ba9b7-124">Nazwa subskrypcji udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="ba9b7-124">Azure data share subscription name</span></span>

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

### <span data-ttu-id="ba9b7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba9b7-125">CommonParameters</span></span>
<span data-ttu-id="ba9b7-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba9b7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba9b7-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ba9b7-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba9b7-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ba9b7-128">INPUTS</span></span>

### <span data-ttu-id="ba9b7-129">System.String</span><span class="sxs-lookup"><span data-stu-id="ba9b7-129">System.String</span></span>

## <span data-ttu-id="ba9b7-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ba9b7-130">OUTPUTS</span></span>

### <span data-ttu-id="ba9b7-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="ba9b7-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span></span>

## <span data-ttu-id="ba9b7-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ba9b7-132">NOTES</span></span>

## <span data-ttu-id="ba9b7-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ba9b7-133">RELATED LINKS</span></span>
