---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsights.md
ms.openlocfilehash: 943089433ca7007ef81648846a48ebdd5684bab2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195307"
---
# <span data-ttu-id="64806-101">Get-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="64806-101">Get-AzApplicationInsights</span></span>

## <span data-ttu-id="64806-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64806-102">SYNOPSIS</span></span>
<span data-ttu-id="64806-103">Uzyskiwanie zasobów szczegółowych informacji o aplikacjach</span><span class="sxs-lookup"><span data-stu-id="64806-103">Get application insights resources</span></span>

## <span data-ttu-id="64806-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="64806-104">SYNTAX</span></span>

### <span data-ttu-id="64806-105">ResourceGroupParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="64806-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzApplicationInsights [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="64806-106">ComponentNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="64806-106">ComponentNameParameterSet</span></span>
```
Get-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Full]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64806-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="64806-107">ResourceIdParameterSet</span></span>
```
Get-AzApplicationInsights [-ResourceId] <String> [-Full] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="64806-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="64806-108">DESCRIPTION</span></span>
<span data-ttu-id="64806-109">Uzyskiwanie zasobów szczegółowych informacji o aplikacjach w grupie zasobów lub określonym zasobie</span><span class="sxs-lookup"><span data-stu-id="64806-109">Get application insights resources in a resource group or specific resource</span></span>

## <span data-ttu-id="64806-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="64806-110">EXAMPLES</span></span>

### <span data-ttu-id="64806-111">Przykład 1. Uzyskiwanie zasobów szczegółowych informacji o aplikacjach</span><span class="sxs-lookup"><span data-stu-id="64806-111">Example 1 Get application insights resource</span></span>
```
PS C:\> Get-AzApplicationInsights -ResourceGroupName "testgroup" -Name "test"

Id                 : /subscriptions/{subid}/resourceGroups/testgroup/providers/microsoft.insights/components/test
ResourceGroupName  : testgroup
Name               : test
Kind               : web
Location           : eastus
Type               : microsoft.insights/components
AppId              : 7c8f0641-d307-41bc-b8f2-d30701adb4b3
ApplicationType    : web
Tags               : {}
CreationDate       : 7/5/2017 4:37:22 PM
FlowType           : Redfield
HockeyAppId        :
HockeyAppToken     :
InstrumentationKey : 1e30d092-4b4b-47c6-ad39-7c10785d80f5
ProvisioningState  : Succeeded
RequestSource      : IbizaAIExtension
SamplingPercentage :
TenantId           : b90b0dec-9b9a-4778-a84e-4ffb73bb17f7
```

<span data-ttu-id="64806-112">Uzyskiwanie zasobu szczegółowych informacji o nazwie "test" w grupie zasobów "grupa testowa"</span><span class="sxs-lookup"><span data-stu-id="64806-112">Get application insights resource named "test" in resource group "testgroup"</span></span>

### <span data-ttu-id="64806-113">Przykład 2. Uzyskiwanie zasobów szczegółowych informacji o aplikacjach z informacjami o planie cen</span><span class="sxs-lookup"><span data-stu-id="64806-113">Example 2 Get application insights resource with pricing plan information</span></span>
```
PS C:\> Get-AzApplicationInsights -ResourceGroupName "testgroup" -Name "test" -IncludePricingPlan

Cap                            : 330
ResetTime                      : 0
StopSendNotificationWhenHitCap : True
CapExpirationTime              :
IsCapped                       : False
Id                 : /subscriptions/{subid}/resourceGroups/testgroup/providers/microsoft.insights/components/test
ResourceGroupName  : testgroup
Name               : test
Kind               : web
Location           : eastus
Type               : microsoft.insights/components
AppId              : 7c8f0641-d307-41bc-b8f2-d30701adb4b3
ApplicationType    : web
Tags               : {}
CreationDate       : 7/5/2017 4:37:22 PM
FlowType           : Redfield
HockeyAppId        :
HockeyAppToken     :
InstrumentationKey : 1e30d092-4b4b-47c6-ad39-7c10785d80f5
ProvisioningState  : Succeeded
RequestSource      : IbizaAIExtension
SamplingPercentage :
TenantId           : b90b0dec-9b9a-4778-a84e-4ffb73bb17f7
PricingPlan        : Basic
```

<span data-ttu-id="64806-114">Uzyskiwanie zasobów szczegółowych informacji o aplikacjach i dołączanie informacji o planie cenowym dla zasobu o nazwie "test" w grupie zasobów "grupa testowa"</span><span class="sxs-lookup"><span data-stu-id="64806-114">Get application insights resource and include pricing plan information for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="64806-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64806-115">PARAMETERS</span></span>

### <span data-ttu-id="64806-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64806-116">-DefaultProfile</span></span>
<span data-ttu-id="64806-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="64806-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64806-118">— Pełne</span><span class="sxs-lookup"><span data-stu-id="64806-118">-Full</span></span>
<span data-ttu-id="64806-119">Jeśli zostanie określona, zostanie ponownie określony plan cenowy/dzienny limit i stan składnika szczegółowych informacji o aplikacjach.</span><span class="sxs-lookup"><span data-stu-id="64806-119">If specified, it will get back pricing plan/daily cap and status of the application insights component.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ComponentNameParameterSet, ResourceIdParameterSet
Aliases: IncludeDailyCap, IncludeDailyCapStatus, IncludePricingPlan

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64806-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="64806-120">-Name</span></span>
<span data-ttu-id="64806-121">Nazwa zasobu szczegółowych informacji o aplikacji.</span><span class="sxs-lookup"><span data-stu-id="64806-121">Application Insights Resource Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64806-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64806-122">-ResourceGroupName</span></span>
<span data-ttu-id="64806-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="64806-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64806-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="64806-124">-ResourceId</span></span>
<span data-ttu-id="64806-125">Identyfikator składnika szczegółowych informacji aplikacji.</span><span class="sxs-lookup"><span data-stu-id="64806-125">Application Insights Component Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64806-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64806-126">CommonParameters</span></span>
<span data-ttu-id="64806-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64806-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64806-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="64806-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64806-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="64806-129">INPUTS</span></span>

### <span data-ttu-id="64806-130">System.String</span><span class="sxs-lookup"><span data-stu-id="64806-130">System.String</span></span>

## <span data-ttu-id="64806-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="64806-131">OUTPUTS</span></span>

### <span data-ttu-id="64806-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="64806-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="64806-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="64806-133">NOTES</span></span>

## <span data-ttu-id="64806-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="64806-134">RELATED LINKS</span></span>
