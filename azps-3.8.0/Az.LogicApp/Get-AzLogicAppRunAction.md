---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 2EA28B90-4BAE-45DF-BD2E-60C74F53FB7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapprunaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
ms.openlocfilehash: 8aae52b52edbdbb456e9332fa96d1f1f78dac266
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895130"
---
# <span data-ttu-id="14d18-101">Get-AzLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="14d18-101">Get-AzLogicAppRunAction</span></span>

## <span data-ttu-id="14d18-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="14d18-102">SYNOPSIS</span></span>
<span data-ttu-id="14d18-103">Pobiera akcję z uruchomienia aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="14d18-103">Gets an action from a logic app run.</span></span>

## <span data-ttu-id="14d18-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="14d18-104">SYNTAX</span></span>

```
Get-AzLogicAppRunAction -ResourceGroupName <String> -Name <String> -RunName <String> [-ActionName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14d18-105">Opis</span><span class="sxs-lookup"><span data-stu-id="14d18-105">DESCRIPTION</span></span>
<span data-ttu-id="14d18-106">Polecenie cmdlet **Get-AzLogicAppRunAction** umożliwia wykonanie akcji z poziomu aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="14d18-106">The **Get-AzLogicAppRunAction** cmdlet gets an action from a logic app run.</span></span>
<span data-ttu-id="14d18-107">To polecenie cmdlet zwraca obiekty **WorkflowRunAction** .</span><span class="sxs-lookup"><span data-stu-id="14d18-107">This cmdlet returns a **WorkflowRunAction** objects.</span></span>
<span data-ttu-id="14d18-108">Określ aplikację logiczną, grupę zasobów i działanie.</span><span class="sxs-lookup"><span data-stu-id="14d18-108">Specify the logic app, resource group, and run.</span></span>
<span data-ttu-id="14d18-109">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="14d18-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="14d18-110">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="14d18-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="14d18-111">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="14d18-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="14d18-112">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="14d18-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="14d18-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="14d18-113">EXAMPLES</span></span>

### <span data-ttu-id="14d18-114">Przykład 1: uzyskiwanie akcji w ramach uruchamiania aplikacji logiki</span><span class="sxs-lookup"><span data-stu-id="14d18-114">Example 1: Get an action from a Logic App run</span></span>
```
PS C:\>Get-AzLogicAppActionRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "LogicAppRun56" -ActionName "LogicAppAction01"
Code        : NotFound
EndTime     : 1/13/2016 2:42:56 PM
Error       : 
InputsLink  : Microsoft.Azure.Management.Logic.Models.ContentLink
Name        : LogicAppAction01
OutputsLink : Microsoft.Azure.Management.Logic.Models.ContentLink
StartTime   : 1/13/2016 2:42:55 PM
Status      : Failed
TrackingId  : 
Type        :
```

<span data-ttu-id="14d18-115">To polecenie pobiera określoną akcję logiczną z aplikacji logicznej o nazwie LogicApp05 dla uruchomienia o nazwie LogicAppRun56.</span><span class="sxs-lookup"><span data-stu-id="14d18-115">This command gets a specific Logic App action from the logic app named LogicApp05 for the run named LogicAppRun56.</span></span>

### <span data-ttu-id="14d18-116">Przykład 2: uzyskiwanie wszystkich akcji z poziomu aplikacji logiki</span><span class="sxs-lookup"><span data-stu-id="14d18-116">Example 2: Get all the actions from a Logic App run</span></span>
```
PS C:\>Get-AzLogicAppActionRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "LogicAppRun56"
Code        : NotFound
EndTime     : 1/13/2016 2:42:56 PM
Error       : 
InputsLink  : Microsoft.Azure.Management.Logic.Models.ContentLink
Name        : LogicAppAction1
OutputsLink : Microsoft.Azure.Management.Logic.Models.ContentLink
StartTime   : 1/13/2016 2:42:55 PM
Status      : Failed
TrackingId  : 
Type        :
```

<span data-ttu-id="14d18-117">To polecenie uzyskuje wszystkie akcje aplikacji logicznych od uruchomienia o nazwie LogicAppRun56 w aplikacji logicznej o nazwie LogicApp05.</span><span class="sxs-lookup"><span data-stu-id="14d18-117">This command gets all Logic App actions from a run named LogicAppRun56 of a logic app named LogicApp05.</span></span>

## <span data-ttu-id="14d18-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="14d18-118">PARAMETERS</span></span>

### <span data-ttu-id="14d18-119">-ActionName</span><span class="sxs-lookup"><span data-stu-id="14d18-119">-ActionName</span></span>
<span data-ttu-id="14d18-120">Określa nazwę akcji w logicznym uruchomieniu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="14d18-120">Specifies the name of an action in a logic app run.</span></span>
<span data-ttu-id="14d18-121">To polecenie cmdlet spowoduje wyświetlenie akcji, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="14d18-121">This cmdlet gets the action that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14d18-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14d18-122">-DefaultProfile</span></span>
<span data-ttu-id="14d18-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="14d18-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="14d18-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="14d18-124">-Name</span></span>
<span data-ttu-id="14d18-125">Określa nazwę aplikacji logicznej, dla której to polecenie cmdlet pobiera akcję.</span><span class="sxs-lookup"><span data-stu-id="14d18-125">Specifies the name of a logic app for which this cmdlet gets an action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14d18-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14d18-126">-ResourceGroupName</span></span>
<span data-ttu-id="14d18-127">Określa nazwę grupy zasobów, w której ten aplet polecenia pobiera akcję.</span><span class="sxs-lookup"><span data-stu-id="14d18-127">Specifies the name of a resource group in which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="14d18-128">-RunName</span><span class="sxs-lookup"><span data-stu-id="14d18-128">-RunName</span></span>
<span data-ttu-id="14d18-129">Określa nazwę uruchomienia aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="14d18-129">Specifies the name of a run of a logic app.</span></span>
<span data-ttu-id="14d18-130">To polecenie cmdlet spowoduje wyświetlenie akcji dotyczącej polecenia Uruchom, które ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="14d18-130">This cmdlet gets an action for the run that this parameter specifies.</span></span>

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

### <span data-ttu-id="14d18-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14d18-131">CommonParameters</span></span>
<span data-ttu-id="14d18-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14d18-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14d18-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14d18-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14d18-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="14d18-134">INPUTS</span></span>

### <span data-ttu-id="14d18-135">System. String</span><span class="sxs-lookup"><span data-stu-id="14d18-135">System.String</span></span>

## <span data-ttu-id="14d18-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="14d18-136">OUTPUTS</span></span>

### <span data-ttu-id="14d18-137">Microsoft. Azure. Management. Logic. MODELES. WorkflowRunAction</span><span class="sxs-lookup"><span data-stu-id="14d18-137">Microsoft.Azure.Management.Logic.Models.WorkflowRunAction</span></span>

## <span data-ttu-id="14d18-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="14d18-138">NOTES</span></span>

## <span data-ttu-id="14d18-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="14d18-139">RELATED LINKS</span></span>

[<span data-ttu-id="14d18-140">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="14d18-140">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="14d18-141">Zatrzymaj — AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="14d18-141">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)


