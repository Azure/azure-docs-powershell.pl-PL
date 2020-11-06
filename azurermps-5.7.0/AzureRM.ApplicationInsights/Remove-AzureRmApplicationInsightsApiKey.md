---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/remove-azurermapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsightsApiKey.md
ms.openlocfilehash: 7fbf269b43868724b015bd087536c49ccce71f73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550724"
---
# <span data-ttu-id="6bb85-101">Remove-AzureRmApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="6bb85-101">Remove-AzureRmApplicationInsightsApiKey</span></span>

## <span data-ttu-id="6bb85-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6bb85-102">SYNOPSIS</span></span>
<span data-ttu-id="6bb85-103">Usuwanie klucza API usługi Application Insights dla zasobu usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="6bb85-103">Remove an application insights api key for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6bb85-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6bb85-104">SYNTAX</span></span>

### <span data-ttu-id="6bb85-105">ComponentNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6bb85-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-ApiKeyId] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bb85-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6bb85-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ApiKeyId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6bb85-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6bb85-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmApplicationInsightsApiKey [-ResourceId] <String> [-ApiKeyId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bb85-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6bb85-108">DESCRIPTION</span></span>
<span data-ttu-id="6bb85-109">Usuwanie klucza API usługi Application Insights dla zasobu usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="6bb85-109">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="6bb85-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6bb85-110">EXAMPLES</span></span>

### <span data-ttu-id="6bb85-111">Przykład 1 Usuwanie klucza interfejsu API usługi Application Insights dla zasobu usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="6bb85-111">Example 1 Remove an application insights api key for an application insights resource</span></span>
```
Get-AzureRmApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"  -ApiKeyId dd173f38-4fd1-4c75-8af5-9
9c29aa0f867 -PassThru
True
```

<span data-ttu-id="6bb85-112">Usuń określony klucz interfejsu API usługi Application Insights o identyfikatorze "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" dla zasobu "test" w grupie zasobów "Tester".</span><span class="sxs-lookup"><span data-stu-id="6bb85-112">Remove specific application insights api key that id is "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="6bb85-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6bb85-113">PARAMETERS</span></span>

### <span data-ttu-id="6bb85-114">-ApiKeyId</span><span class="sxs-lookup"><span data-stu-id="6bb85-114">-ApiKeyId</span></span>
<span data-ttu-id="6bb85-115">Identyfikator klucza API usługi Application Insights.</span><span class="sxs-lookup"><span data-stu-id="6bb85-115">Application Insights API Key ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bb85-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="6bb85-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="6bb85-117">Obiekt składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="6bb85-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="6bb85-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6bb85-118">-Confirm</span></span>
<span data-ttu-id="6bb85-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6bb85-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bb85-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bb85-120">-DefaultProfile</span></span>
<span data-ttu-id="6bb85-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6bb85-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6bb85-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6bb85-122">-Name</span></span>
<span data-ttu-id="6bb85-123">Nazwa składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="6bb85-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="6bb85-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6bb85-124">-PassThru</span></span>
<span data-ttu-id="6bb85-125">Jeśli ta wartość zostanie określona, operacja ta zostanie zapisana jako prawda w przypadku powodzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="6bb85-125">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="6bb85-126">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="6bb85-126">This parameter is optional.</span></span> <span data-ttu-id="6bb85-127">Wartość domyślna to false.</span><span class="sxs-lookup"><span data-stu-id="6bb85-127">Default value is false.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bb85-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bb85-128">-ResourceGroupName</span></span>
<span data-ttu-id="6bb85-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6bb85-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="6bb85-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6bb85-130">-ResourceId</span></span>
<span data-ttu-id="6bb85-131">Identyfikator zasobu składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="6bb85-131">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="6bb85-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bb85-132">-WhatIf</span></span>
<span data-ttu-id="6bb85-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6bb85-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bb85-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6bb85-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bb85-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bb85-135">CommonParameters</span></span>
<span data-ttu-id="6bb85-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bb85-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bb85-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bb85-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bb85-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6bb85-138">INPUTS</span></span>

### <span data-ttu-id="6bb85-139">System. String</span><span class="sxs-lookup"><span data-stu-id="6bb85-139">System.String</span></span>

## <span data-ttu-id="6bb85-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6bb85-140">OUTPUTS</span></span>

### <span data-ttu-id="6bb85-141">System. Object</span><span class="sxs-lookup"><span data-stu-id="6bb85-141">System.Object</span></span>

## <span data-ttu-id="6bb85-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6bb85-142">NOTES</span></span>

## <span data-ttu-id="6bb85-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6bb85-143">RELATED LINKS</span></span>

