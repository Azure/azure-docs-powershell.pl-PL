---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/stop-azurermvm
schema: 2.0.0
ms.openlocfilehash: 6cf37c453d47278958ccd84eaf817e6dc118b16b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717124"
---
# <span data-ttu-id="a25b8-101">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a25b8-101">Stop-AzureRmVM</span></span>

## <span data-ttu-id="a25b8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a25b8-102">SYNOPSIS</span></span>
<span data-ttu-id="a25b8-103">Zatrzymuje maszynę wirtualną platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a25b8-103">Stops an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a25b8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a25b8-104">SYNTAX</span></span>

### <span data-ttu-id="a25b8-105">ResourceGroupNameParameterSetName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a25b8-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzureRmVM [-Name] <String> [-Force] [-StayProvisioned] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a25b8-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="a25b8-106">IdParameterSetName</span></span>
```
Stop-AzureRmVM [-Name] <String> [-Force] [-StayProvisioned] [-Id] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a25b8-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a25b8-107">DESCRIPTION</span></span>
<span data-ttu-id="a25b8-108">Polecenie cmdlet **stop-AzureRmVM** zatrzymuje maszynę wirtualną platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a25b8-108">The **Stop-AzureRmVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="a25b8-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a25b8-109">EXAMPLES</span></span>

### <span data-ttu-id="a25b8-110">Przykład 1: zatrzymywanie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="a25b8-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="a25b8-111">To polecenie zatrzymuje maszynę wirtualną o nazwie VirtualMachine07 w ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="a25b8-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="a25b8-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a25b8-112">PARAMETERS</span></span>

### <span data-ttu-id="a25b8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a25b8-113">-AsJob</span></span>
<span data-ttu-id="a25b8-114">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="a25b8-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a25b8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a25b8-115">-DefaultProfile</span></span>
<span data-ttu-id="a25b8-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a25b8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a25b8-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a25b8-117">-Force</span></span>
<span data-ttu-id="a25b8-118">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a25b8-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a25b8-119">-ID</span><span class="sxs-lookup"><span data-stu-id="a25b8-119">-Id</span></span>
<span data-ttu-id="a25b8-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a25b8-120">The resource group name.</span></span>

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

### <span data-ttu-id="a25b8-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a25b8-121">-Name</span></span>
<span data-ttu-id="a25b8-122">Nazwa maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a25b8-122">The virtual machine name.</span></span>

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

### <span data-ttu-id="a25b8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a25b8-123">-ResourceGroupName</span></span>
<span data-ttu-id="a25b8-124">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a25b8-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="a25b8-125">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="a25b8-125">-StayProvisioned</span></span>
<span data-ttu-id="a25b8-126">Polecenie cmdlet zatrzymuje wszystkie maszyny wirtualne w VMSS, ale nie powoduje ich cofnięcia przydziału.</span><span class="sxs-lookup"><span data-stu-id="a25b8-126">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="a25b8-127">Konto jest obciążane za zatrzymane maszyny wirtualne.</span><span class="sxs-lookup"><span data-stu-id="a25b8-127">The account is charged for the stopped virtual machines.</span></span>

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

### <span data-ttu-id="a25b8-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a25b8-128">-Confirm</span></span>
<span data-ttu-id="a25b8-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a25b8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a25b8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a25b8-130">-WhatIf</span></span>
<span data-ttu-id="a25b8-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a25b8-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a25b8-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a25b8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a25b8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a25b8-133">CommonParameters</span></span>
<span data-ttu-id="a25b8-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a25b8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a25b8-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a25b8-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a25b8-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a25b8-136">INPUTS</span></span>

### <span data-ttu-id="a25b8-137">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a25b8-137">None</span></span>
<span data-ttu-id="a25b8-138">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="a25b8-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a25b8-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a25b8-139">OUTPUTS</span></span>

### <span data-ttu-id="a25b8-140">Microsoft. Azure. Commands. COMPUTE. models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="a25b8-140">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="a25b8-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a25b8-141">NOTES</span></span>

## <span data-ttu-id="a25b8-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a25b8-142">RELATED LINKS</span></span>

[<span data-ttu-id="a25b8-143">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a25b8-143">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="a25b8-144">Nowe — AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a25b8-144">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="a25b8-145">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a25b8-145">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="a25b8-146">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a25b8-146">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="a25b8-147">Start — AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a25b8-147">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="a25b8-148">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a25b8-148">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


