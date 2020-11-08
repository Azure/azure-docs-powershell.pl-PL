---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: 5844863cf56008d5d73fae7eef644dfd8e27c239
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062817"
---
# <span data-ttu-id="e25e8-101">Get-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="e25e8-101">Get-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="e25e8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e25e8-102">SYNOPSIS</span></span>
<span data-ttu-id="e25e8-103">Zwraca informacje o uruchomionych wyzwalaczach.</span><span class="sxs-lookup"><span data-stu-id="e25e8-103">Returns information about trigger runs.</span></span>

## <span data-ttu-id="e25e8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e25e8-104">SYNTAX</span></span>

### <span data-ttu-id="e25e8-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e25e8-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e25e8-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="e25e8-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e25e8-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e25e8-107">DESCRIPTION</span></span>
<span data-ttu-id="e25e8-108">Polecenie **Get-AzDataFactoryV2TriggerRun** zwraca szczegółowe informacje dotyczące wyzwalacza, które są uruchamiane dla określonego wyzwalacza w danym przedziale czasu.</span><span class="sxs-lookup"><span data-stu-id="e25e8-108">The **Get-AzDataFactoryV2TriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="e25e8-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e25e8-109">EXAMPLES</span></span>

### <span data-ttu-id="e25e8-110">Przykład 1: uzyskiwanie informacji o uruchomieniu wyzwalacza</span><span class="sxs-lookup"><span data-stu-id="e25e8-110">Example 1: Get information about trigger run</span></span>
```
PS C:\> Get-AzDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "WikiTrigger" -TriggerRunStartedAfter "2017-09-01" -TriggerRunStartedBefore "2019-09-30"

    ResourceGroupName   : ADF
    DataFactoryName     : WikiADF
    TriggerName         : WikiTrigger
    TriggerRunId        : 08586958400454144995526033731
    TriggerType         : ScheduleTrigger
    TriggerRunTimestamp : 9/18/2017 8:34:00 PM
    Status              : Succeeded
```

<span data-ttu-id="e25e8-111">To polecenie zawiera informacje dotyczące uruchamiania "WikiTrigger" w fabryce "WikiADF", które rozpoczęły się między "2017-09-01" a "2019-09-30".</span><span class="sxs-lookup"><span data-stu-id="e25e8-111">This command shows information about runs for "WikiTrigger" in the factory "WikiADF" that started between "2017-09-01" and "2019-09-30".</span></span>

## <span data-ttu-id="e25e8-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e25e8-112">PARAMETERS</span></span>

### <span data-ttu-id="e25e8-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="e25e8-113">-DataFactory</span></span>
<span data-ttu-id="e25e8-114">Obiekt fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="e25e8-114">The data factory object.</span></span>

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

### <span data-ttu-id="e25e8-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="e25e8-115">-DataFactoryName</span></span>
<span data-ttu-id="e25e8-116">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="e25e8-116">The data factory name.</span></span>

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

### <span data-ttu-id="e25e8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e25e8-117">-DefaultProfile</span></span>
<span data-ttu-id="e25e8-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e25e8-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e25e8-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e25e8-119">-Name</span></span>
<span data-ttu-id="e25e8-120">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="e25e8-120">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e25e8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e25e8-121">-ResourceGroupName</span></span>
<span data-ttu-id="e25e8-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e25e8-122">The resource group name.</span></span>

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

### <span data-ttu-id="e25e8-123">-TriggerRunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="e25e8-123">-TriggerRunStartedAfter</span></span>
<span data-ttu-id="e25e8-124">Czas rozpoczęcia lub po upływie uruchomienia wyzwalacza do wykonania w formacie ISO8601.</span><span class="sxs-lookup"><span data-stu-id="e25e8-124">The time at or after which the trigger run started to execute in ISO8601 format.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e25e8-125">-TriggerRunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="e25e8-125">-TriggerRunStartedBefore</span></span>
<span data-ttu-id="e25e8-126">Czas rozpoczęcia uruchamiania wyzwalacza w formacie ISO8601 lub przed jego uruchomieniem.</span><span class="sxs-lookup"><span data-stu-id="e25e8-126">The time at or before which the trigger run started to execute in ISO8601 format.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e25e8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e25e8-127">CommonParameters</span></span>
<span data-ttu-id="e25e8-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e25e8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e25e8-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e25e8-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e25e8-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e25e8-130">INPUTS</span></span>

### <span data-ttu-id="e25e8-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="e25e8-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="e25e8-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e25e8-132">System.String</span></span>

## <span data-ttu-id="e25e8-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e25e8-133">OUTPUTS</span></span>

### <span data-ttu-id="e25e8-134">Microsoft. Azure. Commands. DataFactoryV2. models. PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="e25e8-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

## <span data-ttu-id="e25e8-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e25e8-135">NOTES</span></span>

## <span data-ttu-id="e25e8-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e25e8-136">RELATED LINKS</span></span>

[<span data-ttu-id="e25e8-137">Start — AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="e25e8-137">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="e25e8-138">Zatrzymaj — AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="e25e8-138">Stop-AzDataFactoryV2Trigger</span></span>]()

