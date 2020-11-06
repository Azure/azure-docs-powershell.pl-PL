---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: dc4630359070e627a3c65c63f21c23f987cb9a31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545408"
---
# <span data-ttu-id="a7e43-101">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="a7e43-101">Set-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="a7e43-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a7e43-102">SYNOPSIS</span></span>
<span data-ttu-id="a7e43-103">Tworzy wyzwalacz w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="a7e43-103">Creates a trigger in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7e43-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a7e43-104">SYNTAX</span></span>

### <span data-ttu-id="a7e43-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a7e43-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2Trigger [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a7e43-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a7e43-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2Trigger [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7e43-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a7e43-107">DESCRIPTION</span></span>
<span data-ttu-id="a7e43-108">Polecenie cmdlet **Set-AzureRmDataFactoryV2Trigger** tworzy wyzwalacz w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="a7e43-108">The **Set-AzureRmDataFactoryV2Trigger** cmdlet creates a trigger in a data factory.</span></span> <span data-ttu-id="a7e43-109">Jeśli określisz nazwę wyzwalacza, który już istnieje, przed zastąpieniem wyzwalacza polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a7e43-109">If you specify a name for a trigger that already exists, the cmdlet prompts for confirmation before replacing the trigger.</span></span> <span data-ttu-id="a7e43-110">Jeśli określisz parametr _Force_ , polecenie cmdlet zastępuje istniejący wyzwalacz bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a7e43-110">If you specify the _Force_ parameter, the cmdlet replaces the existing trigger without prompting for confirmation.</span></span> <span data-ttu-id="a7e43-111">Wyzwalacze są tworzone w stanie "zatrzymane", co oznacza, że nie zaczynają od razu rozpoczynać od siebie potoków, do których się odwołują.</span><span class="sxs-lookup"><span data-stu-id="a7e43-111">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="a7e43-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a7e43-112">EXAMPLES</span></span>

### <span data-ttu-id="a7e43-113">Przykład 1. Tworzenie wyzwalacza</span><span class="sxs-lookup"><span data-stu-id="a7e43-113">Example 1: Create a trigger</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger" -DefinitionFile ".\scheduledTrigger.json"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="a7e43-114">Utwórz nowy wyzwalacz o nazwie "ScheduledTrigger" w fabryce danych "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="a7e43-114">Create a new trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span> <span data-ttu-id="a7e43-115">Wyzwalacz jest tworzony w stanie "zatrzymane", co oznacza, że nie jest od razu uruchomiony.</span><span class="sxs-lookup"><span data-stu-id="a7e43-115">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="a7e43-116">Wyzwalacz można uruchomić przy użyciu `Start-AzureRmDataFactoryV2Trigger` polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7e43-116">A trigger can be started using the `Start-AzureRmDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="a7e43-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a7e43-117">PARAMETERS</span></span>

### <span data-ttu-id="a7e43-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="a7e43-118">-DataFactoryName</span></span>
<span data-ttu-id="a7e43-119">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="a7e43-119">The data factory name.</span></span>

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

### <span data-ttu-id="a7e43-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7e43-120">-DefaultProfile</span></span>
<span data-ttu-id="a7e43-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a7e43-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7e43-122">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="a7e43-122">-DefinitionFile</span></span>
<span data-ttu-id="a7e43-123">Ścieżka pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="a7e43-123">The JSON file path.</span></span>

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

### <span data-ttu-id="a7e43-124">-Force</span><span class="sxs-lookup"><span data-stu-id="a7e43-124">-Force</span></span>
<span data-ttu-id="a7e43-125">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a7e43-125">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="a7e43-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a7e43-126">-Name</span></span>
<span data-ttu-id="a7e43-127">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="a7e43-127">The trigger name.</span></span>

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

### <span data-ttu-id="a7e43-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7e43-128">-ResourceGroupName</span></span>
<span data-ttu-id="a7e43-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a7e43-129">The resource group name.</span></span>

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

### <span data-ttu-id="a7e43-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a7e43-130">-ResourceId</span></span>
<span data-ttu-id="a7e43-131">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a7e43-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="a7e43-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a7e43-132">-Confirm</span></span>
<span data-ttu-id="a7e43-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7e43-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7e43-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7e43-134">-WhatIf</span></span>
<span data-ttu-id="a7e43-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7e43-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="a7e43-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7e43-136">CommonParameters</span></span>
<span data-ttu-id="a7e43-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7e43-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7e43-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7e43-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7e43-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a7e43-139">INPUTS</span></span>

### <span data-ttu-id="a7e43-140">System. String</span><span class="sxs-lookup"><span data-stu-id="a7e43-140">System.String</span></span>

## <span data-ttu-id="a7e43-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a7e43-141">OUTPUTS</span></span>

### <span data-ttu-id="a7e43-142">Microsoft. Azure. Commands. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="a7e43-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="a7e43-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a7e43-143">NOTES</span></span>

## <span data-ttu-id="a7e43-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a7e43-144">RELATED LINKS</span></span>

[<span data-ttu-id="a7e43-145">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="a7e43-145">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="a7e43-146">Start — AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="a7e43-146">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="a7e43-147">Zatrzymaj — AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="a7e43-147">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="a7e43-148">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="a7e43-148">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
