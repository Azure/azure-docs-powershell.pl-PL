---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 15CAC050-F2E9-4872-88E7-516A6D194FAB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMBootDiagnosticsData.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMBootDiagnosticsData.md
ms.openlocfilehash: 5ae237c21c78f206188f23153bdf35c6bea10b19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716856"
---
# <span data-ttu-id="d124e-101">Get-AzureRmVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="d124e-101">Get-AzureRmVMBootDiagnosticsData</span></span>

## <span data-ttu-id="d124e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d124e-102">SYNOPSIS</span></span>
<span data-ttu-id="d124e-103">Pobiera dane diagnostyczne dotyczące rozruchu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d124e-103">Gets boot diagnostics data for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d124e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d124e-104">SYNTAX</span></span>

### <span data-ttu-id="d124e-105">WindowsParamSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d124e-105">WindowsParamSet (Default)</span></span>
```
Get-AzureRmVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Windows]
 [-LocalPath] <String> [<CommonParameters>]
```

### <span data-ttu-id="d124e-106">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="d124e-106">LinuxParamSet</span></span>
```
Get-AzureRmVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Linux]
 [[-LocalPath] <String>] [<CommonParameters>]
```

## <span data-ttu-id="d124e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d124e-107">DESCRIPTION</span></span>
<span data-ttu-id="d124e-108">Polecenie cmdlet **Get-AzureRmVMBootDiagnosticsData** pobiera dane diagnostyczne dotyczące rozruchu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d124e-108">The **Get-AzureRmVMBootDiagnosticsData** cmdlet gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="d124e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d124e-109">EXAMPLES</span></span>

### <span data-ttu-id="d124e-110">Przykład 1: uzyskiwanie danych diagnostycznych rozruchu</span><span class="sxs-lookup"><span data-stu-id="d124e-110">Example 1: Get boot diagnostics data</span></span>
```
PS C:\> Get-AzureRmVMBootDiagnosticsData -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07" -Windows -LocalPath "C:\Contoso\BootDiagnostics"
```

<span data-ttu-id="d124e-111">To polecenie umożliwia wyświetlenie danych diagnostycznych rozruchu maszyny wirtualnej o nazwie ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="d124e-111">This command gets boot diagnostics data for the virtual machine named ContosoVM07.</span></span>
<span data-ttu-id="d124e-112">Ta maszyna wirtualna uruchamia system operacyjny Windows.</span><span class="sxs-lookup"><span data-stu-id="d124e-112">This virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="d124e-113">Polecenie zapisuje dane w określonej ścieżce lokalnej.</span><span class="sxs-lookup"><span data-stu-id="d124e-113">The command stores the data in specified local path.</span></span>

## <span data-ttu-id="d124e-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d124e-114">PARAMETERS</span></span>

### <span data-ttu-id="d124e-115">-Linux</span><span class="sxs-lookup"><span data-stu-id="d124e-115">-Linux</span></span>
<span data-ttu-id="d124e-116">Oznacza, że maszyna wirtualna uruchamia system operacyjny Linux.</span><span class="sxs-lookup"><span data-stu-id="d124e-116">Indicates that the virtual machine runs the Linux operating system.</span></span>

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

### <span data-ttu-id="d124e-117">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="d124e-117">-LocalPath</span></span>
<span data-ttu-id="d124e-118">Określa ścieżkę lokalną danych diagnostycznych rozruchu.</span><span class="sxs-lookup"><span data-stu-id="d124e-118">Specifies the local path for the boot diagnostics data.</span></span>

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

### <span data-ttu-id="d124e-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d124e-119">-Name</span></span>
<span data-ttu-id="d124e-120">Określa nazwę maszyny wirtualnej, dla której to polecenie cmdlet pobiera dane diagnostyczne.</span><span class="sxs-lookup"><span data-stu-id="d124e-120">Specifies the name of the virtual machine for which this cmdlet gets diagnostics data.</span></span>

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

### <span data-ttu-id="d124e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d124e-121">-ResourceGroupName</span></span>
<span data-ttu-id="d124e-122">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d124e-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="d124e-123">-Windows</span><span class="sxs-lookup"><span data-stu-id="d124e-123">-Windows</span></span>
<span data-ttu-id="d124e-124">Oznacza, że maszyna wirtualna uruchamia system operacyjny Windows.</span><span class="sxs-lookup"><span data-stu-id="d124e-124">Indicates that the virtual machine runs the Windows operating system.</span></span>

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

### <span data-ttu-id="d124e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d124e-125">CommonParameters</span></span>
<span data-ttu-id="d124e-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d124e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d124e-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d124e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d124e-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d124e-128">INPUTS</span></span>

### <span data-ttu-id="d124e-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d124e-129">None</span></span>
<span data-ttu-id="d124e-130">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="d124e-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d124e-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d124e-131">OUTPUTS</span></span>

## <span data-ttu-id="d124e-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d124e-132">NOTES</span></span>

## <span data-ttu-id="d124e-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d124e-133">RELATED LINKS</span></span>

[<span data-ttu-id="d124e-134">Set-AzureRmVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="d124e-134">Set-AzureRmVMBootDiagnostics</span></span>](./Set-AzureRmVMBootDiagnostics.md)


