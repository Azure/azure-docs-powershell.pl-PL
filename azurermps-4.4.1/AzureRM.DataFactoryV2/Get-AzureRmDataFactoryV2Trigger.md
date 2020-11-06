---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
gitcommit: https://github.com/Azure/azure-powershell/blob/c396953644d237789e0f4e1f726b553913186d34
ms.openlocfilehash: bc60bbb5b48c4022e7db6a95e26a1f43ef891ae2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553937"
---
# <span data-ttu-id="bc411-101">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="bc411-101">Get-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="bc411-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bc411-102">SYNOPSIS</span></span>
<span data-ttu-id="bc411-103">Pobiera informacje o wyzwalaczach w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="bc411-103">Gets information about triggers in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc411-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bc411-104">SYNTAX</span></span>

### <span data-ttu-id="bc411-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bc411-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
```

### <span data-ttu-id="bc411-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="bc411-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-DataFactory] <PSDataFactory>
```

## <span data-ttu-id="bc411-107">Opis</span><span class="sxs-lookup"><span data-stu-id="bc411-107">DESCRIPTION</span></span>
<span data-ttu-id="bc411-108">Polecenie cmdlet **Get-AzureRmDataFactoryV2Trigger** pobiera informacje o wyzwalaczach w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="bc411-108">The **Get-AzureRmDataFactoryV2Trigger** cmdlet gets information about triggers in a data factory.</span></span> <span data-ttu-id="bc411-109">Jeśli określisz nazwę wyzwalacza, polecenie cmdlet pobiera informacje o tym wyzwalaczu.</span><span class="sxs-lookup"><span data-stu-id="bc411-109">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="bc411-110">Jeśli nie określisz nazwy, polecenie cmdlet pobiera informacje o wszystkich wyzwalaczach w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="bc411-110">If you do not specify a name, the cmdlet gets information about all triggers in the data factory.</span></span>


## <span data-ttu-id="bc411-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bc411-111">EXAMPLES</span></span>

### <span data-ttu-id="bc411-112">Przykład 1: uzyskiwanie informacji na temat określonego wyzwalacza</span><span class="sxs-lookup"><span data-stu-id="bc411-112">Example 1: Get information about a specific trigger</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

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

<span data-ttu-id="bc411-113">Pobiera listę wszystkich wyzwalaczy utworzonych w fabryce danych "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="bc411-113">Gets a list of all triggers that have been created in the data factory "WikiADF".</span></span>

### <span data-ttu-id="bc411-114">Przykład 2: uzyskiwanie informacji o wszystkich wyzwalaczach</span><span class="sxs-lookup"><span data-stu-id="bc411-114">Example 2: Get information about all triggers</span></span>

```
Get-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="bc411-115">Pobiera jeden wyzwalacz o nazwie "ScheduledTrigger" w fabryce danych "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="bc411-115">Gets a single trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="bc411-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bc411-116">PARAMETERS</span></span>

### <span data-ttu-id="bc411-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="bc411-117">-DataFactory</span></span>
<span data-ttu-id="bc411-118">Obiekt fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="bc411-118">The data factory object.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc411-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="bc411-119">-DataFactoryName</span></span>
<span data-ttu-id="bc411-120">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="bc411-120">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc411-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bc411-121">-Name</span></span>
<span data-ttu-id="bc411-122">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="bc411-122">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TriggerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc411-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc411-123">-ResourceGroupName</span></span>
<span data-ttu-id="bc411-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bc411-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="bc411-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bc411-125">INPUTS</span></span>

### <span data-ttu-id="bc411-126">System. String</span><span class="sxs-lookup"><span data-stu-id="bc411-126">System.String</span></span>
<span data-ttu-id="bc411-127">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="bc411-127">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>


## <span data-ttu-id="bc411-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bc411-128">OUTPUTS</span></span>

### <span data-ttu-id="bc411-129">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. DataFactoryV2. MODELES. PSTrigger, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="bc411-129">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="bc411-130">Microsoft. Azure. Commands. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="bc411-130">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>


## <span data-ttu-id="bc411-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bc411-131">NOTES</span></span>

## <span data-ttu-id="bc411-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bc411-132">RELATED LINKS</span></span>
[<span data-ttu-id="bc411-133">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="bc411-133">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="bc411-134">Start — AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="bc411-134">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="bc411-135">Zatrzymaj — AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="bc411-135">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="bc411-136">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="bc411-136">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
