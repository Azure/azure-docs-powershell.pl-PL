---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F271BCB1-6D43-48E5-BB51-00288F57BFFB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapprunhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
ms.openlocfilehash: de1c40dc7c9f8fefb1a275394b066e8af96de211
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232180"
---
# <span data-ttu-id="84bf9-101">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="84bf9-101">Get-AzLogicAppRunHistory</span></span>

## <span data-ttu-id="84bf9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="84bf9-102">SYNOPSIS</span></span>
<span data-ttu-id="84bf9-103">Pobiera historię przebiegu aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="84bf9-103">Gets the run history of a logic app.</span></span>

## <span data-ttu-id="84bf9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="84bf9-104">SYNTAX</span></span>

```
Get-AzLogicAppRunHistory -ResourceGroupName <String> -Name <String> [-RunName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84bf9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="84bf9-105">DESCRIPTION</span></span>
<span data-ttu-id="84bf9-106">Polecenie cmdlet **Get-AzLogicAppRunHistory** pobiera historię przebiegu aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="84bf9-106">The **Get-AzLogicAppRunHistory** cmdlet gets the run history of a logic app.</span></span>
<span data-ttu-id="84bf9-107">To polecenie cmdlet zwraca kolekcję obiektów **WorkflowRun** .</span><span class="sxs-lookup"><span data-stu-id="84bf9-107">This cmdlet returns a collection of **WorkflowRun** objects.</span></span>
<span data-ttu-id="84bf9-108">Określ aplikację logiczną i grupę zasobów.</span><span class="sxs-lookup"><span data-stu-id="84bf9-108">Specify the logic app and resource group.</span></span>
<span data-ttu-id="84bf9-109">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="84bf9-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="84bf9-110">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="84bf9-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="84bf9-111">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="84bf9-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="84bf9-112">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="84bf9-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="84bf9-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="84bf9-113">EXAMPLES</span></span>

### <span data-ttu-id="84bf9-114">Przykład 1: uzyskiwanie historii uruchamiania aplikacji logicznej</span><span class="sxs-lookup"><span data-stu-id="84bf9-114">Example 1: Get the run history of a logic app</span></span>
```powershell
PS C:\>Get-AzLogicAppRunHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03"
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

<span data-ttu-id="84bf9-115">To polecenie pobiera historię przebiegu aplikacji logicznej o nazwie LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="84bf9-115">This command gets the run history of a logic app named LogicApp03.</span></span>

### <span data-ttu-id="84bf9-116">Przykład 2: uzyskiwanie uruchamiania aplikacji logicznej</span><span class="sxs-lookup"><span data-stu-id="84bf9-116">Example 2: Get a logic app run</span></span>
```powershell
PS C:\>Get-AzLogicAppRunHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03" -RunName "08587489104702792076"
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

<span data-ttu-id="84bf9-117">To polecenie pobiera określoną aplikację logiczną w celu uruchomienia aplikacji logicznej o nazwie LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="84bf9-117">This command gets a specific logic app run for the logic app named LogicApp03.</span></span>

### <span data-ttu-id="84bf9-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="84bf9-118">Example 3</span></span>

<span data-ttu-id="84bf9-119">To polecenie pobiera historię przebiegu aplikacji logicznej o nazwie LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="84bf9-119">This command gets the run history of a logic app named LogicApp03.</span></span> <span data-ttu-id="84bf9-120">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="84bf9-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzLogicAppRunHistory -Name 'IntegrationAccount31' -ResourceGroupName MyResourceGroup
```

## <span data-ttu-id="84bf9-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="84bf9-121">PARAMETERS</span></span>

### <span data-ttu-id="84bf9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84bf9-122">-DefaultProfile</span></span>
<span data-ttu-id="84bf9-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="84bf9-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="84bf9-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="84bf9-124">-Name</span></span>
<span data-ttu-id="84bf9-125">Określa nazwę aplikacji logicznej, dla której to polecenie cmdlet pobiera historię uruchamiania.</span><span class="sxs-lookup"><span data-stu-id="84bf9-125">Specifies the name of the logic app for which this cmdlet gets run history.</span></span>

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

### <span data-ttu-id="84bf9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84bf9-126">-ResourceGroupName</span></span>
<span data-ttu-id="84bf9-127">Określa nazwę grupy zasobów zawierającej aplikację logiczną.</span><span class="sxs-lookup"><span data-stu-id="84bf9-127">Specifies the name of a resource group that contains the logic app.</span></span>

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

### <span data-ttu-id="84bf9-128">-RunName</span><span class="sxs-lookup"><span data-stu-id="84bf9-128">-RunName</span></span>
<span data-ttu-id="84bf9-129">Określa nazwę uruchomienia aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="84bf9-129">Specifies the run name of a logic app.</span></span>
<span data-ttu-id="84bf9-130">To polecenie cmdlet umożliwia uruchomienie przepływu pracy, który określa ten aplet polecenia.</span><span class="sxs-lookup"><span data-stu-id="84bf9-130">This cmdlet gets the workflow run that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="84bf9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84bf9-131">CommonParameters</span></span>
<span data-ttu-id="84bf9-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84bf9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84bf9-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84bf9-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84bf9-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="84bf9-134">INPUTS</span></span>

### <span data-ttu-id="84bf9-135">System. String</span><span class="sxs-lookup"><span data-stu-id="84bf9-135">System.String</span></span>

## <span data-ttu-id="84bf9-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="84bf9-136">OUTPUTS</span></span>

### <span data-ttu-id="84bf9-137">Microsoft. Azure. Management. Logic. MODELES. WorkflowRun</span><span class="sxs-lookup"><span data-stu-id="84bf9-137">Microsoft.Azure.Management.Logic.Models.WorkflowRun</span></span>

## <span data-ttu-id="84bf9-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="84bf9-138">NOTES</span></span>

## <span data-ttu-id="84bf9-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="84bf9-139">RELATED LINKS</span></span>

[<span data-ttu-id="84bf9-140">Get-AzLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="84bf9-140">Get-AzLogicAppRunAction</span></span>](./Get-AzLogicAppRunAction.md)

[<span data-ttu-id="84bf9-141">Start — AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="84bf9-141">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)

[<span data-ttu-id="84bf9-142">Zatrzymaj — AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="84bf9-142">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)


