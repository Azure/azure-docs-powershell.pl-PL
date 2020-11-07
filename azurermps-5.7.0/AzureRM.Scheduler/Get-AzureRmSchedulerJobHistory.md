---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: F6D8710D-1D42-493C-B7F1-EDA35FCCDC23
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/get-azurermschedulerjobhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobHistory.md
ms.openlocfilehash: 6c1582c8e82bf344685f9e1feb002625bddd6748
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716983"
---
# <span data-ttu-id="b38c8-101">Get-AzureRmSchedulerJobHistory</span><span class="sxs-lookup"><span data-stu-id="b38c8-101">Get-AzureRmSchedulerJobHistory</span></span>

## <span data-ttu-id="b38c8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b38c8-102">SYNOPSIS</span></span>
<span data-ttu-id="b38c8-103">Pobiera historię zadania.</span><span class="sxs-lookup"><span data-stu-id="b38c8-103">Gets job history.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b38c8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b38c8-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJobHistory -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-JobExecutionStatus <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b38c8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b38c8-105">DESCRIPTION</span></span>
<span data-ttu-id="b38c8-106">Polecenie cmdlet **Get-AzureRmSchedulerJobHistory** pobiera historię zadania usługi Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="b38c8-106">The **Get-AzureRmSchedulerJobHistory** cmdlet gets history for an Azure Scheduler job.</span></span>

## <span data-ttu-id="b38c8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b38c8-107">EXAMPLES</span></span>

## <span data-ttu-id="b38c8-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b38c8-108">PARAMETERS</span></span>

### <span data-ttu-id="b38c8-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b38c8-109">-DefaultProfile</span></span>
<span data-ttu-id="b38c8-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b38c8-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b38c8-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="b38c8-111">-JobCollectionName</span></span>
<span data-ttu-id="b38c8-112">Określa nazwę kolekcji zadań.</span><span class="sxs-lookup"><span data-stu-id="b38c8-112">Specifies the name of a job collection.</span></span>

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

### <span data-ttu-id="b38c8-113">-JobExecutionStatus</span><span class="sxs-lookup"><span data-stu-id="b38c8-113">-JobExecutionStatus</span></span>
<span data-ttu-id="b38c8-114">Określa stan zadania.</span><span class="sxs-lookup"><span data-stu-id="b38c8-114">Specifies the status of a job.</span></span>
<span data-ttu-id="b38c8-115">Ten aplet polecenia umożliwia pobieranie historii zgodnej ze stanem określonym przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b38c8-115">This cmdlet gets history that matches the status that you specify.</span></span>
<span data-ttu-id="b38c8-116">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b38c8-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b38c8-117">Zakończyć</span><span class="sxs-lookup"><span data-stu-id="b38c8-117">Completed</span></span> 
- <span data-ttu-id="b38c8-118">Nie powiodło się</span><span class="sxs-lookup"><span data-stu-id="b38c8-118">Failed</span></span> 
- <span data-ttu-id="b38c8-119">Odroczone</span><span class="sxs-lookup"><span data-stu-id="b38c8-119">Postponed</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Completed, Failed, Postponed

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b38c8-120">-JobName</span><span class="sxs-lookup"><span data-stu-id="b38c8-120">-JobName</span></span>
<span data-ttu-id="b38c8-121">Określa nazwę zadania, którego historia jest pobierana za pomocą tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b38c8-121">Specifies the name of a job for which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="b38c8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b38c8-122">-ResourceGroupName</span></span>
<span data-ttu-id="b38c8-123">Określa grupę zasobów, do której należy zadanie.</span><span class="sxs-lookup"><span data-stu-id="b38c8-123">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="b38c8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b38c8-124">CommonParameters</span></span>
<span data-ttu-id="b38c8-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b38c8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b38c8-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b38c8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b38c8-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b38c8-127">INPUTS</span></span>

### <span data-ttu-id="b38c8-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b38c8-128">None</span></span>
<span data-ttu-id="b38c8-129">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="b38c8-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b38c8-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b38c8-130">OUTPUTS</span></span>

### <span data-ttu-id="b38c8-131">Microsoft. Azure. Commands. Scheduler. models. PSJobHistory</span><span class="sxs-lookup"><span data-stu-id="b38c8-131">Microsoft.Azure.Commands.Scheduler.Models.PSJobHistory</span></span>

## <span data-ttu-id="b38c8-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b38c8-132">NOTES</span></span>

## <span data-ttu-id="b38c8-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b38c8-133">RELATED LINKS</span></span>

[<span data-ttu-id="b38c8-134">Get-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="b38c8-134">Get-AzureRmSchedulerJob</span></span>](./Get-AzureRmSchedulerJob.md)


