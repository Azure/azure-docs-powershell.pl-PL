---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/grant-azdatasharesubscriptionaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Grant-AzDataShareSubscriptionAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Grant-AzDataShareSubscriptionAccess.md
ms.openlocfilehash: 4ad530fdd27c3b87b8e96e1752c00fc149c1dd42
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324422"
---
# <span data-ttu-id="566b7-101">Grant-AzDataShareSubscriptionAccess</span><span class="sxs-lookup"><span data-stu-id="566b7-101">Grant-AzDataShareSubscriptionAccess</span></span>

## <span data-ttu-id="566b7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="566b7-102">SYNOPSIS</span></span>
<span data-ttu-id="566b7-103">Udziela odwołanego udziału w subskrypcji dla udziału źródłowego</span><span class="sxs-lookup"><span data-stu-id="566b7-103">Grants a revoked share subscription access to source share</span></span>

## <span data-ttu-id="566b7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="566b7-104">SYNTAX</span></span>

### <span data-ttu-id="566b7-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="566b7-105">ByFieldsParameterSet (Default)</span></span>
```
Grant-AzDataShareSubscriptionAccess -ResourceGroupName <String> -AccountName <String> [-ShareName <String>]
 -ShareSubscriptionId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="566b7-106">ByProviderShareSubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="566b7-106">ByProviderShareSubscriptionIdParameterSet</span></span>
```
Grant-AzDataShareSubscriptionAccess -ShareSubscriptionId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="566b7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="566b7-107">DESCRIPTION</span></span>
<span data-ttu-id="566b7-108">Polecenie cmdlet **Grant-AzDataShareSubscriptionAccess** udziela abonamentu na udostępnianie do udziału źródłowego</span><span class="sxs-lookup"><span data-stu-id="566b7-108">The **Grant-AzDataShareSubscriptionAccess** cmdlet grants a share subscription access to source share</span></span>

## <span data-ttu-id="566b7-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="566b7-109">EXAMPLES</span></span>

### <span data-ttu-id="566b7-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="566b7-110">Example 1</span></span>
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

<span data-ttu-id="566b7-111">Udziela prawa do udostępniania subskrypcji określonego przez identyfikator 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12</span><span class="sxs-lookup"><span data-stu-id="566b7-111">Grants access to share subscription identified by id 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12</span></span>

## <span data-ttu-id="566b7-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="566b7-112">PARAMETERS</span></span>

### <span data-ttu-id="566b7-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="566b7-113">-AccountName</span></span>
<span data-ttu-id="566b7-114">Nazwa konta udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="566b7-114">Azure data share account name</span></span>

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

### <span data-ttu-id="566b7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="566b7-115">-DefaultProfile</span></span>
<span data-ttu-id="566b7-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="566b7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="566b7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="566b7-117">-ResourceGroupName</span></span>
<span data-ttu-id="566b7-118">Nazwa grupy zasobów konta usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="566b7-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="566b7-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="566b7-119">-ResourceId</span></span>
<span data-ttu-id="566b7-120">Identyfikator zasobu udziału danych usługi Azure</span><span class="sxs-lookup"><span data-stu-id="566b7-120">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="566b7-121">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="566b7-121">-ShareName</span></span>
<span data-ttu-id="566b7-122">Nazwa udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="566b7-122">Azure data share name</span></span>

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

### <span data-ttu-id="566b7-123">-ShareSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="566b7-123">-ShareSubscriptionId</span></span>
<span data-ttu-id="566b7-124">Identyfikator subskrypcji udziału dostawcy z subskrypcją</span><span class="sxs-lookup"><span data-stu-id="566b7-124">The share subscription id of the provider share subscription</span></span>

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

### <span data-ttu-id="566b7-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="566b7-125">-Confirm</span></span>
<span data-ttu-id="566b7-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="566b7-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="566b7-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="566b7-127">-WhatIf</span></span>
<span data-ttu-id="566b7-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="566b7-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="566b7-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="566b7-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="566b7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="566b7-130">CommonParameters</span></span>
<span data-ttu-id="566b7-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="566b7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="566b7-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="566b7-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="566b7-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="566b7-133">INPUTS</span></span>

### <span data-ttu-id="566b7-134">System. String</span><span class="sxs-lookup"><span data-stu-id="566b7-134">System.String</span></span>

## <span data-ttu-id="566b7-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="566b7-135">OUTPUTS</span></span>

### <span data-ttu-id="566b7-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="566b7-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="566b7-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="566b7-137">NOTES</span></span>

## <span data-ttu-id="566b7-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="566b7-138">RELATED LINKS</span></span>
