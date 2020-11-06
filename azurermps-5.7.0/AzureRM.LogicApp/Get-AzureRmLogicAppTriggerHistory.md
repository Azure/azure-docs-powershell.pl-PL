---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: C1F6BBF9-0DB5-46FD-B8A8-9029B0AB6166
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermlogicapptriggerhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTriggerHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTriggerHistory.md
ms.openlocfilehash: 05a47123974ea3aed871e2ada3fb14981f654b27
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528117"
---
# <span data-ttu-id="5f297-101">Get-AzureRmLogicAppTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="5f297-101">Get-AzureRmLogicAppTriggerHistory</span></span>

## <span data-ttu-id="5f297-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5f297-102">SYNOPSIS</span></span>
<span data-ttu-id="5f297-103">Pobiera historię wyzwalaczy w aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="5f297-103">Gets the history of triggers in a logic app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f297-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5f297-104">SYNTAX</span></span>

```
Get-AzureRmLogicAppTriggerHistory -ResourceGroupName <String> -Name <String> -TriggerName <String>
 [-HistoryName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f297-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5f297-105">DESCRIPTION</span></span>
<span data-ttu-id="5f297-106">Polecenie cmdlet **Get-AzureRmLogicAppTriggerHistory** pobiera historię wyzwalaczy w aplikacji logicznej w funkcji aplikacje logiczne.</span><span class="sxs-lookup"><span data-stu-id="5f297-106">The **Get-AzureRmLogicAppTriggerHistory** cmdlet gets the history of triggers in a logic app in the Logic Apps feature.</span></span>
<span data-ttu-id="5f297-107">To polecenie cmdlet zwraca obiekt **WorkflowTriggerHistory** .</span><span class="sxs-lookup"><span data-stu-id="5f297-107">This cmdlet returns a **WorkflowTriggerHistory** object.</span></span>
<span data-ttu-id="5f297-108">Określ aplikację logiczną, grupę zasobów i wyzwalacz.</span><span class="sxs-lookup"><span data-stu-id="5f297-108">Specify the logic app, resource group, and trigger.</span></span>

<span data-ttu-id="5f297-109">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="5f297-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="5f297-110">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="5f297-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="5f297-111">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="5f297-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="5f297-112">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="5f297-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="5f297-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5f297-113">EXAMPLES</span></span>

### <span data-ttu-id="5f297-114">Przykład 1: uzyskiwanie historii wyzwalacza aplikacji logicznej</span><span class="sxs-lookup"><span data-stu-id="5f297-114">Example 1: Get a trigger history of a logic app</span></span>
```
PS C:\>Get-AzureRmLogicAppTriggerHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03" -TriggerName "Trigger01" -HistoryName "08587489107387695768"
Code        : BadRequest
EndTime     : 1/13/2016 2:42:26 PM
Error       : {code, message}
Fired       : False
InputsLink  : https://flowprodcu02by01.blob.core.windows.net/flow3ea9ffd11c684c9f9f258b1a6ea5cb6020160113t000000zcontent/A7392_d1e831de68ac4ef89d19a40f05e663
              cb_httpTrigger:5Finputs:2Ejson?sv=2014-02-14&sr=b&sig=&se=2016-01-14T16%3A15%3A16Z&sp=r
Name        : 08587489107387695768
OutputsLink : 
Run         : 
StartTime   : 1/13/2016 2:42:26 PM
Status      : Failed
TrackingId  : f88a499b-f80f-4a28-9bbf-c4cc0d129700
Type        : Microsoft.Logic/workflows/triggers/histories
```

<span data-ttu-id="5f297-115">To polecenie pobiera określoną historię wyzwalacza aplikacji logiki dla wyzwalacza w aplikacji logicznej o nazwie LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="5f297-115">This command gets a specific logic app trigger history for a trigger in the logic app named LogicApp03.</span></span>

### <span data-ttu-id="5f297-116">Przykład 2: uzyskiwanie historii wyzwalaczy aplikacji logicznej</span><span class="sxs-lookup"><span data-stu-id="5f297-116">Example 2: Get trigger histories of a logic app</span></span>
```
PS C:\>Get-AzureRmLogicAppTriggerHistory -ResourceGroupName "ResourceGroup11" -Name "LogicApp07" -TriggerName "Trigger01"
Code        : BadRequest
EndTime     : 1/13/2016 2:43:33 PM
Error       : {code, message}
Fired       : False
InputsLink  : https://flowprodcu02by01.blob.core.windows.net/flow3ea9ffd11c684c9f9f258b1a6ea5cb6020160113t000000zcontent/CAB46_60e2ad0f0e1947e8b5798716914c5d
              b6_httpTrigger:5Finputs:2Ejson?sv=2014-02-14&sr=b&sig=&se=2016-01-14T16%3A18%3A27Z&sp=r
Name        : 08587489106716457817
OutputsLink : 
Run         : 
StartTime   : 1/13/2016 2:43:33 PM
Status      : Failed
TrackingId  : c91a63f1-48b4-4eae-91eb-8f6dbfa9fe06
Type        : Microsoft.Logic/workflows/triggers/histories

Code        : BadRequest
EndTime     : 1/13/2016 2:42:26 PM
Error       : {code, message}
Fired       : False
InputsLink  : https://flowprodcu02by01.blob.core.windows.net/flow3ea9ffd11c684c9f9f258b1a6ea5cb6020160113t000000zcontent/A7392_d1e831de68ac4ef89d19a40f05e663
              cb_httpTrigger:5Finputs:2Ejson?sv=2014-02-14&sr=b&sig=&se=2016-01-14T16%3A18%3A27Z&sp=r
Name        : 08587489107387695768
OutputsLink : 
Run         : 
StartTime   : 1/13/2016 2:42:26 PM
Status      : Failed
TrackingId  : f88a499b-f80f-4a28-9bbf-c4cc0d129700
Type        : Microsoft.Logic/workflows/triggers/histories
```

<span data-ttu-id="5f297-117">To polecenie pobiera historie wyzwalacza przepływu pracy dla wyzwalacza w aplikacji logicznej o nazwie LogicApp07.</span><span class="sxs-lookup"><span data-stu-id="5f297-117">This command gets the workflow trigger histories for a trigger in the logic app named LogicApp07.</span></span>

## <span data-ttu-id="5f297-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5f297-118">PARAMETERS</span></span>

### <span data-ttu-id="5f297-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f297-119">-DefaultProfile</span></span>
<span data-ttu-id="5f297-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="5f297-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5f297-121">-Historyname</span><span class="sxs-lookup"><span data-stu-id="5f297-121">-HistoryName</span></span>
<span data-ttu-id="5f297-122">Określa nazwę historii, jaką uzyskuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f297-122">Specifies the name of the history that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f297-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5f297-123">-Name</span></span>
<span data-ttu-id="5f297-124">Określa nazwę aplikacji logicznej, dla której to polecenie cmdlet pobiera historię wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="5f297-124">Specifies the name of the logic app for which this cmdlet gets trigger history.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f297-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f297-125">-ResourceGroupName</span></span>
<span data-ttu-id="5f297-126">Określa nazwę grupy zasobów, w której ten aplet polecenia pobiera historię.</span><span class="sxs-lookup"><span data-stu-id="5f297-126">Specifies the name of the resource group in which this cmdlet gets history.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f297-127">-Triggername</span><span class="sxs-lookup"><span data-stu-id="5f297-127">-TriggerName</span></span>
<span data-ttu-id="5f297-128">Określa nazwę wyzwalacza, dla którego jest pobierana historia tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f297-128">Specifies the name of the trigger for which this cmdlet gets history.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f297-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f297-129">CommonParameters</span></span>
<span data-ttu-id="5f297-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f297-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f297-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f297-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f297-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5f297-132">INPUTS</span></span>

### <span data-ttu-id="5f297-133">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="5f297-133">None</span></span>
<span data-ttu-id="5f297-134">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="5f297-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5f297-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5f297-135">OUTPUTS</span></span>

### <span data-ttu-id="5f297-136">Microsoft. Azure. Management. Logic. MODELES. WorkflowTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="5f297-136">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerHistory</span></span>

## <span data-ttu-id="5f297-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5f297-137">NOTES</span></span>

## <span data-ttu-id="5f297-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5f297-138">RELATED LINKS</span></span>

[<span data-ttu-id="5f297-139">Get-AzureRmLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="5f297-139">Get-AzureRmLogicAppRunHistory</span></span>](./Get-AzureRmLogicAppRunHistory.md)

[<span data-ttu-id="5f297-140">Get-AzureRmLogicAppTrigger</span><span class="sxs-lookup"><span data-stu-id="5f297-140">Get-AzureRmLogicAppTrigger</span></span>](./Get-AzureRmLogicAppTrigger.md)

[<span data-ttu-id="5f297-141">Start — AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="5f297-141">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


