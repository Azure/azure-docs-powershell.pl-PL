---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/get-azurermapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Get-AzureRmApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Get-AzureRmApplicationInsights.md
ms.openlocfilehash: 5e8fe7eeb2669bbde07f9ce3c6db868a6775e258
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545831"
---
# <span data-ttu-id="9c52f-101">Get-AzureRmApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="9c52f-101">Get-AzureRmApplicationInsights</span></span>

## <span data-ttu-id="9c52f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9c52f-102">SYNOPSIS</span></span>
<span data-ttu-id="9c52f-103">Uzyskiwanie zasobów w usłudze Application Insights</span><span class="sxs-lookup"><span data-stu-id="9c52f-103">Get application insights resources</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c52f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9c52f-104">SYNTAX</span></span>

### <span data-ttu-id="9c52f-105">ResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9c52f-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmApplicationInsights [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9c52f-106">ComponentNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c52f-106">ComponentNameParameterSet</span></span>
```
Get-AzureRmApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Full]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c52f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c52f-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmApplicationInsights [-ResourceId] <String> [-Full] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9c52f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9c52f-108">DESCRIPTION</span></span>
<span data-ttu-id="9c52f-109">Uzyskiwanie zasobów w usłudze Application Insights w grupie zasobów lub konkretnym zasobie</span><span class="sxs-lookup"><span data-stu-id="9c52f-109">Get application insights resources in a resource group or specific resource</span></span>

## <span data-ttu-id="9c52f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9c52f-110">EXAMPLES</span></span>

### <span data-ttu-id="9c52f-111">Przykład 1 uzyskiwanie zasobu Usługa Application Insights</span><span class="sxs-lookup"><span data-stu-id="9c52f-111">Example 1 Get application insights resource</span></span>
```
PS C:\> Get-AzureRmApplicationInsights -ResourceGroupName "testgroup" -Name "test"

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

<span data-ttu-id="9c52f-112">Uzyskiwanie zasobu Usługa Application Insights o nazwie "test" w grupie resoruce "</span><span class="sxs-lookup"><span data-stu-id="9c52f-112">Get application insights resource named "test" in resoruce group "testgroup"</span></span>

### <span data-ttu-id="9c52f-113">Przykład 2 uzyskiwanie zasobu usługi Application Insights z informacjami o planie cenowym</span><span class="sxs-lookup"><span data-stu-id="9c52f-113">Example 2 Get application insights resource with pricing plan information</span></span>
```
PS C:\> Get-AzureRmApplicationInsights -ResourceGroupName "testgroup" -Name "test" -IncludePricingPlan

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

<span data-ttu-id="9c52f-114">Uzyskiwanie zasobu usługi Application Insights i dołączanie informacji o planie cenowym dla zasobu o nazwie "test" w grupie resoruce "</span><span class="sxs-lookup"><span data-stu-id="9c52f-114">Get application insights resource and include pricing plan information for resource named "test" in resoruce group "testgroup"</span></span>

## <span data-ttu-id="9c52f-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9c52f-115">PARAMETERS</span></span>

### <span data-ttu-id="9c52f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c52f-116">-DefaultProfile</span></span>
<span data-ttu-id="9c52f-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9c52f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>


```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c52f-118">-Pełna</span><span class="sxs-lookup"><span data-stu-id="9c52f-118">-Full</span></span>
<span data-ttu-id="9c52f-119">W przypadku określenia tej funkcji zostanie przywrócony plan cenowy/zakończenie codzienne i stan składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="9c52f-119">If specified, it will get back pricing plan/daily cap and status of the application insights component.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ComponentNameParameterSet, ResourceIdParameterSet
Aliases: IncludeDailyCap, IncludeDailyCapStatus, IncludePricingPlan

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c52f-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9c52f-120">-Name</span></span>
<span data-ttu-id="9c52f-121">Nazwa zasobu w usłudze Application Insights.</span><span class="sxs-lookup"><span data-stu-id="9c52f-121">Application Insights Resource Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c52f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c52f-122">-ResourceGroupName</span></span>
<span data-ttu-id="9c52f-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9c52f-123">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c52f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9c52f-124">-ResourceId</span></span>
<span data-ttu-id="9c52f-125">Identyfikator zasobu składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="9c52f-125">Application Insights Component Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c52f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c52f-126">CommonParameters</span></span>
<span data-ttu-id="9c52f-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c52f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c52f-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c52f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c52f-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9c52f-129">INPUTS</span></span>

### <span data-ttu-id="9c52f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9c52f-130">System.String</span></span>

## <span data-ttu-id="9c52f-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9c52f-131">OUTPUTS</span></span>

### <span data-ttu-id="9c52f-132">Microsoft. Azure. Commands. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="9c52f-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="9c52f-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9c52f-133">NOTES</span></span>

## <span data-ttu-id="9c52f-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9c52f-134">RELATED LINKS</span></span>

