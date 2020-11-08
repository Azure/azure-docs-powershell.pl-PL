---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsApiKey.md
ms.openlocfilehash: 2afb8ebfa1305e736a226f48022f4c56ded2d809
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232142"
---
# <span data-ttu-id="8e9c9-101">New-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="8e9c9-101">New-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="8e9c9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8e9c9-102">SYNOPSIS</span></span>
<span data-ttu-id="8e9c9-103">Tworzenie klucza interfejsu API usługi Application Insights dla zasobu usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="8e9c9-103">Create an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="8e9c9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8e9c9-104">SYNTAX</span></span>

### <span data-ttu-id="8e9c9-105">ComponentNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8e9c9-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-Permissions] <String[]>
 [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e9c9-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e9c9-106">ComponentObjectParameterSet</span></span>
```
New-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-Permissions] <String[]> [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e9c9-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e9c9-107">ResourceIdParameterSet</span></span>
```
New-AzApplicationInsightsApiKey [-ResourceId] <String> [-Permissions] <String[]> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e9c9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8e9c9-108">DESCRIPTION</span></span>
<span data-ttu-id="8e9c9-109">Tworzenie kluczy interfejsu API usługi Application Insights dla zasobu usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="8e9c9-109">Create an application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="8e9c9-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8e9c9-110">EXAMPLES</span></span>

### <span data-ttu-id="8e9c9-111">Przykład 1 Tworzenie nowego klucza interfejsu API dla zasobu usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="8e9c9-111">Example 1 Create a new Api Key for an application insights resource</span></span>
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

<span data-ttu-id="8e9c9-112">Utwórz Opis klucza API usługi Application Insights jako "testapiKey" z uprawnieniami "ReadTelemetry", "WriteAnnotations" dla zasobu "test" w grupie zasób "test".</span><span class="sxs-lookup"><span data-stu-id="8e9c9-112">Create application insights api key description as "testapiKey" with permissions "ReadTelemetry", "WriteAnnotations" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="8e9c9-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8e9c9-113">PARAMETERS</span></span>

### <span data-ttu-id="8e9c9-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="8e9c9-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="8e9c9-115">Obiekt składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="8e9c9-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="8e9c9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e9c9-116">-DefaultProfile</span></span>
<span data-ttu-id="8e9c9-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8e9c9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e9c9-118">— Opis</span><span class="sxs-lookup"><span data-stu-id="8e9c9-118">-Description</span></span>
<span data-ttu-id="8e9c9-119">Opis ułatwiający zidentyfikowanie tego klucza API.</span><span class="sxs-lookup"><span data-stu-id="8e9c9-119">Description to help identify this API key.</span></span>

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

### <span data-ttu-id="8e9c9-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8e9c9-120">-Name</span></span>
<span data-ttu-id="8e9c9-121">Nazwa składnika.</span><span class="sxs-lookup"><span data-stu-id="8e9c9-121">Component Name.</span></span>

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

### <span data-ttu-id="8e9c9-122">-Uprawnienia</span><span class="sxs-lookup"><span data-stu-id="8e9c9-122">-Permissions</span></span>
<span data-ttu-id="8e9c9-123">Uprawnienia, które klucz API zezwala na wykonywanie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="8e9c9-123">Permissions that API key allow apps to do.</span></span>

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

### <span data-ttu-id="8e9c9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e9c9-124">-ResourceGroupName</span></span>
<span data-ttu-id="8e9c9-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8e9c9-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="8e9c9-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e9c9-126">-ResourceId</span></span>
<span data-ttu-id="8e9c9-127">Identyfikator zasobu składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="8e9c9-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="8e9c9-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8e9c9-128">-Confirm</span></span>
<span data-ttu-id="8e9c9-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e9c9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e9c9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e9c9-130">-WhatIf</span></span>
<span data-ttu-id="8e9c9-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e9c9-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8e9c9-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8e9c9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e9c9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e9c9-133">CommonParameters</span></span>
<span data-ttu-id="8e9c9-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e9c9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e9c9-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e9c9-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e9c9-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8e9c9-136">INPUTS</span></span>

### <span data-ttu-id="8e9c9-137">Microsoft. Azure. Commands. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="8e9c9-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="8e9c9-138">System. String</span><span class="sxs-lookup"><span data-stu-id="8e9c9-138">System.String</span></span>

## <span data-ttu-id="8e9c9-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8e9c9-139">OUTPUTS</span></span>

### <span data-ttu-id="8e9c9-140">Microsoft. Azure. Commands. ApplicationInsights. models. PSApiKey</span><span class="sxs-lookup"><span data-stu-id="8e9c9-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span></span>

## <span data-ttu-id="8e9c9-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8e9c9-141">NOTES</span></span>

## <span data-ttu-id="8e9c9-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8e9c9-142">RELATED LINKS</span></span>
