---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2TriggerRun.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: d5ea2dee1f6023b9505c38a58d364b7aa92591db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718545"
---
# <span data-ttu-id="d0f1c-101">Get-AzureRmDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="d0f1c-101">Get-AzureRmDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="d0f1c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d0f1c-102">SYNOPSIS</span></span>
<span data-ttu-id="d0f1c-103">Zwraca informacje o uruchomionych wyzwalaczach.</span><span class="sxs-lookup"><span data-stu-id="d0f1c-103">Returns information about trigger runs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0f1c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d0f1c-104">SYNTAX</span></span>

### <span data-ttu-id="d0f1c-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d0f1c-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-ResourceGroupName] <String> [-DataFactoryName] <String>
```

### <span data-ttu-id="d0f1c-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d0f1c-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-DataFactory] <PSDataFactory>
```

## <span data-ttu-id="d0f1c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d0f1c-107">DESCRIPTION</span></span>
<span data-ttu-id="d0f1c-108">Polecenie **Get-AzureRmDataFactoryV2TriggerRun** zwraca szczegółowe informacje dotyczące wyzwalacza, które są uruchamiane dla określonego wyzwalacza w danym przedziale czasu.</span><span class="sxs-lookup"><span data-stu-id="d0f1c-108">The **Get-AzureRmDataFactoryV2TriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="d0f1c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d0f1c-109">EXAMPLES</span></span>

### <span data-ttu-id="d0f1c-110">Przykład 1: uzyskiwanie informacji o uruchomieniu wyzwalacza</span><span class="sxs-lookup"><span data-stu-id="d0f1c-110">Example 1: Get information about trigger run</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "WikiTrigger" -TriggerRunStartedAfter "2017-09-01" -TriggerRunStartedBefore "2019-09-30"

    ResourceGroupName   : ADF
    DataFactoryName     : WikiADF
    TriggerName         : WikiTrigger
    TriggerRunId        : 08586958400454144995526033731
    TriggerType         : ScheduleTrigger
    TriggerRunTimestamp : 9/18/2017 8:34:00 PM
    Status              : Succeeded

```

<span data-ttu-id="d0f1c-111">To polecenie zawiera informacje dotyczące uruchamiania "WikiTrigger" w fabryce "WikiADF", które rozpoczęły się między "2017-09-01" a "2019-09-30".</span><span class="sxs-lookup"><span data-stu-id="d0f1c-111">This command shows information about runs for "WikiTrigger" in the factory "WikiADF" that started between "2017-09-01" and "2019-09-30".</span></span>

## <span data-ttu-id="d0f1c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d0f1c-112">PARAMETERS</span></span>

### <span data-ttu-id="d0f1c-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="d0f1c-113">-DataFactory</span></span>
<span data-ttu-id="d0f1c-114">Obiekt fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="d0f1c-114">The data factory object.</span></span>

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

### <span data-ttu-id="d0f1c-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="d0f1c-115">-DataFactoryName</span></span>
<span data-ttu-id="d0f1c-116">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="d0f1c-116">The data factory name.</span></span>

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

### <span data-ttu-id="d0f1c-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d0f1c-117">-Name</span></span>
<span data-ttu-id="d0f1c-118">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="d0f1c-118">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0f1c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0f1c-119">-ResourceGroupName</span></span>
<span data-ttu-id="d0f1c-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d0f1c-120">The resource group name.</span></span>

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

### <span data-ttu-id="d0f1c-121">-TriggerRunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="d0f1c-121">-TriggerRunStartedAfter</span></span>
<span data-ttu-id="d0f1c-122">Czas rozpoczęcia lub po upływie uruchomienia wyzwalacza do wykonania w formacie ISO8601.</span><span class="sxs-lookup"><span data-stu-id="d0f1c-122">The time at or after which the trigger run started to execute in ISO8601 format.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0f1c-123">-TriggerRunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="d0f1c-123">-TriggerRunStartedBefore</span></span>
<span data-ttu-id="d0f1c-124">Czas rozpoczęcia uruchamiania wyzwalacza w formacie ISO8601 lub przed jego uruchomieniem.</span><span class="sxs-lookup"><span data-stu-id="d0f1c-124">The time at or before which the trigger run started to execute in ISO8601 format.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="d0f1c-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d0f1c-125">INPUTS</span></span>

### <span data-ttu-id="d0f1c-126">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d0f1c-126">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="d0f1c-127">System. String</span><span class="sxs-lookup"><span data-stu-id="d0f1c-127">System.String</span></span>


## <span data-ttu-id="d0f1c-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d0f1c-128">OUTPUTS</span></span>

### <span data-ttu-id="d0f1c-129">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. DataFactoryV2. MODELES. PSTriggerRun, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d0f1c-129">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="d0f1c-130">Microsoft. Azure. Commands. DataFactoryV2. models. PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="d0f1c-130">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>


## <span data-ttu-id="d0f1c-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d0f1c-131">NOTES</span></span>

## <span data-ttu-id="d0f1c-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d0f1c-132">RELATED LINKS</span></span>
[<span data-ttu-id="d0f1c-133">Start — AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="d0f1c-133">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="d0f1c-134">Zatrzymaj — AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="d0f1c-134">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

