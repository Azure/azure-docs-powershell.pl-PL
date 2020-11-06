---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: BA79EDC8-BE89-4836-92EF-748D6F518886
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Enable-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Enable-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: 16b86028dafa2f9fa35422b4346cd11496194bfe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546060"
---
# <span data-ttu-id="6845c-101">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="6845c-101">Enable-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="6845c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6845c-102">SYNOPSIS</span></span>
<span data-ttu-id="6845c-103">Umożliwia zbieranie zadań.</span><span class="sxs-lookup"><span data-stu-id="6845c-103">Enables a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6845c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6845c-104">SYNTAX</span></span>

```
Enable-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6845c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6845c-105">DESCRIPTION</span></span>
<span data-ttu-id="6845c-106">Polecenie cmdlet **enable-AzureRmSchedulerJobCollection** umożliwia zbieranie zadań w usłudze Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="6845c-106">The **Enable-AzureRmSchedulerJobCollection** cmdlet enables a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="6845c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6845c-107">EXAMPLES</span></span>

## <span data-ttu-id="6845c-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6845c-108">PARAMETERS</span></span>

### <span data-ttu-id="6845c-109">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="6845c-109">-JobCollectionName</span></span>
<span data-ttu-id="6845c-110">Określa nazwę kolekcji zadań.</span><span class="sxs-lookup"><span data-stu-id="6845c-110">Specifies the name of a job collection.</span></span>

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

### <span data-ttu-id="6845c-111">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6845c-111">-PassThru</span></span>
<span data-ttu-id="6845c-112">Wskazuje, że to polecenie cmdlet zwraca wartość sukcesu po powodzeniu.</span><span class="sxs-lookup"><span data-stu-id="6845c-112">Indicates that this cmdlet returns a value of Success on success.</span></span>
<span data-ttu-id="6845c-113">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="6845c-113">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6845c-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6845c-114">-ResourceGroupName</span></span>
<span data-ttu-id="6845c-115">Określa grupę zasobów kolekcji zadań.</span><span class="sxs-lookup"><span data-stu-id="6845c-115">Specifies the resource group of the job collection.</span></span>

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

### <span data-ttu-id="6845c-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6845c-116">-Confirm</span></span>
<span data-ttu-id="6845c-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6845c-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6845c-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6845c-118">-WhatIf</span></span>
<span data-ttu-id="6845c-119">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6845c-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6845c-120">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6845c-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6845c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6845c-121">-DefaultProfile</span></span>
<span data-ttu-id="6845c-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6845c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6845c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6845c-123">CommonParameters</span></span>
<span data-ttu-id="6845c-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6845c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6845c-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6845c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6845c-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6845c-126">INPUTS</span></span>

## <span data-ttu-id="6845c-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6845c-127">OUTPUTS</span></span>

## <span data-ttu-id="6845c-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6845c-128">NOTES</span></span>

## <span data-ttu-id="6845c-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6845c-129">RELATED LINKS</span></span>

[<span data-ttu-id="6845c-130">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="6845c-130">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="6845c-131">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="6845c-131">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="6845c-132">Nowe — AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="6845c-132">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="6845c-133">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="6845c-133">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="6845c-134">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="6845c-134">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


