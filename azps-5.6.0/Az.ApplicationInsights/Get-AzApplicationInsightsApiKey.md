---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/get-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsApiKey.md
ms.openlocfilehash: 96887bebdfddec0a5393ca41bc3b552119cffe81
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965258"
---
# <span data-ttu-id="ecf39-101">Get-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="ecf39-101">Get-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="ecf39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecf39-102">SYNOPSIS</span></span>
<span data-ttu-id="ecf39-103">Uzyskiwanie kluczy interfejsu API szczegółowych informacji o aplikacjach dla zasobu szczegółowych informacji o aplikacjach</span><span class="sxs-lookup"><span data-stu-id="ecf39-103">Get application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="ecf39-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ecf39-104">SYNTAX</span></span>

### <span data-ttu-id="ecf39-105">ComponentNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="ecf39-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [[-ApiKeyId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecf39-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ecf39-106">ComponentObjectParameterSet</span></span>
```
Get-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [[-ApiKeyId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecf39-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ecf39-107">ResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsApiKey [-ResourceId] <String> [[-ApiKeyId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecf39-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="ecf39-108">DESCRIPTION</span></span>
<span data-ttu-id="ecf39-109">Uzyskiwanie kluczy interfejsu API szczegółowych informacji o aplikacjach dla zasobu szczegółowych informacji o aplikacjach</span><span class="sxs-lookup"><span data-stu-id="ecf39-109">Get application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="ecf39-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ecf39-110">EXAMPLES</span></span>

### <span data-ttu-id="ecf39-111">Przykład 1. Uzyskiwanie kluczy interfejsu API dla zasobu szczegółowych informacji aplikacji</span><span class="sxs-lookup"><span data-stu-id="ecf39-111">Example 1 Get Api Keys for an application insights resource</span></span>
```
PS C:\>  Get-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"

Id                                   Description Permissions                       CreatedDate                   ApiKey
--                                   ----------- -----------                       -----------                   ------
7c4c61dc-b392-4aa4-992f-ee92b84e5dee test1 ReadTelemetry                     Wed, 18 Oct 2017 23:36:40 GMT
63657030-dea6-4c52-82f4-6f5128cb92cb test2  {ReadTelemetry, WriteAnnotations} Wed, 18 Oct 2017 21:46:41 GMT
82549f39-f3ae-492e-8f94-f7aada75fa57 test3  ReadTelemetry                     Wed, 18 Oct 2017 22:30:23 GMT
```

<span data-ttu-id="ecf39-112">Uzyskaj klucze interfejsu API analizy aplikacji dla "testu" zasobu w grupie zasobów "testGroup".</span><span class="sxs-lookup"><span data-stu-id="ecf39-112">Get application insights api keys for resource "test" in resource group "testGroup".</span></span>

### <span data-ttu-id="ecf39-113">Przykład 2. Uzyskiwanie określonego klucza interfejsu API dla zasobu szczegółowych informacji aplikacji</span><span class="sxs-lookup"><span data-stu-id="ecf39-113">Example 2 Get specific API key for an application insights resource</span></span>
```
PS C:\>  Get-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"  -ApiKeyId 
7c4c61dc-b392-4aa4-992f-ee92b84e5dee
ApiKey      :
CreatedDate : Wed, 18 Oct 2017 23:36:40 GMT
Id          : 7c4c61dc-b392-4aa4-992f-ee92b84e5dee
Permissions : {ReadTelemetry}
Description : test1
```

<span data-ttu-id="ecf39-114">Uzyskaj klucz interfejsu api szczegółowej analizy aplikacji, który ma identyfikator "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" dla zasobu "test" w grupie zasobów "testGroup".</span><span class="sxs-lookup"><span data-stu-id="ecf39-114">Get specific application insights api key that id is "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="ecf39-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ecf39-115">PARAMETERS</span></span>

### <span data-ttu-id="ecf39-116">-ApiKeyId</span><span class="sxs-lookup"><span data-stu-id="ecf39-116">-ApiKeyId</span></span>
<span data-ttu-id="ecf39-117">Identyfikator klucza interfejsu API aplikacji Insights.</span><span class="sxs-lookup"><span data-stu-id="ecf39-117">Application Insights Api Key Id.</span></span>

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

### <span data-ttu-id="ecf39-118">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="ecf39-118">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="ecf39-119">Obiekt składnika Szczegółowe informacje o aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ecf39-119">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="ecf39-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecf39-120">-DefaultProfile</span></span>
<span data-ttu-id="ecf39-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ecf39-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ecf39-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ecf39-122">-Name</span></span>
<span data-ttu-id="ecf39-123">Nazwa składnika szczegółowych informacji aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ecf39-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="ecf39-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecf39-124">-ResourceGroupName</span></span>
<span data-ttu-id="ecf39-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ecf39-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="ecf39-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ecf39-126">-ResourceId</span></span>
<span data-ttu-id="ecf39-127">Identyfikator składnika szczegółowych informacji aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ecf39-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="ecf39-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecf39-128">CommonParameters</span></span>
<span data-ttu-id="ecf39-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecf39-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecf39-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecf39-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecf39-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ecf39-131">INPUTS</span></span>

### <span data-ttu-id="ecf39-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="ecf39-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="ecf39-133">System.String</span><span class="sxs-lookup"><span data-stu-id="ecf39-133">System.String</span></span>

## <span data-ttu-id="ecf39-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ecf39-134">OUTPUTS</span></span>

### <span data-ttu-id="ecf39-135">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span><span class="sxs-lookup"><span data-stu-id="ecf39-135">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span></span>

## <span data-ttu-id="ecf39-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ecf39-136">NOTES</span></span>

## <span data-ttu-id="ecf39-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ecf39-137">RELATED LINKS</span></span>
