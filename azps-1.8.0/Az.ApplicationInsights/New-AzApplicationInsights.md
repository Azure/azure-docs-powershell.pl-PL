---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
ms.openlocfilehash: d04b2e54e10a88edd3273ecd96697ab993e97c98
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869291"
---
# <span data-ttu-id="e4c15-101">New-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="e4c15-101">New-AzApplicationInsights</span></span>

## <span data-ttu-id="e4c15-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e4c15-102">SYNOPSIS</span></span>
<span data-ttu-id="e4c15-103">Tworzenie nowego zasobu Usługa Application Insights</span><span class="sxs-lookup"><span data-stu-id="e4c15-103">Create a new application insights resource</span></span>

## <span data-ttu-id="e4c15-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e4c15-104">SYNTAX</span></span>

```
New-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Kind <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4c15-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e4c15-105">DESCRIPTION</span></span>
<span data-ttu-id="e4c15-106">Tworzenie nowego zasobu Usługa Application Insights</span><span class="sxs-lookup"><span data-stu-id="e4c15-106">Create a new application insights resource</span></span>

## <span data-ttu-id="e4c15-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e4c15-107">EXAMPLES</span></span>

### <span data-ttu-id="e4c15-108">Przykład 1 Tworzenie nowego zasobu Usługa Application Insights</span><span class="sxs-lookup"><span data-stu-id="e4c15-108">Example 1 Create a new application insights resource</span></span>
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

<span data-ttu-id="e4c15-109">Dodaj nowy zasób usługi Application Insights o nazwie "test" w grupie zasób "z typem" Java ".</span><span class="sxs-lookup"><span data-stu-id="e4c15-109">Add a new application insights resource named as "test" in resource group "testgroup" with kind "java".</span></span>

## <span data-ttu-id="e4c15-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e4c15-110">PARAMETERS</span></span>

### <span data-ttu-id="e4c15-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4c15-111">-DefaultProfile</span></span>
<span data-ttu-id="e4c15-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e4c15-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4c15-113">-Kind</span><span class="sxs-lookup"><span data-stu-id="e4c15-113">-Kind</span></span>
<span data-ttu-id="e4c15-114">Rodzaj aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e4c15-114">Application kind.</span></span>

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

### <span data-ttu-id="e4c15-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e4c15-115">-Location</span></span>
<span data-ttu-id="e4c15-116">Lokalizacja zasobu w usłudze Application Insights.</span><span class="sxs-lookup"><span data-stu-id="e4c15-116">Application Insights Resource Location.</span></span>

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

### <span data-ttu-id="e4c15-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e4c15-117">-Name</span></span>
<span data-ttu-id="e4c15-118">Nazwa zasobu w usłudze Application Insights.</span><span class="sxs-lookup"><span data-stu-id="e4c15-118">Application Insights Resource Name.</span></span>

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

### <span data-ttu-id="e4c15-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4c15-119">-ResourceGroupName</span></span>
<span data-ttu-id="e4c15-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e4c15-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="e4c15-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="e4c15-121">-Tag</span></span>
<span data-ttu-id="e4c15-122">Znaczniki składników.</span><span class="sxs-lookup"><span data-stu-id="e4c15-122">Component Tags.</span></span>

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

### <span data-ttu-id="e4c15-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e4c15-123">-Confirm</span></span>
<span data-ttu-id="e4c15-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4c15-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4c15-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4c15-125">-WhatIf</span></span>
<span data-ttu-id="e4c15-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4c15-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e4c15-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e4c15-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4c15-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4c15-128">CommonParameters</span></span>
<span data-ttu-id="e4c15-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4c15-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4c15-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4c15-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4c15-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e4c15-131">INPUTS</span></span>

### <span data-ttu-id="e4c15-132">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e4c15-132">None</span></span>

## <span data-ttu-id="e4c15-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e4c15-133">OUTPUTS</span></span>

### <span data-ttu-id="e4c15-134">Microsoft. Azure. Commands. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="e4c15-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="e4c15-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e4c15-135">NOTES</span></span>

## <span data-ttu-id="e4c15-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e4c15-136">RELATED LINKS</span></span>
