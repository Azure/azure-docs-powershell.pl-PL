---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVM.md
ms.openlocfilehash: 4cdf61c8a5afca78f1701314476d9eacb862cdfb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893557"
---
# <span data-ttu-id="9fa99-101">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="9fa99-101">Remove-AzVM</span></span>

## <span data-ttu-id="9fa99-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9fa99-102">SYNOPSIS</span></span>
<span data-ttu-id="9fa99-103">Umożliwia usunięcie maszyny wirtualnej z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9fa99-103">Removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="9fa99-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9fa99-104">SYNTAX</span></span>

### <span data-ttu-id="9fa99-105">ResourceGroupNameParameterSetName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9fa99-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzVM [-Name] <String> [-Force] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fa99-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="9fa99-106">IdParameterSetName</span></span>
```
Remove-AzVM [-Name] <String> [-Force] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fa99-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9fa99-107">DESCRIPTION</span></span>
<span data-ttu-id="9fa99-108">Polecenie cmdlet **Remove-AzVM** umożliwia usunięcie maszyny wirtualnej z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9fa99-108">The **Remove-AzVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="9fa99-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9fa99-109">EXAMPLES</span></span>

### <span data-ttu-id="9fa99-110">Przykład 1: usuwanie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="9fa99-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="9fa99-111">To polecenie powoduje usunięcie maszyny wirtualnej o nazwie VirtualMachine07 w ResourceGroup11 grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9fa99-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="9fa99-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9fa99-112">PARAMETERS</span></span>

### <span data-ttu-id="9fa99-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9fa99-113">-AsJob</span></span>
<span data-ttu-id="9fa99-114">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="9fa99-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="9fa99-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fa99-115">-DefaultProfile</span></span>
<span data-ttu-id="9fa99-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9fa99-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9fa99-117">-Force</span><span class="sxs-lookup"><span data-stu-id="9fa99-117">-Force</span></span>
<span data-ttu-id="9fa99-118">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9fa99-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fa99-119">-ID</span><span class="sxs-lookup"><span data-stu-id="9fa99-119">-Id</span></span>
<span data-ttu-id="9fa99-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9fa99-120">The resource group name.</span></span>

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

### <span data-ttu-id="9fa99-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9fa99-121">-Name</span></span>
<span data-ttu-id="9fa99-122">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="9fa99-122">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fa99-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fa99-123">-ResourceGroupName</span></span>
<span data-ttu-id="9fa99-124">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9fa99-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="9fa99-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9fa99-125">-Confirm</span></span>
<span data-ttu-id="9fa99-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fa99-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fa99-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fa99-127">-WhatIf</span></span>
<span data-ttu-id="9fa99-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fa99-128">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="9fa99-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9fa99-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fa99-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fa99-130">CommonParameters</span></span>
<span data-ttu-id="9fa99-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fa99-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fa99-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fa99-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fa99-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9fa99-133">INPUTS</span></span>

### <span data-ttu-id="9fa99-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9fa99-134">None</span></span>
<span data-ttu-id="9fa99-135">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="9fa99-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9fa99-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9fa99-136">OUTPUTS</span></span>

### <span data-ttu-id="9fa99-137">Microsoft. Azure. Commands. COMPUTE. models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="9fa99-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="9fa99-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9fa99-138">NOTES</span></span>

## <span data-ttu-id="9fa99-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9fa99-139">RELATED LINKS</span></span>

[<span data-ttu-id="9fa99-140">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="9fa99-140">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="9fa99-141">Nowe — AzVM</span><span class="sxs-lookup"><span data-stu-id="9fa99-141">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="9fa99-142">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="9fa99-142">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="9fa99-143">Start — AzVM</span><span class="sxs-lookup"><span data-stu-id="9fa99-143">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="9fa99-144">Zatrzymaj — AzVM</span><span class="sxs-lookup"><span data-stu-id="9fa99-144">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="9fa99-145">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="9fa99-145">Update-AzVM</span></span>](./Update-AzVM.md)


