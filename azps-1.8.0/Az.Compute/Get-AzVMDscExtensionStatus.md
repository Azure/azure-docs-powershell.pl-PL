---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 695F224D-DA25-49F2-916E-25DA2A48A4A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdscextensionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtensionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtensionStatus.md
ms.openlocfilehash: caf6f142c9669ba3f1b5f343c4bbb1a4dc978a97
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869084"
---
# <span data-ttu-id="6a577-101">Get-AzVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="6a577-101">Get-AzVMDscExtensionStatus</span></span>

## <span data-ttu-id="6a577-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6a577-102">SYNOPSIS</span></span>
<span data-ttu-id="6a577-103">Pobiera stan obsługi rozszerzeń DSC dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6a577-103">Gets the status of the DSC extension handler for a virtual machine.</span></span>

## <span data-ttu-id="6a577-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6a577-104">SYNTAX</span></span>

```
Get-AzVMDscExtensionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a577-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6a577-105">DESCRIPTION</span></span>
<span data-ttu-id="6a577-106">Polecenie cmdlet **Get-AzVMDscExtensionStatus** Pobiera stan programu obsługi rozszerzeń konfiguracji stanu (DSC) dla maszyny wirtualnej w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="6a577-106">The **Get-AzVMDscExtensionStatus** cmdlet gets the status of the Desired State Configuration (DSC) extension handler for a virtual machine in a resource group.</span></span>
<span data-ttu-id="6a577-107">Po zastosowaniu konfiguracji to polecenie cmdlet zapewnia spójność danych wyjściowych za pomocą polecenia cmdlet Start-DscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="6a577-107">When a configuration is applied this cmdlet produces output consistent with the Start-DscConfiguration cmdlet.</span></span>

## <span data-ttu-id="6a577-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6a577-108">EXAMPLES</span></span>

## <span data-ttu-id="6a577-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6a577-109">PARAMETERS</span></span>

### <span data-ttu-id="6a577-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a577-110">-DefaultProfile</span></span>
<span data-ttu-id="6a577-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6a577-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a577-112">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6a577-112">-Name</span></span>
<span data-ttu-id="6a577-113">Określa nazwę zasobu Menedżera zasobów Azure, który reprezentuje rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="6a577-113">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="6a577-114">Polecenie cmdlet Set-AzVMDscExtension powoduje ustawienie tej nazwy na Microsoft. PowerShell. DSC, która jest taka sama, jak wartość używana przez polecenie **Get-AzVMDscExtensionStatus**.</span><span class="sxs-lookup"><span data-stu-id="6a577-114">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzVMDscExtensionStatus**.</span></span>
<span data-ttu-id="6a577-115">Ten parametr należy określić tylko wtedy, gdy w szablonie Menedżera zasobów zmieniono nazwę domyślną w polu Set cmdlet lub użyto innej nazwy zasobu.</span><span class="sxs-lookup"><span data-stu-id="6a577-115">Specify this parameter only if you changed the default name in the Set cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a577-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a577-116">-ResourceGroupName</span></span>
<span data-ttu-id="6a577-117">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6a577-117">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="6a577-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="6a577-118">-VMName</span></span>
<span data-ttu-id="6a577-119">Określa nazwę maszyny wirtualnej, dla której to polecenie cmdlet pobiera stan rozszerzenia DSC.</span><span class="sxs-lookup"><span data-stu-id="6a577-119">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a577-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a577-120">CommonParameters</span></span>
<span data-ttu-id="6a577-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a577-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a577-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6a577-122">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a577-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6a577-123">INPUTS</span></span>

### <span data-ttu-id="6a577-124">System. String</span><span class="sxs-lookup"><span data-stu-id="6a577-124">System.String</span></span>

## <span data-ttu-id="6a577-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6a577-125">OUTPUTS</span></span>

### <span data-ttu-id="6a577-126">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="6a577-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="6a577-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6a577-127">NOTES</span></span>

## <span data-ttu-id="6a577-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6a577-128">RELATED LINKS</span></span>

[<span data-ttu-id="6a577-129">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="6a577-129">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


