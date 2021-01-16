---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F271BCB1-6D43-48E5-BB51-00288F57BFFB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapprunhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
ms.openlocfilehash: 1e847131a67e55fa7a9c520c6ce5a5d96f0475f3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358570"
---
# <span data-ttu-id="3cee3-101">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="3cee3-101">Get-AzLogicAppRunHistory</span></span>

## <span data-ttu-id="3cee3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3cee3-102">SYNOPSIS</span></span>
<span data-ttu-id="3cee3-103">Pobiera historię przebiegu aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="3cee3-103">Gets the run history of a logic app.</span></span>

## <span data-ttu-id="3cee3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3cee3-104">SYNTAX</span></span>

```
Get-AzLogicAppRunHistory -ResourceGroupName <String> -Name <String> [-RunName <String>] [-FollowNextPageLink]
 [-MaximumFollowNextPageLink <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3cee3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3cee3-105">DESCRIPTION</span></span>
<span data-ttu-id="3cee3-106">Polecenie cmdlet **Get-AzLogicAppRunHistory** pobiera historię przebiegu aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="3cee3-106">The **Get-AzLogicAppRunHistory** cmdlet gets the run history of a logic app.</span></span>
<span data-ttu-id="3cee3-107">To polecenie cmdlet zwraca kolekcję obiektów **WorkflowRun** .</span><span class="sxs-lookup"><span data-stu-id="3cee3-107">This cmdlet returns a collection of **WorkflowRun** objects.</span></span>
<span data-ttu-id="3cee3-108">Określ aplikację logiczną i grupę zasobów.</span><span class="sxs-lookup"><span data-stu-id="3cee3-108">Specify the logic app and resource group.</span></span>
<span data-ttu-id="3cee3-109">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="3cee3-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="3cee3-110">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="3cee3-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="3cee3-111">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="3cee3-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="3cee3-112">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="3cee3-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="3cee3-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3cee3-113">EXAMPLES</span></span>

### <span data-ttu-id="3cee3-114">Przykład 1: uzyskiwanie historii uruchamiania aplikacji logicznej</span><span class="sxs-lookup"><span data-stu-id="3cee3-114">Example 1: Get the run history of a logic app</span></span>
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

<span data-ttu-id="3cee3-115">To polecenie pobiera historię przebiegu aplikacji logicznej o nazwie LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="3cee3-115">This command gets the run history of a logic app named LogicApp03.</span></span>

### <span data-ttu-id="3cee3-116">Przykład 2: uzyskiwanie uruchamiania aplikacji logicznej</span><span class="sxs-lookup"><span data-stu-id="3cee3-116">Example 2: Get a logic app run</span></span>
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

<span data-ttu-id="3cee3-117">To polecenie pobiera określoną aplikację logiczną w celu uruchomienia aplikacji logicznej o nazwie LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="3cee3-117">This command gets a specific logic app run for the logic app named LogicApp03.</span></span>

### <span data-ttu-id="3cee3-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="3cee3-118">Example 3</span></span>

```powershell
Get-AzLogicAppRunHistory -Name 'LogicApp03' -ResourceGroupName MyResourceGroup -FollowNextPageLink
```

<span data-ttu-id="3cee3-119">To polecenie pobiera całą historię przebiegu aplikacji logicznej o nazwie LogicApp03, wykonując NextPageLink.</span><span class="sxs-lookup"><span data-stu-id="3cee3-119">This command gets the entire run history of a logic app named LogicApp03 by following the NextPageLink.</span></span>

### <span data-ttu-id="3cee3-120">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="3cee3-120">Example 4</span></span>

```powershell
Get-AzLogicAppRunHistory -Name 'LogicApp03' -ResourceGroupName MyResourceGroup -FollowNextPageLink -MaximumFollowNextPageLink 1
```

<span data-ttu-id="3cee3-121">To polecenie umożliwia pobieranie pierwszych dwóch stron historii uruchamiania aplikacji logicznej o nazwie LogicApp03, wykonując NextPageLink i ograniczając rozmiar wyniku do dwóch stron.</span><span class="sxs-lookup"><span data-stu-id="3cee3-121">This command gets the first two pages of run history of a logic app named LogicApp03 by following the NextPageLink and limiting the result size to two pages.</span></span>
<span data-ttu-id="3cee3-122">Każda Strona zawiera trzydzieści wyników.</span><span class="sxs-lookup"><span data-stu-id="3cee3-122">Each page contains thirty results.</span></span>

## <span data-ttu-id="3cee3-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3cee3-123">PARAMETERS</span></span>

### <span data-ttu-id="3cee3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cee3-124">-DefaultProfile</span></span>
<span data-ttu-id="3cee3-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="3cee3-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3cee3-126">-FollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="3cee3-126">-FollowNextPageLink</span></span>
<span data-ttu-id="3cee3-127">Wskazuje, że polecenie cmdlet powinno śledzić linki Następna strona.</span><span class="sxs-lookup"><span data-stu-id="3cee3-127">Indicates the cmdlet should follow next page links.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: FL

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cee3-128">-MaximumFollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="3cee3-128">-MaximumFollowNextPageLink</span></span>
<span data-ttu-id="3cee3-129">Określa, ile razy należy śledzić łącza Następna strona, jeśli FollowNextPageLink jest używana.</span><span class="sxs-lookup"><span data-stu-id="3cee3-129">Specifies how many times to follow next page links if FollowNextPageLink is used.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: ML

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cee3-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3cee3-130">-Name</span></span>
<span data-ttu-id="3cee3-131">Określa nazwę aplikacji logicznej, dla której to polecenie cmdlet pobiera historię uruchamiania.</span><span class="sxs-lookup"><span data-stu-id="3cee3-131">Specifies the name of the logic app for which this cmdlet gets run history.</span></span>

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

### <span data-ttu-id="3cee3-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cee3-132">-ResourceGroupName</span></span>
<span data-ttu-id="3cee3-133">Określa nazwę grupy zasobów zawierającej aplikację logiczną.</span><span class="sxs-lookup"><span data-stu-id="3cee3-133">Specifies the name of a resource group that contains the logic app.</span></span>

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

### <span data-ttu-id="3cee3-134">-RunName</span><span class="sxs-lookup"><span data-stu-id="3cee3-134">-RunName</span></span>
<span data-ttu-id="3cee3-135">Określa nazwę uruchomienia aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="3cee3-135">Specifies the run name of a logic app.</span></span>
<span data-ttu-id="3cee3-136">To polecenie cmdlet umożliwia uruchomienie przepływu pracy, który określa ten aplet polecenia.</span><span class="sxs-lookup"><span data-stu-id="3cee3-136">This cmdlet gets the workflow run that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="3cee3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cee3-137">CommonParameters</span></span>
<span data-ttu-id="3cee3-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cee3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cee3-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3cee3-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cee3-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3cee3-140">INPUTS</span></span>

### <span data-ttu-id="3cee3-141">System. String</span><span class="sxs-lookup"><span data-stu-id="3cee3-141">System.String</span></span>

## <span data-ttu-id="3cee3-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3cee3-142">OUTPUTS</span></span>

### <span data-ttu-id="3cee3-143">Microsoft. Azure. Management. Logic. MODELES. WorkflowRun</span><span class="sxs-lookup"><span data-stu-id="3cee3-143">Microsoft.Azure.Management.Logic.Models.WorkflowRun</span></span>

## <span data-ttu-id="3cee3-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3cee3-144">NOTES</span></span>

## <span data-ttu-id="3cee3-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3cee3-145">RELATED LINKS</span></span>

[<span data-ttu-id="3cee3-146">Get-AzLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="3cee3-146">Get-AzLogicAppRunAction</span></span>](./Get-AzLogicAppRunAction.md)

[<span data-ttu-id="3cee3-147">Start — AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="3cee3-147">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)

[<span data-ttu-id="3cee3-148">Zatrzymaj — AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="3cee3-148">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)


