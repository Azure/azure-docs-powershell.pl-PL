---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 473C71A8-1DF7-487A-B239-B80E2BB63B82
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMChefExtension.md
ms.openlocfilehash: 79b16afbd6188682ff68ba5b2f2d9ccae67ff630
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051081"
---
# <span data-ttu-id="ed5aa-101">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="ed5aa-101">Remove-AzVMChefExtension</span></span>

## <span data-ttu-id="ed5aa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ed5aa-102">SYNOPSIS</span></span>
<span data-ttu-id="ed5aa-103">Usuwa rozszerzenie Kuchmistrz z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ed5aa-103">Removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="ed5aa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ed5aa-104">SYNTAX</span></span>

### <span data-ttu-id="ed5aa-105">Linux</span><span class="sxs-lookup"><span data-stu-id="ed5aa-105">Linux</span></span>
```
Remove-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Linux] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed5aa-106">Microsoft</span><span class="sxs-lookup"><span data-stu-id="ed5aa-106">Windows</span></span>
```
Remove-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Windows]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed5aa-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ed5aa-107">DESCRIPTION</span></span>
<span data-ttu-id="ed5aa-108">Polecenie cmdlet **Remove-AzVMChefExtension** usuwa rozszerzenie Kuchmistrz z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ed5aa-108">The **Remove-AzVMChefExtension** cmdlet removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="ed5aa-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ed5aa-109">EXAMPLES</span></span>

### <span data-ttu-id="ed5aa-110">Przykład 1: Usuwanie rozszerzenia Kuchmistrz z maszyny wirtualnej systemu Windows</span><span class="sxs-lookup"><span data-stu-id="ed5aa-110">Example 1: Remove a Chef extension from a Windows virtual machine</span></span>
```
PS C:\> Remove-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="ed5aa-111">To polecenie usuwa rozszerzenie Kuchmistrz z maszyny wirtualnej opartej na systemie Windows o nazwie WindowsVM001 należącej do grupy zasobów o nazwie ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="ed5aa-111">This command removes a Chef extension from a Windows based virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="ed5aa-112">Przykład 2: Usuwanie rozszerzenia Kuchmistrz z maszyny wirtualnej Linux</span><span class="sxs-lookup"><span data-stu-id="ed5aa-112">Example 2: Remove a Chef extension from a Linux virtual machine</span></span>
```
PS C:\> Remove-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="ed5aa-113">To polecenie usuwa rozszerzenie Kuchmistrz z maszyny wirtualnej opartej na systemie Linux o nazwie LinuxVM001 należącej do grupy zasobów o nazwie ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="ed5aa-113">This command removes a Chef extension from a Linux based virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="ed5aa-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ed5aa-114">PARAMETERS</span></span>

### <span data-ttu-id="ed5aa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed5aa-115">-DefaultProfile</span></span>
<span data-ttu-id="ed5aa-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ed5aa-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed5aa-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="ed5aa-117">-Linux</span></span>
<span data-ttu-id="ed5aa-118">Wskazuje, że to polecenie cmdlet ma element docelowy maszyny wirtualnej Linux.</span><span class="sxs-lookup"><span data-stu-id="ed5aa-118">Indicates that this cmdlet targets a Linux virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed5aa-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ed5aa-119">-Name</span></span>
<span data-ttu-id="ed5aa-120">Określa nazwę rozszerzenia Kuchmistrz, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed5aa-120">Specifies the name of the Chef extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed5aa-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="ed5aa-121">-NoWait</span></span>
<span data-ttu-id="ed5aa-122">Rozpoczyna operację i wraca natychmiast, zanim operacja zostanie ukończona.</span><span class="sxs-lookup"><span data-stu-id="ed5aa-122">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="ed5aa-123">W celu ustalenia, czy operacja została wykonana pomyślnie, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="ed5aa-123">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="ed5aa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed5aa-124">-ResourceGroupName</span></span>
<span data-ttu-id="ed5aa-125">Określa nazwę grupy zasobów zawierającej maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="ed5aa-125">Specifies the name of the resource group that contains the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed5aa-126">-VMName</span><span class="sxs-lookup"><span data-stu-id="ed5aa-126">-VMName</span></span>
<span data-ttu-id="ed5aa-127">Określa nazwę maszyny wirtualnej, dla której to polecenie cmdlet usuwa rozszerzenie Kuchmistrz.</span><span class="sxs-lookup"><span data-stu-id="ed5aa-127">Specifies the name of a virtual machine for which this cmdlet removes the Chef extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed5aa-128">-Windows</span><span class="sxs-lookup"><span data-stu-id="ed5aa-128">-Windows</span></span>
<span data-ttu-id="ed5aa-129">Wskazuje, że to polecenie cmdlet ma element docelowy maszyny wirtualnej systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="ed5aa-129">Indicates that this cmdlet targets a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed5aa-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ed5aa-130">-Confirm</span></span>
<span data-ttu-id="ed5aa-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed5aa-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed5aa-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed5aa-132">-WhatIf</span></span>
<span data-ttu-id="ed5aa-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed5aa-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed5aa-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ed5aa-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed5aa-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed5aa-135">CommonParameters</span></span>
<span data-ttu-id="ed5aa-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed5aa-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed5aa-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ed5aa-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed5aa-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ed5aa-138">INPUTS</span></span>

### <span data-ttu-id="ed5aa-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ed5aa-139">System.String</span></span>

## <span data-ttu-id="ed5aa-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ed5aa-140">OUTPUTS</span></span>

### <span data-ttu-id="ed5aa-141">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ed5aa-141">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="ed5aa-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ed5aa-142">NOTES</span></span>

## <span data-ttu-id="ed5aa-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ed5aa-143">RELATED LINKS</span></span>

[<span data-ttu-id="ed5aa-144">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="ed5aa-144">Get-AzVMChefExtension</span></span>](./Get-AzVMChefExtension.md)

[<span data-ttu-id="ed5aa-145">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="ed5aa-145">Set-AzVMChefExtension</span></span>](./Set-AzVMChefExtension.md)
