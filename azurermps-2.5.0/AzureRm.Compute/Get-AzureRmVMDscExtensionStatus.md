---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 695F224D-DA25-49F2-916E-25DA2A48A4A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmdscextensionstatus
schema: 2.0.0
ms.openlocfilehash: b6ec9918657c191e31e10c04b799603654d39d56
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897489"
---
# <span data-ttu-id="79311-101">Get-AzureRmVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="79311-101">Get-AzureRmVMDscExtensionStatus</span></span>

## <span data-ttu-id="79311-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="79311-102">SYNOPSIS</span></span>
<span data-ttu-id="79311-103">Pobiera stan obsługi rozszerzeń DSC dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="79311-103">Gets the status of the DSC extension handler for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79311-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="79311-104">SYNTAX</span></span>

```
Get-AzureRmVMDscExtensionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79311-105">Opis</span><span class="sxs-lookup"><span data-stu-id="79311-105">DESCRIPTION</span></span>
<span data-ttu-id="79311-106">Polecenie cmdlet **Get-AzureRmVMDscExtensionStatus** Pobiera stan programu obsługi rozszerzeń konfiguracji stanu (DSC) dla maszyny wirtualnej w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="79311-106">The **Get-AzureRmVMDscExtensionStatus** cmdlet gets the status of the Desired State Configuration (DSC) extension handler for a virtual machine in a resource group.</span></span>
<span data-ttu-id="79311-107">Po zastosowaniu konfiguracji to polecenie cmdlet zapewnia spójność danych wyjściowych za pomocą polecenia cmdlet Start-DscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="79311-107">When a configuration is applied this cmdlet produces output consistent with the Start-DscConfiguration cmdlet.</span></span>

## <span data-ttu-id="79311-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="79311-108">EXAMPLES</span></span>

### <span data-ttu-id="79311-109">1:1</span><span class="sxs-lookup"><span data-stu-id="79311-109">1:</span></span>
```

```

## <span data-ttu-id="79311-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="79311-110">PARAMETERS</span></span>

### <span data-ttu-id="79311-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79311-111">-DefaultProfile</span></span>
<span data-ttu-id="79311-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="79311-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79311-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="79311-113">-Name</span></span>
<span data-ttu-id="79311-114">Określa nazwę zasobu Menedżera zasobów Azure, który reprezentuje rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="79311-114">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="79311-115">Polecenie cmdlet Set-AzureRmVMDscExtension powoduje ustawienie tej nazwy na Microsoft. PowerShell. DSC, która jest taka sama, jak wartość używana przez polecenie **Get-AzureRmVMDscExtensionStatus**.</span><span class="sxs-lookup"><span data-stu-id="79311-115">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzureRmVMDscExtensionStatus**.</span></span>
<span data-ttu-id="79311-116">Ten parametr należy określić tylko wtedy, gdy w szablonie Menedżera zasobów zmieniono nazwę domyślną w polu Set cmdlet lub użyto innej nazwy zasobu.</span><span class="sxs-lookup"><span data-stu-id="79311-116">Specify this parameter only if you changed the default name in the Set cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79311-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79311-117">-ResourceGroupName</span></span>
<span data-ttu-id="79311-118">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="79311-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="79311-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="79311-119">-VMName</span></span>
<span data-ttu-id="79311-120">Określa nazwę maszyny wirtualnej, dla której to polecenie cmdlet pobiera stan rozszerzenia DSC.</span><span class="sxs-lookup"><span data-stu-id="79311-120">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79311-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79311-121">CommonParameters</span></span>
<span data-ttu-id="79311-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79311-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79311-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79311-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79311-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79311-124">INPUTS</span></span>

### <span data-ttu-id="79311-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="79311-125">None</span></span>
<span data-ttu-id="79311-126">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="79311-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="79311-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="79311-127">OUTPUTS</span></span>

### <span data-ttu-id="79311-128">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="79311-128">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="79311-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="79311-129">NOTES</span></span>

## <span data-ttu-id="79311-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="79311-130">RELATED LINKS</span></span>

[<span data-ttu-id="79311-131">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="79311-131">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


