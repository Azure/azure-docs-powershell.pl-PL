---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Trigger.md
ms.openlocfilehash: 989a898605488fc7cfaa828bfd8c5b9b61378a27
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062819"
---
# <span data-ttu-id="5fa4a-101">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5fa4a-101">Get-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="5fa4a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5fa4a-102">SYNOPSIS</span></span>
<span data-ttu-id="5fa4a-103">Pobiera informacje o wyzwalaczach w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="5fa4a-103">Gets information about triggers in a data factory.</span></span>

## <span data-ttu-id="5fa4a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5fa4a-104">SYNTAX</span></span>

### <span data-ttu-id="5fa4a-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5fa4a-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Trigger [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5fa4a-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="5fa4a-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Trigger [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5fa4a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5fa4a-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Trigger [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5fa4a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5fa4a-108">DESCRIPTION</span></span>
<span data-ttu-id="5fa4a-109">Polecenie cmdlet **Get-AzDataFactoryV2Trigger** pobiera informacje o wyzwalaczach w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="5fa4a-109">The **Get-AzDataFactoryV2Trigger** cmdlet gets information about triggers in a data factory.</span></span> <span data-ttu-id="5fa4a-110">Jeśli określisz nazwę wyzwalacza, polecenie cmdlet pobiera informacje o tym wyzwalaczu.</span><span class="sxs-lookup"><span data-stu-id="5fa4a-110">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="5fa4a-111">Jeśli nie określisz nazwy, polecenie cmdlet pobiera informacje o wszystkich wyzwalaczach w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="5fa4a-111">If you do not specify a name, the cmdlet gets information about all triggers in the data factory.</span></span>

## <span data-ttu-id="5fa4a-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5fa4a-112">EXAMPLES</span></span>

### <span data-ttu-id="5fa4a-113">Przykład 1: uzyskiwanie informacji na temat określonego wyzwalacza</span><span class="sxs-lookup"><span data-stu-id="5fa4a-113">Example 1: Get information about a specific trigger</span></span>
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

<span data-ttu-id="5fa4a-114">Pobiera listę wszystkich wyzwalaczy utworzonych w fabryce danych "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="5fa4a-114">Gets a list of all triggers that have been created in the data factory "WikiADF".</span></span>

### <span data-ttu-id="5fa4a-115">Przykład 2: uzyskiwanie informacji o wszystkich wyzwalaczach</span><span class="sxs-lookup"><span data-stu-id="5fa4a-115">Example 2: Get information about all triggers</span></span>
```
Get-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="5fa4a-116">Pobiera jeden wyzwalacz o nazwie "ScheduledTrigger" w fabryce danych "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="5fa4a-116">Gets a single trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="5fa4a-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5fa4a-117">PARAMETERS</span></span>

### <span data-ttu-id="5fa4a-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="5fa4a-118">-DataFactory</span></span>
<span data-ttu-id="5fa4a-119">Obiekt fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="5fa4a-119">The data factory object.</span></span>

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

### <span data-ttu-id="5fa4a-120">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="5fa4a-120">-DataFactoryName</span></span>
<span data-ttu-id="5fa4a-121">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="5fa4a-121">The data factory name.</span></span>

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

### <span data-ttu-id="5fa4a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fa4a-122">-DefaultProfile</span></span>
<span data-ttu-id="5fa4a-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5fa4a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5fa4a-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5fa4a-124">-Name</span></span>
<span data-ttu-id="5fa4a-125">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="5fa4a-125">The trigger name.</span></span>

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

### <span data-ttu-id="5fa4a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fa4a-126">-ResourceGroupName</span></span>
<span data-ttu-id="5fa4a-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5fa4a-127">The resource group name.</span></span>

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

### <span data-ttu-id="5fa4a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5fa4a-128">-ResourceId</span></span>
<span data-ttu-id="5fa4a-129">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5fa4a-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="5fa4a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fa4a-130">CommonParameters</span></span>
<span data-ttu-id="5fa4a-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fa4a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fa4a-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fa4a-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fa4a-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5fa4a-133">INPUTS</span></span>

### <span data-ttu-id="5fa4a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="5fa4a-134">System.String</span></span>

### <span data-ttu-id="5fa4a-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="5fa4a-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="5fa4a-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5fa4a-136">OUTPUTS</span></span>

### <span data-ttu-id="5fa4a-137">Microsoft. Azure. Commands. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="5fa4a-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="5fa4a-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5fa4a-138">NOTES</span></span>

## <span data-ttu-id="5fa4a-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5fa4a-139">RELATED LINKS</span></span>

[<span data-ttu-id="5fa4a-140">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5fa4a-140">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="5fa4a-141">Start — AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5fa4a-141">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="5fa4a-142">Zatrzymaj — AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5fa4a-142">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="5fa4a-143">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5fa4a-143">Remove-AzDataFactoryV2Trigger</span></span>]()
