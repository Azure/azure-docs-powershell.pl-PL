---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: BA79EDC8-BE89-4836-92EF-748D6F518886
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/enable-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Enable-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Enable-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: 832b7659da0b71d804ddc1a8f19703b85fc8500b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718467"
---
# <span data-ttu-id="ab9db-101">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="ab9db-101">Enable-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="ab9db-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ab9db-102">SYNOPSIS</span></span>
<span data-ttu-id="ab9db-103">Umożliwia zbieranie zadań.</span><span class="sxs-lookup"><span data-stu-id="ab9db-103">Enables a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab9db-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ab9db-104">SYNTAX</span></span>

```
Enable-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab9db-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ab9db-105">DESCRIPTION</span></span>
<span data-ttu-id="ab9db-106">Polecenie cmdlet **enable-AzureRmSchedulerJobCollection** umożliwia zbieranie zadań w usłudze Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="ab9db-106">The **Enable-AzureRmSchedulerJobCollection** cmdlet enables a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="ab9db-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ab9db-107">EXAMPLES</span></span>

## <span data-ttu-id="ab9db-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ab9db-108">PARAMETERS</span></span>

### <span data-ttu-id="ab9db-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab9db-109">-DefaultProfile</span></span>
<span data-ttu-id="ab9db-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ab9db-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab9db-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="ab9db-111">-JobCollectionName</span></span>
<span data-ttu-id="ab9db-112">Określa nazwę kolekcji zadań.</span><span class="sxs-lookup"><span data-stu-id="ab9db-112">Specifies the name of a job collection.</span></span>

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

### <span data-ttu-id="ab9db-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ab9db-113">-PassThru</span></span>
<span data-ttu-id="ab9db-114">Wskazuje, że to polecenie cmdlet zwraca wartość sukcesu po powodzeniu.</span><span class="sxs-lookup"><span data-stu-id="ab9db-114">Indicates that this cmdlet returns a value of Success on success.</span></span>
<span data-ttu-id="ab9db-115">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="ab9db-115">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab9db-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab9db-116">-ResourceGroupName</span></span>
<span data-ttu-id="ab9db-117">Określa grupę zasobów kolekcji zadań.</span><span class="sxs-lookup"><span data-stu-id="ab9db-117">Specifies the resource group of the job collection.</span></span>

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

### <span data-ttu-id="ab9db-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ab9db-118">-Confirm</span></span>
<span data-ttu-id="ab9db-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab9db-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab9db-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab9db-120">-WhatIf</span></span>
<span data-ttu-id="ab9db-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab9db-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab9db-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ab9db-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab9db-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab9db-123">CommonParameters</span></span>
<span data-ttu-id="ab9db-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab9db-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab9db-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab9db-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab9db-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ab9db-126">INPUTS</span></span>

### <span data-ttu-id="ab9db-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="ab9db-127">None</span></span>
<span data-ttu-id="ab9db-128">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="ab9db-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ab9db-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ab9db-129">OUTPUTS</span></span>

## <span data-ttu-id="ab9db-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ab9db-130">NOTES</span></span>

## <span data-ttu-id="ab9db-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ab9db-131">RELATED LINKS</span></span>

[<span data-ttu-id="ab9db-132">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="ab9db-132">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="ab9db-133">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="ab9db-133">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="ab9db-134">Nowe — AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="ab9db-134">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="ab9db-135">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="ab9db-135">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="ab9db-136">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="ab9db-136">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


