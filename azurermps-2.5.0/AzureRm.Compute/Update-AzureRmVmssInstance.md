---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E8C9D68E-7C68-43D0-B348-72E9713CB99F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermvmssinstance
schema: 2.0.0
ms.openlocfilehash: 07b068587848bc8af92fc49b039155c0a2c4fdd8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898935"
---
# <span data-ttu-id="0e72b-101">Update-AzureRmVmssInstance</span><span class="sxs-lookup"><span data-stu-id="0e72b-101">Update-AzureRmVmssInstance</span></span>

## <span data-ttu-id="0e72b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0e72b-102">SYNOPSIS</span></span>
<span data-ttu-id="0e72b-103">Rozpoczyna ręczne uaktualnienie wystąpienia usługi VMSS.</span><span class="sxs-lookup"><span data-stu-id="0e72b-103">Starts a manual upgrade of the VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e72b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0e72b-104">SYNTAX</span></span>

```
Update-AzureRmVmssInstance [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e72b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0e72b-105">DESCRIPTION</span></span>
<span data-ttu-id="0e72b-106">Polecenie cmdlet Update-AzureRmVmssInstance rozpoczyna ręczne uaktualnianie określonego wystąpienia zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="0e72b-106">The Update-AzureRmVmssInstance cmdlet starts a manual upgrade of the specified Virtual Machine Scale Set (VMSS) instance.</span></span>
<span data-ttu-id="0e72b-107">Ta funkcja jest używana, gdy w ustawieniach skali VMSS ustawiono wartość ręcznie.</span><span class="sxs-lookup"><span data-stu-id="0e72b-107">This is used when the upgrade policy on the VMSS Scale Set is set to manual.</span></span>

## <span data-ttu-id="0e72b-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0e72b-108">EXAMPLES</span></span>

### <span data-ttu-id="0e72b-109">Przykład 1. Rozpocznij uaktualnienie wystąpienia programu VMSS</span><span class="sxs-lookup"><span data-stu-id="0e72b-109">Example 1: Start an upgrade of the VMSS instance</span></span>
```
PS C:\> Update-AzureRmVmssInstance -ResourceGroupName "Group011" -VMScaleSetName "VMScaleSet001" -InstanceId "0"
```

<span data-ttu-id="0e72b-110">To polecenie rozpoczyna uaktualnienie VMSS o nazwie VMScaleSet001 o IDENTYFIKATORze wystąpienia 0.</span><span class="sxs-lookup"><span data-stu-id="0e72b-110">This command starts an upgrade of the VMSS named VMScaleSet001 that has the instance ID of 0.</span></span>

## <span data-ttu-id="0e72b-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0e72b-111">PARAMETERS</span></span>

### <span data-ttu-id="0e72b-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0e72b-112">-AsJob</span></span>
<span data-ttu-id="0e72b-113">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="0e72b-113">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e72b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e72b-114">-DefaultProfile</span></span>
<span data-ttu-id="0e72b-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0e72b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e72b-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="0e72b-116">-InstanceId</span></span>
<span data-ttu-id="0e72b-117">Określa, jako tablicę ciągów, identyfikator lub identyfikatory wystąpienia, które ma zostać uaktualnione.</span><span class="sxs-lookup"><span data-stu-id="0e72b-117">Specifies, as a string array, the ID or IDs of the instance to upgrade.</span></span>

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

### <span data-ttu-id="0e72b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e72b-118">-ResourceGroupName</span></span>
<span data-ttu-id="0e72b-119">Określa nazwę grupy zasobów VMSS.</span><span class="sxs-lookup"><span data-stu-id="0e72b-119">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="0e72b-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="0e72b-120">-VMScaleSetName</span></span>
<span data-ttu-id="0e72b-121">Określa nazwę wystąpienia VMSS, które to polecenie cmdlet jest uaktualniane.</span><span class="sxs-lookup"><span data-stu-id="0e72b-121">Specifies the name of the VMSS instance that this cmdlet upgrades.</span></span>

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

### <span data-ttu-id="0e72b-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0e72b-122">-Confirm</span></span>
<span data-ttu-id="0e72b-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e72b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e72b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e72b-124">-WhatIf</span></span>
<span data-ttu-id="0e72b-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e72b-125">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="0e72b-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0e72b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e72b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e72b-127">CommonParameters</span></span>
<span data-ttu-id="0e72b-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e72b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e72b-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e72b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e72b-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0e72b-130">INPUTS</span></span>

### <span data-ttu-id="0e72b-131">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="0e72b-131">None</span></span>
<span data-ttu-id="0e72b-132">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="0e72b-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0e72b-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0e72b-133">OUTPUTS</span></span>

###  
<span data-ttu-id="0e72b-134">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="0e72b-134">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="0e72b-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0e72b-135">NOTES</span></span>

## <span data-ttu-id="0e72b-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0e72b-136">RELATED LINKS</span></span>

[<span data-ttu-id="0e72b-137">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0e72b-137">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


