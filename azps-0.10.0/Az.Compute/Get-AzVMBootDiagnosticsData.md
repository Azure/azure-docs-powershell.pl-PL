---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 15CAC050-F2E9-4872-88E7-516A6D194FAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmbootdiagnosticsdata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMBootDiagnosticsData.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMBootDiagnosticsData.md
ms.openlocfilehash: ab7bae5430bf2b588997d57e92a18a4408ca4334
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893781"
---
# <span data-ttu-id="3e981-101">Get-AzVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="3e981-101">Get-AzVMBootDiagnosticsData</span></span>

## <span data-ttu-id="3e981-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3e981-102">SYNOPSIS</span></span>
<span data-ttu-id="3e981-103">Pobiera dane diagnostyczne dotyczące rozruchu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3e981-103">Gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="3e981-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3e981-104">SYNTAX</span></span>

### <span data-ttu-id="3e981-105">WindowsParamSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3e981-105">WindowsParamSet (Default)</span></span>
```
Get-AzVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Windows]
 [-LocalPath] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e981-106">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="3e981-106">LinuxParamSet</span></span>
```
Get-AzVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Linux]
 [[-LocalPath] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e981-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3e981-107">DESCRIPTION</span></span>
<span data-ttu-id="3e981-108">Polecenie cmdlet **Get-AzVMBootDiagnosticsData** pobiera dane diagnostyczne dotyczące rozruchu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3e981-108">The **Get-AzVMBootDiagnosticsData** cmdlet gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="3e981-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3e981-109">EXAMPLES</span></span>

### <span data-ttu-id="3e981-110">Przykład 1: uzyskiwanie danych diagnostycznych rozruchu</span><span class="sxs-lookup"><span data-stu-id="3e981-110">Example 1: Get boot diagnostics data</span></span>
```
PS C:\> Get-AzVMBootDiagnosticsData -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07" -Windows -LocalPath "C:\Contoso\BootDiagnostics"
```

<span data-ttu-id="3e981-111">To polecenie umożliwia wyświetlenie danych diagnostycznych rozruchu maszyny wirtualnej o nazwie ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="3e981-111">This command gets boot diagnostics data for the virtual machine named ContosoVM07.</span></span>
<span data-ttu-id="3e981-112">Ta maszyna wirtualna uruchamia system operacyjny Windows.</span><span class="sxs-lookup"><span data-stu-id="3e981-112">This virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="3e981-113">Polecenie zapisuje dane w określonej ścieżce lokalnej.</span><span class="sxs-lookup"><span data-stu-id="3e981-113">The command stores the data in specified local path.</span></span>

## <span data-ttu-id="3e981-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3e981-114">PARAMETERS</span></span>

### <span data-ttu-id="3e981-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e981-115">-DefaultProfile</span></span>
<span data-ttu-id="3e981-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3e981-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e981-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="3e981-117">-Linux</span></span>
<span data-ttu-id="3e981-118">Oznacza, że maszyna wirtualna uruchamia system operacyjny Linux.</span><span class="sxs-lookup"><span data-stu-id="3e981-118">Indicates that the virtual machine runs the Linux operating system.</span></span>

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

### <span data-ttu-id="3e981-119">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="3e981-119">-LocalPath</span></span>
<span data-ttu-id="3e981-120">Określa ścieżkę lokalną danych diagnostycznych rozruchu.</span><span class="sxs-lookup"><span data-stu-id="3e981-120">Specifies the local path for the boot diagnostics data.</span></span>

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

### <span data-ttu-id="3e981-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3e981-121">-Name</span></span>
<span data-ttu-id="3e981-122">Określa nazwę maszyny wirtualnej, dla której to polecenie cmdlet pobiera dane diagnostyczne.</span><span class="sxs-lookup"><span data-stu-id="3e981-122">Specifies the name of the virtual machine for which this cmdlet gets diagnostics data.</span></span>

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

### <span data-ttu-id="3e981-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e981-123">-ResourceGroupName</span></span>
<span data-ttu-id="3e981-124">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3e981-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="3e981-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="3e981-125">-Windows</span></span>
<span data-ttu-id="3e981-126">Oznacza, że maszyna wirtualna uruchamia system operacyjny Windows.</span><span class="sxs-lookup"><span data-stu-id="3e981-126">Indicates that the virtual machine runs the Windows operating system.</span></span>

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

### <span data-ttu-id="3e981-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e981-127">CommonParameters</span></span>
<span data-ttu-id="3e981-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e981-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e981-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e981-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e981-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3e981-130">INPUTS</span></span>

### <span data-ttu-id="3e981-131">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3e981-131">None</span></span>
<span data-ttu-id="3e981-132">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="3e981-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3e981-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3e981-133">OUTPUTS</span></span>

### <span data-ttu-id="3e981-134">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="3e981-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="3e981-135">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="3e981-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="3e981-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3e981-136">NOTES</span></span>

## <span data-ttu-id="3e981-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3e981-137">RELATED LINKS</span></span>

[<span data-ttu-id="3e981-138">Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="3e981-138">Set-AzVMBootDiagnostic</span></span>](./Set-AzVMBootDiagnostic.md)


