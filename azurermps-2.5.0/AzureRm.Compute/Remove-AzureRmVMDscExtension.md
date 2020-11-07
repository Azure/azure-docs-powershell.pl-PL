---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C7FCF2CA-2C8D-4280-BF68-10DEA96642A5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmdscextension
schema: 2.0.0
ms.openlocfilehash: f93d461bddb78230be3168cb1df534a4cde842e2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898789"
---
# <span data-ttu-id="41cd1-101">Remove-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="41cd1-101">Remove-AzureRmVMDscExtension</span></span>

## <span data-ttu-id="41cd1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="41cd1-102">SYNOPSIS</span></span>
<span data-ttu-id="41cd1-103">Usuwa obsługę rozszerzeń DSC z maszyny wirtualnej w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="41cd1-103">Removes a DSC extension handler from a virtual machine in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41cd1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="41cd1-104">SYNTAX</span></span>

```
Remove-AzureRmVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41cd1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="41cd1-105">DESCRIPTION</span></span>
<span data-ttu-id="41cd1-106">Polecenie cmdlet **Remove-AzureRmVMDscExtension** usuwa zażądaną obsługę rozszerzeń konfiguracji stanu z maszyny wirtualnej w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="41cd1-106">The **Remove-AzureRmVMDscExtension** cmdlet removes a Desired State Configuration (DSC) extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="41cd1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="41cd1-107">EXAMPLES</span></span>

### <span data-ttu-id="41cd1-108">Przykład 1: Usuwanie rozszerzenia DSC</span><span class="sxs-lookup"><span data-stu-id="41cd1-108">Example 1: Remove a DSC extension</span></span>
```
PS C:\> Remove-AzureRmVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="41cd1-109">To polecenie usuwa rozszerzenie o nazwie DSC na maszynie wirtualnej o nazwie VM07.</span><span class="sxs-lookup"><span data-stu-id="41cd1-109">This command removes the extension named DSC on virtual machine named VM07.</span></span>

## <span data-ttu-id="41cd1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="41cd1-110">PARAMETERS</span></span>

### <span data-ttu-id="41cd1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41cd1-111">-DefaultProfile</span></span>
<span data-ttu-id="41cd1-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="41cd1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41cd1-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="41cd1-113">-Name</span></span>
<span data-ttu-id="41cd1-114">Określa nazwę rozszerzenia DSC, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41cd1-114">Specifies the name of the DSC extension that this cmdlet removes.</span></span>
<span data-ttu-id="41cd1-115">Polecenie cmdlet Set-AzureRmVMDscExtension ustawia tę nazwę na Microsoft. PowerShell. DSC, która jest wartością domyślną używaną przez polecenie **Remove-AzureRmVMDscExtension**.</span><span class="sxs-lookup"><span data-stu-id="41cd1-115">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the default value used by **Remove-AzureRmVMDscExtension**.</span></span>

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

### <span data-ttu-id="41cd1-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41cd1-116">-ResourceGroupName</span></span>
<span data-ttu-id="41cd1-117">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="41cd1-117">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="41cd1-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="41cd1-118">-VMName</span></span>
<span data-ttu-id="41cd1-119">Określa nazwę maszyny wirtualnej, z poziomu której to polecenie cmdlet usuwa rozszerzenie DSC.</span><span class="sxs-lookup"><span data-stu-id="41cd1-119">Specifies the name of a virtual machine from which this cmdlet removes the DSC extension.</span></span>

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

### <span data-ttu-id="41cd1-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="41cd1-120">-Confirm</span></span>
<span data-ttu-id="41cd1-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41cd1-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41cd1-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41cd1-122">-WhatIf</span></span>
<span data-ttu-id="41cd1-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41cd1-123">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="41cd1-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="41cd1-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41cd1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41cd1-125">CommonParameters</span></span>
<span data-ttu-id="41cd1-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41cd1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41cd1-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41cd1-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41cd1-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="41cd1-128">INPUTS</span></span>

### <span data-ttu-id="41cd1-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="41cd1-129">None</span></span>
<span data-ttu-id="41cd1-130">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="41cd1-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="41cd1-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="41cd1-131">OUTPUTS</span></span>

### <span data-ttu-id="41cd1-132">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="41cd1-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="41cd1-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="41cd1-133">NOTES</span></span>

## <span data-ttu-id="41cd1-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="41cd1-134">RELATED LINKS</span></span>

[<span data-ttu-id="41cd1-135">Get-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="41cd1-135">Get-AzureRmVMDscExtension</span></span>](./Get-AzureRmVMDscExtension.md)

[<span data-ttu-id="41cd1-136">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="41cd1-136">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


