---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Start-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Start-AzVM.md
ms.openlocfilehash: e343b9e16f793a760166736edcef6658bde34723
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891630"
---
# <span data-ttu-id="8945a-101">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="8945a-101">Start-AzVM</span></span>

## <span data-ttu-id="8945a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8945a-102">SYNOPSIS</span></span>
<span data-ttu-id="8945a-103">Rozpoczynanie maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8945a-103">Starts an Azure virtual machine.</span></span>

## <span data-ttu-id="8945a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8945a-104">SYNTAX</span></span>

### <span data-ttu-id="8945a-105">ResourceGroupNameParameterSetName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8945a-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzVM [-Name] <String> [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8945a-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="8945a-106">IdParameterSetName</span></span>
```
Start-AzVM [-Name] <String> [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8945a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8945a-107">DESCRIPTION</span></span>
<span data-ttu-id="8945a-108">Polecenie cmdlet **Start-AzVM** rozpoczyna działanie maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8945a-108">The **Start-AzVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="8945a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8945a-109">EXAMPLES</span></span>

### <span data-ttu-id="8945a-110">Przykład 1. uruchomienie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="8945a-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="8945a-111">To polecenie umożliwia uruchomienie maszyny wirtualnej o nazwie VirtualMachine07 w ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="8945a-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="8945a-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8945a-112">PARAMETERS</span></span>

### <span data-ttu-id="8945a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8945a-113">-AsJob</span></span>
<span data-ttu-id="8945a-114">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="8945a-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="8945a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8945a-115">-DefaultProfile</span></span>
<span data-ttu-id="8945a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8945a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8945a-117">-ID</span><span class="sxs-lookup"><span data-stu-id="8945a-117">-Id</span></span>
<span data-ttu-id="8945a-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8945a-118">The resource group name.</span></span>

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

### <span data-ttu-id="8945a-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8945a-119">-Name</span></span>
<span data-ttu-id="8945a-120">Nazwa maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8945a-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="8945a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8945a-121">-ResourceGroupName</span></span>
<span data-ttu-id="8945a-122">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8945a-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="8945a-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8945a-123">-Confirm</span></span>
<span data-ttu-id="8945a-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8945a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8945a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8945a-125">-WhatIf</span></span>
<span data-ttu-id="8945a-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8945a-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8945a-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8945a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8945a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8945a-128">CommonParameters</span></span>
<span data-ttu-id="8945a-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8945a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8945a-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8945a-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8945a-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8945a-131">INPUTS</span></span>

### <span data-ttu-id="8945a-132">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="8945a-132">None</span></span>
<span data-ttu-id="8945a-133">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="8945a-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8945a-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8945a-134">OUTPUTS</span></span>

### <span data-ttu-id="8945a-135">Microsoft. Azure. Commands. COMPUTE. models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="8945a-135">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="8945a-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8945a-136">NOTES</span></span>

## <span data-ttu-id="8945a-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8945a-137">RELATED LINKS</span></span>

[<span data-ttu-id="8945a-138">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="8945a-138">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="8945a-139">Nowe — AzVM</span><span class="sxs-lookup"><span data-stu-id="8945a-139">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="8945a-140">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="8945a-140">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="8945a-141">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="8945a-141">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="8945a-142">Zatrzymaj — AzVM</span><span class="sxs-lookup"><span data-stu-id="8945a-142">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="8945a-143">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="8945a-143">Update-AzVM</span></span>](./Update-AzVM.md)


