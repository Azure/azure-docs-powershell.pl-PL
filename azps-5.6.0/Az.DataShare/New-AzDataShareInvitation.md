---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/new-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareInvitation.md
ms.openlocfilehash: a27989a1637443335389ba8b35bd90279a8976f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996724"
---
# <span data-ttu-id="bee51-101">New-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="bee51-101">New-AzDataShareInvitation</span></span>

## <span data-ttu-id="bee51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bee51-102">SYNOPSIS</span></span>
<span data-ttu-id="bee51-103">Tworzy zaproszenie do udostępniania.</span><span class="sxs-lookup"><span data-stu-id="bee51-103">Creates an invitation for share.</span></span>

## <span data-ttu-id="bee51-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bee51-104">SYNTAX</span></span>

### <span data-ttu-id="bee51-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="bee51-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareInvitation [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bee51-106">ByInvitationEmailParameterSet</span><span class="sxs-lookup"><span data-stu-id="bee51-106">ByInvitationEmailParameterSet</span></span>
```
New-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -TargetEmail <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bee51-107">ByInvitationTenantParameterSet</span><span class="sxs-lookup"><span data-stu-id="bee51-107">ByInvitationTenantParameterSet</span></span>
```
New-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -TargetObjectId <String> -TargetTenantId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bee51-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="bee51-108">DESCRIPTION</span></span>
<span data-ttu-id="bee51-109">Polecenie **cmdlet New-AzDataShareInvitation** wysyła zaproszenie do klienta docelowego z informacjami na temat udziału dostawcy.</span><span class="sxs-lookup"><span data-stu-id="bee51-109">The **New-AzDataShareInvitation** cmdlet sends an invitation to the target consumer with information about the provider share.</span></span> 

## <span data-ttu-id="bee51-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bee51-110">EXAMPLES</span></span>

### <span data-ttu-id="bee51-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bee51-111">Example 1</span></span>
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

<span data-ttu-id="bee51-112">To polecenie powoduje utworzenie zaproszenia adsinvitation dla udostępniania usługi AdsShare i wysłanie go do docelowej wiadomości adstest@microsoft.com e-mail.</span><span class="sxs-lookup"><span data-stu-id="bee51-112">This command creates an invitation AdsInvitation for share AdsShare and sends it to target email adstest@microsoft.com.</span></span>

## <span data-ttu-id="bee51-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bee51-113">PARAMETERS</span></span>

### <span data-ttu-id="bee51-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bee51-114">-AccountName</span></span>
<span data-ttu-id="bee51-115">Nazwa konta współużytkowego danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="bee51-115">Azure data share account name</span></span>

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

### <span data-ttu-id="bee51-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bee51-116">-DefaultProfile</span></span>
<span data-ttu-id="bee51-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bee51-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bee51-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="bee51-118">-Name</span></span>
<span data-ttu-id="bee51-119">Nazwa zaproszenia do udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="bee51-119">Azure data share invitation name</span></span>

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

### <span data-ttu-id="bee51-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bee51-120">-ResourceGroupName</span></span>
<span data-ttu-id="bee51-121">Nazwa grupy zasobów konta udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="bee51-121">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="bee51-122">-ShareName</span><span class="sxs-lookup"><span data-stu-id="bee51-122">-ShareName</span></span>
<span data-ttu-id="bee51-123">Nazwa udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="bee51-123">Azure data share name</span></span>

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

### <span data-ttu-id="bee51-124">-TargetEmail</span><span class="sxs-lookup"><span data-stu-id="bee51-124">-TargetEmail</span></span>
<span data-ttu-id="bee51-125">Docelowy identyfikator e-mail</span><span class="sxs-lookup"><span data-stu-id="bee51-125">Target email id</span></span>

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

### <span data-ttu-id="bee51-126">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="bee51-126">-TargetObjectId</span></span>
<span data-ttu-id="bee51-127">Identyfikator obiektu docelowego</span><span class="sxs-lookup"><span data-stu-id="bee51-127">Target object id</span></span>

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

### <span data-ttu-id="bee51-128">-TargetTenantId</span><span class="sxs-lookup"><span data-stu-id="bee51-128">-TargetTenantId</span></span>
<span data-ttu-id="bee51-129">Identyfikator dzierżawy docelowej</span><span class="sxs-lookup"><span data-stu-id="bee51-129">Target tenant id</span></span>

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

### <span data-ttu-id="bee51-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bee51-130">-Confirm</span></span>
<span data-ttu-id="bee51-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bee51-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bee51-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bee51-132">-WhatIf</span></span>
<span data-ttu-id="bee51-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bee51-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bee51-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="bee51-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bee51-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bee51-135">CommonParameters</span></span>
<span data-ttu-id="bee51-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bee51-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bee51-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bee51-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bee51-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bee51-138">INPUTS</span></span>

### <span data-ttu-id="bee51-139">Brak</span><span class="sxs-lookup"><span data-stu-id="bee51-139">None</span></span>

## <span data-ttu-id="bee51-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bee51-140">OUTPUTS</span></span>

### <span data-ttu-id="bee51-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="bee51-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="bee51-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bee51-142">NOTES</span></span>

## <span data-ttu-id="bee51-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bee51-143">RELATED LINKS</span></span>
