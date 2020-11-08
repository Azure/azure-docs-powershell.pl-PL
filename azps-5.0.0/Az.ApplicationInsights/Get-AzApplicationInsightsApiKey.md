---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsApiKey.md
ms.openlocfilehash: 802dabc8373e1f3a97c66b9a9a7a121383b68287
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225889"
---
# <span data-ttu-id="65def-101">Get-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="65def-101">Get-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="65def-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="65def-102">SYNOPSIS</span></span>
<span data-ttu-id="65def-103">Uzyskiwanie kluczy interfejsu API usługi Application Insights dla zasobu usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="65def-103">Get application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="65def-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="65def-104">SYNTAX</span></span>

### <span data-ttu-id="65def-105">ComponentNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="65def-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [[-ApiKeyId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65def-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="65def-106">ComponentObjectParameterSet</span></span>
```
Get-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [[-ApiKeyId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65def-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="65def-107">ResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsApiKey [-ResourceId] <String> [[-ApiKeyId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65def-108">Opis</span><span class="sxs-lookup"><span data-stu-id="65def-108">DESCRIPTION</span></span>
<span data-ttu-id="65def-109">Uzyskiwanie kluczy interfejsu API usługi Application Insights dla zasobu usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="65def-109">Get application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="65def-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="65def-110">EXAMPLES</span></span>

### <span data-ttu-id="65def-111">Przykład 1 uzyskiwanie kluczy interfejsu API dla zasobu usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="65def-111">Example 1 Get Api Keys for an application insights resource</span></span>
```
PS C:\>  Get-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"

Id                                   Description Permissions                       CreatedDate                   ApiKey
--                                   ----------- -----------                       -----------                   ------
7c4c61dc-b392-4aa4-992f-ee92b84e5dee test1 ReadTelemetry                     Wed, 18 Oct 2017 23:36:40 GMT
63657030-dea6-4c52-82f4-6f5128cb92cb test2  {ReadTelemetry, WriteAnnotations} Wed, 18 Oct 2017 21:46:41 GMT
82549f39-f3ae-492e-8f94-f7aada75fa57 test3  ReadTelemetry                     Wed, 18 Oct 2017 22:30:23 GMT
```

<span data-ttu-id="65def-112">Pobierz klucze interfejsu API usługi Application Insights dla zasobu "test" w grupie zasobów "Tester".</span><span class="sxs-lookup"><span data-stu-id="65def-112">Get application insights api keys for resource "test" in resource group "testGroup".</span></span>

### <span data-ttu-id="65def-113">Przykład 2 uzyskiwanie określonego klucza interfejsu API dla zasobu usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="65def-113">Example 2 Get specific API key for an application insights resource</span></span>
```
PS C:\>  Get-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"  -ApiKeyId 
7c4c61dc-b392-4aa4-992f-ee92b84e5dee
ApiKey      :
CreatedDate : Wed, 18 Oct 2017 23:36:40 GMT
Id          : 7c4c61dc-b392-4aa4-992f-ee92b84e5dee
Permissions : {ReadTelemetry}
Description : test1
```

<span data-ttu-id="65def-114">Pobierz określony klucz interfejsu API usługi Application Insights o identyfikatorze "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" dla zasobu "test" w grupie "Tester".</span><span class="sxs-lookup"><span data-stu-id="65def-114">Get specific application insights api key that id is "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="65def-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="65def-115">PARAMETERS</span></span>

### <span data-ttu-id="65def-116">-ApiKeyId</span><span class="sxs-lookup"><span data-stu-id="65def-116">-ApiKeyId</span></span>
<span data-ttu-id="65def-117">Identyfikator klucza API usługi Application Insights.</span><span class="sxs-lookup"><span data-stu-id="65def-117">Application Insights Api Key Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65def-118">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="65def-118">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="65def-119">Obiekt składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="65def-119">Application Insights Component Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65def-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65def-120">-DefaultProfile</span></span>
<span data-ttu-id="65def-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="65def-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65def-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="65def-122">-Name</span></span>
<span data-ttu-id="65def-123">Nazwa składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="65def-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="65def-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65def-124">-ResourceGroupName</span></span>
<span data-ttu-id="65def-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="65def-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="65def-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65def-126">-ResourceId</span></span>
<span data-ttu-id="65def-127">Identyfikator zasobu składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="65def-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="65def-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65def-128">CommonParameters</span></span>
<span data-ttu-id="65def-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65def-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65def-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65def-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65def-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="65def-131">INPUTS</span></span>

### <span data-ttu-id="65def-132">Microsoft. Azure. Commands. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="65def-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="65def-133">System. String</span><span class="sxs-lookup"><span data-stu-id="65def-133">System.String</span></span>

## <span data-ttu-id="65def-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="65def-134">OUTPUTS</span></span>

### <span data-ttu-id="65def-135">Microsoft. Azure. Commands. ApplicationInsights. models. PSApiKey</span><span class="sxs-lookup"><span data-stu-id="65def-135">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span></span>

## <span data-ttu-id="65def-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="65def-136">NOTES</span></span>

## <span data-ttu-id="65def-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="65def-137">RELATED LINKS</span></span>
