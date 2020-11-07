---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Stop-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Stop-AzVM.md
ms.openlocfilehash: c35326449678578492b5b8a7d4a3f5b8bff5a41d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891617"
---
# <span data-ttu-id="1dfbe-101">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="1dfbe-101">Stop-AzVM</span></span>

## <span data-ttu-id="1dfbe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1dfbe-102">SYNOPSIS</span></span>
<span data-ttu-id="1dfbe-103">Zatrzymuje maszynę wirtualną platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1dfbe-103">Stops an Azure virtual machine.</span></span>

## <span data-ttu-id="1dfbe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1dfbe-104">SYNTAX</span></span>

### <span data-ttu-id="1dfbe-105">ResourceGroupNameParameterSetName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1dfbe-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzVM [-Name] <String> [-Force] [-StayProvisioned] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dfbe-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="1dfbe-106">IdParameterSetName</span></span>
```
Stop-AzVM [-Name] <String> [-Force] [-StayProvisioned] [-Id] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1dfbe-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1dfbe-107">DESCRIPTION</span></span>
<span data-ttu-id="1dfbe-108">Polecenie cmdlet **stop-AzVM** zatrzymuje maszynę wirtualną platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1dfbe-108">The **Stop-AzVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="1dfbe-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1dfbe-109">EXAMPLES</span></span>

### <span data-ttu-id="1dfbe-110">Przykład 1: zatrzymywanie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="1dfbe-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="1dfbe-111">To polecenie zatrzymuje maszynę wirtualną o nazwie VirtualMachine07 w ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="1dfbe-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="1dfbe-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1dfbe-112">PARAMETERS</span></span>

### <span data-ttu-id="1dfbe-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1dfbe-113">-AsJob</span></span>
<span data-ttu-id="1dfbe-114">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="1dfbe-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="1dfbe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dfbe-115">-DefaultProfile</span></span>
<span data-ttu-id="1dfbe-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1dfbe-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1dfbe-117">-Force</span><span class="sxs-lookup"><span data-stu-id="1dfbe-117">-Force</span></span>
<span data-ttu-id="1dfbe-118">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="1dfbe-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1dfbe-119">-ID</span><span class="sxs-lookup"><span data-stu-id="1dfbe-119">-Id</span></span>
<span data-ttu-id="1dfbe-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1dfbe-120">The resource group name.</span></span>

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

### <span data-ttu-id="1dfbe-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1dfbe-121">-Name</span></span>
<span data-ttu-id="1dfbe-122">Nazwa maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1dfbe-122">The virtual machine name.</span></span>

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

### <span data-ttu-id="1dfbe-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dfbe-123">-ResourceGroupName</span></span>
<span data-ttu-id="1dfbe-124">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1dfbe-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="1dfbe-125">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="1dfbe-125">-StayProvisioned</span></span>
<span data-ttu-id="1dfbe-126">Polecenie cmdlet zatrzymuje wszystkie maszyny wirtualne w VMSS, ale nie powoduje ich cofnięcia przydziału.</span><span class="sxs-lookup"><span data-stu-id="1dfbe-126">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="1dfbe-127">Konto jest obciążane za zatrzymane maszyny wirtualne.</span><span class="sxs-lookup"><span data-stu-id="1dfbe-127">The account is charged for the stopped virtual machines.</span></span>

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

### <span data-ttu-id="1dfbe-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1dfbe-128">-Confirm</span></span>
<span data-ttu-id="1dfbe-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1dfbe-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dfbe-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dfbe-130">-WhatIf</span></span>
<span data-ttu-id="1dfbe-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1dfbe-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1dfbe-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1dfbe-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dfbe-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dfbe-133">CommonParameters</span></span>
<span data-ttu-id="1dfbe-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dfbe-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dfbe-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dfbe-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dfbe-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1dfbe-136">INPUTS</span></span>

### <span data-ttu-id="1dfbe-137">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="1dfbe-137">None</span></span>
<span data-ttu-id="1dfbe-138">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="1dfbe-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1dfbe-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1dfbe-139">OUTPUTS</span></span>

### <span data-ttu-id="1dfbe-140">Microsoft. Azure. Commands. COMPUTE. models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="1dfbe-140">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="1dfbe-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1dfbe-141">NOTES</span></span>

## <span data-ttu-id="1dfbe-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1dfbe-142">RELATED LINKS</span></span>

[<span data-ttu-id="1dfbe-143">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="1dfbe-143">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="1dfbe-144">Nowe — AzVM</span><span class="sxs-lookup"><span data-stu-id="1dfbe-144">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="1dfbe-145">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="1dfbe-145">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="1dfbe-146">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="1dfbe-146">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="1dfbe-147">Start — AzVM</span><span class="sxs-lookup"><span data-stu-id="1dfbe-147">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="1dfbe-148">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="1dfbe-148">Update-AzVM</span></span>](./Update-AzVM.md)


