---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: DC151161-72C0-40F7-B2F0-45FA01142AE1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/get-azurermschedulerjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJob.md
ms.openlocfilehash: d22f1acf8f99f15df83be95aafdc8ff0aefd2a29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718466"
---
# <span data-ttu-id="c2676-101">Get-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="c2676-101">Get-AzureRmSchedulerJob</span></span>

## <span data-ttu-id="c2676-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c2676-102">SYNOPSIS</span></span>
<span data-ttu-id="c2676-103">Pobiera zadania harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="c2676-103">Gets Scheduler jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2676-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c2676-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJob -ResourceGroupName <String> -JobCollectionName <String> [-JobName <String>]
 [-JobState <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2676-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c2676-105">DESCRIPTION</span></span>
<span data-ttu-id="c2676-106">Polecenie cmdlet **Get-AzureRmSchedulerJob** pobiera zadania w usłudze Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="c2676-106">The **Get-AzureRmSchedulerJob** cmdlet gets Azure Scheduler jobs.</span></span>

## <span data-ttu-id="c2676-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c2676-107">EXAMPLES</span></span>

## <span data-ttu-id="c2676-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c2676-108">PARAMETERS</span></span>

### <span data-ttu-id="c2676-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2676-109">-DefaultProfile</span></span>
<span data-ttu-id="c2676-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c2676-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2676-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="c2676-111">-JobCollectionName</span></span>
<span data-ttu-id="c2676-112">Określa nazwę kolekcji zadań zawierającej zadania do pobrania.</span><span class="sxs-lookup"><span data-stu-id="c2676-112">Specifies the name of a job collection that contains jobs to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2676-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="c2676-113">-JobName</span></span>
<span data-ttu-id="c2676-114">Określa nazwę zadania do pobrania.</span><span class="sxs-lookup"><span data-stu-id="c2676-114">Specifies the name of a job to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2676-115">-JobState</span><span class="sxs-lookup"><span data-stu-id="c2676-115">-JobState</span></span>
<span data-ttu-id="c2676-116">Określa stan zadania, do którego należy uzyskać zadania.</span><span class="sxs-lookup"><span data-stu-id="c2676-116">Specifies a job state of jobs to get.</span></span>
<span data-ttu-id="c2676-117">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="c2676-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c2676-118">Wyłączona</span><span class="sxs-lookup"><span data-stu-id="c2676-118">Enabled</span></span> 
- <span data-ttu-id="c2676-119">Łącza</span><span class="sxs-lookup"><span data-stu-id="c2676-119">Disabled</span></span> 
- <span data-ttu-id="c2676-120">Błąd</span><span class="sxs-lookup"><span data-stu-id="c2676-120">Faulted</span></span> 
- <span data-ttu-id="c2676-121">Zakończyć</span><span class="sxs-lookup"><span data-stu-id="c2676-121">Completed</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled, Faulted, Completed

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2676-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2676-122">-ResourceGroupName</span></span>
<span data-ttu-id="c2676-123">Określa grupę zasobów zadań, które należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="c2676-123">Specifies the resource group of the jobs to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2676-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2676-124">CommonParameters</span></span>
<span data-ttu-id="c2676-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2676-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2676-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2676-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2676-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2676-127">INPUTS</span></span>

### <span data-ttu-id="c2676-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c2676-128">None</span></span>
<span data-ttu-id="c2676-129">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="c2676-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c2676-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c2676-130">OUTPUTS</span></span>

### <span data-ttu-id="c2676-131">Microsoft. Azure. Commands. Scheduler. models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="c2676-131">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="c2676-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c2676-132">NOTES</span></span>

## <span data-ttu-id="c2676-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c2676-133">RELATED LINKS</span></span>

[<span data-ttu-id="c2676-134">Nowe — AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="c2676-134">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="c2676-135">Nowe — AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="c2676-135">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="c2676-136">Nowe — AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="c2676-136">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="c2676-137">Nowe — AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="c2676-137">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="c2676-138">Nowe — AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="c2676-138">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="c2676-139">Remove-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="c2676-139">Remove-AzureRmSchedulerJob</span></span>](./Remove-AzureRmSchedulerJob.md)

[<span data-ttu-id="c2676-140">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="c2676-140">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="c2676-141">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="c2676-141">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="c2676-142">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="c2676-142">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="c2676-143">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="c2676-143">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


