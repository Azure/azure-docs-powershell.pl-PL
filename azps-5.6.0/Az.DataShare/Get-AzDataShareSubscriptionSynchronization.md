---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: 8a80277508f9cd2998668185af6a8c0b5bbec128
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962282"
---
# <span data-ttu-id="6c14b-101">Get-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="6c14b-101">Get-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="6c14b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c14b-102">SYNOPSIS</span></span>
<span data-ttu-id="6c14b-103">Informacje o synchronizacji są uruchamiane w ramach subskrypcji udostępniania.</span><span class="sxs-lookup"><span data-stu-id="6c14b-103">Gets information about synchronization runs in share subscription.</span></span>

## <span data-ttu-id="6c14b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6c14b-104">SYNTAX</span></span>

### <span data-ttu-id="6c14b-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="6c14b-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c14b-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c14b-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscriptionSynchronization -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6c14b-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="6c14b-107">DESCRIPTION</span></span>
<span data-ttu-id="6c14b-108">Polecenie **cmdlet Get-AzDataShareSubscriptionSynchronization** udostępnia informacje o wszystkich uruchomieniach synchronizacji w subskrypcji udostępniania w ramach konta udziału danych na klientach.</span><span class="sxs-lookup"><span data-stu-id="6c14b-108">The **Get-AzDataShareSubscriptionSynchronization** cmdlet provides informaiton about all synchronization runs in a share subscription under a data share account on the consumer.</span></span>

## <span data-ttu-id="6c14b-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6c14b-109">EXAMPLES</span></span>

### <span data-ttu-id="6c14b-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6c14b-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSubscriptionSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds"  -ShareSubscriptionName "AdsShareSubscription"

durationMs        : 83660
endTime           : 7/10/2019 9:01:23 AM
message           :
startTime         : 7/10/2019 9:00:04 AM
status            : Succeeded
synchronizationId : b087e1a5-9144-4e1d-86d1-2a4adcf551d4
```

<span data-ttu-id="6c14b-111">To polecenie zawiera informacje o całej synchronizacji dla subskrypcji udostępniania AdsShareSubscription w obszarze WikiAds konta udostępniania danych.</span><span class="sxs-lookup"><span data-stu-id="6c14b-111">This command provides information about all the synchronization runs for a share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="6c14b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c14b-112">PARAMETERS</span></span>

### <span data-ttu-id="6c14b-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6c14b-113">-AccountName</span></span>
<span data-ttu-id="6c14b-114">Nazwa konta współużytkowego danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="6c14b-114">Azure data share account name</span></span>

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

### <span data-ttu-id="6c14b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c14b-115">-DefaultProfile</span></span>
<span data-ttu-id="6c14b-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6c14b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c14b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c14b-117">-ResourceGroupName</span></span>
<span data-ttu-id="6c14b-118">Nazwa grupy zasobów konta usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="6c14b-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="6c14b-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c14b-119">-ResourceId</span></span>
<span data-ttu-id="6c14b-120">Identyfikator zasobu subskrypcji udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="6c14b-120">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="6c14b-121">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="6c14b-121">-ShareSubscriptionName</span></span>
<span data-ttu-id="6c14b-122">Nazwa subskrypcji udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="6c14b-122">Azure data share subscription name</span></span>

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

### <span data-ttu-id="6c14b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c14b-123">CommonParameters</span></span>
<span data-ttu-id="6c14b-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c14b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c14b-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6c14b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c14b-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6c14b-126">INPUTS</span></span>

### <span data-ttu-id="6c14b-127">System.String</span><span class="sxs-lookup"><span data-stu-id="6c14b-127">System.String</span></span>

## <span data-ttu-id="6c14b-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6c14b-128">OUTPUTS</span></span>

### <span data-ttu-id="6c14b-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="6c14b-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="6c14b-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6c14b-130">NOTES</span></span>

## <span data-ttu-id="6c14b-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6c14b-131">RELATED LINKS</span></span>
