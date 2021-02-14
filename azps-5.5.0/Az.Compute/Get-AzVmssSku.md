---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsssku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssSku.md
ms.openlocfilehash: 4b17cbb748a9841e0c22f4b8d8742562876fb9db
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100244146"
---
# <span data-ttu-id="86c46-101">Get-AzVmssSku</span><span class="sxs-lookup"><span data-stu-id="86c46-101">Get-AzVmssSku</span></span>

## <span data-ttu-id="86c46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86c46-102">SYNOPSIS</span></span>
<span data-ttu-id="86c46-103">Pobiera dostępne jednostki SKU dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="86c46-103">Gets the available SKUs for the VMSS.</span></span>

## <span data-ttu-id="86c46-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="86c46-104">SYNTAX</span></span>

```
Get-AzVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86c46-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="86c46-105">DESCRIPTION</span></span>
<span data-ttu-id="86c46-106">Polecenie **cmdlet Get-AzVmssSku** pobiera dostępne jednostki SKU dla zestawu skal maszyny wirtualnej (VIRTUAL Machine Scale Set).</span><span class="sxs-lookup"><span data-stu-id="86c46-106">The **Get-AzVmssSku** cmdlet gets the available SKUs for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="86c46-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="86c46-107">EXAMPLES</span></span>

### <span data-ttu-id="86c46-108">Przykład 1. Uzyskiwanie wszystkich dostępnych wersji SKU z usługi MASZYNY.WIRTUALNE</span><span class="sxs-lookup"><span data-stu-id="86c46-108">Example 1: Get all available SKUs from the VMSS</span></span>
```
PS C:\> Get-AzVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="86c46-109">To polecenie pobiera wszystkie dostępne jednostki SKU z usług MASZYNY WIRTUALNE o nazwie ContosoVMSS, które należą do grupy zasobów o nazwie ContosoGroup.</span><span class="sxs-lookup"><span data-stu-id="86c46-109">This command gets all the available SKUs from the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="86c46-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86c46-110">PARAMETERS</span></span>

### <span data-ttu-id="86c46-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86c46-111">-DefaultProfile</span></span>
<span data-ttu-id="86c46-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="86c46-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86c46-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86c46-113">-ResourceGroupName</span></span>
<span data-ttu-id="86c46-114">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="86c46-114">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="86c46-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="86c46-115">-VMScaleSetName</span></span>
<span data-ttu-id="86c46-116">Nazwa maszyny wirtualnej to "gatunek".</span><span class="sxs-lookup"><span data-stu-id="86c46-116">Species the name of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86c46-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86c46-117">CommonParameters</span></span>
<span data-ttu-id="86c46-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86c46-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86c46-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="86c46-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86c46-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="86c46-120">INPUTS</span></span>

### <span data-ttu-id="86c46-121">System.String</span><span class="sxs-lookup"><span data-stu-id="86c46-121">System.String</span></span>

## <span data-ttu-id="86c46-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="86c46-122">OUTPUTS</span></span>

### <span data-ttu-id="86c46-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetSku</span><span class="sxs-lookup"><span data-stu-id="86c46-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetSku</span></span>

## <span data-ttu-id="86c46-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="86c46-124">NOTES</span></span>

## <span data-ttu-id="86c46-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="86c46-125">RELATED LINKS</span></span>

[<span data-ttu-id="86c46-126">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="86c46-126">Get-AzVmss</span></span>](./Get-AzVmss.md)


