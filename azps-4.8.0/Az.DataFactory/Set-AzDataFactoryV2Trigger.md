---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Trigger.md
ms.openlocfilehash: cb0d548e1fcbc7acecf1ae1457eb762d4cf81645
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062342"
---
# <span data-ttu-id="cc0d3-101">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="cc0d3-101">Set-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="cc0d3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cc0d3-102">SYNOPSIS</span></span>
<span data-ttu-id="cc0d3-103">Tworzy wyzwalacz w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="cc0d3-103">Creates a trigger in a data factory.</span></span>

## <span data-ttu-id="cc0d3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cc0d3-104">SYNTAX</span></span>

### <span data-ttu-id="cc0d3-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cc0d3-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2Trigger [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cc0d3-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cc0d3-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2Trigger [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc0d3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="cc0d3-107">DESCRIPTION</span></span>
<span data-ttu-id="cc0d3-108">Polecenie cmdlet **Set-AzDataFactoryV2Trigger** tworzy wyzwalacz w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="cc0d3-108">The **Set-AzDataFactoryV2Trigger** cmdlet creates a trigger in a data factory.</span></span> <span data-ttu-id="cc0d3-109">Jeśli określisz nazwę wyzwalacza, który już istnieje, przed zastąpieniem wyzwalacza polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cc0d3-109">If you specify a name for a trigger that already exists, the cmdlet prompts for confirmation before replacing the trigger.</span></span> <span data-ttu-id="cc0d3-110">Jeśli określisz parametr _Force_ , polecenie cmdlet zastępuje istniejący wyzwalacz bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cc0d3-110">If you specify the _Force_ parameter, the cmdlet replaces the existing trigger without prompting for confirmation.</span></span> <span data-ttu-id="cc0d3-111">Wyzwalacze są tworzone w stanie "zatrzymane", co oznacza, że nie zaczynają od razu rozpoczynać od siebie potoków, do których się odwołują.</span><span class="sxs-lookup"><span data-stu-id="cc0d3-111">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="cc0d3-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cc0d3-112">EXAMPLES</span></span>

### <span data-ttu-id="cc0d3-113">Przykład 1. Tworzenie wyzwalacza</span><span class="sxs-lookup"><span data-stu-id="cc0d3-113">Example 1: Create a trigger</span></span>
```
PS C:\> Set-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger" -DefinitionFile ".\scheduledTrigger.json"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="cc0d3-114">Utwórz nowy wyzwalacz o nazwie "ScheduledTrigger" w fabryce danych "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="cc0d3-114">Create a new trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span> <span data-ttu-id="cc0d3-115">Wyzwalacz jest tworzony w stanie "zatrzymane", co oznacza, że nie jest od razu uruchomiony.</span><span class="sxs-lookup"><span data-stu-id="cc0d3-115">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="cc0d3-116">Wyzwalacz można uruchomić przy użyciu `Start-AzDataFactoryV2Trigger` polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc0d3-116">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="cc0d3-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cc0d3-117">PARAMETERS</span></span>

### <span data-ttu-id="cc0d3-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="cc0d3-118">-DataFactoryName</span></span>
<span data-ttu-id="cc0d3-119">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="cc0d3-119">The data factory name.</span></span>

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

### <span data-ttu-id="cc0d3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc0d3-120">-DefaultProfile</span></span>
<span data-ttu-id="cc0d3-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cc0d3-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc0d3-122">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="cc0d3-122">-DefinitionFile</span></span>
<span data-ttu-id="cc0d3-123">Ścieżka pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="cc0d3-123">The JSON file path.</span></span>

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

### <span data-ttu-id="cc0d3-124">-Force</span><span class="sxs-lookup"><span data-stu-id="cc0d3-124">-Force</span></span>
<span data-ttu-id="cc0d3-125">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cc0d3-125">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="cc0d3-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cc0d3-126">-Name</span></span>
<span data-ttu-id="cc0d3-127">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="cc0d3-127">The trigger name.</span></span>

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

### <span data-ttu-id="cc0d3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc0d3-128">-ResourceGroupName</span></span>
<span data-ttu-id="cc0d3-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cc0d3-129">The resource group name.</span></span>

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

### <span data-ttu-id="cc0d3-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cc0d3-130">-ResourceId</span></span>
<span data-ttu-id="cc0d3-131">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cc0d3-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="cc0d3-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cc0d3-132">-Confirm</span></span>
<span data-ttu-id="cc0d3-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc0d3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc0d3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc0d3-134">-WhatIf</span></span>
<span data-ttu-id="cc0d3-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc0d3-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="cc0d3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc0d3-136">CommonParameters</span></span>
<span data-ttu-id="cc0d3-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc0d3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc0d3-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc0d3-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc0d3-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cc0d3-139">INPUTS</span></span>

### <span data-ttu-id="cc0d3-140">System. String</span><span class="sxs-lookup"><span data-stu-id="cc0d3-140">System.String</span></span>

## <span data-ttu-id="cc0d3-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cc0d3-141">OUTPUTS</span></span>

### <span data-ttu-id="cc0d3-142">Microsoft. Azure. Commands. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="cc0d3-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="cc0d3-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cc0d3-143">NOTES</span></span>

## <span data-ttu-id="cc0d3-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cc0d3-144">RELATED LINKS</span></span>

[<span data-ttu-id="cc0d3-145">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="cc0d3-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="cc0d3-146">Start — AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="cc0d3-146">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="cc0d3-147">Zatrzymaj — AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="cc0d3-147">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="cc0d3-148">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="cc0d3-148">Remove-AzDataFactoryV2Trigger</span></span>]()
