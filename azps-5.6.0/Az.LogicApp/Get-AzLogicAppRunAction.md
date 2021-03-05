---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 2EA28B90-4BAE-45DF-BD2E-60C74F53FB7B
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azlogicapprunaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
ms.openlocfilehash: 6835fb2ce58e834e9270af293fdc4f0d07fc01aa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008970"
---
# <span data-ttu-id="de8c0-101">Get-AzLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="de8c0-101">Get-AzLogicAppRunAction</span></span>

## <span data-ttu-id="de8c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de8c0-102">SYNOPSIS</span></span>

<span data-ttu-id="de8c0-103">Pobiera akcję z uruchomienia aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="de8c0-103">Gets an action from a logic app run.</span></span>

## <span data-ttu-id="de8c0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="de8c0-104">SYNTAX</span></span>

```powershell
Get-AzLogicAppRunAction -ResourceGroupName <String> -Name <String> -RunName <String> [-ActionName <String>]
 [-FollowNextPageLink] [-MaximumFollowNextPageLink <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="de8c0-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="de8c0-105">DESCRIPTION</span></span>

<span data-ttu-id="de8c0-106">Polecenie **cmdlet Get-AzLogicAppRunAction** pobiera akcję z uruchomienia aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="de8c0-106">The **Get-AzLogicAppRunAction** cmdlet gets an action from a logic app run.</span></span>
<span data-ttu-id="de8c0-107">To polecenie cmdlet zwraca obiekty **WorkflowRunAction.**</span><span class="sxs-lookup"><span data-stu-id="de8c0-107">This cmdlet returns a **WorkflowRunAction** objects.</span></span>
<span data-ttu-id="de8c0-108">Określanie aplikacji logiki, grupy zasobów i uruchamianie.</span><span class="sxs-lookup"><span data-stu-id="de8c0-108">Specify the logic app, resource group, and run.</span></span>
<span data-ttu-id="de8c0-109">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="de8c0-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="de8c0-110">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="de8c0-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="de8c0-111">Aby wykryć nazwy parametrów dynamicznych, wpisz łącznik (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić przez dostępne parametry.</span><span class="sxs-lookup"><span data-stu-id="de8c0-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="de8c0-112">Jeśli pominiesz wymagany parametr szablonu, polecenie cmdlet wyświetli monit o wartość.</span><span class="sxs-lookup"><span data-stu-id="de8c0-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="de8c0-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="de8c0-113">EXAMPLES</span></span>

### <span data-ttu-id="de8c0-114">Przykład 1. Uzyskiwanie akcji z uruchomienia aplikacji logiki</span><span class="sxs-lookup"><span data-stu-id="de8c0-114">Example 1: Get an action from a Logic App run</span></span>

```powershell
PS C:\>Get-AzLogicAppRunAction -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "08585925184423369718380498702CU26" -ActionName "LogicAppAction01"
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

<span data-ttu-id="de8c0-115">To polecenie pobiera określoną akcję aplikacji logiki z aplikacji logiki o nazwie LogicApp05 dla uruchomienia z identyfikatorem 08585925184423369718380498702CU26.</span><span class="sxs-lookup"><span data-stu-id="de8c0-115">This command gets a specific Logic App action from the logic app named LogicApp05 for the run with identifier 08585925184423369718380498702CU26.</span></span>

### <span data-ttu-id="de8c0-116">Przykład 2. Uzyskiwanie wszystkich akcji z uruchomienia aplikacji logiki</span><span class="sxs-lookup"><span data-stu-id="de8c0-116">Example 2: Get all the actions from a Logic App run</span></span>

```powershell
PS C:\>Get-AzLogicAppRunAction -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "08585925184423369718380498702CU26" -FollowNextPageLink
```

<span data-ttu-id="de8c0-117">To polecenie pobiera wszystkie akcje aplikacji logiki z uruchomienia z identyfikatorem 08585925184423369718380498702CU26 aplikacji logiki o nazwie LogicApp05.</span><span class="sxs-lookup"><span data-stu-id="de8c0-117">This command gets all Logic App actions from a run with identifier 08585925184423369718380498702CU26 of a logic app named LogicApp05.</span></span>

## <span data-ttu-id="de8c0-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="de8c0-118">PARAMETERS</span></span>

### <span data-ttu-id="de8c0-119">-ActionName</span><span class="sxs-lookup"><span data-stu-id="de8c0-119">-ActionName</span></span>

<span data-ttu-id="de8c0-120">Określa nazwę akcji w uruchomieniu aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="de8c0-120">Specifies the name of an action in a logic app run.</span></span>
<span data-ttu-id="de8c0-121">To polecenie cmdlet pobiera akcję określaną przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="de8c0-121">This cmdlet gets the action that this parameter specifies.</span></span>

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

### <span data-ttu-id="de8c0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de8c0-122">-DefaultProfile</span></span>

<span data-ttu-id="de8c0-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="de8c0-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="de8c0-124">-FollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="de8c0-124">-FollowNextPageLink</span></span>

<span data-ttu-id="de8c0-125">Wskazuje, że polecenie cmdlet powinno postępować zgodnie z linkami do następnej strony.</span><span class="sxs-lookup"><span data-stu-id="de8c0-125">Indicates the cmdlet should follow next page links.</span></span>

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

### <span data-ttu-id="de8c0-126">-MaximumFollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="de8c0-126">-MaximumFollowNextPageLink</span></span>

<span data-ttu-id="de8c0-127">Określa, ile razy mają być używane łącza następnej strony, jeśli jest używana opcja FollowNextPageLink.</span><span class="sxs-lookup"><span data-stu-id="de8c0-127">Specifies how many times to follow next page links if FollowNextPageLink is used.</span></span>

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

### <span data-ttu-id="de8c0-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="de8c0-128">-Name</span></span>

<span data-ttu-id="de8c0-129">Określa nazwę aplikacji logiki, dla której to polecenie cmdlet uzyskuje akcję.</span><span class="sxs-lookup"><span data-stu-id="de8c0-129">Specifies the name of a logic app for which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="de8c0-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de8c0-130">-ResourceGroupName</span></span>

<span data-ttu-id="de8c0-131">Określa nazwę grupy zasobów, w której to polecenie cmdlet pobiera akcję.</span><span class="sxs-lookup"><span data-stu-id="de8c0-131">Specifies the name of a resource group in which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="de8c0-132">-RunName</span><span class="sxs-lookup"><span data-stu-id="de8c0-132">-RunName</span></span>

<span data-ttu-id="de8c0-133">Określa nazwę uruchomienia aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="de8c0-133">Specifies the name of a run of a logic app.</span></span>
<span data-ttu-id="de8c0-134">To polecenie cmdlet pobiera akcję dla uruchomienia, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="de8c0-134">This cmdlet gets an action for the run that this parameter specifies.</span></span>

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

### <span data-ttu-id="de8c0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de8c0-135">CommonParameters</span></span>

<span data-ttu-id="de8c0-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de8c0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de8c0-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="de8c0-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de8c0-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="de8c0-138">INPUTS</span></span>

### <span data-ttu-id="de8c0-139">System.String</span><span class="sxs-lookup"><span data-stu-id="de8c0-139">System.String</span></span>

## <span data-ttu-id="de8c0-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="de8c0-140">OUTPUTS</span></span>

### <span data-ttu-id="de8c0-141">Microsoft.Azure.Management.Logic.Models.WorkflowRunAction</span><span class="sxs-lookup"><span data-stu-id="de8c0-141">Microsoft.Azure.Management.Logic.Models.WorkflowRunAction</span></span>

## <span data-ttu-id="de8c0-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="de8c0-142">NOTES</span></span>

## <span data-ttu-id="de8c0-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="de8c0-143">RELATED LINKS</span></span>

[<span data-ttu-id="de8c0-144">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="de8c0-144">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="de8c0-145">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="de8c0-145">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)
