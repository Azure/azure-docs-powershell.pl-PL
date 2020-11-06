---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVM.md
ms.openlocfilehash: bbfbf2a8a0cace2580dbd929a81bfec8a120cfe0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526250"
---
# <span data-ttu-id="e81f0-101">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e81f0-101">Remove-AzureRmVM</span></span>

## <span data-ttu-id="e81f0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e81f0-102">SYNOPSIS</span></span>
<span data-ttu-id="e81f0-103">Umożliwia usunięcie maszyny wirtualnej z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e81f0-103">Removes a virtual machine from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e81f0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e81f0-104">SYNTAX</span></span>

### <span data-ttu-id="e81f0-105">ResourceGroupNameParameterSetName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e81f0-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzureRmVM [-Name] <String> [-Force] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e81f0-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="e81f0-106">IdParameterSetName</span></span>
```
Remove-AzureRmVM [-Name] <String> [-Force] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e81f0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e81f0-107">DESCRIPTION</span></span>
<span data-ttu-id="e81f0-108">Polecenie cmdlet **Remove-AzureRmVM** umożliwia usunięcie maszyny wirtualnej z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e81f0-108">The **Remove-AzureRmVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="e81f0-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e81f0-109">EXAMPLES</span></span>

### <span data-ttu-id="e81f0-110">Przykład 1: usuwanie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="e81f0-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="e81f0-111">To polecenie powoduje usunięcie maszyny wirtualnej o nazwie VirtualMachine07 w ResourceGroup11 grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e81f0-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="e81f0-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e81f0-112">PARAMETERS</span></span>

### <span data-ttu-id="e81f0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e81f0-113">-AsJob</span></span>
<span data-ttu-id="e81f0-114">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="e81f0-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="e81f0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e81f0-115">-DefaultProfile</span></span>
<span data-ttu-id="e81f0-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e81f0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e81f0-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e81f0-117">-Force</span></span>
<span data-ttu-id="e81f0-118">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e81f0-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e81f0-119">-ID</span><span class="sxs-lookup"><span data-stu-id="e81f0-119">-Id</span></span>
<span data-ttu-id="e81f0-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e81f0-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e81f0-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e81f0-121">-Name</span></span>
<span data-ttu-id="e81f0-122">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="e81f0-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e81f0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e81f0-123">-ResourceGroupName</span></span>
<span data-ttu-id="e81f0-124">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e81f0-124">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e81f0-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e81f0-125">-Confirm</span></span>
<span data-ttu-id="e81f0-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e81f0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e81f0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e81f0-127">-WhatIf</span></span>
<span data-ttu-id="e81f0-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e81f0-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e81f0-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e81f0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e81f0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e81f0-130">CommonParameters</span></span>
<span data-ttu-id="e81f0-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e81f0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e81f0-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e81f0-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e81f0-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e81f0-133">INPUTS</span></span>

### <span data-ttu-id="e81f0-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e81f0-134">System.String</span></span>

## <span data-ttu-id="e81f0-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e81f0-135">OUTPUTS</span></span>

### <span data-ttu-id="e81f0-136">Microsoft. Azure. Commands. COMPUTE. models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="e81f0-136">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="e81f0-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e81f0-137">NOTES</span></span>

## <span data-ttu-id="e81f0-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e81f0-138">RELATED LINKS</span></span>

[<span data-ttu-id="e81f0-139">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e81f0-139">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="e81f0-140">Nowe — AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e81f0-140">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="e81f0-141">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e81f0-141">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="e81f0-142">Start — AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e81f0-142">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="e81f0-143">Zatrzymaj — AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e81f0-143">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="e81f0-144">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e81f0-144">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


