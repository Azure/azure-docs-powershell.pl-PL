---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D5BEA683-44AE-4D71-827D-02A03F0BEAE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiagnosticsExtension.md
ms.openlocfilehash: bd56d9e76ffc71d75de0a29fa40291cb405e57fe
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94054018"
---
# <span data-ttu-id="e64a6-101">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="e64a6-101">Get-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="e64a6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e64a6-102">SYNOPSIS</span></span>
<span data-ttu-id="e64a6-103">Pobiera ustawienia rozszerzenia diagnostycznego na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e64a6-103">Gets the settings of the Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="e64a6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e64a6-104">SYNTAX</span></span>

```
Get-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e64a6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e64a6-105">DESCRIPTION</span></span>
<span data-ttu-id="e64a6-106">Polecenie cmdlet **Get-AzVMDiagnosticsExtension** pobiera ustawienia rozszerzenia Diagnostyka platformy Azure na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e64a6-106">The **Get-AzVMDiagnosticsExtension** cmdlet gets the settings of the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="e64a6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e64a6-107">EXAMPLES</span></span>

### <span data-ttu-id="e64a6-108">Przykład 1: uzyskiwanie rozszerzenia diagnostycznego zastosowanego do maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="e64a6-108">Example 1: Get the diagnostics extension applied to a virtual machine</span></span>
```
PS C:\> Get-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22"
```

<span data-ttu-id="e64a6-109">To polecenie powoduje wyświetlenie rozszerzenia diagnostycznego zastosowanego do maszyny wirtualnej o nazwie ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="e64a6-109">This command gets the diagnostics extension applied to the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="e64a6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e64a6-110">PARAMETERS</span></span>

### <span data-ttu-id="e64a6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e64a6-111">-DefaultProfile</span></span>
<span data-ttu-id="e64a6-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e64a6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e64a6-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e64a6-113">-Name</span></span>
<span data-ttu-id="e64a6-114">Określa nazwę rozszerzenia diagnostycznego, dla którego to polecenie cmdlet pobiera ustawienia.</span><span class="sxs-lookup"><span data-stu-id="e64a6-114">Specifies the name of the Diagnostics extension for which this cmdlet gets settings.</span></span>

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

### <span data-ttu-id="e64a6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e64a6-115">-ResourceGroupName</span></span>
<span data-ttu-id="e64a6-116">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e64a6-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="e64a6-117">-Status</span><span class="sxs-lookup"><span data-stu-id="e64a6-117">-Status</span></span>
<span data-ttu-id="e64a6-118">Wskazuje, że w tym poleceniu cmdlet jest używana wartość stanu.</span><span class="sxs-lookup"><span data-stu-id="e64a6-118">Indicates that this cmdlet uses the Status value.</span></span>

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

### <span data-ttu-id="e64a6-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="e64a6-119">-VMName</span></span>
<span data-ttu-id="e64a6-120">Określa nazwę maszyny wirtualnej, z której to polecenie cmdlet uzyskuje rozszerzenie diagnostyczne.</span><span class="sxs-lookup"><span data-stu-id="e64a6-120">Specifies the name of the virtual machine from which this cmdlet gets the Diagnostics extension.</span></span>

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

### <span data-ttu-id="e64a6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e64a6-121">CommonParameters</span></span>
<span data-ttu-id="e64a6-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e64a6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e64a6-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e64a6-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e64a6-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e64a6-124">INPUTS</span></span>

### <span data-ttu-id="e64a6-125">System. String</span><span class="sxs-lookup"><span data-stu-id="e64a6-125">System.String</span></span>

### <span data-ttu-id="e64a6-126">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e64a6-126">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e64a6-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e64a6-127">OUTPUTS</span></span>

### <span data-ttu-id="e64a6-128">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="e64a6-128">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="e64a6-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e64a6-129">NOTES</span></span>

## <span data-ttu-id="e64a6-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e64a6-130">RELATED LINKS</span></span>

[<span data-ttu-id="e64a6-131">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="e64a6-131">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="e64a6-132">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="e64a6-132">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)


