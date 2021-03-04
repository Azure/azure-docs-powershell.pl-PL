---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmsssku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssSku.md
ms.openlocfilehash: b89bf343c1737080867bbe5e8cb5397fd52f6a4d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952801"
---
# <span data-ttu-id="48b97-101">Get-AzVmssSku</span><span class="sxs-lookup"><span data-stu-id="48b97-101">Get-AzVmssSku</span></span>

## <span data-ttu-id="48b97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48b97-102">SYNOPSIS</span></span>
<span data-ttu-id="48b97-103">Pobiera dostępne jednostki SKU dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="48b97-103">Gets the available SKUs for the VMSS.</span></span>

## <span data-ttu-id="48b97-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="48b97-104">SYNTAX</span></span>

```
Get-AzVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48b97-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="48b97-105">DESCRIPTION</span></span>
<span data-ttu-id="48b97-106">Polecenie **cmdlet Get-AzVmssSku** pobiera dostępne jednostki SKU dla zestawu skal maszyny wirtualnej (VIRTUAL Machine Scale Set).</span><span class="sxs-lookup"><span data-stu-id="48b97-106">The **Get-AzVmssSku** cmdlet gets the available SKUs for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="48b97-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="48b97-107">EXAMPLES</span></span>

### <span data-ttu-id="48b97-108">Przykład 1. Uzyskiwanie wszystkich dostępnych wersji SKU z usługi MASZYNY.WIRTUALNE</span><span class="sxs-lookup"><span data-stu-id="48b97-108">Example 1: Get all available SKUs from the VMSS</span></span>
```
PS C:\> Get-AzVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="48b97-109">To polecenie pobiera wszystkie dostępne jednostki SKU z usług MASZYNY WIRTUALNE o nazwie ContosoVMSS, które należą do grupy zasobów o nazwie ContosoGroup.</span><span class="sxs-lookup"><span data-stu-id="48b97-109">This command gets all the available SKUs from the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="48b97-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48b97-110">PARAMETERS</span></span>

### <span data-ttu-id="48b97-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48b97-111">-DefaultProfile</span></span>
<span data-ttu-id="48b97-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="48b97-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48b97-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48b97-113">-ResourceGroupName</span></span>
<span data-ttu-id="48b97-114">Określa nazwę grupy zasobów maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="48b97-114">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="48b97-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="48b97-115">-VMScaleSetName</span></span>
<span data-ttu-id="48b97-116">Nazwa maszyny wirtualnej to "gatunek".</span><span class="sxs-lookup"><span data-stu-id="48b97-116">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="48b97-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48b97-117">CommonParameters</span></span>
<span data-ttu-id="48b97-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48b97-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48b97-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="48b97-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48b97-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="48b97-120">INPUTS</span></span>

### <span data-ttu-id="48b97-121">System.String</span><span class="sxs-lookup"><span data-stu-id="48b97-121">System.String</span></span>

## <span data-ttu-id="48b97-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="48b97-122">OUTPUTS</span></span>

### <span data-ttu-id="48b97-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetSku</span><span class="sxs-lookup"><span data-stu-id="48b97-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetSku</span></span>

## <span data-ttu-id="48b97-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="48b97-124">NOTES</span></span>

## <span data-ttu-id="48b97-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="48b97-125">RELATED LINKS</span></span>

[<span data-ttu-id="48b97-126">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="48b97-126">Get-AzVmss</span></span>](./Get-AzVmss.md)


