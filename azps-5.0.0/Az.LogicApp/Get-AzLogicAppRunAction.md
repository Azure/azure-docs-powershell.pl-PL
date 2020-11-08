---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 2EA28B90-4BAE-45DF-BD2E-60C74F53FB7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapprunaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
ms.openlocfilehash: c382b4bb9a02150beaa6880fd88d8f7b376b7c34
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234634"
---
# <span data-ttu-id="0be62-101">Get-AzLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="0be62-101">Get-AzLogicAppRunAction</span></span>

## <span data-ttu-id="0be62-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0be62-102">SYNOPSIS</span></span>
<span data-ttu-id="0be62-103">Pobiera akcję z uruchomienia aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="0be62-103">Gets an action from a logic app run.</span></span>

## <span data-ttu-id="0be62-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0be62-104">SYNTAX</span></span>

```
Get-AzLogicAppRunAction -ResourceGroupName <String> -Name <String> -RunName <String> [-ActionName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0be62-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0be62-105">DESCRIPTION</span></span>
<span data-ttu-id="0be62-106">Polecenie cmdlet **Get-AzLogicAppRunAction** umożliwia wykonanie akcji z poziomu aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="0be62-106">The **Get-AzLogicAppRunAction** cmdlet gets an action from a logic app run.</span></span>
<span data-ttu-id="0be62-107">To polecenie cmdlet zwraca obiekty **WorkflowRunAction** .</span><span class="sxs-lookup"><span data-stu-id="0be62-107">This cmdlet returns a **WorkflowRunAction** objects.</span></span>
<span data-ttu-id="0be62-108">Określ aplikację logiczną, grupę zasobów i działanie.</span><span class="sxs-lookup"><span data-stu-id="0be62-108">Specify the logic app, resource group, and run.</span></span>
<span data-ttu-id="0be62-109">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="0be62-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="0be62-110">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="0be62-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="0be62-111">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="0be62-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="0be62-112">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="0be62-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="0be62-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0be62-113">EXAMPLES</span></span>

### <span data-ttu-id="0be62-114">Przykład 1: uzyskiwanie akcji w ramach uruchamiania aplikacji logiki</span><span class="sxs-lookup"><span data-stu-id="0be62-114">Example 1: Get an action from a Logic App run</span></span>
```powershell
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

<span data-ttu-id="0be62-115">To polecenie pobiera określoną akcję logiczną z aplikacji logicznej o nazwie LogicApp05 dla uruchomienia o nazwie LogicAppRun56.</span><span class="sxs-lookup"><span data-stu-id="0be62-115">This command gets a specific Logic App action from the logic app named LogicApp05 for the run named LogicAppRun56.</span></span>

### <span data-ttu-id="0be62-116">Przykład 2: uzyskiwanie wszystkich akcji z poziomu aplikacji logiki</span><span class="sxs-lookup"><span data-stu-id="0be62-116">Example 2: Get all the actions from a Logic App run</span></span>
```powershell
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

<span data-ttu-id="0be62-117">To polecenie uzyskuje wszystkie akcje aplikacji logicznych od uruchomienia o nazwie LogicAppRun56 w aplikacji logicznej o nazwie LogicApp05.</span><span class="sxs-lookup"><span data-stu-id="0be62-117">This command gets all Logic App actions from a run named LogicAppRun56 of a logic app named LogicApp05.</span></span>

### <span data-ttu-id="0be62-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="0be62-118">Example 3</span></span>

<span data-ttu-id="0be62-119">To polecenie uzyskuje wszystkie akcje aplikacji logicznych od uruchomienia o nazwie LogicAppRun56 w aplikacji logicznej o nazwie LogicApp05.</span><span class="sxs-lookup"><span data-stu-id="0be62-119">This command gets all Logic App actions from a run named LogicAppRun56 of a logic app named LogicApp05.</span></span> <span data-ttu-id="0be62-120">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="0be62-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzLogicAppRunAction -Name 'IntegrationAccount31' -ResourceGroupName MyResourceGroup -RunName '08587489104702792076'
```

## <span data-ttu-id="0be62-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0be62-121">PARAMETERS</span></span>

### <span data-ttu-id="0be62-122">-ActionName</span><span class="sxs-lookup"><span data-stu-id="0be62-122">-ActionName</span></span>
<span data-ttu-id="0be62-123">Określa nazwę akcji w logicznym uruchomieniu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="0be62-123">Specifies the name of an action in a logic app run.</span></span>
<span data-ttu-id="0be62-124">To polecenie cmdlet spowoduje wyświetlenie akcji, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="0be62-124">This cmdlet gets the action that this parameter specifies.</span></span>

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

### <span data-ttu-id="0be62-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0be62-125">-DefaultProfile</span></span>
<span data-ttu-id="0be62-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="0be62-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0be62-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0be62-127">-Name</span></span>
<span data-ttu-id="0be62-128">Określa nazwę aplikacji logicznej, dla której to polecenie cmdlet pobiera akcję.</span><span class="sxs-lookup"><span data-stu-id="0be62-128">Specifies the name of a logic app for which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="0be62-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0be62-129">-ResourceGroupName</span></span>
<span data-ttu-id="0be62-130">Określa nazwę grupy zasobów, w której ten aplet polecenia pobiera akcję.</span><span class="sxs-lookup"><span data-stu-id="0be62-130">Specifies the name of a resource group in which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="0be62-131">-RunName</span><span class="sxs-lookup"><span data-stu-id="0be62-131">-RunName</span></span>
<span data-ttu-id="0be62-132">Określa nazwę uruchomienia aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="0be62-132">Specifies the name of a run of a logic app.</span></span>
<span data-ttu-id="0be62-133">To polecenie cmdlet spowoduje wyświetlenie akcji dotyczącej polecenia Uruchom, które ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="0be62-133">This cmdlet gets an action for the run that this parameter specifies.</span></span>

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

### <span data-ttu-id="0be62-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0be62-134">CommonParameters</span></span>
<span data-ttu-id="0be62-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0be62-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0be62-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0be62-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0be62-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0be62-137">INPUTS</span></span>

### <span data-ttu-id="0be62-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0be62-138">System.String</span></span>

## <span data-ttu-id="0be62-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0be62-139">OUTPUTS</span></span>

### <span data-ttu-id="0be62-140">Microsoft. Azure. Management. Logic. MODELES. WorkflowRunAction</span><span class="sxs-lookup"><span data-stu-id="0be62-140">Microsoft.Azure.Management.Logic.Models.WorkflowRunAction</span></span>

## <span data-ttu-id="0be62-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0be62-141">NOTES</span></span>

## <span data-ttu-id="0be62-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0be62-142">RELATED LINKS</span></span>

[<span data-ttu-id="0be62-143">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="0be62-143">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="0be62-144">Zatrzymaj — AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="0be62-144">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)


