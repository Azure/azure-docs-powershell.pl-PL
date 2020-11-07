---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2TriggerRun.md
ms.openlocfilehash: 7d3f1ca73712753ad38b46c186a51bd7aa159b46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716742"
---
# <span data-ttu-id="1dd5e-101">Get-AzureRmDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="1dd5e-101">Get-AzureRmDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="1dd5e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1dd5e-102">SYNOPSIS</span></span>
<span data-ttu-id="1dd5e-103">Zwraca informacje o uruchomionych wyzwalaczach.</span><span class="sxs-lookup"><span data-stu-id="1dd5e-103">Returns information about trigger runs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1dd5e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1dd5e-104">SYNTAX</span></span>

### <span data-ttu-id="1dd5e-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1dd5e-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1dd5e-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="1dd5e-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1dd5e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1dd5e-107">DESCRIPTION</span></span>
<span data-ttu-id="1dd5e-108">Polecenie **Get-AzureRmDataFactoryV2TriggerRun** zwraca szczegółowe informacje dotyczące wyzwalacza, które są uruchamiane dla określonego wyzwalacza w danym przedziale czasu.</span><span class="sxs-lookup"><span data-stu-id="1dd5e-108">The **Get-AzureRmDataFactoryV2TriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="1dd5e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1dd5e-109">EXAMPLES</span></span>

### <span data-ttu-id="1dd5e-110">Przykład 1: uzyskiwanie informacji o uruchomieniu wyzwalacza</span><span class="sxs-lookup"><span data-stu-id="1dd5e-110">Example 1: Get information about trigger run</span></span>
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

<span data-ttu-id="1dd5e-111">To polecenie zawiera informacje dotyczące uruchamiania "WikiTrigger" w fabryce "WikiADF", które rozpoczęły się między "2017-09-01" a "2019-09-30".</span><span class="sxs-lookup"><span data-stu-id="1dd5e-111">This command shows information about runs for "WikiTrigger" in the factory "WikiADF" that started between "2017-09-01" and "2019-09-30".</span></span>

## <span data-ttu-id="1dd5e-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1dd5e-112">PARAMETERS</span></span>

### <span data-ttu-id="1dd5e-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="1dd5e-113">-DataFactory</span></span>
<span data-ttu-id="1dd5e-114">Obiekt fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="1dd5e-114">The data factory object.</span></span>

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

### <span data-ttu-id="1dd5e-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="1dd5e-115">-DataFactoryName</span></span>
<span data-ttu-id="1dd5e-116">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="1dd5e-116">The data factory name.</span></span>

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

### <span data-ttu-id="1dd5e-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1dd5e-117">-Name</span></span>
<span data-ttu-id="1dd5e-118">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="1dd5e-118">The trigger name.</span></span>

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

### <span data-ttu-id="1dd5e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dd5e-119">-ResourceGroupName</span></span>
<span data-ttu-id="1dd5e-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1dd5e-120">The resource group name.</span></span>

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

### <span data-ttu-id="1dd5e-121">-TriggerRunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="1dd5e-121">-TriggerRunStartedAfter</span></span>
<span data-ttu-id="1dd5e-122">Czas rozpoczęcia lub po upływie uruchomienia wyzwalacza do wykonania w formacie ISO8601.</span><span class="sxs-lookup"><span data-stu-id="1dd5e-122">The time at or after which the trigger run started to execute in ISO8601 format.</span></span>

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

### <span data-ttu-id="1dd5e-123">-TriggerRunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="1dd5e-123">-TriggerRunStartedBefore</span></span>
<span data-ttu-id="1dd5e-124">Czas rozpoczęcia uruchamiania wyzwalacza w formacie ISO8601 lub przed jego uruchomieniem.</span><span class="sxs-lookup"><span data-stu-id="1dd5e-124">The time at or before which the trigger run started to execute in ISO8601 format.</span></span>

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

### <span data-ttu-id="1dd5e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dd5e-125">-DefaultProfile</span></span>
<span data-ttu-id="1dd5e-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1dd5e-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1dd5e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dd5e-127">CommonParameters</span></span>
<span data-ttu-id="1dd5e-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dd5e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dd5e-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dd5e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dd5e-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1dd5e-130">INPUTS</span></span>

### <span data-ttu-id="1dd5e-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="1dd5e-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="1dd5e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="1dd5e-132">System.String</span></span>

## <span data-ttu-id="1dd5e-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1dd5e-133">OUTPUTS</span></span>

### <span data-ttu-id="1dd5e-134">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. DataFactoryV2. MODELES. PSTriggerRun, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="1dd5e-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="1dd5e-135">Microsoft. Azure. Commands. DataFactoryV2. models. PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="1dd5e-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

## <span data-ttu-id="1dd5e-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1dd5e-136">NOTES</span></span>

## <span data-ttu-id="1dd5e-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1dd5e-137">RELATED LINKS</span></span>

[<span data-ttu-id="1dd5e-138">Start — AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="1dd5e-138">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="1dd5e-139">Zatrzymaj — AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="1dd5e-139">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

