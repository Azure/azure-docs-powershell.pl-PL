---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: f1527cfcb947f802cb4a2710ab2f25a1d7b9bf75
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223985"
---
# <span data-ttu-id="b4443-101">Get-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="b4443-101">Get-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="b4443-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b4443-102">SYNOPSIS</span></span>
<span data-ttu-id="b4443-103">Pobiera informacje o synchronizacji są uruchamiane w ramach akcji Udostępnij.</span><span class="sxs-lookup"><span data-stu-id="b4443-103">Gets information about synchronization runs in share subscription.</span></span>

## <span data-ttu-id="b4443-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b4443-104">SYNTAX</span></span>

### <span data-ttu-id="b4443-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b4443-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4443-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4443-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscriptionSynchronization -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b4443-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b4443-107">DESCRIPTION</span></span>
<span data-ttu-id="b4443-108">Polecenie cmdlet **Get-AzDataShareSubscriptionSynchronization** zawiera informaiton o wszystkich synchronizacjach w subskrypcji udostępnionej w ramach konta udziału danych w danym klienta.</span><span class="sxs-lookup"><span data-stu-id="b4443-108">The **Get-AzDataShareSubscriptionSynchronization** cmdlet provides informaiton about all synchronization runs in a share subscription under a data share account on the consumer.</span></span>

## <span data-ttu-id="b4443-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b4443-109">EXAMPLES</span></span>

### <span data-ttu-id="b4443-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b4443-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSubscriptionSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds"  -ShareSubscriptionName "AdsShareSubscription"

durationMs        : 83660
endTime           : 7/10/2019 9:01:23 AM
message           :
startTime         : 7/10/2019 9:00:04 AM
status            : Succeeded
synchronizationId : b087e1a5-9144-4e1d-86d1-2a4adcf551d4
```

<span data-ttu-id="b4443-111">To polecenie udostępnia informacje o wszystkich synchronizacjach dla subskrypcji udziału AdsShareSubscription w obszarze WikiAds konta udostępniania danych.</span><span class="sxs-lookup"><span data-stu-id="b4443-111">This command provides information about all the synchronization runs for a share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="b4443-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b4443-112">PARAMETERS</span></span>

### <span data-ttu-id="b4443-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b4443-113">-AccountName</span></span>
<span data-ttu-id="b4443-114">Nazwa konta udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="b4443-114">Azure data share account name</span></span>

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

### <span data-ttu-id="b4443-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4443-115">-DefaultProfile</span></span>
<span data-ttu-id="b4443-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b4443-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4443-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4443-117">-ResourceGroupName</span></span>
<span data-ttu-id="b4443-118">Nazwa grupy zasobów konta usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="b4443-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="b4443-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4443-119">-ResourceId</span></span>
<span data-ttu-id="b4443-120">Identyfikator zasobu subskrypcji usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="b4443-120">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="b4443-121">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="b4443-121">-ShareSubscriptionName</span></span>
<span data-ttu-id="b4443-122">Nazwa subskrypcji udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="b4443-122">Azure data share subscription name</span></span>

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

### <span data-ttu-id="b4443-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4443-123">CommonParameters</span></span>
<span data-ttu-id="b4443-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4443-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4443-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4443-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4443-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b4443-126">INPUTS</span></span>

### <span data-ttu-id="b4443-127">System. String</span><span class="sxs-lookup"><span data-stu-id="b4443-127">System.String</span></span>

## <span data-ttu-id="b4443-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b4443-128">OUTPUTS</span></span>

### <span data-ttu-id="b4443-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="b4443-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="b4443-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b4443-130">NOTES</span></span>

## <span data-ttu-id="b4443-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b4443-131">RELATED LINKS</span></span>
