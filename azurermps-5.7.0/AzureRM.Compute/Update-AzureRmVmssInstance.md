---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: E8C9D68E-7C68-43D0-B348-72E9713CB99F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmssInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmssInstance.md
ms.openlocfilehash: 75b8190c34d5335904d40d386cabc76e8cbf0b0f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525233"
---
# <span data-ttu-id="f3634-101">Update-AzureRmVmssInstance</span><span class="sxs-lookup"><span data-stu-id="f3634-101">Update-AzureRmVmssInstance</span></span>

## <span data-ttu-id="f3634-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f3634-102">SYNOPSIS</span></span>
<span data-ttu-id="f3634-103">Rozpoczyna ręczne uaktualnienie wystąpienia usługi VMSS.</span><span class="sxs-lookup"><span data-stu-id="f3634-103">Starts a manual upgrade of the VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3634-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f3634-104">SYNTAX</span></span>

```
Update-AzureRmVmssInstance [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String[]>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3634-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f3634-105">DESCRIPTION</span></span>
<span data-ttu-id="f3634-106">Polecenie cmdlet Update-AzureRmVmssInstance rozpoczyna ręczne uaktualnianie określonego wystąpienia zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="f3634-106">The Update-AzureRmVmssInstance cmdlet starts a manual upgrade of the specified Virtual Machine Scale Set (VMSS) instance.</span></span>
<span data-ttu-id="f3634-107">Ta funkcja jest używana, gdy w ustawieniach skali VMSS ustawiono wartość ręcznie.</span><span class="sxs-lookup"><span data-stu-id="f3634-107">This is used when the upgrade policy on the VMSS Scale Set is set to manual.</span></span>

## <span data-ttu-id="f3634-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f3634-108">EXAMPLES</span></span>

### <span data-ttu-id="f3634-109">Przykład 1. Rozpocznij uaktualnienie wystąpienia programu VMSS</span><span class="sxs-lookup"><span data-stu-id="f3634-109">Example 1: Start an upgrade of the VMSS instance</span></span>
```
PS C:\> Update-AzureRmVmssInstance -ResourceGroupName "Group011" -VMScaleSetName "VMScaleSet001" -InstanceId "0"
```

<span data-ttu-id="f3634-110">To polecenie rozpoczyna uaktualnienie VMSS o nazwie VMScaleSet001 o IDENTYFIKATORze wystąpienia 0.</span><span class="sxs-lookup"><span data-stu-id="f3634-110">This command starts an upgrade of the VMSS named VMScaleSet001 that has the instance ID of 0.</span></span>

## <span data-ttu-id="f3634-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f3634-111">PARAMETERS</span></span>

### <span data-ttu-id="f3634-112">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="f3634-112">-InstanceId</span></span>
<span data-ttu-id="f3634-113">Określa, jako tablicę ciągów, identyfikator lub identyfikatory wystąpienia, które ma zostać uaktualnione.</span><span class="sxs-lookup"><span data-stu-id="f3634-113">Specifies, as a string array, the ID or IDs of the instance to upgrade.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3634-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3634-114">-ResourceGroupName</span></span>
<span data-ttu-id="f3634-115">Określa nazwę grupy zasobów VMSS.</span><span class="sxs-lookup"><span data-stu-id="f3634-115">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="f3634-116">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="f3634-116">-VMScaleSetName</span></span>
<span data-ttu-id="f3634-117">Określa nazwę wystąpienia VMSS, które to polecenie cmdlet jest uaktualniane.</span><span class="sxs-lookup"><span data-stu-id="f3634-117">Specifies the name of the VMSS instance that this cmdlet upgrades.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3634-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f3634-118">-Confirm</span></span>
<span data-ttu-id="f3634-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3634-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3634-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3634-120">-WhatIf</span></span>
<span data-ttu-id="f3634-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3634-121">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="f3634-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f3634-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3634-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3634-123">CommonParameters</span></span>
<span data-ttu-id="f3634-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3634-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3634-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3634-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3634-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f3634-126">INPUTS</span></span>

### <span data-ttu-id="f3634-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f3634-127">None</span></span>
<span data-ttu-id="f3634-128">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="f3634-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f3634-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f3634-129">OUTPUTS</span></span>

###  
<span data-ttu-id="f3634-130">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="f3634-130">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="f3634-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f3634-131">NOTES</span></span>

## <span data-ttu-id="f3634-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f3634-132">RELATED LINKS</span></span>

[<span data-ttu-id="f3634-133">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f3634-133">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


