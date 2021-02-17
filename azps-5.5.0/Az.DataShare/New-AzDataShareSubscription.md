---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSubscription.md
ms.openlocfilehash: e6b911831a84ce708af93ef6cc7b9f9be919758b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198050"
---
# <span data-ttu-id="49609-101">New-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="49609-101">New-AzDataShareSubscription</span></span>

## <span data-ttu-id="49609-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49609-102">SYNOPSIS</span></span>
<span data-ttu-id="49609-103">Tworzy nową subskrypcję udostępniania.</span><span class="sxs-lookup"><span data-stu-id="49609-103">Creates a new share subscription.</span></span>

## <span data-ttu-id="49609-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="49609-104">SYNTAX</span></span>

```
New-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String>
 -InvitationId <String> -SourceShareLocation <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49609-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="49609-105">DESCRIPTION</span></span>
<span data-ttu-id="49609-106">Polecenie **cmdlet New-AzDataShareSubscription** tworzy subskrypcję udostępniania w określonym koncie udziału danych i identyfikatorze zaproszenia.</span><span class="sxs-lookup"><span data-stu-id="49609-106">The **New-AzDataShareSubscription** cmdlet creates a share subscription in specified data share account and invitation id.</span></span>

## <span data-ttu-id="49609-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="49609-107">EXAMPLES</span></span>

### <span data-ttu-id="49609-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="49609-108">Example 1</span></span>
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

<span data-ttu-id="49609-109">To polecenia tworzy nową subskrypcję udostępniania AdsShareSubscription dla inpalionId w obszarze wikiAds konta udostępniania danych.</span><span class="sxs-lookup"><span data-stu-id="49609-109">This commands creates a new share subscription AdsShareSubscription for invitaionId under data share account WikiAds.</span></span>

## <span data-ttu-id="49609-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49609-110">PARAMETERS</span></span>

### <span data-ttu-id="49609-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="49609-111">-AccountName</span></span>
<span data-ttu-id="49609-112">Nazwa konta współużytkowego danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="49609-112">Azure data share account name</span></span>

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

### <span data-ttu-id="49609-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49609-113">-DefaultProfile</span></span>
<span data-ttu-id="49609-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="49609-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49609-115">- InvitationId</span><span class="sxs-lookup"><span data-stu-id="49609-115">-InvitationId</span></span>
<span data-ttu-id="49609-116">Azure data share invitationId</span><span class="sxs-lookup"><span data-stu-id="49609-116">Azure data share invitationId</span></span>

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

### <span data-ttu-id="49609-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="49609-117">-Name</span></span>
<span data-ttu-id="49609-118">Nazwa subskrypcji udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="49609-118">Azure data share subscription name</span></span>

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

### <span data-ttu-id="49609-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49609-119">-ResourceGroupName</span></span>
<span data-ttu-id="49609-120">Nazwa grupy zasobów konta udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="49609-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="49609-121">-SourceShareLocation</span><span class="sxs-lookup"><span data-stu-id="49609-121">-SourceShareLocation</span></span>
<span data-ttu-id="49609-122">Lokalizacja udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="49609-122">Azure data share location</span></span>

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

### <span data-ttu-id="49609-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="49609-123">-Confirm</span></span>
<span data-ttu-id="49609-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="49609-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49609-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49609-125">-WhatIf</span></span>
<span data-ttu-id="49609-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49609-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49609-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="49609-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49609-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49609-128">CommonParameters</span></span>
<span data-ttu-id="49609-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49609-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49609-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49609-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49609-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49609-131">INPUTS</span></span>

### <span data-ttu-id="49609-132">Brak</span><span class="sxs-lookup"><span data-stu-id="49609-132">None</span></span>

## <span data-ttu-id="49609-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="49609-133">OUTPUTS</span></span>

### <span data-ttu-id="49609-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="49609-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="49609-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="49609-135">NOTES</span></span>

## <span data-ttu-id="49609-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="49609-136">RELATED LINKS</span></span>
