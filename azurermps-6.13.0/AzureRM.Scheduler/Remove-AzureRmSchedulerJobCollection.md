---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: F315B193-C17B-41A9-B61D-0A0212B6B643
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/remove-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: 1a977578b278c51d8e66b0f502ba12fbac39e810
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541467"
---
# <span data-ttu-id="566f4-101">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="566f4-101">Remove-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="566f4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="566f4-102">SYNOPSIS</span></span>
<span data-ttu-id="566f4-103">Usuwa kolekcję zadań.</span><span class="sxs-lookup"><span data-stu-id="566f4-103">Removes a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="566f4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="566f4-104">SYNTAX</span></span>

```
Remove-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="566f4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="566f4-105">DESCRIPTION</span></span>
<span data-ttu-id="566f4-106">Polecenie cmdlet **Remove-AzureRmSchedulerJobCollection** usuwa kolekcję zadań w usłudze Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="566f4-106">The **Remove-AzureRmSchedulerJobCollection** cmdlet removes a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="566f4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="566f4-107">EXAMPLES</span></span>

## <span data-ttu-id="566f4-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="566f4-108">PARAMETERS</span></span>

### <span data-ttu-id="566f4-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="566f4-109">-DefaultProfile</span></span>
<span data-ttu-id="566f4-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="566f4-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="566f4-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="566f4-111">-JobCollectionName</span></span>
<span data-ttu-id="566f4-112">Określa nazwę kolekcji zadań.</span><span class="sxs-lookup"><span data-stu-id="566f4-112">Specifies the name of a job collection.</span></span>

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

### <span data-ttu-id="566f4-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="566f4-113">-PassThru</span></span>
<span data-ttu-id="566f4-114">Wskazuje, że to polecenie cmdlet zwraca wartość sukcesu po powodzeniu.</span><span class="sxs-lookup"><span data-stu-id="566f4-114">Indicates that this cmdlet returns a value of Success on success.</span></span>
<span data-ttu-id="566f4-115">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="566f4-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="566f4-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="566f4-116">-ResourceGroupName</span></span>
<span data-ttu-id="566f4-117">Określa grupę zasobów kolekcji zadań.</span><span class="sxs-lookup"><span data-stu-id="566f4-117">Specifies the resource group of the job collection.</span></span>

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

### <span data-ttu-id="566f4-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="566f4-118">-Confirm</span></span>
<span data-ttu-id="566f4-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="566f4-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="566f4-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="566f4-120">-WhatIf</span></span>
<span data-ttu-id="566f4-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="566f4-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="566f4-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="566f4-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="566f4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="566f4-123">CommonParameters</span></span>
<span data-ttu-id="566f4-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="566f4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="566f4-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="566f4-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="566f4-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="566f4-126">INPUTS</span></span>

### <span data-ttu-id="566f4-127">System. String</span><span class="sxs-lookup"><span data-stu-id="566f4-127">System.String</span></span>

## <span data-ttu-id="566f4-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="566f4-128">OUTPUTS</span></span>

### <span data-ttu-id="566f4-129">System. String</span><span class="sxs-lookup"><span data-stu-id="566f4-129">System.String</span></span>

## <span data-ttu-id="566f4-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="566f4-130">NOTES</span></span>

## <span data-ttu-id="566f4-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="566f4-131">RELATED LINKS</span></span>

[<span data-ttu-id="566f4-132">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="566f4-132">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="566f4-133">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="566f4-133">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="566f4-134">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="566f4-134">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="566f4-135">Nowe — AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="566f4-135">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="566f4-136">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="566f4-136">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


