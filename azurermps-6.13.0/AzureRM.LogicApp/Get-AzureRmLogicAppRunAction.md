---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 2EA28B90-4BAE-45DF-BD2E-60C74F53FB7B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermlogicapprunaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppRunAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppRunAction.md
ms.openlocfilehash: 4aa135adf8db8cc1044eba761b33f570abd0396b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716716"
---
# <span data-ttu-id="4d843-101">Get-AzureRmLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="4d843-101">Get-AzureRmLogicAppRunAction</span></span>

## <span data-ttu-id="4d843-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4d843-102">SYNOPSIS</span></span>
<span data-ttu-id="4d843-103">Pobiera akcję z uruchomienia aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="4d843-103">Gets an action from a logic app run.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d843-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4d843-104">SYNTAX</span></span>

```
Get-AzureRmLogicAppRunAction -ResourceGroupName <String> -Name <String> -RunName <String>
 [-ActionName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d843-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4d843-105">DESCRIPTION</span></span>
<span data-ttu-id="4d843-106">Polecenie cmdlet **Get-AzureRmLogicAppRunAction** umożliwia wykonanie akcji z poziomu aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="4d843-106">The **Get-AzureRmLogicAppRunAction** cmdlet gets an action from a logic app run.</span></span>
<span data-ttu-id="4d843-107">To polecenie cmdlet zwraca obiekty **WorkflowRunAction** .</span><span class="sxs-lookup"><span data-stu-id="4d843-107">This cmdlet returns a **WorkflowRunAction** objects.</span></span>
<span data-ttu-id="4d843-108">Określ aplikację logiczną, grupę zasobów i działanie.</span><span class="sxs-lookup"><span data-stu-id="4d843-108">Specify the logic app, resource group, and run.</span></span>
<span data-ttu-id="4d843-109">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="4d843-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="4d843-110">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="4d843-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="4d843-111">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="4d843-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="4d843-112">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="4d843-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="4d843-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4d843-113">EXAMPLES</span></span>

### <span data-ttu-id="4d843-114">Przykład 1: uzyskiwanie akcji w ramach uruchamiania aplikacji logiki</span><span class="sxs-lookup"><span data-stu-id="4d843-114">Example 1: Get an action from a Logic App run</span></span>
```
PS C:\>Get-AzureRmLogicAppActionRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "LogicAppRun56" -ActionName "LogicAppAction01"
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

<span data-ttu-id="4d843-115">To polecenie pobiera określoną akcję logiczną z aplikacji logicznej o nazwie LogicApp05 dla uruchomienia o nazwie LogicAppRun56.</span><span class="sxs-lookup"><span data-stu-id="4d843-115">This command gets a specific Logic App action from the logic app named LogicApp05 for the run named LogicAppRun56.</span></span>

### <span data-ttu-id="4d843-116">Przykład 2: uzyskiwanie wszystkich akcji z poziomu aplikacji logiki</span><span class="sxs-lookup"><span data-stu-id="4d843-116">Example 2: Get all the actions from a Logic App run</span></span>
```
PS C:\>Get-AzureRmLogicAppActionRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "LogicAppRun56"
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

<span data-ttu-id="4d843-117">To polecenie uzyskuje wszystkie akcje aplikacji logicznych od uruchomienia o nazwie LogicAppRun56 w aplikacji logicznej o nazwie LogicApp05.</span><span class="sxs-lookup"><span data-stu-id="4d843-117">This command gets all Logic App actions from a run named LogicAppRun56 of a logic app named LogicApp05.</span></span>

## <span data-ttu-id="4d843-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4d843-118">PARAMETERS</span></span>

### <span data-ttu-id="4d843-119">-ActionName</span><span class="sxs-lookup"><span data-stu-id="4d843-119">-ActionName</span></span>
<span data-ttu-id="4d843-120">Określa nazwę akcji w logicznym uruchomieniu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4d843-120">Specifies the name of an action in a logic app run.</span></span>
<span data-ttu-id="4d843-121">To polecenie cmdlet spowoduje wyświetlenie akcji, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="4d843-121">This cmdlet gets the action that this parameter specifies.</span></span>

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

### <span data-ttu-id="4d843-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d843-122">-DefaultProfile</span></span>
<span data-ttu-id="4d843-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="4d843-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d843-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4d843-124">-Name</span></span>
<span data-ttu-id="4d843-125">Określa nazwę aplikacji logicznej, dla której to polecenie cmdlet pobiera akcję.</span><span class="sxs-lookup"><span data-stu-id="4d843-125">Specifies the name of a logic app for which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="4d843-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d843-126">-ResourceGroupName</span></span>
<span data-ttu-id="4d843-127">Określa nazwę grupy zasobów, w której ten aplet polecenia pobiera akcję.</span><span class="sxs-lookup"><span data-stu-id="4d843-127">Specifies the name of a resource group in which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="4d843-128">-RunName</span><span class="sxs-lookup"><span data-stu-id="4d843-128">-RunName</span></span>
<span data-ttu-id="4d843-129">Określa nazwę uruchomienia aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="4d843-129">Specifies the name of a run of a logic app.</span></span>
<span data-ttu-id="4d843-130">To polecenie cmdlet spowoduje wyświetlenie akcji dotyczącej polecenia Uruchom, które ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="4d843-130">This cmdlet gets an action for the run that this parameter specifies.</span></span>

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

### <span data-ttu-id="4d843-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d843-131">CommonParameters</span></span>
<span data-ttu-id="4d843-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d843-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d843-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d843-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d843-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4d843-134">INPUTS</span></span>

### <span data-ttu-id="4d843-135">System. String</span><span class="sxs-lookup"><span data-stu-id="4d843-135">System.String</span></span>

## <span data-ttu-id="4d843-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4d843-136">OUTPUTS</span></span>

### <span data-ttu-id="4d843-137">Microsoft. Azure. Management. Logic. MODELES. WorkflowRunAction</span><span class="sxs-lookup"><span data-stu-id="4d843-137">Microsoft.Azure.Management.Logic.Models.WorkflowRunAction</span></span>

## <span data-ttu-id="4d843-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4d843-138">NOTES</span></span>

## <span data-ttu-id="4d843-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4d843-139">RELATED LINKS</span></span>

[<span data-ttu-id="4d843-140">Get-AzureRmLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="4d843-140">Get-AzureRmLogicAppRunHistory</span></span>](./Get-AzureRmLogicAppRunHistory.md)

[<span data-ttu-id="4d843-141">Zatrzymaj — AzureRmLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="4d843-141">Stop-AzureRmLogicAppRun</span></span>](./Stop-AzureRmLogicAppRun.md)


