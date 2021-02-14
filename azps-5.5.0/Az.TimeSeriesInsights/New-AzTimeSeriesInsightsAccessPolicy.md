---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: b9024c0d5105344fa505832a0357c55393c55ed8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197290"
---
# <span data-ttu-id="fee42-101">New-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fee42-101">New-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="fee42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fee42-102">SYNOPSIS</span></span>
<span data-ttu-id="fee42-103">Tworzenie lub aktualizowanie zasad dostępu w określonym środowisku.</span><span class="sxs-lookup"><span data-stu-id="fee42-103">Create or update an access policy in the specified environment.</span></span>

## <span data-ttu-id="fee42-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fee42-104">SYNTAX</span></span>

```
New-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-PrincipalObjectId <String>] [-Role <AccessPolicyRole[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fee42-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="fee42-105">DESCRIPTION</span></span>
<span data-ttu-id="fee42-106">Tworzenie lub aktualizowanie zasad dostępu w określonym środowisku.</span><span class="sxs-lookup"><span data-stu-id="fee42-106">Create or update an access policy in the specified environment.</span></span>

## <span data-ttu-id="fee42-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fee42-107">EXAMPLES</span></span>

### <span data-ttu-id="fee42-108">Przykład 1. Tworzenie zasad dostępu dla określonego środowiska</span><span class="sxs-lookup"><span data-stu-id="fee42-108">Example 1: Create an access policy for a specified environment</span></span>
```powershell
PS C:\> New-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -PrincipalObjectId ce74a389-b5e8-4f16-89c7-787031ddd903 -Role Contributor -Name policy001

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="fee42-109">To polecenie tworzy zasady dostępu dla określonego środowiska.</span><span class="sxs-lookup"><span data-stu-id="fee42-109">This command creates an access policy for a specified environment.</span></span>

## <span data-ttu-id="fee42-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fee42-110">PARAMETERS</span></span>

### <span data-ttu-id="fee42-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fee42-111">-DefaultProfile</span></span>
<span data-ttu-id="fee42-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fee42-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fee42-113">— Opis</span><span class="sxs-lookup"><span data-stu-id="fee42-113">-Description</span></span>
<span data-ttu-id="fee42-114">Opis zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="fee42-114">An description of the access policy.</span></span>

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

### <span data-ttu-id="fee42-115">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="fee42-115">-EnvironmentName</span></span>
<span data-ttu-id="fee42-116">Nazwa środowiska szczegółowych informacji szeregu czasowego skojarzonego z określoną grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="fee42-116">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="fee42-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fee42-117">-Name</span></span>
<span data-ttu-id="fee42-118">Nazwa zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="fee42-118">Name of the access policy.</span></span>

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

### <span data-ttu-id="fee42-119">-PrincipalObjectId</span><span class="sxs-lookup"><span data-stu-id="fee42-119">-PrincipalObjectId</span></span>
<span data-ttu-id="fee42-120">ObjectId podmiotu zabezpieczeń w usłudze Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="fee42-120">The objectId of the principal in Azure Active Directory.</span></span>

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

### <span data-ttu-id="fee42-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fee42-121">-ResourceGroupName</span></span>
<span data-ttu-id="fee42-122">Nazwa grupy usługi Azure Resource.</span><span class="sxs-lookup"><span data-stu-id="fee42-122">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="fee42-123">- Rola</span><span class="sxs-lookup"><span data-stu-id="fee42-123">-Role</span></span>
<span data-ttu-id="fee42-124">Lista ról przypisanych do środowiska przez podmiot zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="fee42-124">The list of roles the principal is assigned on the environment.</span></span>

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

### <span data-ttu-id="fee42-125">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fee42-125">-SubscriptionId</span></span>
<span data-ttu-id="fee42-126">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fee42-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="fee42-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fee42-127">-Confirm</span></span>
<span data-ttu-id="fee42-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fee42-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fee42-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fee42-129">-WhatIf</span></span>
<span data-ttu-id="fee42-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fee42-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fee42-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="fee42-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fee42-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fee42-132">CommonParameters</span></span>
<span data-ttu-id="fee42-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fee42-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fee42-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fee42-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fee42-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fee42-135">INPUTS</span></span>

## <span data-ttu-id="fee42-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fee42-136">OUTPUTS</span></span>

### <span data-ttu-id="fee42-137">Microsoft.Azure.PowerShell.Cmdlet.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span><span class="sxs-lookup"><span data-stu-id="fee42-137">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="fee42-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fee42-138">NOTES</span></span>

<span data-ttu-id="fee42-139">ALIASY</span><span class="sxs-lookup"><span data-stu-id="fee42-139">ALIASES</span></span>

## <span data-ttu-id="fee42-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fee42-140">RELATED LINKS</span></span>

