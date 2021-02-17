---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/grant-azdatasharesubscriptionaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Grant-AzDataShareSubscriptionAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Grant-AzDataShareSubscriptionAccess.md
ms.openlocfilehash: 4ad530fdd27c3b87b8e96e1752c00fc149c1dd42
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196531"
---
# <span data-ttu-id="5e902-101">Grant-AzDataShareSubscriptionAccess</span><span class="sxs-lookup"><span data-stu-id="5e902-101">Grant-AzDataShareSubscriptionAccess</span></span>

## <span data-ttu-id="5e902-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e902-102">SYNOPSIS</span></span>
<span data-ttu-id="5e902-103">Udziela cofniętego dostępu do subskrypcji udostępniania źródłowego</span><span class="sxs-lookup"><span data-stu-id="5e902-103">Grants a revoked share subscription access to source share</span></span>

## <span data-ttu-id="5e902-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5e902-104">SYNTAX</span></span>

### <span data-ttu-id="5e902-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="5e902-105">ByFieldsParameterSet (Default)</span></span>
```
Grant-AzDataShareSubscriptionAccess -ResourceGroupName <String> -AccountName <String> [-ShareName <String>]
 -ShareSubscriptionId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5e902-106">ByProviderShareSubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e902-106">ByProviderShareSubscriptionIdParameterSet</span></span>
```
Grant-AzDataShareSubscriptionAccess -ShareSubscriptionId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e902-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="5e902-107">DESCRIPTION</span></span>
<span data-ttu-id="5e902-108">Polecenie **cmdlet Grant-AzDataShareSubscriptionAccess** udziela subskrypcji udostępniania do udziału źródłowego</span><span class="sxs-lookup"><span data-stu-id="5e902-108">The **Grant-AzDataShareSubscriptionAccess** cmdlet grants a share subscription access to source share</span></span>

## <span data-ttu-id="5e902-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5e902-109">EXAMPLES</span></span>

### <span data-ttu-id="5e902-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5e902-110">Example 1</span></span>
```
PS C:\> Grant-AzDataShareSubscriptionAccess -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -ShareName "AdsShare" -ShareSubscriptionId 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12

Company                   : ADS
CreatedAt                 : 6/15/2019 1:02:28 AM
CreatedBy                 : abc@microsoft.com
SharedAt                  : 6/15/2019 12:08:48 AM
SharedBy                  : abc@microsoft.com
ShareSubscriptionObjectId : 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12
ShareSubscriptionStatus   : Active
Id                        : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare/shareSubscriptions/8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12
Name                      : AdsShare
Type                      : Microsoft.DataShare/ShareSubscriptions
```

<span data-ttu-id="5e902-111">Udziela dostępu do udostępniania subskrypcji oznaczonej identyfikatorem 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12</span><span class="sxs-lookup"><span data-stu-id="5e902-111">Grants access to share subscription identified by id 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12</span></span>

## <span data-ttu-id="5e902-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5e902-112">PARAMETERS</span></span>

### <span data-ttu-id="5e902-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5e902-113">-AccountName</span></span>
<span data-ttu-id="5e902-114">Nazwa konta współużytkowego danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="5e902-114">Azure data share account name</span></span>

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

### <span data-ttu-id="5e902-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e902-115">-DefaultProfile</span></span>
<span data-ttu-id="5e902-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5e902-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e902-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e902-117">-ResourceGroupName</span></span>
<span data-ttu-id="5e902-118">Nazwa grupy zasobów konta udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="5e902-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="5e902-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e902-119">-ResourceId</span></span>
<span data-ttu-id="5e902-120">Identyfikator zasobu udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="5e902-120">The resource id of the azure data share</span></span>

```yaml
Type: System.String
Parameter Sets: ByProviderShareSubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e902-121">-ShareName</span><span class="sxs-lookup"><span data-stu-id="5e902-121">-ShareName</span></span>
<span data-ttu-id="5e902-122">Nazwa udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="5e902-122">Azure data share name</span></span>

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

### <span data-ttu-id="5e902-123">-ShareSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5e902-123">-ShareSubscriptionId</span></span>
<span data-ttu-id="5e902-124">Identyfikator subskrypcji udostępniania subskrypcji dostawcy</span><span class="sxs-lookup"><span data-stu-id="5e902-124">The share subscription id of the provider share subscription</span></span>

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

### <span data-ttu-id="5e902-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5e902-125">-Confirm</span></span>
<span data-ttu-id="5e902-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5e902-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e902-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e902-127">-WhatIf</span></span>
<span data-ttu-id="5e902-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e902-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5e902-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5e902-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e902-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e902-130">CommonParameters</span></span>
<span data-ttu-id="5e902-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e902-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e902-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5e902-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e902-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5e902-133">INPUTS</span></span>

### <span data-ttu-id="5e902-134">System.String</span><span class="sxs-lookup"><span data-stu-id="5e902-134">System.String</span></span>

## <span data-ttu-id="5e902-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5e902-135">OUTPUTS</span></span>

### <span data-ttu-id="5e902-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="5e902-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="5e902-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5e902-137">NOTES</span></span>

## <span data-ttu-id="5e902-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5e902-138">RELATED LINKS</span></span>
