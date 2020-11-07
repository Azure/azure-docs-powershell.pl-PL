---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmssextension
schema: 2.0.0
ms.openlocfilehash: 224b0302da76fd1c748cd77a183aa9a302dd3c9b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897482"
---
# <span data-ttu-id="9a90d-101">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="9a90d-101">Remove-AzureRmVmssExtension</span></span>

## <span data-ttu-id="9a90d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9a90d-102">SYNOPSIS</span></span>
<span data-ttu-id="9a90d-103">Usuwa rozszerzenie z VMSS.</span><span class="sxs-lookup"><span data-stu-id="9a90d-103">Removes an extension from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a90d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9a90d-104">SYNTAX</span></span>

### <span data-ttu-id="9a90d-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a90d-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a90d-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a90d-106">IdParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a90d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9a90d-107">DESCRIPTION</span></span>
<span data-ttu-id="9a90d-108">Polecenie cmdlet **Remove-AzureRmVmssExtension** usuwa rozszerzenie z zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="9a90d-108">The **Remove-AzureRmVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="9a90d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9a90d-109">EXAMPLES</span></span>

## <span data-ttu-id="9a90d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9a90d-110">PARAMETERS</span></span>

### <span data-ttu-id="9a90d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a90d-111">-DefaultProfile</span></span>
<span data-ttu-id="9a90d-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9a90d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a90d-113">-ID</span><span class="sxs-lookup"><span data-stu-id="9a90d-113">-Id</span></span>
<span data-ttu-id="9a90d-114">Określa identyfikator rozszerzenia, które zostanie usunięte przez to polecenie cmdlet z VMSS.</span><span class="sxs-lookup"><span data-stu-id="9a90d-114">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a90d-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9a90d-115">-Name</span></span>
<span data-ttu-id="9a90d-116">Określa nazwę rozszerzenia, które zostanie usunięte przez to polecenie cmdlet z VMSS.</span><span class="sxs-lookup"><span data-stu-id="9a90d-116">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a90d-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="9a90d-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="9a90d-118">Określa VMSS, z którego ma zostać usunięte rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="9a90d-118">Specifies the VMSS from which to remove the extension from.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a90d-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9a90d-119">-Confirm</span></span>
<span data-ttu-id="9a90d-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a90d-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a90d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a90d-121">-WhatIf</span></span>
<span data-ttu-id="9a90d-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a90d-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9a90d-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9a90d-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a90d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a90d-124">CommonParameters</span></span>
<span data-ttu-id="9a90d-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a90d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a90d-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a90d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a90d-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9a90d-127">INPUTS</span></span>

### <span data-ttu-id="9a90d-128">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="9a90d-128">VirtualMachineScaleSet</span></span>
<span data-ttu-id="9a90d-129">Parametr "VirtualMachineScaleSet" akceptuje wartość typu "VirtualMachineScaleSet" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="9a90d-129">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="9a90d-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9a90d-130">OUTPUTS</span></span>

### <span data-ttu-id="9a90d-131">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="9a90d-131">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="9a90d-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9a90d-132">NOTES</span></span>

## <span data-ttu-id="9a90d-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9a90d-133">RELATED LINKS</span></span>

[<span data-ttu-id="9a90d-134">Dodaj-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="9a90d-134">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)
