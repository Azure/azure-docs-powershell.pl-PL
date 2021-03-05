---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/new-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsApiKey.md
ms.openlocfilehash: 0137a349408234f31f0002849230e023c0544f68
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987078"
---
# <span data-ttu-id="176bf-101">New-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="176bf-101">New-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="176bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="176bf-102">SYNOPSIS</span></span>
<span data-ttu-id="176bf-103">Tworzenie klucza interfejsu API szczegółowej analizy aplikacji dla zasobu szczegółowych informacji o aplikacjach</span><span class="sxs-lookup"><span data-stu-id="176bf-103">Create an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="176bf-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="176bf-104">SYNTAX</span></span>

### <span data-ttu-id="176bf-105">ComponentNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="176bf-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-Permissions] <String[]>
 [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="176bf-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="176bf-106">ComponentObjectParameterSet</span></span>
```
New-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-Permissions] <String[]> [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="176bf-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="176bf-107">ResourceIdParameterSet</span></span>
```
New-AzApplicationInsightsApiKey [-ResourceId] <String> [-Permissions] <String[]> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="176bf-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="176bf-108">DESCRIPTION</span></span>
<span data-ttu-id="176bf-109">Tworzenie kluczy interfejsu API szczegółowych informacji aplikacji dla zasobu szczegółowych informacji aplikacji</span><span class="sxs-lookup"><span data-stu-id="176bf-109">Create an application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="176bf-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="176bf-110">EXAMPLES</span></span>

### <span data-ttu-id="176bf-111">Przykład 1. Tworzenie nowego klucza interfejsu API dla zasobu szczegółowych informacji aplikacji</span><span class="sxs-lookup"><span data-stu-id="176bf-111">Example 1 Create a new Api Key for an application insights resource</span></span>
```
PS C:\>$apiKeyDescription="testapiKey"
PS C:\>$permissions = @("ReadTelemetry", "WriteAnnotations")
PS C:\>New-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test" -Description $apiKeyDescription -Permissions $permissions

ApiKey      : st0rfelw7m3oimfspozrtwgccxihiftbdwqjdfkg
CreatedDate : Fri, 27 Oct 2017 16:59:19 GMT
Id          : 1ed593f9-1561-4981-922d-6917971eecd3
Permissions : {ReadTelemetry, WriteAnnotations}
Description : testapiKey
```

<span data-ttu-id="176bf-112">Utwórz opis klucza interfejsu API insights aplikacji jako "testapiKey" z uprawnieniami "ReadTelemetry", "WriteAnnotations" dla zasobu "test" w grupie zasobów "testGroup".</span><span class="sxs-lookup"><span data-stu-id="176bf-112">Create application insights api key description as "testapiKey" with permissions "ReadTelemetry", "WriteAnnotations" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="176bf-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="176bf-113">PARAMETERS</span></span>

### <span data-ttu-id="176bf-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="176bf-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="176bf-115">Obiekt składnika Szczegółowe informacje o aplikacji.</span><span class="sxs-lookup"><span data-stu-id="176bf-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="176bf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="176bf-116">-DefaultProfile</span></span>
<span data-ttu-id="176bf-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="176bf-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="176bf-118">— Opis</span><span class="sxs-lookup"><span data-stu-id="176bf-118">-Description</span></span>
<span data-ttu-id="176bf-119">Opis ułatwiający zidentyfikowanie tego klucza interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="176bf-119">Description to help identify this API key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="176bf-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="176bf-120">-Name</span></span>
<span data-ttu-id="176bf-121">Nazwa składnika.</span><span class="sxs-lookup"><span data-stu-id="176bf-121">Component Name.</span></span>

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

### <span data-ttu-id="176bf-122">— Uprawnienia</span><span class="sxs-lookup"><span data-stu-id="176bf-122">-Permissions</span></span>
<span data-ttu-id="176bf-123">Uprawnienia, na które zezwalają aplikacje przy użyciu klucza interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="176bf-123">Permissions that API key allow apps to do.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: ReadTelemetry, WriteAnnotations, AuthenticateSDKControlChannel

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="176bf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="176bf-124">-ResourceGroupName</span></span>
<span data-ttu-id="176bf-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="176bf-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="176bf-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="176bf-126">-ResourceId</span></span>
<span data-ttu-id="176bf-127">Identyfikator składnika szczegółowych informacji aplikacji.</span><span class="sxs-lookup"><span data-stu-id="176bf-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="176bf-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="176bf-128">-Confirm</span></span>
<span data-ttu-id="176bf-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="176bf-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="176bf-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="176bf-130">-WhatIf</span></span>
<span data-ttu-id="176bf-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="176bf-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="176bf-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="176bf-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="176bf-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="176bf-133">CommonParameters</span></span>
<span data-ttu-id="176bf-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="176bf-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="176bf-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="176bf-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="176bf-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="176bf-136">INPUTS</span></span>

### <span data-ttu-id="176bf-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="176bf-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="176bf-138">System.String</span><span class="sxs-lookup"><span data-stu-id="176bf-138">System.String</span></span>

## <span data-ttu-id="176bf-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="176bf-139">OUTPUTS</span></span>

### <span data-ttu-id="176bf-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span><span class="sxs-lookup"><span data-stu-id="176bf-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span></span>

## <span data-ttu-id="176bf-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="176bf-141">NOTES</span></span>

## <span data-ttu-id="176bf-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="176bf-142">RELATED LINKS</span></span>
