---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: F41953F1-9515-4081-8624-6A1494DA4BB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMChefExtension.md
ms.openlocfilehash: 02647fc2148069e2c408c979e4b258fd0a641fc0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177723"
---
# <span data-ttu-id="5fe3a-101">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="5fe3a-101">Get-AzVMChefExtension</span></span>

## <span data-ttu-id="5fe3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fe3a-102">SYNOPSIS</span></span>
<span data-ttu-id="5fe3a-103">Pobiera informacje o rozszerzeniu Nas.</span><span class="sxs-lookup"><span data-stu-id="5fe3a-103">Gets information about a Chef extension.</span></span>

## <span data-ttu-id="5fe3a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5fe3a-104">SYNTAX</span></span>

### <span data-ttu-id="5fe3a-105">Linux</span><span class="sxs-lookup"><span data-stu-id="5fe3a-105">Linux</span></span>
```
Get-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status] [-Linux]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5fe3a-106">Windows</span><span class="sxs-lookup"><span data-stu-id="5fe3a-106">Windows</span></span>
```
Get-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status] [-Windows]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5fe3a-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="5fe3a-107">DESCRIPTION</span></span>
<span data-ttu-id="5fe3a-108">Polecenie **cmdlet Get-AzVMChefExtension** pobiera informacje o rozszerzeniaCh zainstalowanego na komputerze wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="5fe3a-108">The **Get-AzVMChefExtension** cmdlet gets information about a Chef extension installed on a virtual machine.</span></span>

## <span data-ttu-id="5fe3a-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5fe3a-109">EXAMPLES</span></span>

### <span data-ttu-id="5fe3a-110">Przykład 1. Uzyskaj szczegółowe informacje o rozszerzeniu Dla maszyny wirtualnej systemu Windows</span><span class="sxs-lookup"><span data-stu-id="5fe3a-110">Example 1: Get the details of Chef extension for a Windows virtual machine</span></span>
```
PS C:\> Get-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="5fe3a-111">To polecenie pobiera rozszerzenie Doc z maszyny wirtualnej systemu Windows o nazwie WindowsVM001, która należy do grupy zasobów o nazwie ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="5fe3a-111">This command gets the Chef extension from a Windows virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="5fe3a-112">Przykład 2. Uzyskaj szczegółowe informacje o rozszerzeniu Dla maszyny wirtualnej systemu Linux</span><span class="sxs-lookup"><span data-stu-id="5fe3a-112">Example 2: Get the details of Chef extension for a Linux virtual machine</span></span>
```
PS C:\> Get-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="5fe3a-113">To polecenie pobiera rozszerzenie Doc z maszyny wirtualnej systemu Linux o nazwie LinuxVM001, która należy do grupy zasobów o nazwie ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="5fe3a-113">This command gets the Chef extension from a Linux virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="5fe3a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5fe3a-114">PARAMETERS</span></span>

### <span data-ttu-id="5fe3a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fe3a-115">-DefaultProfile</span></span>
<span data-ttu-id="5fe3a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5fe3a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5fe3a-117">— Linux</span><span class="sxs-lookup"><span data-stu-id="5fe3a-117">-Linux</span></span>
<span data-ttu-id="5fe3a-118">Wskazuje, że to polecenie cmdlet działa na maszyny wirtualnej systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="5fe3a-118">Indicates that this cmdlet works on a Linux virtual machine.</span></span>

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

### <span data-ttu-id="5fe3a-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5fe3a-119">-Name</span></span>
<span data-ttu-id="5fe3a-120">Określa nazwę rozszerzenia Doc.</span><span class="sxs-lookup"><span data-stu-id="5fe3a-120">Specifies the name of the Chef extension.</span></span>

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

### <span data-ttu-id="5fe3a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fe3a-121">-ResourceGroupName</span></span>
<span data-ttu-id="5fe3a-122">Określa nazwę grupy zasobów zawierającej maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="5fe3a-122">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="5fe3a-123">— Status</span><span class="sxs-lookup"><span data-stu-id="5fe3a-123">-Status</span></span>
<span data-ttu-id="5fe3a-124">Wskazuje, że to polecenie cmdlet pobiera tylko widok wystąpienia rozszerzenia Do.</span><span class="sxs-lookup"><span data-stu-id="5fe3a-124">Indicates that this cmdlet gets only the instance view of the Chef extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fe3a-125">-NAZWA.MASZYNY.WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="5fe3a-125">-VMName</span></span>
<span data-ttu-id="5fe3a-126">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5fe3a-126">Specifies the name of a virtual machine.</span></span>

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

### <span data-ttu-id="5fe3a-127">— Windows</span><span class="sxs-lookup"><span data-stu-id="5fe3a-127">-Windows</span></span>
<span data-ttu-id="5fe3a-128">Wskazuje, że to polecenie cmdlet jest dla maszyny wirtualnej systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="5fe3a-128">Indicates that this cmdlet is for a Windows virtual machine.</span></span>

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

### <span data-ttu-id="5fe3a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fe3a-129">CommonParameters</span></span>
<span data-ttu-id="5fe3a-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fe3a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fe3a-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5fe3a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fe3a-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5fe3a-132">INPUTS</span></span>

### <span data-ttu-id="5fe3a-133">System.String</span><span class="sxs-lookup"><span data-stu-id="5fe3a-133">System.String</span></span>

### <span data-ttu-id="5fe3a-134">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="5fe3a-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5fe3a-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5fe3a-135">OUTPUTS</span></span>

### <span data-ttu-id="5fe3a-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="5fe3a-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="5fe3a-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5fe3a-137">NOTES</span></span>

## <span data-ttu-id="5fe3a-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5fe3a-138">RELATED LINKS</span></span>

[<span data-ttu-id="5fe3a-139">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="5fe3a-139">Set-AzVMChefExtension</span></span>](./Set-AzVMChefExtension.md)

[<span data-ttu-id="5fe3a-140">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="5fe3a-140">Remove-AzVMChefExtension</span></span>](./Remove-AzVMChefExtension.md)


