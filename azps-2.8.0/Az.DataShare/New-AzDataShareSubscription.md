---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSubscription.md
ms.openlocfilehash: 64309b77801646e61e3a144bc4a7405e4e978aa6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705669"
---
# <span data-ttu-id="d1a45-101">New-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="d1a45-101">New-AzDataShareSubscription</span></span>

## <span data-ttu-id="d1a45-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d1a45-102">SYNOPSIS</span></span>
<span data-ttu-id="d1a45-103">Tworzy nowy abonament udostępniania.</span><span class="sxs-lookup"><span data-stu-id="d1a45-103">Creates a new share subscription.</span></span>

## <span data-ttu-id="d1a45-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d1a45-104">SYNTAX</span></span>

```
New-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String>
 -InvitationId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1a45-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d1a45-105">DESCRIPTION</span></span>
<span data-ttu-id="d1a45-106">Polecenie cmdlet **New-AzDataShareSubscription** umożliwia utworzenie subskrypcji udziału w określonym koncie udziału danych i identyfikatorze zaproszenia.</span><span class="sxs-lookup"><span data-stu-id="d1a45-106">The **New-AzDataShareSubscription** cmdlet creates a share subscription in specified data share account and invitation id.</span></span>

## <span data-ttu-id="d1a45-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d1a45-107">EXAMPLES</span></span>

### <span data-ttu-id="d1a45-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d1a45-108">Example 1</span></span>
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

<span data-ttu-id="d1a45-109">To polecenie tworzy nową subskrypcję AdsShareSubscription dla invitaionId w obszarze konto udziału danych WikiAds.</span><span class="sxs-lookup"><span data-stu-id="d1a45-109">This commands creates a new share subscription AdsShareSubscription for invitaionId under data share account WikiAds.</span></span>

## <span data-ttu-id="d1a45-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d1a45-110">PARAMETERS</span></span>

### <span data-ttu-id="d1a45-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d1a45-111">-AccountName</span></span>
<span data-ttu-id="d1a45-112">Nazwa konta udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="d1a45-112">Azure data share account name</span></span>

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

### <span data-ttu-id="d1a45-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1a45-113">-DefaultProfile</span></span>
<span data-ttu-id="d1a45-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d1a45-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1a45-115">-InvitationId</span><span class="sxs-lookup"><span data-stu-id="d1a45-115">-InvitationId</span></span>
<span data-ttu-id="d1a45-116">Usługa Azure Data Share invitationId</span><span class="sxs-lookup"><span data-stu-id="d1a45-116">Azure data share invitationId</span></span>

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

### <span data-ttu-id="d1a45-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d1a45-117">-Name</span></span>
<span data-ttu-id="d1a45-118">Nazwa subskrypcji udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="d1a45-118">Azure data share subscription name</span></span>

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

### <span data-ttu-id="d1a45-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1a45-119">-ResourceGroupName</span></span>
<span data-ttu-id="d1a45-120">Nazwa grupy zasobów konta usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="d1a45-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="d1a45-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d1a45-121">-Confirm</span></span>
<span data-ttu-id="d1a45-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1a45-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1a45-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1a45-123">-WhatIf</span></span>
<span data-ttu-id="d1a45-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1a45-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1a45-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d1a45-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1a45-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1a45-126">CommonParameters</span></span>
<span data-ttu-id="d1a45-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1a45-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1a45-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1a45-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1a45-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d1a45-129">INPUTS</span></span>

### <span data-ttu-id="d1a45-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d1a45-130">None</span></span>

## <span data-ttu-id="d1a45-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d1a45-131">OUTPUTS</span></span>

### <span data-ttu-id="d1a45-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="d1a45-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="d1a45-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d1a45-133">NOTES</span></span>

## <span data-ttu-id="d1a45-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d1a45-134">RELATED LINKS</span></span>
