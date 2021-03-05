---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: ba9ea38f5915f5a89326c806e11a055ec6aeed75
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975121"
---
# <span data-ttu-id="ab89a-101">Get-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="ab89a-101">Get-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="ab89a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab89a-102">SYNOPSIS</span></span>
<span data-ttu-id="ab89a-103">Zwraca informacje o uruchomieniach wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="ab89a-103">Returns information about trigger runs.</span></span>

## <span data-ttu-id="ab89a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ab89a-104">SYNTAX</span></span>

### <span data-ttu-id="ab89a-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="ab89a-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab89a-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ab89a-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab89a-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="ab89a-107">DESCRIPTION</span></span>
<span data-ttu-id="ab89a-108">Polecenie **Get-AzDataFactoryV2TriggerRun** zwraca szczegółowe informacje o wyzwalaczu uruchamianym dla określonego wyzwalacza w danym przedziale czasu.</span><span class="sxs-lookup"><span data-stu-id="ab89a-108">The **Get-AzDataFactoryV2TriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="ab89a-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ab89a-109">EXAMPLES</span></span>

### <span data-ttu-id="ab89a-110">Przykład 1. Uzyskiwanie informacji o uruchomieniu wyzwalacza</span><span class="sxs-lookup"><span data-stu-id="ab89a-110">Example 1: Get information about trigger run</span></span>
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

<span data-ttu-id="ab89a-111">To polecenie zawiera informacje o uruchamianiu ciągu "WikiTrigger" w fabrycznej układzie "WikiADF", które rozpoczęło się w okresie od "2017-09-01" do "2019-09-30".</span><span class="sxs-lookup"><span data-stu-id="ab89a-111">This command shows information about runs for "WikiTrigger" in the factory "WikiADF" that started between "2017-09-01" and "2019-09-30".</span></span>

## <span data-ttu-id="ab89a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab89a-112">PARAMETERS</span></span>

### <span data-ttu-id="ab89a-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="ab89a-113">-DataFactory</span></span>
<span data-ttu-id="ab89a-114">Obiekt data factory.</span><span class="sxs-lookup"><span data-stu-id="ab89a-114">The data factory object.</span></span>

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

### <span data-ttu-id="ab89a-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ab89a-115">-DataFactoryName</span></span>
<span data-ttu-id="ab89a-116">Nazwa fabryczna danych.</span><span class="sxs-lookup"><span data-stu-id="ab89a-116">The data factory name.</span></span>

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

### <span data-ttu-id="ab89a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab89a-117">-DefaultProfile</span></span>
<span data-ttu-id="ab89a-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ab89a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab89a-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ab89a-119">-Name</span></span>
<span data-ttu-id="ab89a-120">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="ab89a-120">The trigger name.</span></span>

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

### <span data-ttu-id="ab89a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab89a-121">-ResourceGroupName</span></span>
<span data-ttu-id="ab89a-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ab89a-122">The resource group name.</span></span>

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

### <span data-ttu-id="ab89a-123">-TriggerRunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="ab89a-123">-TriggerRunStartedAfter</span></span>
<span data-ttu-id="ab89a-124">Godzina rozpoczęcia uruchomienia wyzwalacza w formacie ISO8601 lub później.</span><span class="sxs-lookup"><span data-stu-id="ab89a-124">The time at or after which the trigger run started to execute in ISO8601 format.</span></span>

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

### <span data-ttu-id="ab89a-125">-TriggerRunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="ab89a-125">-TriggerRunStartedBefore</span></span>
<span data-ttu-id="ab89a-126">Godzina rozpoczęcia uruchomienia wyzwalacza w formacie ISO8601 lub wcześniej.</span><span class="sxs-lookup"><span data-stu-id="ab89a-126">The time at or before which the trigger run started to execute in ISO8601 format.</span></span>

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

### <span data-ttu-id="ab89a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab89a-127">CommonParameters</span></span>
<span data-ttu-id="ab89a-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab89a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab89a-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab89a-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab89a-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ab89a-130">INPUTS</span></span>

### <span data-ttu-id="ab89a-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="ab89a-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="ab89a-132">System.String</span><span class="sxs-lookup"><span data-stu-id="ab89a-132">System.String</span></span>

## <span data-ttu-id="ab89a-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ab89a-133">OUTPUTS</span></span>

### <span data-ttu-id="ab89a-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="ab89a-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

## <span data-ttu-id="ab89a-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ab89a-135">NOTES</span></span>

## <span data-ttu-id="ab89a-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ab89a-136">RELATED LINKS</span></span>

[<span data-ttu-id="ab89a-137">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="ab89a-137">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="ab89a-138">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="ab89a-138">Stop-AzDataFactoryV2Trigger</span></span>]()

