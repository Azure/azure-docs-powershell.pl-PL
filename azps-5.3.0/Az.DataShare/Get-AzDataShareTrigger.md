---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareTrigger.md
ms.openlocfilehash: 23554c4de23062fa44a690843232dbc6337e3c9e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377344"
---
# <span data-ttu-id="8a576-101">Get-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="8a576-101">Get-AzDataShareTrigger</span></span>

## <span data-ttu-id="8a576-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8a576-102">SYNOPSIS</span></span>
<span data-ttu-id="8a576-103">Pobiera informacje o wyzwalaczu w ramach udostępniania subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="8a576-103">Gets information about a trigger in share subscription.</span></span>

## <span data-ttu-id="8a576-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8a576-104">SYNTAX</span></span>

### <span data-ttu-id="8a576-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8a576-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a576-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a576-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a576-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8a576-107">DESCRIPTION</span></span>
<span data-ttu-id="8a576-108">Polecenie cmdlet **Get-AzDataShareTrigger** pobiera informacje o wyzwalaczu udostępniania subskrypcji w obszarze konto udziału danych.</span><span class="sxs-lookup"><span data-stu-id="8a576-108">The **Get-AzDataShareTrigger** cmdlet gets information about trigger for share subscription under data share account.</span></span>

## <span data-ttu-id="8a576-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8a576-109">EXAMPLES</span></span>

### <span data-ttu-id="8a576-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8a576-110">Example 1</span></span>
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

<span data-ttu-id="8a576-111">To polecenie pobiera informacje dotyczące polecenia Trigger AdsTrigger dla subskrypcji AdsShareSubscription w obszarze konto udziału danych WikiAds.</span><span class="sxs-lookup"><span data-stu-id="8a576-111">This command gets information about trigger AdsTrigger for share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="8a576-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8a576-112">PARAMETERS</span></span>

### <span data-ttu-id="8a576-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8a576-113">-AccountName</span></span>
<span data-ttu-id="8a576-114">Nazwa konta udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="8a576-114">Azure data share account name</span></span>

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

### <span data-ttu-id="8a576-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a576-115">-DefaultProfile</span></span>
<span data-ttu-id="8a576-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8a576-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a576-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8a576-117">-Name</span></span>
<span data-ttu-id="8a576-118">Nazwa wyzwalacza udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="8a576-118">Azure data share trigger name</span></span>

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

### <span data-ttu-id="8a576-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a576-119">-ResourceGroupName</span></span>
<span data-ttu-id="8a576-120">Nazwa grupy zasobów konta usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="8a576-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="8a576-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a576-121">-ResourceId</span></span>
<span data-ttu-id="8a576-122">Identyfikator zasobu wyzwalacza</span><span class="sxs-lookup"><span data-stu-id="8a576-122">The resource id of the trigger</span></span>

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

### <span data-ttu-id="8a576-123">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="8a576-123">-ShareSubscriptionName</span></span>
<span data-ttu-id="8a576-124">Nazwa subskrypcji udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="8a576-124">Azure data share subscription name</span></span>

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

### <span data-ttu-id="8a576-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a576-125">CommonParameters</span></span>
<span data-ttu-id="8a576-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a576-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a576-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a576-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a576-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8a576-128">INPUTS</span></span>

### <span data-ttu-id="8a576-129">System. String</span><span class="sxs-lookup"><span data-stu-id="8a576-129">System.String</span></span>

## <span data-ttu-id="8a576-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8a576-130">OUTPUTS</span></span>

### <span data-ttu-id="8a576-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="8a576-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span></span>

## <span data-ttu-id="8a576-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8a576-132">NOTES</span></span>

## <span data-ttu-id="8a576-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8a576-133">RELATED LINKS</span></span>
