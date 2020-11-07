---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F271BCB1-6D43-48E5-BB51-00288F57BFFB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapprunhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
ms.openlocfilehash: cff5113c37580b375bbaaea24850d5b55cd110ef
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867727"
---
# <span data-ttu-id="60c00-101">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="60c00-101">Get-AzLogicAppRunHistory</span></span>

## <span data-ttu-id="60c00-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="60c00-102">SYNOPSIS</span></span>
<span data-ttu-id="60c00-103">Pobiera historię przebiegu aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="60c00-103">Gets the run history of a logic app.</span></span>

## <span data-ttu-id="60c00-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="60c00-104">SYNTAX</span></span>

```
Get-AzLogicAppRunHistory -ResourceGroupName <String> -Name <String> [-RunName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60c00-105">Opis</span><span class="sxs-lookup"><span data-stu-id="60c00-105">DESCRIPTION</span></span>
<span data-ttu-id="60c00-106">Polecenie cmdlet **Get-AzLogicAppRunHistory** pobiera historię przebiegu aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="60c00-106">The **Get-AzLogicAppRunHistory** cmdlet gets the run history of a logic app.</span></span>
<span data-ttu-id="60c00-107">To polecenie cmdlet zwraca kolekcję obiektów **WorkflowRun** .</span><span class="sxs-lookup"><span data-stu-id="60c00-107">This cmdlet returns a collection of **WorkflowRun** objects.</span></span>
<span data-ttu-id="60c00-108">Określ aplikację logiczną i grupę zasobów.</span><span class="sxs-lookup"><span data-stu-id="60c00-108">Specify the logic app and resource group.</span></span>
<span data-ttu-id="60c00-109">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="60c00-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="60c00-110">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="60c00-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="60c00-111">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="60c00-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="60c00-112">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="60c00-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="60c00-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="60c00-113">EXAMPLES</span></span>

### <span data-ttu-id="60c00-114">Przykład 1: uzyskiwanie historii uruchamiania aplikacji logicznej</span><span class="sxs-lookup"><span data-stu-id="60c00-114">Example 1: Get the run history of a logic app</span></span>
```
PS C:\>Get-AzLogicAppActionRunHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03"
CorrelationId    : 55830326-9042-404d-a4c3-fab198106a57
EndTime          : 1/13/2016 2:46:55 PM
Error            : {code, message}
Name             : 08587489104702792076
Outputs          : {}
StartTime        : 1/13/2016 2:46:55 PM
Status           : Failed
TriggerName      : 
LogicAppName     : LogicApp03
LogicAppVersion  : 08587489107859952540

CorrelationId    : d3ddc917-9aaa-47b3-8814-c621c2ae530b
EndTime          : 1/13/2016 2:42:56 PM
Error            : {code, message}
Name             : 08587489107100664541
Outputs          : {}
StartTime        : 1/13/2016 2:42:55 PM
Status           : Failed
TriggerName      : httpTrigger
LogicAppName     : LogicApp03
LogicAppVersion  : 08587489107859952120
```

<span data-ttu-id="60c00-115">To polecenie pobiera historię przebiegu aplikacji logicznej o nazwie LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="60c00-115">This command gets the run history of a logic app named LogicApp03.</span></span>

### <span data-ttu-id="60c00-116">Przykład 2: uzyskiwanie uruchamiania aplikacji logicznej</span><span class="sxs-lookup"><span data-stu-id="60c00-116">Example 2: Get a logic app run</span></span>
```
PS C:\>Get-AzLogicAppActionRunHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03" -RunName "08587489104702792076"
CorrelationId    : 55830326-9042-404d-a4c3-fab198106a57
EndTime          : 1/13/2016 2:46:55 PM
Error            : {code, message}
Name             : 08587489104702792076
Outputs          : {}
StartTime        : 1/13/2016 2:46:55 PM
Status           : Failed
TriggerName      : 
LogicAppName     : LogicApp03
LogicAppVersion  : 08587489107859952120
```

<span data-ttu-id="60c00-117">To polecenie pobiera określoną aplikację logiczną w celu uruchomienia aplikacji logicznej o nazwie LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="60c00-117">This command gets a specific logic app run for the logic app named LogicApp03.</span></span>

## <span data-ttu-id="60c00-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="60c00-118">PARAMETERS</span></span>

### <span data-ttu-id="60c00-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60c00-119">-DefaultProfile</span></span>
<span data-ttu-id="60c00-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="60c00-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60c00-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="60c00-121">-Name</span></span>
<span data-ttu-id="60c00-122">Określa nazwę aplikacji logicznej, dla której to polecenie cmdlet pobiera historię uruchamiania.</span><span class="sxs-lookup"><span data-stu-id="60c00-122">Specifies the name of the logic app for which this cmdlet gets run history.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60c00-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60c00-123">-ResourceGroupName</span></span>
<span data-ttu-id="60c00-124">Określa nazwę grupy zasobów zawierającej aplikację logiczną.</span><span class="sxs-lookup"><span data-stu-id="60c00-124">Specifies the name of a resource group that contains the logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60c00-125">-RunName</span><span class="sxs-lookup"><span data-stu-id="60c00-125">-RunName</span></span>
<span data-ttu-id="60c00-126">Określa nazwę uruchomienia aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="60c00-126">Specifies the run name of a logic app.</span></span>
<span data-ttu-id="60c00-127">To polecenie cmdlet umożliwia uruchomienie przepływu pracy, który określa ten aplet polecenia.</span><span class="sxs-lookup"><span data-stu-id="60c00-127">This cmdlet gets the workflow run that this cmdlet specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60c00-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60c00-128">CommonParameters</span></span>
<span data-ttu-id="60c00-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60c00-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60c00-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60c00-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60c00-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="60c00-131">INPUTS</span></span>

### <span data-ttu-id="60c00-132">System. String</span><span class="sxs-lookup"><span data-stu-id="60c00-132">System.String</span></span>

## <span data-ttu-id="60c00-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="60c00-133">OUTPUTS</span></span>

### <span data-ttu-id="60c00-134">Microsoft. Azure. Management. Logic. MODELES. WorkflowRun</span><span class="sxs-lookup"><span data-stu-id="60c00-134">Microsoft.Azure.Management.Logic.Models.WorkflowRun</span></span>

## <span data-ttu-id="60c00-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="60c00-135">NOTES</span></span>

## <span data-ttu-id="60c00-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="60c00-136">RELATED LINKS</span></span>

[<span data-ttu-id="60c00-137">Get-AzLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="60c00-137">Get-AzLogicAppRunAction</span></span>](./Get-AzLogicAppRunAction.md)

[<span data-ttu-id="60c00-138">Start — AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="60c00-138">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)

[<span data-ttu-id="60c00-139">Zatrzymaj — AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="60c00-139">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)


