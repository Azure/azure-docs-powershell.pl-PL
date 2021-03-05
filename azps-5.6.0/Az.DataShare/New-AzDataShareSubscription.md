---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/new-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSubscription.md
ms.openlocfilehash: a7b3a60d97692d01eb8be374ab9670af4b331f95
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996710"
---
# <span data-ttu-id="ed074-101">New-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="ed074-101">New-AzDataShareSubscription</span></span>

## <span data-ttu-id="ed074-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed074-102">SYNOPSIS</span></span>
<span data-ttu-id="ed074-103">Tworzy nową subskrypcję udostępniania.</span><span class="sxs-lookup"><span data-stu-id="ed074-103">Creates a new share subscription.</span></span>

## <span data-ttu-id="ed074-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ed074-104">SYNTAX</span></span>

```
New-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String>
 -InvitationId <String> -SourceShareLocation <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed074-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ed074-105">DESCRIPTION</span></span>
<span data-ttu-id="ed074-106">Polecenie **cmdlet New-AzDataShareSubscription** tworzy subskrypcję udostępniania w określonym koncie udziału danych i identyfikatorze zaproszenia.</span><span class="sxs-lookup"><span data-stu-id="ed074-106">The **New-AzDataShareSubscription** cmdlet creates a share subscription in specified data share account and invitation id.</span></span>

## <span data-ttu-id="ed074-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ed074-107">EXAMPLES</span></span>

### <span data-ttu-id="ed074-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ed074-108">Example 1</span></span>
```
PS C:\> New-AzDataShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShareSubscription" -InvitationId "167e06ff-567f-4bc7-be0c-645a6de710f3"
CreatedAt               : 6/30/2019 12:42:12 AM
CreatedBy               : adstest@microsoft.com
InvitationId            : 167e06ff-567f-4bc7-be0c-645a6de710f3
ProvisioningState       : Succeeded
ShareName               : AdsShare
ShareSender             : adsprovider@microsoft.com
ShareSenderCompanyName  : ADS Company
ShareDescription        : Test description  
ShareTerms              : Test terms of use
ShareSubscriptionStatus : Active
ShareKind               : CopyBased
Id                      : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription
Name                    : AdsShareSubscription
Type                    : Microsoft.DataShare/ShareSubscriptions
```

<span data-ttu-id="ed074-109">To polecenia tworzy nową subskrypcję udostępniania AdsShareSubscription dla inpalionId w obszarze wikiAds konta udostępniania danych.</span><span class="sxs-lookup"><span data-stu-id="ed074-109">This commands creates a new share subscription AdsShareSubscription for invitaionId under data share account WikiAds.</span></span>

## <span data-ttu-id="ed074-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed074-110">PARAMETERS</span></span>

### <span data-ttu-id="ed074-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ed074-111">-AccountName</span></span>
<span data-ttu-id="ed074-112">Nazwa konta współużytkowego danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="ed074-112">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed074-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed074-113">-DefaultProfile</span></span>
<span data-ttu-id="ed074-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ed074-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed074-115">- InvitationId</span><span class="sxs-lookup"><span data-stu-id="ed074-115">-InvitationId</span></span>
<span data-ttu-id="ed074-116">Azure data share invitationId</span><span class="sxs-lookup"><span data-stu-id="ed074-116">Azure data share invitationId</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed074-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ed074-117">-Name</span></span>
<span data-ttu-id="ed074-118">Nazwa subskrypcji udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="ed074-118">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed074-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed074-119">-ResourceGroupName</span></span>
<span data-ttu-id="ed074-120">Nazwa grupy zasobów konta udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="ed074-120">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed074-121">-SourceShareLocation</span><span class="sxs-lookup"><span data-stu-id="ed074-121">-SourceShareLocation</span></span>
<span data-ttu-id="ed074-122">Lokalizacja udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="ed074-122">Azure data share location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed074-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ed074-123">-Confirm</span></span>
<span data-ttu-id="ed074-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ed074-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed074-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed074-125">-WhatIf</span></span>
<span data-ttu-id="ed074-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed074-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed074-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ed074-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed074-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed074-128">CommonParameters</span></span>
<span data-ttu-id="ed074-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed074-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed074-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed074-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed074-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ed074-131">INPUTS</span></span>

### <span data-ttu-id="ed074-132">Brak</span><span class="sxs-lookup"><span data-stu-id="ed074-132">None</span></span>

## <span data-ttu-id="ed074-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ed074-133">OUTPUTS</span></span>

### <span data-ttu-id="ed074-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="ed074-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="ed074-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ed074-135">NOTES</span></span>

## <span data-ttu-id="ed074-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ed074-136">RELATED LINKS</span></span>
