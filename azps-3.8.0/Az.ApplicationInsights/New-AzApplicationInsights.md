---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
ms.openlocfilehash: 550fb398dbd636ba9c43c66d31b78384610cf42b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053113"
---
# <span data-ttu-id="f6fcb-101">New-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="f6fcb-101">New-AzApplicationInsights</span></span>

## <span data-ttu-id="f6fcb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f6fcb-102">SYNOPSIS</span></span>
<span data-ttu-id="f6fcb-103">Tworzenie nowego zasobu Usługa Application Insights</span><span class="sxs-lookup"><span data-stu-id="f6fcb-103">Create a new application insights resource</span></span>

## <span data-ttu-id="f6fcb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f6fcb-104">SYNTAX</span></span>

```
New-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Kind <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6fcb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f6fcb-105">DESCRIPTION</span></span>
<span data-ttu-id="f6fcb-106">Tworzenie nowego zasobu Usługa Application Insights</span><span class="sxs-lookup"><span data-stu-id="f6fcb-106">Create a new application insights resource</span></span>

## <span data-ttu-id="f6fcb-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f6fcb-107">EXAMPLES</span></span>

### <span data-ttu-id="f6fcb-108">Przykład 1 Tworzenie nowego zasobu Usługa Application Insights</span><span class="sxs-lookup"><span data-stu-id="f6fcb-108">Example 1 Create a new application insights resource</span></span>
```
PS C:\>  New-AzApplicationInsights -Kind java -ResourceGroupName testgroup -Name test1027 -location eastus
Id                 : /subscriptions/{subid}/resourceGroups/testgroup/providers/microsoft.insights/components/test1027
ResourceGroupName  : testgroup
Name               : test1027
Kind               : web
Location           : eastus
Type               : microsoft.insights/components
AppId              : 8323fb13-32aa-46af-b467-8355cf4f8f98
ApplicationType    : web
Tags               : {}
CreationDate       : 10/27/2017 4:56:40 PM
FlowType           :
HockeyAppId        :
HockeyAppToken     :
InstrumentationKey : 083112ed-ed9b-464e-a9b0-8cf126fbfced
ProvisioningState  : Succeeded
RequestSource      : AzurePowerShell
SamplingPercentage :
TenantId           : {subid}
```

<span data-ttu-id="f6fcb-109">Dodaj nowy zasób usługi Application Insights o nazwie "test" w grupie zasób "z typem" Java ".</span><span class="sxs-lookup"><span data-stu-id="f6fcb-109">Add a new application insights resource named as "test" in resource group "testgroup" with kind "java".</span></span>

## <span data-ttu-id="f6fcb-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f6fcb-110">PARAMETERS</span></span>

### <span data-ttu-id="f6fcb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6fcb-111">-DefaultProfile</span></span>
<span data-ttu-id="f6fcb-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f6fcb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6fcb-113">-Kind</span><span class="sxs-lookup"><span data-stu-id="f6fcb-113">-Kind</span></span>
<span data-ttu-id="f6fcb-114">Rodzaj aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f6fcb-114">Application kind.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationKind
Accepted values: web, other, Node.js, java

Required: False
Position: Named
Default value: web
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6fcb-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f6fcb-115">-Location</span></span>
<span data-ttu-id="f6fcb-116">Lokalizacja zasobu w usłudze Application Insights.</span><span class="sxs-lookup"><span data-stu-id="f6fcb-116">Application Insights Resource Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6fcb-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f6fcb-117">-Name</span></span>
<span data-ttu-id="f6fcb-118">Nazwa zasobu w usłudze Application Insights.</span><span class="sxs-lookup"><span data-stu-id="f6fcb-118">Application Insights Resource Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6fcb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6fcb-119">-ResourceGroupName</span></span>
<span data-ttu-id="f6fcb-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f6fcb-120">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6fcb-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="f6fcb-121">-Tag</span></span>
<span data-ttu-id="f6fcb-122">Znaczniki składników.</span><span class="sxs-lookup"><span data-stu-id="f6fcb-122">Component Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6fcb-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f6fcb-123">-Confirm</span></span>
<span data-ttu-id="f6fcb-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6fcb-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6fcb-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6fcb-125">-WhatIf</span></span>
<span data-ttu-id="f6fcb-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6fcb-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f6fcb-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f6fcb-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6fcb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6fcb-128">CommonParameters</span></span>
<span data-ttu-id="f6fcb-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6fcb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6fcb-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6fcb-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6fcb-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f6fcb-131">INPUTS</span></span>

### <span data-ttu-id="f6fcb-132">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f6fcb-132">None</span></span>

## <span data-ttu-id="f6fcb-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f6fcb-133">OUTPUTS</span></span>

### <span data-ttu-id="f6fcb-134">Microsoft. Azure. Commands. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="f6fcb-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="f6fcb-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f6fcb-135">NOTES</span></span>

## <span data-ttu-id="f6fcb-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f6fcb-136">RELATED LINKS</span></span>
