---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 15CAC050-F2E9-4872-88E7-516A6D194FAB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmbootdiagnosticsdata
schema: 2.0.0
ms.openlocfilehash: 867f2c14e90eddd9649e0720d41f56aa896c61ff
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898049"
---
# <span data-ttu-id="5e49d-101">Get-AzureRmVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="5e49d-101">Get-AzureRmVMBootDiagnosticsData</span></span>

## <span data-ttu-id="5e49d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5e49d-102">SYNOPSIS</span></span>
<span data-ttu-id="5e49d-103">Pobiera dane diagnostyczne dotyczące rozruchu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5e49d-103">Gets boot diagnostics data for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e49d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5e49d-104">SYNTAX</span></span>

### <span data-ttu-id="5e49d-105">WindowsParamSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5e49d-105">WindowsParamSet (Default)</span></span>
```
Get-AzureRmVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Windows]
 [-LocalPath] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e49d-106">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="5e49d-106">LinuxParamSet</span></span>
```
Get-AzureRmVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Linux]
 [[-LocalPath] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e49d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5e49d-107">DESCRIPTION</span></span>
<span data-ttu-id="5e49d-108">Polecenie cmdlet **Get-AzureRmVMBootDiagnosticsData** pobiera dane diagnostyczne dotyczące rozruchu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5e49d-108">The **Get-AzureRmVMBootDiagnosticsData** cmdlet gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="5e49d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5e49d-109">EXAMPLES</span></span>

### <span data-ttu-id="5e49d-110">Przykład 1: uzyskiwanie danych diagnostycznych rozruchu</span><span class="sxs-lookup"><span data-stu-id="5e49d-110">Example 1: Get boot diagnostics data</span></span>
```
PS C:\> Get-AzureRmVMBootDiagnosticsData -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07" -Windows -LocalPath "C:\Contoso\BootDiagnostics"
```

<span data-ttu-id="5e49d-111">To polecenie umożliwia wyświetlenie danych diagnostycznych rozruchu maszyny wirtualnej o nazwie ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="5e49d-111">This command gets boot diagnostics data for the virtual machine named ContosoVM07.</span></span>
<span data-ttu-id="5e49d-112">Ta maszyna wirtualna uruchamia system operacyjny Windows.</span><span class="sxs-lookup"><span data-stu-id="5e49d-112">This virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="5e49d-113">Polecenie zapisuje dane w określonej ścieżce lokalnej.</span><span class="sxs-lookup"><span data-stu-id="5e49d-113">The command stores the data in specified local path.</span></span>

## <span data-ttu-id="5e49d-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5e49d-114">PARAMETERS</span></span>

### <span data-ttu-id="5e49d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e49d-115">-DefaultProfile</span></span>
<span data-ttu-id="5e49d-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5e49d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e49d-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="5e49d-117">-Linux</span></span>
<span data-ttu-id="5e49d-118">Oznacza, że maszyna wirtualna uruchamia system operacyjny Linux.</span><span class="sxs-lookup"><span data-stu-id="5e49d-118">Indicates that the virtual machine runs the Linux operating system.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LinuxParamSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e49d-119">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="5e49d-119">-LocalPath</span></span>
<span data-ttu-id="5e49d-120">Określa ścieżkę lokalną danych diagnostycznych rozruchu.</span><span class="sxs-lookup"><span data-stu-id="5e49d-120">Specifies the local path for the boot diagnostics data.</span></span>

```yaml
Type: String
Parameter Sets: WindowsParamSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: LinuxParamSet
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e49d-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5e49d-121">-Name</span></span>
<span data-ttu-id="5e49d-122">Określa nazwę maszyny wirtualnej, dla której to polecenie cmdlet pobiera dane diagnostyczne.</span><span class="sxs-lookup"><span data-stu-id="5e49d-122">Specifies the name of the virtual machine for which this cmdlet gets diagnostics data.</span></span>

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

### <span data-ttu-id="5e49d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e49d-123">-ResourceGroupName</span></span>
<span data-ttu-id="5e49d-124">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5e49d-124">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e49d-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="5e49d-125">-Windows</span></span>
<span data-ttu-id="5e49d-126">Oznacza, że maszyna wirtualna uruchamia system operacyjny Windows.</span><span class="sxs-lookup"><span data-stu-id="5e49d-126">Indicates that the virtual machine runs the Windows operating system.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WindowsParamSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e49d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e49d-127">CommonParameters</span></span>
<span data-ttu-id="5e49d-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e49d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e49d-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e49d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e49d-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5e49d-130">INPUTS</span></span>

### <span data-ttu-id="5e49d-131">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="5e49d-131">None</span></span>
<span data-ttu-id="5e49d-132">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="5e49d-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5e49d-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5e49d-133">OUTPUTS</span></span>

### <span data-ttu-id="5e49d-134">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="5e49d-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="5e49d-135">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="5e49d-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="5e49d-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5e49d-136">NOTES</span></span>

## <span data-ttu-id="5e49d-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5e49d-137">RELATED LINKS</span></span>

[<span data-ttu-id="5e49d-138">Set-AzureRmVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="5e49d-138">Set-AzureRmVMBootDiagnostics</span></span>](./Set-AzureRmVMBootDiagnostics.md)


