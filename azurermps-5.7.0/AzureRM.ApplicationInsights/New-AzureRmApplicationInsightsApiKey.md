---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/new-azurermapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsightsApiKey.md
ms.openlocfilehash: 4c7f488e7a9ffca823128cccff18ba33b88dabfd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548243"
---
# <span data-ttu-id="ee341-101">New-AzureRmApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="ee341-101">New-AzureRmApplicationInsightsApiKey</span></span>

## <span data-ttu-id="ee341-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ee341-102">SYNOPSIS</span></span>
<span data-ttu-id="ee341-103">Tworzenie klucza interfejsu API usługi Application Insights dla zasobu usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="ee341-103">Create an application insights api key for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee341-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ee341-104">SYNTAX</span></span>

### <span data-ttu-id="ee341-105">ComponentNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ee341-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-Permissions] <String[]>
 [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee341-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee341-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-Permissions] <String[]> [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee341-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee341-107">ResourceIdParameterSet</span></span>
```
New-AzureRmApplicationInsightsApiKey [-ResourceId] <String> [-Permissions] <String[]> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee341-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ee341-108">DESCRIPTION</span></span>
<span data-ttu-id="ee341-109">Tworzenie kluczy interfejsu API usługi Application Insights dla zasobu usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="ee341-109">Create an application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="ee341-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ee341-110">EXAMPLES</span></span>

### <span data-ttu-id="ee341-111">Przykład 1 Tworzenie nowego klucza interfejsu API dla zasobu usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="ee341-111">Example 1 Create a new Api Key for an application insights resource</span></span>
```
PS C:\>$apiKeyDescription="testapiKey"
PS C:\>$permissions = @("ReadTelemetry", "WriteAnnotations")
PS C:\>New-AzureRmApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test" -Description $apiKeyDescription -Permissions $permissions

ApiKey      : st0rfelw7m3oimfspozrtwgccxihiftbdwqjdfkg
CreatedDate : Fri, 27 Oct 2017 16:59:19 GMT
Id          : 1ed593f9-1561-4981-922d-6917971eecd3
Permissions : {ReadTelemetry, WriteAnnotations}
Description : testapiKey
```

<span data-ttu-id="ee341-112">Utwórz Opis klucza API usługi Application Insights jako "testapiKey" z uprawnieniami "ReadTelemetry", "WriteAnnotations" dla zasobu "test" w grupie zasób "test".</span><span class="sxs-lookup"><span data-stu-id="ee341-112">Create application insights api key description as "testapiKey" with permissions "ReadTelemetry", "WriteAnnotations" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="ee341-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ee341-113">PARAMETERS</span></span>

### <span data-ttu-id="ee341-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="ee341-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="ee341-115">Obiekt składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="ee341-115">Application Insights Component Object.</span></span>

```yaml
Type: PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee341-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ee341-116">-Confirm</span></span>
<span data-ttu-id="ee341-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee341-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee341-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee341-118">-DefaultProfile</span></span>
<span data-ttu-id="ee341-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ee341-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee341-120">— Opis</span><span class="sxs-lookup"><span data-stu-id="ee341-120">-Description</span></span>
<span data-ttu-id="ee341-121">Opis ułatwiający zidentyfikowanie tego klucza API.</span><span class="sxs-lookup"><span data-stu-id="ee341-121">Description to help identify this API key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee341-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ee341-122">-Name</span></span>
<span data-ttu-id="ee341-123">Nazwa składnika.</span><span class="sxs-lookup"><span data-stu-id="ee341-123">Component Name.</span></span>

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

### <span data-ttu-id="ee341-124">-Uprawnienia</span><span class="sxs-lookup"><span data-stu-id="ee341-124">-Permissions</span></span>
<span data-ttu-id="ee341-125">Uprawnienia, które klucz API zezwala na wykonywanie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ee341-125">Permissions that API key allow apps to do.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 
Accepted values: ReadTelemetry, WriteAnnotations, AuthenticateSDKControlChannel

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee341-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee341-126">-ResourceGroupName</span></span>
<span data-ttu-id="ee341-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ee341-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="ee341-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee341-128">-ResourceId</span></span>
<span data-ttu-id="ee341-129">Identyfikator zasobu składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="ee341-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="ee341-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee341-130">-WhatIf</span></span>
<span data-ttu-id="ee341-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee341-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ee341-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ee341-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee341-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee341-133">CommonParameters</span></span>
<span data-ttu-id="ee341-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee341-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee341-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee341-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee341-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ee341-136">INPUTS</span></span>

### <span data-ttu-id="ee341-137">System. String</span><span class="sxs-lookup"><span data-stu-id="ee341-137">System.String</span></span>
<span data-ttu-id="ee341-138">System. String []</span><span class="sxs-lookup"><span data-stu-id="ee341-138">System.String[]</span></span>

## <span data-ttu-id="ee341-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ee341-139">OUTPUTS</span></span>

### <span data-ttu-id="ee341-140">Microsoft. Azure. Commands. ApplicationInsights. models. PSApiKey</span><span class="sxs-lookup"><span data-stu-id="ee341-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span></span>

## <span data-ttu-id="ee341-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ee341-141">NOTES</span></span>

## <span data-ttu-id="ee341-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ee341-142">RELATED LINKS</span></span>

