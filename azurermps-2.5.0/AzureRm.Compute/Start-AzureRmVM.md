---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/start-azurermvm
schema: 2.0.0
ms.openlocfilehash: 04110cb46d3f0ed0e5e09e6b12544b927cf6ae25
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898758"
---
# <span data-ttu-id="4addd-101">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="4addd-101">Start-AzureRmVM</span></span>

## <span data-ttu-id="4addd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4addd-102">SYNOPSIS</span></span>
<span data-ttu-id="4addd-103">Rozpoczynanie maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4addd-103">Starts an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4addd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4addd-104">SYNTAX</span></span>

### <span data-ttu-id="4addd-105">ResourceGroupNameParameterSetName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4addd-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzureRmVM [-Name] <String> [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4addd-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="4addd-106">IdParameterSetName</span></span>
```
Start-AzureRmVM [-Name] <String> [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4addd-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4addd-107">DESCRIPTION</span></span>
<span data-ttu-id="4addd-108">Polecenie cmdlet **Start-AzureRmVM** rozpoczyna działanie maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4addd-108">The **Start-AzureRmVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="4addd-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4addd-109">EXAMPLES</span></span>

### <span data-ttu-id="4addd-110">Przykład 1. uruchomienie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="4addd-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="4addd-111">To polecenie umożliwia uruchomienie maszyny wirtualnej o nazwie VirtualMachine07 w ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="4addd-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="4addd-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4addd-112">PARAMETERS</span></span>

### <span data-ttu-id="4addd-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4addd-113">-AsJob</span></span>
<span data-ttu-id="4addd-114">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="4addd-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="4addd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4addd-115">-DefaultProfile</span></span>
<span data-ttu-id="4addd-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4addd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4addd-117">-ID</span><span class="sxs-lookup"><span data-stu-id="4addd-117">-Id</span></span>
<span data-ttu-id="4addd-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4addd-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4addd-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4addd-119">-Name</span></span>
<span data-ttu-id="4addd-120">Nazwa maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4addd-120">The virtual machine name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4addd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4addd-121">-ResourceGroupName</span></span>
<span data-ttu-id="4addd-122">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4addd-122">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4addd-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4addd-123">-Confirm</span></span>
<span data-ttu-id="4addd-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4addd-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4addd-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4addd-125">-WhatIf</span></span>
<span data-ttu-id="4addd-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4addd-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4addd-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4addd-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4addd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4addd-128">CommonParameters</span></span>
<span data-ttu-id="4addd-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4addd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4addd-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4addd-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4addd-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4addd-131">INPUTS</span></span>

### <span data-ttu-id="4addd-132">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="4addd-132">None</span></span>
<span data-ttu-id="4addd-133">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="4addd-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4addd-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4addd-134">OUTPUTS</span></span>

### <span data-ttu-id="4addd-135">Microsoft. Azure. Commands. COMPUTE. models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="4addd-135">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="4addd-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4addd-136">NOTES</span></span>

## <span data-ttu-id="4addd-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4addd-137">RELATED LINKS</span></span>

[<span data-ttu-id="4addd-138">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="4addd-138">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="4addd-139">Nowe — AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="4addd-139">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="4addd-140">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="4addd-140">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="4addd-141">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="4addd-141">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="4addd-142">Zatrzymaj — AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="4addd-142">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="4addd-143">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="4addd-143">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


