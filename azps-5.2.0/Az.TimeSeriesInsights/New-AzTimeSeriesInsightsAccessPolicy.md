---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: b9024c0d5105344fa505832a0357c55393c55ed8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337690"
---
# <span data-ttu-id="afd3c-101">New-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="afd3c-101">New-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="afd3c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="afd3c-102">SYNOPSIS</span></span>
<span data-ttu-id="afd3c-103">Tworzenie lub aktualizowanie zasad dostępu w określonym środowisku.</span><span class="sxs-lookup"><span data-stu-id="afd3c-103">Create or update an access policy in the specified environment.</span></span>

## <span data-ttu-id="afd3c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="afd3c-104">SYNTAX</span></span>

```
New-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-PrincipalObjectId <String>] [-Role <AccessPolicyRole[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="afd3c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="afd3c-105">DESCRIPTION</span></span>
<span data-ttu-id="afd3c-106">Tworzenie lub aktualizowanie zasad dostępu w określonym środowisku.</span><span class="sxs-lookup"><span data-stu-id="afd3c-106">Create or update an access policy in the specified environment.</span></span>

## <span data-ttu-id="afd3c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="afd3c-107">EXAMPLES</span></span>

### <span data-ttu-id="afd3c-108">Przykład 1: Tworzenie zasad dostępu dla określonego środowiska</span><span class="sxs-lookup"><span data-stu-id="afd3c-108">Example 1: Create an access policy for a specified environment</span></span>
```powershell
PS C:\> New-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -PrincipalObjectId ce74a389-b5e8-4f16-89c7-787031ddd903 -Role Contributor -Name policy001

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="afd3c-109">To polecenie tworzy zasady dostępu dla określonego środowiska.</span><span class="sxs-lookup"><span data-stu-id="afd3c-109">This command creates an access policy for a specified environment.</span></span>

## <span data-ttu-id="afd3c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="afd3c-110">PARAMETERS</span></span>

### <span data-ttu-id="afd3c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afd3c-111">-DefaultProfile</span></span>
<span data-ttu-id="afd3c-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="afd3c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd3c-113">— Opis</span><span class="sxs-lookup"><span data-stu-id="afd3c-113">-Description</span></span>
<span data-ttu-id="afd3c-114">Opis zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="afd3c-114">An description of the access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd3c-115">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="afd3c-115">-EnvironmentName</span></span>
<span data-ttu-id="afd3c-116">Nazwa środowiska informacji o serii czasowej skojarzonego z określoną grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="afd3c-116">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="afd3c-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="afd3c-117">-Name</span></span>
<span data-ttu-id="afd3c-118">Nazwa zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="afd3c-118">Name of the access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccessPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd3c-119">-PrincipalObjectId</span><span class="sxs-lookup"><span data-stu-id="afd3c-119">-PrincipalObjectId</span></span>
<span data-ttu-id="afd3c-120">Identyfikator obiektu (objectId) podmiotu zabezpieczeń w usłudze Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="afd3c-120">The objectId of the principal in Azure Active Directory.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd3c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afd3c-121">-ResourceGroupName</span></span>
<span data-ttu-id="afd3c-122">Nazwa grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="afd3c-122">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="afd3c-123">-Rola</span><span class="sxs-lookup"><span data-stu-id="afd3c-123">-Role</span></span>
<span data-ttu-id="afd3c-124">Lista ról, do których podmiot zabezpieczeń jest przydzielony w środowisku.</span><span class="sxs-lookup"><span data-stu-id="afd3c-124">The list of roles the principal is assigned on the environment.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.AccessPolicyRole[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd3c-125">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="afd3c-125">-SubscriptionId</span></span>
<span data-ttu-id="afd3c-126">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="afd3c-126">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd3c-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="afd3c-127">-Confirm</span></span>
<span data-ttu-id="afd3c-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afd3c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afd3c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afd3c-129">-WhatIf</span></span>
<span data-ttu-id="afd3c-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afd3c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afd3c-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="afd3c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afd3c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afd3c-132">CommonParameters</span></span>
<span data-ttu-id="afd3c-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afd3c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afd3c-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="afd3c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afd3c-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="afd3c-135">INPUTS</span></span>

## <span data-ttu-id="afd3c-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="afd3c-136">OUTPUTS</span></span>

### <span data-ttu-id="afd3c-137">Microsoft. Azure. PowerShell. polecenia. TimeSeriesInsights. models. Api20200515. IAccessPolicyResource</span><span class="sxs-lookup"><span data-stu-id="afd3c-137">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="afd3c-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="afd3c-138">NOTES</span></span>

<span data-ttu-id="afd3c-139">PISUJE</span><span class="sxs-lookup"><span data-stu-id="afd3c-139">ALIASES</span></span>

## <span data-ttu-id="afd3c-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="afd3c-140">RELATED LINKS</span></span>

