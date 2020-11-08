---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 15CAC050-F2E9-4872-88E7-516A6D194FAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmbootdiagnosticsdata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMBootDiagnosticsData.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMBootDiagnosticsData.md
ms.openlocfilehash: 96248492feac9997d1afdba83fdda943c75fa363
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233877"
---
# <span data-ttu-id="f8c14-101">Get-AzVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="f8c14-101">Get-AzVMBootDiagnosticsData</span></span>

## <span data-ttu-id="f8c14-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f8c14-102">SYNOPSIS</span></span>
<span data-ttu-id="f8c14-103">Pobiera dane diagnostyczne dotyczące rozruchu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f8c14-103">Gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="f8c14-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f8c14-104">SYNTAX</span></span>

### <span data-ttu-id="f8c14-105">WindowsParamSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f8c14-105">WindowsParamSet (Default)</span></span>
```
Get-AzVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Windows] [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8c14-106">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="f8c14-106">LinuxParamSet</span></span>
```
Get-AzVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Linux] [[-LocalPath] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8c14-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f8c14-107">DESCRIPTION</span></span>
<span data-ttu-id="f8c14-108">Polecenie cmdlet **Get-AzVMBootDiagnosticsData** pobiera dane diagnostyczne dotyczące rozruchu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f8c14-108">The **Get-AzVMBootDiagnosticsData** cmdlet gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="f8c14-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f8c14-109">EXAMPLES</span></span>

### <span data-ttu-id="f8c14-110">Przykład 1: uzyskiwanie danych diagnostycznych rozruchu</span><span class="sxs-lookup"><span data-stu-id="f8c14-110">Example 1: Get boot diagnostics data</span></span>
```
PS C:\> Get-AzVMBootDiagnosticsData -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07" -Windows -LocalPath "C:\Contoso\BootDiagnostics"
```

<span data-ttu-id="f8c14-111">To polecenie umożliwia wyświetlenie danych diagnostycznych rozruchu maszyny wirtualnej o nazwie ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="f8c14-111">This command gets boot diagnostics data for the virtual machine named ContosoVM07.</span></span>
<span data-ttu-id="f8c14-112">Ta maszyna wirtualna uruchamia system operacyjny Windows.</span><span class="sxs-lookup"><span data-stu-id="f8c14-112">This virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="f8c14-113">Polecenie zapisuje dane w określonej ścieżce lokalnej.</span><span class="sxs-lookup"><span data-stu-id="f8c14-113">The command stores the data in specified local path.</span></span>

## <span data-ttu-id="f8c14-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f8c14-114">PARAMETERS</span></span>

### <span data-ttu-id="f8c14-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8c14-115">-DefaultProfile</span></span>
<span data-ttu-id="f8c14-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f8c14-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8c14-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="f8c14-117">-Linux</span></span>
<span data-ttu-id="f8c14-118">Oznacza, że maszyna wirtualna uruchamia system operacyjny Linux.</span><span class="sxs-lookup"><span data-stu-id="f8c14-118">Indicates that the virtual machine runs the Linux operating system.</span></span>

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

### <span data-ttu-id="f8c14-119">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="f8c14-119">-LocalPath</span></span>
<span data-ttu-id="f8c14-120">Określa ścieżkę lokalną danych diagnostycznych rozruchu.</span><span class="sxs-lookup"><span data-stu-id="f8c14-120">Specifies the local path for the boot diagnostics data.</span></span>

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

### <span data-ttu-id="f8c14-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f8c14-121">-Name</span></span>
<span data-ttu-id="f8c14-122">Określa nazwę maszyny wirtualnej, dla której to polecenie cmdlet pobiera dane diagnostyczne.</span><span class="sxs-lookup"><span data-stu-id="f8c14-122">Specifies the name of the virtual machine for which this cmdlet gets diagnostics data.</span></span>

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

### <span data-ttu-id="f8c14-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8c14-123">-ResourceGroupName</span></span>
<span data-ttu-id="f8c14-124">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f8c14-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="f8c14-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="f8c14-125">-Windows</span></span>
<span data-ttu-id="f8c14-126">Oznacza, że maszyna wirtualna uruchamia system operacyjny Windows.</span><span class="sxs-lookup"><span data-stu-id="f8c14-126">Indicates that the virtual machine runs the Windows operating system.</span></span>

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

### <span data-ttu-id="f8c14-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8c14-127">CommonParameters</span></span>
<span data-ttu-id="f8c14-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8c14-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8c14-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f8c14-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8c14-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f8c14-130">INPUTS</span></span>

### <span data-ttu-id="f8c14-131">System. String</span><span class="sxs-lookup"><span data-stu-id="f8c14-131">System.String</span></span>

## <span data-ttu-id="f8c14-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f8c14-132">OUTPUTS</span></span>

### <span data-ttu-id="f8c14-133">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="f8c14-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="f8c14-134">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="f8c14-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="f8c14-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f8c14-135">NOTES</span></span>

## <span data-ttu-id="f8c14-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f8c14-136">RELATED LINKS</span></span>

[<span data-ttu-id="f8c14-137">Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="f8c14-137">Set-AzVMBootDiagnostic</span></span>](./Set-AzVMBootDiagnostic.md)


