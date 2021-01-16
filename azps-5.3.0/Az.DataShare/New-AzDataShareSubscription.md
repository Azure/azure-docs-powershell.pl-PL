---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSubscription.md
ms.openlocfilehash: e6b911831a84ce708af93ef6cc7b9f9be919758b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377232"
---
# <span data-ttu-id="fe35a-101">New-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="fe35a-101">New-AzDataShareSubscription</span></span>

## <span data-ttu-id="fe35a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fe35a-102">SYNOPSIS</span></span>
<span data-ttu-id="fe35a-103">Tworzy nowy abonament udostępniania.</span><span class="sxs-lookup"><span data-stu-id="fe35a-103">Creates a new share subscription.</span></span>

## <span data-ttu-id="fe35a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fe35a-104">SYNTAX</span></span>

```
New-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String>
 -InvitationId <String> -SourceShareLocation <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe35a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fe35a-105">DESCRIPTION</span></span>
<span data-ttu-id="fe35a-106">Polecenie cmdlet **New-AzDataShareSubscription** umożliwia utworzenie subskrypcji udziału w określonym koncie udziału danych i identyfikatorze zaproszenia.</span><span class="sxs-lookup"><span data-stu-id="fe35a-106">The **New-AzDataShareSubscription** cmdlet creates a share subscription in specified data share account and invitation id.</span></span>

## <span data-ttu-id="fe35a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fe35a-107">EXAMPLES</span></span>

### <span data-ttu-id="fe35a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fe35a-108">Example 1</span></span>
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

<span data-ttu-id="fe35a-109">To polecenie tworzy nową subskrypcję AdsShareSubscription dla invitaionId w obszarze konto udziału danych WikiAds.</span><span class="sxs-lookup"><span data-stu-id="fe35a-109">This commands creates a new share subscription AdsShareSubscription for invitaionId under data share account WikiAds.</span></span>

## <span data-ttu-id="fe35a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fe35a-110">PARAMETERS</span></span>

### <span data-ttu-id="fe35a-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fe35a-111">-AccountName</span></span>
<span data-ttu-id="fe35a-112">Nazwa konta udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="fe35a-112">Azure data share account name</span></span>

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

### <span data-ttu-id="fe35a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe35a-113">-DefaultProfile</span></span>
<span data-ttu-id="fe35a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fe35a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe35a-115">-InvitationId</span><span class="sxs-lookup"><span data-stu-id="fe35a-115">-InvitationId</span></span>
<span data-ttu-id="fe35a-116">Usługa Azure Data Share invitationId</span><span class="sxs-lookup"><span data-stu-id="fe35a-116">Azure data share invitationId</span></span>

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

### <span data-ttu-id="fe35a-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fe35a-117">-Name</span></span>
<span data-ttu-id="fe35a-118">Nazwa subskrypcji udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="fe35a-118">Azure data share subscription name</span></span>

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

### <span data-ttu-id="fe35a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe35a-119">-ResourceGroupName</span></span>
<span data-ttu-id="fe35a-120">Nazwa grupy zasobów konta usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="fe35a-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="fe35a-121">-SourceShareLocation</span><span class="sxs-lookup"><span data-stu-id="fe35a-121">-SourceShareLocation</span></span>
<span data-ttu-id="fe35a-122">Lokalizacja udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="fe35a-122">Azure data share location</span></span>

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

### <span data-ttu-id="fe35a-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fe35a-123">-Confirm</span></span>
<span data-ttu-id="fe35a-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe35a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe35a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe35a-125">-WhatIf</span></span>
<span data-ttu-id="fe35a-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe35a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe35a-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fe35a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe35a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe35a-128">CommonParameters</span></span>
<span data-ttu-id="fe35a-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe35a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe35a-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fe35a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe35a-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe35a-131">INPUTS</span></span>

### <span data-ttu-id="fe35a-132">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="fe35a-132">None</span></span>

## <span data-ttu-id="fe35a-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fe35a-133">OUTPUTS</span></span>

### <span data-ttu-id="fe35a-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="fe35a-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="fe35a-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fe35a-135">NOTES</span></span>

## <span data-ttu-id="fe35a-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fe35a-136">RELATED LINKS</span></span>
