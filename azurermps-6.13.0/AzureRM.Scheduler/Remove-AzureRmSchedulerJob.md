---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 774699A8-8916-4F2A-973E-97E5E487D42E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/remove-azurermschedulerjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJob.md
ms.openlocfilehash: 6a15f51290efec856494737881693c3d1fae0620
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541471"
---
# <span data-ttu-id="5fbb4-101">Remove-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="5fbb4-101">Remove-AzureRmSchedulerJob</span></span>

## <span data-ttu-id="5fbb4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5fbb4-102">SYNOPSIS</span></span>
<span data-ttu-id="5fbb4-103">Usuwa zadanie harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="5fbb4-103">Removes a Scheduler job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5fbb4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5fbb4-104">SYNTAX</span></span>

```
Remove-AzureRmSchedulerJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fbb4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5fbb4-105">DESCRIPTION</span></span>
<span data-ttu-id="5fbb4-106">Polecenie cmdlet **Remove-AzureRmSchedulerJob** usuwa zadanie usługi Harmonogram Azure.</span><span class="sxs-lookup"><span data-stu-id="5fbb4-106">The **Remove-AzureRmSchedulerJob** cmdlet removes an Azure Scheduler job.</span></span>

## <span data-ttu-id="5fbb4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5fbb4-107">EXAMPLES</span></span>

## <span data-ttu-id="5fbb4-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5fbb4-108">PARAMETERS</span></span>

### <span data-ttu-id="5fbb4-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fbb4-109">-DefaultProfile</span></span>
<span data-ttu-id="5fbb4-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5fbb4-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5fbb4-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="5fbb4-111">-JobCollectionName</span></span>
<span data-ttu-id="5fbb4-112">Określa nazwę kolekcji zadań zawierającej zadanie do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="5fbb4-112">Specifies the name of a job collection that contains the job to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fbb4-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="5fbb4-113">-JobName</span></span>
<span data-ttu-id="5fbb4-114">Określa nazwę zadania do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="5fbb4-114">Specifies the name of a job to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fbb4-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5fbb4-115">-PassThru</span></span>
<span data-ttu-id="5fbb4-116">Wskazuje, że to polecenie cmdlet zwraca wartość sukcesu po powodzeniu.</span><span class="sxs-lookup"><span data-stu-id="5fbb4-116">Indicates that this cmdlet returns a value of Success on success.</span></span>
<span data-ttu-id="5fbb4-117">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="5fbb4-117">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fbb4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fbb4-118">-ResourceGroupName</span></span>
<span data-ttu-id="5fbb4-119">Określa grupę zasobów zadania, które należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="5fbb4-119">Specifies the resource group of the job to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fbb4-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5fbb4-120">-Confirm</span></span>
<span data-ttu-id="5fbb4-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5fbb4-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fbb4-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fbb4-122">-WhatIf</span></span>
<span data-ttu-id="5fbb4-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5fbb4-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fbb4-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5fbb4-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fbb4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fbb4-125">CommonParameters</span></span>
<span data-ttu-id="5fbb4-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fbb4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fbb4-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fbb4-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fbb4-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5fbb4-128">INPUTS</span></span>

### <span data-ttu-id="5fbb4-129">System. String</span><span class="sxs-lookup"><span data-stu-id="5fbb4-129">System.String</span></span>

## <span data-ttu-id="5fbb4-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5fbb4-130">OUTPUTS</span></span>

### <span data-ttu-id="5fbb4-131">System. String</span><span class="sxs-lookup"><span data-stu-id="5fbb4-131">System.String</span></span>

## <span data-ttu-id="5fbb4-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5fbb4-132">NOTES</span></span>

## <span data-ttu-id="5fbb4-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5fbb4-133">RELATED LINKS</span></span>

[<span data-ttu-id="5fbb4-134">Get-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="5fbb4-134">Get-AzureRmSchedulerJob</span></span>](./Get-AzureRmSchedulerJob.md)


