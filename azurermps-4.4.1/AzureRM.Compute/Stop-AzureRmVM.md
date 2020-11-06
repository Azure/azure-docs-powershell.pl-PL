---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVM.md
ms.openlocfilehash: f0d6ab84e457894b3c1ff7309efc6914350a03e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549235"
---
# <span data-ttu-id="599c4-101">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="599c4-101">Stop-AzureRmVM</span></span>

## <span data-ttu-id="599c4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="599c4-102">SYNOPSIS</span></span>
<span data-ttu-id="599c4-103">Zatrzymuje maszynę wirtualną platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="599c4-103">Stops an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="599c4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="599c4-104">SYNTAX</span></span>

### <span data-ttu-id="599c4-105">ResourceGroupNameParameterSetName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="599c4-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzureRmVM [-Name] <String> [-Force] [-StayProvisioned] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="599c4-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="599c4-106">IdParameterSetName</span></span>
```
Stop-AzureRmVM [-Name] <String> [-Force] [-StayProvisioned] [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="599c4-107">Opis</span><span class="sxs-lookup"><span data-stu-id="599c4-107">DESCRIPTION</span></span>
<span data-ttu-id="599c4-108">Polecenie cmdlet **stop-AzureRmVM** zatrzymuje maszynę wirtualną platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="599c4-108">The **Stop-AzureRmVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="599c4-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="599c4-109">EXAMPLES</span></span>

### <span data-ttu-id="599c4-110">Przykład 1: zatrzymywanie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="599c4-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="599c4-111">To polecenie zatrzymuje maszynę wirtualną o nazwie VirtualMachine07 w ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="599c4-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="599c4-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="599c4-112">PARAMETERS</span></span>

### <span data-ttu-id="599c4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="599c4-113">-DefaultProfile</span></span>
<span data-ttu-id="599c4-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="599c4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="599c4-115">-Force</span><span class="sxs-lookup"><span data-stu-id="599c4-115">-Force</span></span>
<span data-ttu-id="599c4-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="599c4-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="599c4-117">-ID</span><span class="sxs-lookup"><span data-stu-id="599c4-117">-Id</span></span>
<span data-ttu-id="599c4-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="599c4-118">The resource group name.</span></span>

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

### <span data-ttu-id="599c4-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="599c4-119">-Name</span></span>
<span data-ttu-id="599c4-120">Nazwa maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="599c4-120">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="599c4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="599c4-121">-ResourceGroupName</span></span>
<span data-ttu-id="599c4-122">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="599c4-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="599c4-123">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="599c4-123">-StayProvisioned</span></span>
<span data-ttu-id="599c4-124">Polecenie cmdlet zatrzymuje wszystkie maszyny wirtualne w VMSS, ale nie powoduje ich cofnięcia przydziału.</span><span class="sxs-lookup"><span data-stu-id="599c4-124">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="599c4-125">Konto jest obciążane za zatrzymane maszyny wirtualne.</span><span class="sxs-lookup"><span data-stu-id="599c4-125">The account is charged for the stopped virtual machines.</span></span>

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

### <span data-ttu-id="599c4-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="599c4-126">-Confirm</span></span>
<span data-ttu-id="599c4-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="599c4-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="599c4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="599c4-128">-WhatIf</span></span>
<span data-ttu-id="599c4-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="599c4-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="599c4-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="599c4-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="599c4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="599c4-131">CommonParameters</span></span>
<span data-ttu-id="599c4-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="599c4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="599c4-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="599c4-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="599c4-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="599c4-134">INPUTS</span></span>

## <span data-ttu-id="599c4-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="599c4-135">OUTPUTS</span></span>

## <span data-ttu-id="599c4-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="599c4-136">NOTES</span></span>

## <span data-ttu-id="599c4-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="599c4-137">RELATED LINKS</span></span>

[<span data-ttu-id="599c4-138">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="599c4-138">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="599c4-139">Nowe — AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="599c4-139">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="599c4-140">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="599c4-140">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="599c4-141">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="599c4-141">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="599c4-142">Start — AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="599c4-142">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="599c4-143">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="599c4-143">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


