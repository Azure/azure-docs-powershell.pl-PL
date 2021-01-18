---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 15CAC050-F2E9-4872-88E7-516A6D194FAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmbootdiagnosticsdata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMBootDiagnosticsData.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMBootDiagnosticsData.md
ms.openlocfilehash: 96248492feac9997d1afdba83fdda943c75fa363
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504120"
---
# <span data-ttu-id="dfaba-101">Get-AzVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="dfaba-101">Get-AzVMBootDiagnosticsData</span></span>

## <span data-ttu-id="dfaba-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dfaba-102">SYNOPSIS</span></span>
<span data-ttu-id="dfaba-103">Pobiera dane diagnostyczne dotyczące rozruchu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="dfaba-103">Gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="dfaba-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dfaba-104">SYNTAX</span></span>

### <span data-ttu-id="dfaba-105">WindowsParamSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="dfaba-105">WindowsParamSet (Default)</span></span>
```
Get-AzVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Windows] [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dfaba-106">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="dfaba-106">LinuxParamSet</span></span>
```
Get-AzVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Linux] [[-LocalPath] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dfaba-107">Opis</span><span class="sxs-lookup"><span data-stu-id="dfaba-107">DESCRIPTION</span></span>
<span data-ttu-id="dfaba-108">Polecenie cmdlet **Get-AzVMBootDiagnosticsData** pobiera dane diagnostyczne dotyczące rozruchu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="dfaba-108">The **Get-AzVMBootDiagnosticsData** cmdlet gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="dfaba-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dfaba-109">EXAMPLES</span></span>

### <span data-ttu-id="dfaba-110">Przykład 1: uzyskiwanie danych diagnostycznych rozruchu</span><span class="sxs-lookup"><span data-stu-id="dfaba-110">Example 1: Get boot diagnostics data</span></span>
```
PS C:\> Get-AzVMBootDiagnosticsData -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07" -Windows -LocalPath "C:\Contoso\BootDiagnostics"
```

<span data-ttu-id="dfaba-111">To polecenie umożliwia wyświetlenie danych diagnostycznych rozruchu maszyny wirtualnej o nazwie ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="dfaba-111">This command gets boot diagnostics data for the virtual machine named ContosoVM07.</span></span>
<span data-ttu-id="dfaba-112">Ta maszyna wirtualna uruchamia system operacyjny Windows.</span><span class="sxs-lookup"><span data-stu-id="dfaba-112">This virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="dfaba-113">Polecenie zapisuje dane w określonej ścieżce lokalnej.</span><span class="sxs-lookup"><span data-stu-id="dfaba-113">The command stores the data in specified local path.</span></span>

## <span data-ttu-id="dfaba-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dfaba-114">PARAMETERS</span></span>

### <span data-ttu-id="dfaba-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfaba-115">-DefaultProfile</span></span>
<span data-ttu-id="dfaba-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dfaba-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfaba-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="dfaba-117">-Linux</span></span>
<span data-ttu-id="dfaba-118">Oznacza, że maszyna wirtualna uruchamia system operacyjny Linux.</span><span class="sxs-lookup"><span data-stu-id="dfaba-118">Indicates that the virtual machine runs the Linux operating system.</span></span>

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

### <span data-ttu-id="dfaba-119">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="dfaba-119">-LocalPath</span></span>
<span data-ttu-id="dfaba-120">Określa ścieżkę lokalną danych diagnostycznych rozruchu.</span><span class="sxs-lookup"><span data-stu-id="dfaba-120">Specifies the local path for the boot diagnostics data.</span></span>

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

### <span data-ttu-id="dfaba-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dfaba-121">-Name</span></span>
<span data-ttu-id="dfaba-122">Określa nazwę maszyny wirtualnej, dla której to polecenie cmdlet pobiera dane diagnostyczne.</span><span class="sxs-lookup"><span data-stu-id="dfaba-122">Specifies the name of the virtual machine for which this cmdlet gets diagnostics data.</span></span>

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

### <span data-ttu-id="dfaba-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfaba-123">-ResourceGroupName</span></span>
<span data-ttu-id="dfaba-124">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="dfaba-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="dfaba-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="dfaba-125">-Windows</span></span>
<span data-ttu-id="dfaba-126">Oznacza, że maszyna wirtualna uruchamia system operacyjny Windows.</span><span class="sxs-lookup"><span data-stu-id="dfaba-126">Indicates that the virtual machine runs the Windows operating system.</span></span>

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

### <span data-ttu-id="dfaba-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfaba-127">CommonParameters</span></span>
<span data-ttu-id="dfaba-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfaba-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfaba-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dfaba-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfaba-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dfaba-130">INPUTS</span></span>

### <span data-ttu-id="dfaba-131">System. String</span><span class="sxs-lookup"><span data-stu-id="dfaba-131">System.String</span></span>

## <span data-ttu-id="dfaba-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dfaba-132">OUTPUTS</span></span>

### <span data-ttu-id="dfaba-133">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="dfaba-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="dfaba-134">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="dfaba-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="dfaba-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dfaba-135">NOTES</span></span>

## <span data-ttu-id="dfaba-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dfaba-136">RELATED LINKS</span></span>

[<span data-ttu-id="dfaba-137">Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="dfaba-137">Set-AzVMBootDiagnostic</span></span>](./Set-AzVMBootDiagnostic.md)


