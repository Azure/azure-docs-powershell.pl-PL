---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/revoke-azdatasharesubscriptionaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Revoke-AzDataShareSubscriptionAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Revoke-AzDataShareSubscriptionAccess.md
ms.openlocfilehash: 540426cc8612f4cee7364a7875bb9a142bca07ef
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305118"
---
# <span data-ttu-id="5572b-101">Revoke-AzDataShareSubscriptionAccess</span><span class="sxs-lookup"><span data-stu-id="5572b-101">Revoke-AzDataShareSubscriptionAccess</span></span>

## <span data-ttu-id="5572b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5572b-102">SYNOPSIS</span></span>
<span data-ttu-id="5572b-103">Odwoływanie udostępniania abonamentu dostęp do udziału źródłowego</span><span class="sxs-lookup"><span data-stu-id="5572b-103">Revokes share subscription access to source share</span></span>

## <span data-ttu-id="5572b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5572b-104">SYNTAX</span></span>

### <span data-ttu-id="5572b-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5572b-105">ByFieldsParameterSet (Default)</span></span>
```
Revoke-AzDataShareSubscriptionAccess -ResourceGroupName <String> -AccountName <String> [-ShareName <String>]
 -ShareSubscriptionId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5572b-106">ByProviderShareSubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5572b-106">ByProviderShareSubscriptionIdParameterSet</span></span>
```
Revoke-AzDataShareSubscriptionAccess -ShareSubscriptionId <String> -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5572b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5572b-107">DESCRIPTION</span></span>
<span data-ttu-id="5572b-108">Polecenie cmdlet **REVOKE-AzDataShareSubscriptionAccess** udziela abonamentu na udostępnianie uprawnień do udziału źródłowego</span><span class="sxs-lookup"><span data-stu-id="5572b-108">The **Revoke-AzDataShareSubscriptionAccess** cmdlet grants a share subscription access to source share</span></span>

## <span data-ttu-id="5572b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5572b-109">EXAMPLES</span></span>

### <span data-ttu-id="5572b-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5572b-110">Example 1</span></span>
```
PS C:\> Revoke-AzDataShareSubscriptionAccess -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -ShareName "AdsShare" -ShareSubscriptionId 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12

Company                   : ADS
CreatedAt                 : 6/15/2019 1:02:28 AM
CreatedBy                 : abc@microsoft.com
SharedAt                  : 6/15/2019 12:08:48 AM
SharedBy                  : abc@microsoft.com
ShareSubscriptionObjectId : 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12
ShareSubscriptionStatus   : Revoked
Id                        : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare/shareSubscriptions/8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12
Name                      : AdsShare
Type                      : Microsoft.DataShare/ShareSubscriptions
```

<span data-ttu-id="5572b-111">Odwołuje się do abonamentu udziału określonego za pomocą identyfikatora 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12</span><span class="sxs-lookup"><span data-stu-id="5572b-111">Revokes access of share subscription identified by id 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12</span></span>

## <span data-ttu-id="5572b-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5572b-112">PARAMETERS</span></span>

### <span data-ttu-id="5572b-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5572b-113">-AccountName</span></span>
<span data-ttu-id="5572b-114">Nazwa konta udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="5572b-114">Azure data share account name</span></span>

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

### <span data-ttu-id="5572b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5572b-115">-AsJob</span></span>
<span data-ttu-id="5572b-116">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="5572b-116">{{Fill AsJob Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5572b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5572b-117">-DefaultProfile</span></span>
<span data-ttu-id="5572b-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5572b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5572b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5572b-119">-ResourceGroupName</span></span>
<span data-ttu-id="5572b-120">Nazwa grupy zasobów konta usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="5572b-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="5572b-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5572b-121">-ResourceId</span></span>
<span data-ttu-id="5572b-122">Identyfikator zasobu udziału danych usługi Azure</span><span class="sxs-lookup"><span data-stu-id="5572b-122">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="5572b-123">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="5572b-123">-ShareName</span></span>
<span data-ttu-id="5572b-124">Nazwa udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="5572b-124">Azure data share name</span></span>

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

### <span data-ttu-id="5572b-125">-ShareSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5572b-125">-ShareSubscriptionId</span></span>
<span data-ttu-id="5572b-126">Identyfikator subskrypcji udziału dostawcy z subskrypcją</span><span class="sxs-lookup"><span data-stu-id="5572b-126">The share subscription id of the provider share subscription</span></span>

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

### <span data-ttu-id="5572b-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5572b-127">-Confirm</span></span>
<span data-ttu-id="5572b-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5572b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5572b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5572b-129">-WhatIf</span></span>
<span data-ttu-id="5572b-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5572b-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5572b-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5572b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5572b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5572b-132">CommonParameters</span></span>
<span data-ttu-id="5572b-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5572b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5572b-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5572b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5572b-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5572b-135">INPUTS</span></span>

### <span data-ttu-id="5572b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="5572b-136">System.String</span></span>

## <span data-ttu-id="5572b-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5572b-137">OUTPUTS</span></span>

### <span data-ttu-id="5572b-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="5572b-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="5572b-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5572b-139">NOTES</span></span>

## <span data-ttu-id="5572b-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5572b-140">RELATED LINKS</span></span>
