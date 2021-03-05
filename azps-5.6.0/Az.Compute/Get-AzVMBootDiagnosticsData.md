---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 15CAC050-F2E9-4872-88E7-516A6D194FAB
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmbootdiagnosticsdata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMBootDiagnosticsData.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMBootDiagnosticsData.md
ms.openlocfilehash: 539e8b0a91c72d275f0997f2ebc69e86f4a9c901
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013866"
---
# <span data-ttu-id="7bbf6-101">Get-AzVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="7bbf6-101">Get-AzVMBootDiagnosticsData</span></span>

## <span data-ttu-id="7bbf6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bbf6-102">SYNOPSIS</span></span>
<span data-ttu-id="7bbf6-103">Pobiera dane diagnostyczne rozruchu dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7bbf6-103">Gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="7bbf6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7bbf6-104">SYNTAX</span></span>

### <span data-ttu-id="7bbf6-105">WindowsParamSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="7bbf6-105">WindowsParamSet (Default)</span></span>
```
Get-AzVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Windows] [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7bbf6-106">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="7bbf6-106">LinuxParamSet</span></span>
```
Get-AzVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Linux] [[-LocalPath] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7bbf6-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="7bbf6-107">DESCRIPTION</span></span>
<span data-ttu-id="7bbf6-108">Polecenie **cmdlet Get-AzVMBootDiagnosticsData** pobiera dane diagnostyczne rozruchu dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7bbf6-108">The **Get-AzVMBootDiagnosticsData** cmdlet gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="7bbf6-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7bbf6-109">EXAMPLES</span></span>

### <span data-ttu-id="7bbf6-110">Przykład 1. Uzyskiwanie danych diagnostycznych rozruchu</span><span class="sxs-lookup"><span data-stu-id="7bbf6-110">Example 1: Get boot diagnostics data</span></span>
```
PS C:\> Get-AzVMBootDiagnosticsData -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07" -Windows -LocalPath "C:\Contoso\BootDiagnostics"
```

<span data-ttu-id="7bbf6-111">To polecenie pobiera dane diagnostyczne rozruchu dla maszyny wirtualnej o nazwie ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="7bbf6-111">This command gets boot diagnostics data for the virtual machine named ContosoVM07.</span></span>
<span data-ttu-id="7bbf6-112">Ta maszyny wirtualnej działa system operacyjny Windows.</span><span class="sxs-lookup"><span data-stu-id="7bbf6-112">This virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="7bbf6-113">Polecenie przechowuje dane w określonej ścieżce lokalnej.</span><span class="sxs-lookup"><span data-stu-id="7bbf6-113">The command stores the data in specified local path.</span></span>

## <span data-ttu-id="7bbf6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7bbf6-114">PARAMETERS</span></span>

### <span data-ttu-id="7bbf6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bbf6-115">-DefaultProfile</span></span>
<span data-ttu-id="7bbf6-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7bbf6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7bbf6-117">— Linux</span><span class="sxs-lookup"><span data-stu-id="7bbf6-117">-Linux</span></span>
<span data-ttu-id="7bbf6-118">Wskazuje, że maszyną wirtualną jest system operacyjny Linux.</span><span class="sxs-lookup"><span data-stu-id="7bbf6-118">Indicates that the virtual machine runs the Linux operating system.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LinuxParamSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bbf6-119">— LocalPath</span><span class="sxs-lookup"><span data-stu-id="7bbf6-119">-LocalPath</span></span>
<span data-ttu-id="7bbf6-120">Określa ścieżkę lokalną dla danych diagnostycznych rozruchu.</span><span class="sxs-lookup"><span data-stu-id="7bbf6-120">Specifies the local path for the boot diagnostics data.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsParamSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: LinuxParamSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bbf6-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7bbf6-121">-Name</span></span>
<span data-ttu-id="7bbf6-122">Określa nazwę maszyny wirtualnej, dla której to polecenie cmdlet pobiera dane diagnostyczne.</span><span class="sxs-lookup"><span data-stu-id="7bbf6-122">Specifies the name of the virtual machine for which this cmdlet gets diagnostics data.</span></span>

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

### <span data-ttu-id="7bbf6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bbf6-123">-ResourceGroupName</span></span>
<span data-ttu-id="7bbf6-124">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7bbf6-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="7bbf6-125">— Windows</span><span class="sxs-lookup"><span data-stu-id="7bbf6-125">-Windows</span></span>
<span data-ttu-id="7bbf6-126">Wskazuje, że na maszyny wirtualnej działa system operacyjny Windows.</span><span class="sxs-lookup"><span data-stu-id="7bbf6-126">Indicates that the virtual machine runs the Windows operating system.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsParamSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bbf6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bbf6-127">CommonParameters</span></span>
<span data-ttu-id="7bbf6-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bbf6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bbf6-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7bbf6-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bbf6-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7bbf6-130">INPUTS</span></span>

### <span data-ttu-id="7bbf6-131">System.String</span><span class="sxs-lookup"><span data-stu-id="7bbf6-131">System.String</span></span>

## <span data-ttu-id="7bbf6-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7bbf6-132">OUTPUTS</span></span>

### <span data-ttu-id="7bbf6-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="7bbf6-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="7bbf6-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="7bbf6-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="7bbf6-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7bbf6-135">NOTES</span></span>

## <span data-ttu-id="7bbf6-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7bbf6-136">RELATED LINKS</span></span>

[<span data-ttu-id="7bbf6-137">Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="7bbf6-137">Set-AzVMBootDiagnostic</span></span>](./Set-AzVMBootDiagnostic.md)


