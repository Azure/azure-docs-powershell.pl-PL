---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 5307F1F1-E84C-4949-A557-99EF0012C3DF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermlogicapptrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTrigger.md
ms.openlocfilehash: f9f21689a894e46a9cd8d53d591d1cb17099fad8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528121"
---
# <span data-ttu-id="5d64d-101">Get-AzureRmLogicAppTrigger</span><span class="sxs-lookup"><span data-stu-id="5d64d-101">Get-AzureRmLogicAppTrigger</span></span>

## <span data-ttu-id="5d64d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5d64d-102">SYNOPSIS</span></span>
<span data-ttu-id="5d64d-103">Pobiera wyzwalacze aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="5d64d-103">Gets the triggers of a logic app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d64d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5d64d-104">SYNTAX</span></span>

```
Get-AzureRmLogicAppTrigger -ResourceGroupName <String> -Name <String> [-TriggerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d64d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5d64d-105">DESCRIPTION</span></span>
<span data-ttu-id="5d64d-106">Polecenie cmdlet **Get-AzureRmLogicAppTrigger** pobiera wyzwalacze z aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="5d64d-106">The **Get-AzureRmLogicAppTrigger** cmdlet gets triggers from a logic app.</span></span>
<span data-ttu-id="5d64d-107">To polecenie cmdlet zwraca obiekt **WorkflowTrigger** .</span><span class="sxs-lookup"><span data-stu-id="5d64d-107">This cmdlet returns a **WorkflowTrigger** object.</span></span>
<span data-ttu-id="5d64d-108">Określ przepływ pracy, grupę zasobów i wyzwalacz.</span><span class="sxs-lookup"><span data-stu-id="5d64d-108">Specify the workflow, resource group, and trigger.</span></span>

<span data-ttu-id="5d64d-109">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="5d64d-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="5d64d-110">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="5d64d-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="5d64d-111">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="5d64d-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="5d64d-112">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="5d64d-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="5d64d-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5d64d-113">EXAMPLES</span></span>

### <span data-ttu-id="5d64d-114">Przykład 1: uzyskiwanie wyzwalacza aplikacji logicznej</span><span class="sxs-lookup"><span data-stu-id="5d64d-114">Example 1: Get a trigger of a logic app</span></span>
```
PS C:\>Get-AzureRmLogicAppTrigger -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -TriggerName "Trigger01"
ChangedTime         : 1/14/2016 11:45:07 AM
CreatedTime         : 1/13/2016 2:42:26 PM
LastExecutionTime   : 1/14/2016 11:45:07 AM
Name                : Trigger01
NextExecutionTime   : 1/14/2016 12:45:07 PM
RecurrenceFrequency : Minute
RecurrenceInterval  : 60
Status              : Waiting
Type                : Microsoft.Logic/workflows/triggers
LogicAppName        : LogicApp05
LogicAppVersion     : 08587489107406290826
```

<span data-ttu-id="5d64d-115">To polecenie pobiera wyzwalacz o nazwie Trigger01 z aplikacji logiki o nazwie LogicApp05.</span><span class="sxs-lookup"><span data-stu-id="5d64d-115">This command gets the trigger named Trigger01 from the logic app named LogicApp05.</span></span>

### <span data-ttu-id="5d64d-116">Przykład 2: uzyskiwanie wszystkich wyzwalaczy aplikacji logicznej</span><span class="sxs-lookup"><span data-stu-id="5d64d-116">Example 2: Get all triggers of a logic app</span></span>
```
PS C:\>Get-AzureRmLogicAppTrigger -ResourceGroupName "ResourceGroup11" -Name "LogicApp07"
ChangedTime         : 1/14/2016 11:45:07 AM
CreatedTime         : 1/13/2016 2:42:26 PM
LastExecutionTime   : 1/14/2016 11:45:07 AM
Name                : Trigger02
NextExecutionTime   : 1/14/2016 12:45:07 PM
RecurrenceFrequency : Minute
RecurrenceInterval  : 60
Status              : Waiting
Type                : Microsoft.Logic/workflows/triggers
LogicAppName        : LogicApp07
LogicAppVersion     : 08587489107406290826
```

<span data-ttu-id="5d64d-117">To polecenie pobiera wyzwalacze aplikacji logicznej o nazwie LogicApp07.</span><span class="sxs-lookup"><span data-stu-id="5d64d-117">This command gets the triggers of the logic app named LogicApp07.</span></span>

## <span data-ttu-id="5d64d-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5d64d-118">PARAMETERS</span></span>

### <span data-ttu-id="5d64d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d64d-119">-DefaultProfile</span></span>
<span data-ttu-id="5d64d-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="5d64d-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5d64d-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5d64d-121">-Name</span></span>
<span data-ttu-id="5d64d-122">Określa nazwę aplikacji logicznej, z poziomu której to polecenie cmdlet pobiera wyzwalacz.</span><span class="sxs-lookup"><span data-stu-id="5d64d-122">Specifies the name of the logic app from which this cmdlet gets a trigger.</span></span>

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

### <span data-ttu-id="5d64d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d64d-123">-ResourceGroupName</span></span>
<span data-ttu-id="5d64d-124">Określa nazwę grupy zasobów, w której ten aplet polecenia pobiera wyzwalacz.</span><span class="sxs-lookup"><span data-stu-id="5d64d-124">Specifies the name of a resource group in which this cmdlet gets a trigger.</span></span>

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

### <span data-ttu-id="5d64d-125">-Triggername</span><span class="sxs-lookup"><span data-stu-id="5d64d-125">-TriggerName</span></span>
<span data-ttu-id="5d64d-126">Określa nazwę wyzwalacza, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d64d-126">Specifies the name of the trigger that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d64d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d64d-127">CommonParameters</span></span>
<span data-ttu-id="5d64d-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d64d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d64d-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d64d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d64d-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5d64d-130">INPUTS</span></span>

### <span data-ttu-id="5d64d-131">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="5d64d-131">None</span></span>
<span data-ttu-id="5d64d-132">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="5d64d-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5d64d-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5d64d-133">OUTPUTS</span></span>

### <span data-ttu-id="5d64d-134">Microsoft. Azure. Management. Logic. MODELES. WorkflowTrigger</span><span class="sxs-lookup"><span data-stu-id="5d64d-134">Microsoft.Azure.Management.Logic.Models.WorkflowTrigger</span></span>

## <span data-ttu-id="5d64d-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5d64d-135">NOTES</span></span>

## <span data-ttu-id="5d64d-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5d64d-136">RELATED LINKS</span></span>

[<span data-ttu-id="5d64d-137">Get-AzureRmLogicAppTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="5d64d-137">Get-AzureRmLogicAppTriggerHistory</span></span>](./Get-AzureRmLogicAppTriggerHistory.md)

[<span data-ttu-id="5d64d-138">Start — AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="5d64d-138">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)

