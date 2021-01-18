---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Trigger.md
ms.openlocfilehash: d315ae997a468abc3cd5f4e33601c1c9e770a40a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503682"
---
# <span data-ttu-id="f6d92-101">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="f6d92-101">Get-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="f6d92-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f6d92-102">SYNOPSIS</span></span>
<span data-ttu-id="f6d92-103">Pobiera informacje o wyzwalaczach w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="f6d92-103">Gets information about triggers in a data factory.</span></span>

## <span data-ttu-id="f6d92-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f6d92-104">SYNTAX</span></span>

### <span data-ttu-id="f6d92-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f6d92-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Trigger [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6d92-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f6d92-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Trigger [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6d92-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f6d92-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Trigger [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f6d92-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f6d92-108">DESCRIPTION</span></span>
<span data-ttu-id="f6d92-109">Polecenie cmdlet **Get-AzDataFactoryV2Trigger** pobiera informacje o wyzwalaczach w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="f6d92-109">The **Get-AzDataFactoryV2Trigger** cmdlet gets information about triggers in a data factory.</span></span> <span data-ttu-id="f6d92-110">Jeśli określisz nazwę wyzwalacza, polecenie cmdlet pobiera informacje o tym wyzwalaczu.</span><span class="sxs-lookup"><span data-stu-id="f6d92-110">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="f6d92-111">Jeśli nie określisz nazwy, polecenie cmdlet pobiera informacje o wszystkich wyzwalaczach w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="f6d92-111">If you do not specify a name, the cmdlet gets information about all triggers in the data factory.</span></span>

## <span data-ttu-id="f6d92-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f6d92-112">EXAMPLES</span></span>

### <span data-ttu-id="f6d92-113">Przykład 1: uzyskiwanie informacji o wszystkich wyzwalaczach</span><span class="sxs-lookup"><span data-stu-id="f6d92-113">Example 1: Get information about all triggers</span></span>
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

<span data-ttu-id="f6d92-114">Pobiera listę wszystkich wyzwalaczy utworzonych w fabryce danych "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="f6d92-114">Gets a list of all triggers that have been created in the data factory "WikiADF".</span></span>

### <span data-ttu-id="f6d92-115">Przykład 2: uzyskiwanie informacji na temat określonego wyzwalacza</span><span class="sxs-lookup"><span data-stu-id="f6d92-115">Example 2: Get information about a specific trigger</span></span>
```
Get-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="f6d92-116">Pobiera jeden wyzwalacz o nazwie "ScheduledTrigger" w fabryce danych "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="f6d92-116">Gets a single trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="f6d92-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f6d92-117">PARAMETERS</span></span>

### <span data-ttu-id="f6d92-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="f6d92-118">-DataFactory</span></span>
<span data-ttu-id="f6d92-119">Obiekt fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="f6d92-119">The data factory object.</span></span>

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

### <span data-ttu-id="f6d92-120">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="f6d92-120">-DataFactoryName</span></span>
<span data-ttu-id="f6d92-121">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="f6d92-121">The data factory name.</span></span>

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

### <span data-ttu-id="f6d92-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6d92-122">-DefaultProfile</span></span>
<span data-ttu-id="f6d92-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f6d92-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6d92-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f6d92-124">-Name</span></span>
<span data-ttu-id="f6d92-125">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="f6d92-125">The trigger name.</span></span>

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

### <span data-ttu-id="f6d92-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6d92-126">-ResourceGroupName</span></span>
<span data-ttu-id="f6d92-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f6d92-127">The resource group name.</span></span>

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

### <span data-ttu-id="f6d92-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f6d92-128">-ResourceId</span></span>
<span data-ttu-id="f6d92-129">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f6d92-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="f6d92-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6d92-130">CommonParameters</span></span>
<span data-ttu-id="f6d92-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6d92-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6d92-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6d92-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6d92-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f6d92-133">INPUTS</span></span>

### <span data-ttu-id="f6d92-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f6d92-134">System.String</span></span>

### <span data-ttu-id="f6d92-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="f6d92-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="f6d92-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f6d92-136">OUTPUTS</span></span>

### <span data-ttu-id="f6d92-137">Microsoft. Azure. Commands. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="f6d92-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="f6d92-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f6d92-138">NOTES</span></span>

## <span data-ttu-id="f6d92-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f6d92-139">RELATED LINKS</span></span>

[<span data-ttu-id="f6d92-140">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="f6d92-140">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="f6d92-141">Start — AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="f6d92-141">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="f6d92-142">Zatrzymaj — AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="f6d92-142">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="f6d92-143">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="f6d92-143">Remove-AzDataFactoryV2Trigger</span></span>]()
