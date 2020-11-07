---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 473C71A8-1DF7-487A-B239-B80E2BB63B82
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMChefExtension.md
ms.openlocfilehash: 052082672dd822b78ff6c47abf7710c87c35a746
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868959"
---
# <span data-ttu-id="31e96-101">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="31e96-101">Remove-AzVMChefExtension</span></span>

## <span data-ttu-id="31e96-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="31e96-102">SYNOPSIS</span></span>
<span data-ttu-id="31e96-103">Usuwa rozszerzenie Kuchmistrz z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="31e96-103">Removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="31e96-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="31e96-104">SYNTAX</span></span>

### <span data-ttu-id="31e96-105">Linux</span><span class="sxs-lookup"><span data-stu-id="31e96-105">Linux</span></span>
```
Remove-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Linux]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31e96-106">Microsoft</span><span class="sxs-lookup"><span data-stu-id="31e96-106">Windows</span></span>
```
Remove-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Windows]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31e96-107">Opis</span><span class="sxs-lookup"><span data-stu-id="31e96-107">DESCRIPTION</span></span>
<span data-ttu-id="31e96-108">Polecenie cmdlet **Remove-AzVMChefExtension** usuwa rozszerzenie Kuchmistrz z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="31e96-108">The **Remove-AzVMChefExtension** cmdlet removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="31e96-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="31e96-109">EXAMPLES</span></span>

### <span data-ttu-id="31e96-110">Przykład 1: Usuwanie rozszerzenia Kuchmistrz z maszyny wirtualnej systemu Windows</span><span class="sxs-lookup"><span data-stu-id="31e96-110">Example 1: Remove a Chef extension from a Windows virtual machine</span></span>
```
PS C:\> Remove-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="31e96-111">To polecenie usuwa rozszerzenie Kuchmistrz z maszyny wirtualnej opartej na systemie Windows o nazwie WindowsVM001 należącej do grupy zasobów o nazwie ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="31e96-111">This command removes a Chef extension from a Windows based virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="31e96-112">Przykład 2: Usuwanie rozszerzenia Kuchmistrz z maszyny wirtualnej Linux</span><span class="sxs-lookup"><span data-stu-id="31e96-112">Example 2: Remove a Chef extension from a Linux virtual machine</span></span>
```
PS C:\> Remove-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="31e96-113">To polecenie usuwa rozszerzenie Kuchmistrz z maszyny wirtualnej opartej na systemie Linux o nazwie LinuxVM001 należącej do grupy zasobów o nazwie ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="31e96-113">This command removes a Chef extension from a Linux based virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="31e96-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="31e96-114">PARAMETERS</span></span>

### <span data-ttu-id="31e96-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31e96-115">-DefaultProfile</span></span>
<span data-ttu-id="31e96-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="31e96-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31e96-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="31e96-117">-Linux</span></span>
<span data-ttu-id="31e96-118">Wskazuje, że to polecenie cmdlet ma element docelowy maszyny wirtualnej Linux.</span><span class="sxs-lookup"><span data-stu-id="31e96-118">Indicates that this cmdlet targets a Linux virtual machine.</span></span>

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

### <span data-ttu-id="31e96-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="31e96-119">-Name</span></span>
<span data-ttu-id="31e96-120">Określa nazwę rozszerzenia Kuchmistrz, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31e96-120">Specifies the name of the Chef extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="31e96-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31e96-121">-ResourceGroupName</span></span>
<span data-ttu-id="31e96-122">Określa nazwę grupy zasobów zawierającej maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="31e96-122">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="31e96-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="31e96-123">-VMName</span></span>
<span data-ttu-id="31e96-124">Określa nazwę maszyny wirtualnej, dla której to polecenie cmdlet usuwa rozszerzenie Kuchmistrz.</span><span class="sxs-lookup"><span data-stu-id="31e96-124">Specifies the name of a virtual machine for which this cmdlet removes the Chef extension.</span></span>

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

### <span data-ttu-id="31e96-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="31e96-125">-Windows</span></span>
<span data-ttu-id="31e96-126">Wskazuje, że to polecenie cmdlet ma element docelowy maszyny wirtualnej systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="31e96-126">Indicates that this cmdlet targets a Windows virtual machine.</span></span>

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

### <span data-ttu-id="31e96-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="31e96-127">-Confirm</span></span>
<span data-ttu-id="31e96-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31e96-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31e96-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31e96-129">-WhatIf</span></span>
<span data-ttu-id="31e96-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31e96-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31e96-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="31e96-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31e96-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31e96-132">CommonParameters</span></span>
<span data-ttu-id="31e96-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31e96-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31e96-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31e96-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31e96-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="31e96-135">INPUTS</span></span>

### <span data-ttu-id="31e96-136">System. String</span><span class="sxs-lookup"><span data-stu-id="31e96-136">System.String</span></span>

## <span data-ttu-id="31e96-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="31e96-137">OUTPUTS</span></span>

### <span data-ttu-id="31e96-138">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="31e96-138">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="31e96-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="31e96-139">NOTES</span></span>

## <span data-ttu-id="31e96-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="31e96-140">RELATED LINKS</span></span>

[<span data-ttu-id="31e96-141">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="31e96-141">Get-AzVMChefExtension</span></span>](./Get-AzVMChefExtension.md)

[<span data-ttu-id="31e96-142">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="31e96-142">Set-AzVMChefExtension</span></span>](./Set-AzVMChefExtension.md)
