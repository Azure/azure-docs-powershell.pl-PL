---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Trigger.md
ms.openlocfilehash: cb0d548e1fcbc7acecf1ae1457eb762d4cf81645
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355285"
---
# <span data-ttu-id="36ca0-101">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="36ca0-101">Set-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="36ca0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="36ca0-102">SYNOPSIS</span></span>
<span data-ttu-id="36ca0-103">Tworzy wyzwalacz w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="36ca0-103">Creates a trigger in a data factory.</span></span>

## <span data-ttu-id="36ca0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="36ca0-104">SYNTAX</span></span>

### <span data-ttu-id="36ca0-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="36ca0-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2Trigger [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="36ca0-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="36ca0-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2Trigger [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36ca0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="36ca0-107">DESCRIPTION</span></span>
<span data-ttu-id="36ca0-108">Polecenie cmdlet **Set-AzDataFactoryV2Trigger** tworzy wyzwalacz w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="36ca0-108">The **Set-AzDataFactoryV2Trigger** cmdlet creates a trigger in a data factory.</span></span> <span data-ttu-id="36ca0-109">Jeśli określisz nazwę wyzwalacza, który już istnieje, przed zastąpieniem wyzwalacza polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="36ca0-109">If you specify a name for a trigger that already exists, the cmdlet prompts for confirmation before replacing the trigger.</span></span> <span data-ttu-id="36ca0-110">Jeśli określisz parametr _Force_ , polecenie cmdlet zastępuje istniejący wyzwalacz bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="36ca0-110">If you specify the _Force_ parameter, the cmdlet replaces the existing trigger without prompting for confirmation.</span></span> <span data-ttu-id="36ca0-111">Wyzwalacze są tworzone w stanie "zatrzymane", co oznacza, że nie zaczynają od razu rozpoczynać od siebie potoków, do których się odwołują.</span><span class="sxs-lookup"><span data-stu-id="36ca0-111">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="36ca0-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="36ca0-112">EXAMPLES</span></span>

### <span data-ttu-id="36ca0-113">Przykład 1. Tworzenie wyzwalacza</span><span class="sxs-lookup"><span data-stu-id="36ca0-113">Example 1: Create a trigger</span></span>
```
PS C:\> Set-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger" -DefinitionFile ".\scheduledTrigger.json"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="36ca0-114">Utwórz nowy wyzwalacz o nazwie "ScheduledTrigger" w fabryce danych "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="36ca0-114">Create a new trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span> <span data-ttu-id="36ca0-115">Wyzwalacz jest tworzony w stanie "zatrzymane", co oznacza, że nie jest od razu uruchomiony.</span><span class="sxs-lookup"><span data-stu-id="36ca0-115">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="36ca0-116">Wyzwalacz można uruchomić przy użyciu `Start-AzDataFactoryV2Trigger` polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36ca0-116">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="36ca0-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="36ca0-117">PARAMETERS</span></span>

### <span data-ttu-id="36ca0-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="36ca0-118">-DataFactoryName</span></span>
<span data-ttu-id="36ca0-119">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="36ca0-119">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36ca0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36ca0-120">-DefaultProfile</span></span>
<span data-ttu-id="36ca0-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="36ca0-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36ca0-122">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="36ca0-122">-DefinitionFile</span></span>
<span data-ttu-id="36ca0-123">Ścieżka pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="36ca0-123">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36ca0-124">-Force</span><span class="sxs-lookup"><span data-stu-id="36ca0-124">-Force</span></span>
<span data-ttu-id="36ca0-125">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="36ca0-125">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36ca0-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="36ca0-126">-Name</span></span>
<span data-ttu-id="36ca0-127">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="36ca0-127">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36ca0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36ca0-128">-ResourceGroupName</span></span>
<span data-ttu-id="36ca0-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="36ca0-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36ca0-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36ca0-130">-ResourceId</span></span>
<span data-ttu-id="36ca0-131">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="36ca0-131">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36ca0-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="36ca0-132">-Confirm</span></span>
<span data-ttu-id="36ca0-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36ca0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36ca0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36ca0-134">-WhatIf</span></span>
<span data-ttu-id="36ca0-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36ca0-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="36ca0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36ca0-136">CommonParameters</span></span>
<span data-ttu-id="36ca0-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36ca0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36ca0-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36ca0-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36ca0-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36ca0-139">INPUTS</span></span>

### <span data-ttu-id="36ca0-140">System. String</span><span class="sxs-lookup"><span data-stu-id="36ca0-140">System.String</span></span>

## <span data-ttu-id="36ca0-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="36ca0-141">OUTPUTS</span></span>

### <span data-ttu-id="36ca0-142">Microsoft. Azure. Commands. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="36ca0-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="36ca0-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="36ca0-143">NOTES</span></span>

## <span data-ttu-id="36ca0-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="36ca0-144">RELATED LINKS</span></span>

[<span data-ttu-id="36ca0-145">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="36ca0-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="36ca0-146">Start — AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="36ca0-146">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="36ca0-147">Zatrzymaj — AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="36ca0-147">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="36ca0-148">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="36ca0-148">Remove-AzDataFactoryV2Trigger</span></span>]()
