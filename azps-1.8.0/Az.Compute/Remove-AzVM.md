---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVM.md
ms.openlocfilehash: 5a7f03cbd4fdac75743fed491697ac2bb4ff6dac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868972"
---
# <span data-ttu-id="1945c-101">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="1945c-101">Remove-AzVM</span></span>

## <span data-ttu-id="1945c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1945c-102">SYNOPSIS</span></span>
<span data-ttu-id="1945c-103">Umożliwia usunięcie maszyny wirtualnej z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1945c-103">Removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="1945c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1945c-104">SYNTAX</span></span>

### <span data-ttu-id="1945c-105">ResourceGroupNameParameterSetName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1945c-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzVM [-Name] <String> [-Force] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1945c-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="1945c-106">IdParameterSetName</span></span>
```
Remove-AzVM [[-Name] <String>] [-Force] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1945c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1945c-107">DESCRIPTION</span></span>
<span data-ttu-id="1945c-108">Polecenie cmdlet **Remove-AzVM** umożliwia usunięcie maszyny wirtualnej z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1945c-108">The **Remove-AzVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="1945c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1945c-109">EXAMPLES</span></span>

### <span data-ttu-id="1945c-110">Przykład 1: usuwanie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="1945c-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="1945c-111">To polecenie powoduje usunięcie maszyny wirtualnej o nazwie VirtualMachine07 w ResourceGroup11 grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1945c-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="1945c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1945c-112">PARAMETERS</span></span>

### <span data-ttu-id="1945c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1945c-113">-AsJob</span></span>
<span data-ttu-id="1945c-114">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="1945c-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="1945c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1945c-115">-DefaultProfile</span></span>
<span data-ttu-id="1945c-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1945c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1945c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="1945c-117">-Force</span></span>
<span data-ttu-id="1945c-118">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="1945c-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1945c-119">-ID</span><span class="sxs-lookup"><span data-stu-id="1945c-119">-Id</span></span>
<span data-ttu-id="1945c-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1945c-120">The resource group name.</span></span>

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

### <span data-ttu-id="1945c-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1945c-121">-Name</span></span>
<span data-ttu-id="1945c-122">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="1945c-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases: ResourceName, VMName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1945c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1945c-123">-ResourceGroupName</span></span>
<span data-ttu-id="1945c-124">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1945c-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="1945c-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1945c-125">-Confirm</span></span>
<span data-ttu-id="1945c-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1945c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1945c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1945c-127">-WhatIf</span></span>
<span data-ttu-id="1945c-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1945c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1945c-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1945c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1945c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1945c-130">CommonParameters</span></span>
<span data-ttu-id="1945c-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1945c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1945c-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1945c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1945c-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1945c-133">INPUTS</span></span>

### <span data-ttu-id="1945c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="1945c-134">System.String</span></span>

## <span data-ttu-id="1945c-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1945c-135">OUTPUTS</span></span>

### <span data-ttu-id="1945c-136">Microsoft. Azure. Commands. COMPUTE. models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="1945c-136">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="1945c-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1945c-137">NOTES</span></span>

## <span data-ttu-id="1945c-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1945c-138">RELATED LINKS</span></span>

[<span data-ttu-id="1945c-139">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="1945c-139">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="1945c-140">Nowe — AzVM</span><span class="sxs-lookup"><span data-stu-id="1945c-140">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="1945c-141">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="1945c-141">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="1945c-142">Start — AzVM</span><span class="sxs-lookup"><span data-stu-id="1945c-142">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="1945c-143">Zatrzymaj — AzVM</span><span class="sxs-lookup"><span data-stu-id="1945c-143">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="1945c-144">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="1945c-144">Update-AzVM</span></span>](./Update-AzVM.md)


