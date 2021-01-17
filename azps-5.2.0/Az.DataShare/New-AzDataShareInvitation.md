---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareInvitation.md
ms.openlocfilehash: ea042cb0db8fcb1995a935086d188efbb6c0647f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324371"
---
# <span data-ttu-id="107fb-101">New-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="107fb-101">New-AzDataShareInvitation</span></span>

## <span data-ttu-id="107fb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="107fb-102">SYNOPSIS</span></span>
<span data-ttu-id="107fb-103">Tworzy zaproszenie do udostępnienia.</span><span class="sxs-lookup"><span data-stu-id="107fb-103">Creates an invitation for share.</span></span>

## <span data-ttu-id="107fb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="107fb-104">SYNTAX</span></span>

### <span data-ttu-id="107fb-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="107fb-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareInvitation [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="107fb-106">ByInvitationEmailParameterSet</span><span class="sxs-lookup"><span data-stu-id="107fb-106">ByInvitationEmailParameterSet</span></span>
```
New-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -TargetEmail <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="107fb-107">ByInvitationTenantParameterSet</span><span class="sxs-lookup"><span data-stu-id="107fb-107">ByInvitationTenantParameterSet</span></span>
```
New-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -TargetObjectId <String> -TargetTenantId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="107fb-108">Opis</span><span class="sxs-lookup"><span data-stu-id="107fb-108">DESCRIPTION</span></span>
<span data-ttu-id="107fb-109">Polecenie cmdlet **New-AzDataShareInvitation** wysyła zaproszenie do konsumenta docelowego, korzystając z informacji o udziale dostawcy.</span><span class="sxs-lookup"><span data-stu-id="107fb-109">The **New-AzDataShareInvitation** cmdlet sends an invitation to the target consumer with information about the provider share.</span></span> 

## <span data-ttu-id="107fb-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="107fb-110">EXAMPLES</span></span>

### <span data-ttu-id="107fb-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="107fb-111">Example 1</span></span>
```
PS C:\> New-AzDataShareInvitation -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsInvitation" -TargetEmail "adstest@microsoft.com"
InvitationId     : 167e06ff-567f-4bc7-be0c-645a6de710f3
InvitationStatus : Pending
Sender           : adsprovider@microsoft.com
SentAt           : 7/8/2019 10:47:10 PM
TargetEmail      : adstest@microsoft.com
TargetObjectId   :
TargetTenantId   :
Id               : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/        providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/invitations/AdsInvitation
Name             : AdsInvitation
Type             : Microsoft.DataShare/Invitations
```

<span data-ttu-id="107fb-112">To polecenie tworzy AdsInvitation zaproszenia do udostępniania AdsShare i wysyła je do docelowej poczty e-mail adstest@microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="107fb-112">This command creates an invitation AdsInvitation for share AdsShare and sends it to target email adstest@microsoft.com.</span></span>

## <span data-ttu-id="107fb-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="107fb-113">PARAMETERS</span></span>

### <span data-ttu-id="107fb-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="107fb-114">-AccountName</span></span>
<span data-ttu-id="107fb-115">Nazwa konta udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="107fb-115">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet, ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="107fb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="107fb-116">-DefaultProfile</span></span>
<span data-ttu-id="107fb-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="107fb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="107fb-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="107fb-118">-Name</span></span>
<span data-ttu-id="107fb-119">Nazwa zaproszenia do udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="107fb-119">Azure data share invitation name</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet, ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="107fb-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="107fb-120">-ResourceGroupName</span></span>
<span data-ttu-id="107fb-121">Nazwa grupy zasobów konta usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="107fb-121">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet, ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="107fb-122">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="107fb-122">-ShareName</span></span>
<span data-ttu-id="107fb-123">Nazwa udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="107fb-123">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet, ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="107fb-124">-TargetEmail</span><span class="sxs-lookup"><span data-stu-id="107fb-124">-TargetEmail</span></span>
<span data-ttu-id="107fb-125">Docelowy identyfikator e-mail</span><span class="sxs-lookup"><span data-stu-id="107fb-125">Target email id</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="107fb-126">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="107fb-126">-TargetObjectId</span></span>
<span data-ttu-id="107fb-127">Identyfikator obiektu docelowego</span><span class="sxs-lookup"><span data-stu-id="107fb-127">Target object id</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="107fb-128">-TargetTenantId</span><span class="sxs-lookup"><span data-stu-id="107fb-128">-TargetTenantId</span></span>
<span data-ttu-id="107fb-129">Identyfikator dzierżawy docelowej</span><span class="sxs-lookup"><span data-stu-id="107fb-129">Target tenant id</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="107fb-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="107fb-130">-Confirm</span></span>
<span data-ttu-id="107fb-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="107fb-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="107fb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="107fb-132">-WhatIf</span></span>
<span data-ttu-id="107fb-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="107fb-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="107fb-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="107fb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="107fb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="107fb-135">CommonParameters</span></span>
<span data-ttu-id="107fb-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="107fb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="107fb-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="107fb-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="107fb-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="107fb-138">INPUTS</span></span>

### <span data-ttu-id="107fb-139">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="107fb-139">None</span></span>

## <span data-ttu-id="107fb-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="107fb-140">OUTPUTS</span></span>

### <span data-ttu-id="107fb-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="107fb-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="107fb-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="107fb-142">NOTES</span></span>

## <span data-ttu-id="107fb-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="107fb-143">RELATED LINKS</span></span>
