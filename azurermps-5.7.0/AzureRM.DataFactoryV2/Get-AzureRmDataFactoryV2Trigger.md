---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: 5004b50cf5bb5b22a95ef00bf19f0e783fd04cb2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552951"
---
# <span data-ttu-id="41070-101">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="41070-101">Get-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="41070-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="41070-102">SYNOPSIS</span></span>
<span data-ttu-id="41070-103">Pobiera informacje o wyzwalaczach w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="41070-103">Gets information about triggers in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41070-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="41070-104">SYNTAX</span></span>

### <span data-ttu-id="41070-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="41070-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41070-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="41070-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41070-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="41070-107">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2Trigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="41070-108">Opis</span><span class="sxs-lookup"><span data-stu-id="41070-108">DESCRIPTION</span></span>
<span data-ttu-id="41070-109">Polecenie cmdlet **Get-AzureRmDataFactoryV2Trigger** pobiera informacje o wyzwalaczach w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="41070-109">The **Get-AzureRmDataFactoryV2Trigger** cmdlet gets information about triggers in a data factory.</span></span> <span data-ttu-id="41070-110">Jeśli określisz nazwę wyzwalacza, polecenie cmdlet pobiera informacje o tym wyzwalaczu.</span><span class="sxs-lookup"><span data-stu-id="41070-110">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="41070-111">Jeśli nie określisz nazwy, polecenie cmdlet pobiera informacje o wszystkich wyzwalaczach w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="41070-111">If you do not specify a name, the cmdlet gets information about all triggers in the data factory.</span></span>

## <span data-ttu-id="41070-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="41070-112">EXAMPLES</span></span>

### <span data-ttu-id="41070-113">Przykład 1: uzyskiwanie informacji na temat określonego wyzwalacza</span><span class="sxs-lookup"><span data-stu-id="41070-113">Example 1: Get information about a specific trigger</span></span>
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

<span data-ttu-id="41070-114">Pobiera listę wszystkich wyzwalaczy utworzonych w fabryce danych "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="41070-114">Gets a list of all triggers that have been created in the data factory "WikiADF".</span></span>

### <span data-ttu-id="41070-115">Przykład 2: uzyskiwanie informacji o wszystkich wyzwalaczach</span><span class="sxs-lookup"><span data-stu-id="41070-115">Example 2: Get information about all triggers</span></span>
```
Get-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="41070-116">Pobiera jeden wyzwalacz o nazwie "ScheduledTrigger" w fabryce danych "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="41070-116">Gets a single trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="41070-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="41070-117">PARAMETERS</span></span>

### <span data-ttu-id="41070-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="41070-118">-DataFactory</span></span>
<span data-ttu-id="41070-119">Obiekt fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="41070-119">The data factory object.</span></span>

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

### <span data-ttu-id="41070-120">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="41070-120">-DataFactoryName</span></span>
<span data-ttu-id="41070-121">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="41070-121">The data factory name.</span></span>

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

### <span data-ttu-id="41070-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41070-122">-DefaultProfile</span></span>
<span data-ttu-id="41070-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="41070-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41070-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="41070-124">-Name</span></span>
<span data-ttu-id="41070-125">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="41070-125">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: TriggerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41070-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41070-126">-ResourceGroupName</span></span>
<span data-ttu-id="41070-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="41070-127">The resource group name.</span></span>

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

### <span data-ttu-id="41070-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41070-128">-ResourceId</span></span>
<span data-ttu-id="41070-129">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="41070-129">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41070-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41070-130">CommonParameters</span></span>
<span data-ttu-id="41070-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41070-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41070-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41070-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41070-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="41070-133">INPUTS</span></span>

### <span data-ttu-id="41070-134">System. String</span><span class="sxs-lookup"><span data-stu-id="41070-134">System.String</span></span>
<span data-ttu-id="41070-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="41070-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="41070-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="41070-136">OUTPUTS</span></span>

### <span data-ttu-id="41070-137">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. DataFactoryV2. MODELES. PSTrigger, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="41070-137">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="41070-138">Microsoft. Azure. Commands. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="41070-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="41070-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="41070-139">NOTES</span></span>

## <span data-ttu-id="41070-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="41070-140">RELATED LINKS</span></span>

[<span data-ttu-id="41070-141">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="41070-141">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="41070-142">Start — AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="41070-142">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="41070-143">Zatrzymaj — AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="41070-143">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="41070-144">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="41070-144">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
