---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Trigger.md
ms.openlocfilehash: d315ae997a468abc3cd5f4e33601c1c9e770a40a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198859"
---
# <span data-ttu-id="293a9-101">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="293a9-101">Get-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="293a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="293a9-102">SYNOPSIS</span></span>
<span data-ttu-id="293a9-103">Pobiera informacje o wyzwalaczach w zakładzie danych.</span><span class="sxs-lookup"><span data-stu-id="293a9-103">Gets information about triggers in a data factory.</span></span>

## <span data-ttu-id="293a9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="293a9-104">SYNTAX</span></span>

### <span data-ttu-id="293a9-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="293a9-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Trigger [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="293a9-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="293a9-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Trigger [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="293a9-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="293a9-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Trigger [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="293a9-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="293a9-108">DESCRIPTION</span></span>
<span data-ttu-id="293a9-109">Polecenie **cmdlet Get-AzDataFactoryV2Trigger** pobiera informacje o wyzwalaczach w fabrycznej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="293a9-109">The **Get-AzDataFactoryV2Trigger** cmdlet gets information about triggers in a data factory.</span></span> <span data-ttu-id="293a9-110">Jeśli określisz nazwę wyzwalacza, polecenie cmdlet pobiera informacje o tym wyzwalaczu.</span><span class="sxs-lookup"><span data-stu-id="293a9-110">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="293a9-111">Jeśli nie określisz nazwy, polecenie cmdlet pobiera informacje o wszystkich wyzwalaczach w zakładzie danych.</span><span class="sxs-lookup"><span data-stu-id="293a9-111">If you do not specify a name, the cmdlet gets information about all triggers in the data factory.</span></span>

## <span data-ttu-id="293a9-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="293a9-112">EXAMPLES</span></span>

### <span data-ttu-id="293a9-113">Przykład 1. Uzyskiwanie informacji o wszystkich wyzwalaczach</span><span class="sxs-lookup"><span data-stu-id="293a9-113">Example 1: Get information about all triggers</span></span>
```
PS C:\> Get-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped

    TriggerName       : ScheduledTrigger2
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="293a9-114">Pobiera listę wszystkich wyzwalaczy utworzonych w zakładzie danych "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="293a9-114">Gets a list of all triggers that have been created in the data factory "WikiADF".</span></span>

### <span data-ttu-id="293a9-115">Przykład 2. Uzyskiwanie informacji o określonym wyzwalaczu</span><span class="sxs-lookup"><span data-stu-id="293a9-115">Example 2: Get information about a specific trigger</span></span>
```
Get-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="293a9-116">Pobiera pojedynczy wyzwalacz o nazwie "ScheduledTrigger" w fabrycznej układzie danych "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="293a9-116">Gets a single trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="293a9-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="293a9-117">PARAMETERS</span></span>

### <span data-ttu-id="293a9-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="293a9-118">-DataFactory</span></span>
<span data-ttu-id="293a9-119">Obiekt data factory.</span><span class="sxs-lookup"><span data-stu-id="293a9-119">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="293a9-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="293a9-120">-DataFactoryName</span></span>
<span data-ttu-id="293a9-121">Nazwa fabryczna danych.</span><span class="sxs-lookup"><span data-stu-id="293a9-121">The data factory name.</span></span>

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

### <span data-ttu-id="293a9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="293a9-122">-DefaultProfile</span></span>
<span data-ttu-id="293a9-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="293a9-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="293a9-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="293a9-124">-Name</span></span>
<span data-ttu-id="293a9-125">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="293a9-125">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: TriggerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="293a9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="293a9-126">-ResourceGroupName</span></span>
<span data-ttu-id="293a9-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="293a9-127">The resource group name.</span></span>

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

### <span data-ttu-id="293a9-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="293a9-128">-ResourceId</span></span>
<span data-ttu-id="293a9-129">Identyfikator zasobu Azure.</span><span class="sxs-lookup"><span data-stu-id="293a9-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="293a9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="293a9-130">CommonParameters</span></span>
<span data-ttu-id="293a9-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="293a9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="293a9-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="293a9-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="293a9-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="293a9-133">INPUTS</span></span>

### <span data-ttu-id="293a9-134">System.String</span><span class="sxs-lookup"><span data-stu-id="293a9-134">System.String</span></span>

### <span data-ttu-id="293a9-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="293a9-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="293a9-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="293a9-136">OUTPUTS</span></span>

### <span data-ttu-id="293a9-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="293a9-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="293a9-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="293a9-138">NOTES</span></span>

## <span data-ttu-id="293a9-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="293a9-139">RELATED LINKS</span></span>

[<span data-ttu-id="293a9-140">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="293a9-140">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="293a9-141">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="293a9-141">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="293a9-142">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="293a9-142">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="293a9-143">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="293a9-143">Remove-AzDataFactoryV2Trigger</span></span>]()
