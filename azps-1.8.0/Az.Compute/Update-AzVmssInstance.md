---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E8C9D68E-7C68-43D0-B348-72E9713CB99F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmssinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssInstance.md
ms.openlocfilehash: b4be578734dc712a6dcb3b8362621d2521261a11
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868827"
---
# <span data-ttu-id="3d722-101">Update-AzVmssInstance</span><span class="sxs-lookup"><span data-stu-id="3d722-101">Update-AzVmssInstance</span></span>

## <span data-ttu-id="3d722-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3d722-102">SYNOPSIS</span></span>
<span data-ttu-id="3d722-103">Rozpoczyna ręczne uaktualnienie wystąpienia usługi VMSS.</span><span class="sxs-lookup"><span data-stu-id="3d722-103">Starts a manual upgrade of the VMSS instance.</span></span>

## <span data-ttu-id="3d722-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3d722-104">SYNTAX</span></span>

```
Update-AzVmssInstance [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d722-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3d722-105">DESCRIPTION</span></span>
<span data-ttu-id="3d722-106">Polecenie cmdlet Update-AzVmssInstance rozpoczyna ręczne uaktualnianie określonego wystąpienia zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="3d722-106">The Update-AzVmssInstance cmdlet starts a manual upgrade of the specified Virtual Machine Scale Set (VMSS) instance.</span></span>
<span data-ttu-id="3d722-107">Ta funkcja jest używana, gdy w ustawieniach skali VMSS ustawiono wartość ręcznie.</span><span class="sxs-lookup"><span data-stu-id="3d722-107">This is used when the upgrade policy on the VMSS Scale Set is set to manual.</span></span>

## <span data-ttu-id="3d722-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3d722-108">EXAMPLES</span></span>

### <span data-ttu-id="3d722-109">Przykład 1. Rozpocznij uaktualnienie wystąpienia programu VMSS</span><span class="sxs-lookup"><span data-stu-id="3d722-109">Example 1: Start an upgrade of the VMSS instance</span></span>
```
PS C:\> Update-AzVmssInstance -ResourceGroupName "Group011" -VMScaleSetName "VMScaleSet001" -InstanceId "0"
```

<span data-ttu-id="3d722-110">To polecenie rozpoczyna uaktualnienie VMSS o nazwie VMScaleSet001 o IDENTYFIKATORze wystąpienia 0.</span><span class="sxs-lookup"><span data-stu-id="3d722-110">This command starts an upgrade of the VMSS named VMScaleSet001 that has the instance ID of 0.</span></span>

## <span data-ttu-id="3d722-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3d722-111">PARAMETERS</span></span>

### <span data-ttu-id="3d722-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3d722-112">-AsJob</span></span>
<span data-ttu-id="3d722-113">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="3d722-113">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d722-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d722-114">-DefaultProfile</span></span>
<span data-ttu-id="3d722-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3d722-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d722-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="3d722-116">-InstanceId</span></span>
<span data-ttu-id="3d722-117">Określa, jako tablicę ciągów, identyfikator lub identyfikatory wystąpienia, które ma zostać uaktualnione.</span><span class="sxs-lookup"><span data-stu-id="3d722-117">Specifies, as a string array, the ID or IDs of the instance to upgrade.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d722-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d722-118">-ResourceGroupName</span></span>
<span data-ttu-id="3d722-119">Określa nazwę grupy zasobów VMSS.</span><span class="sxs-lookup"><span data-stu-id="3d722-119">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="3d722-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="3d722-120">-VMScaleSetName</span></span>
<span data-ttu-id="3d722-121">Określa nazwę wystąpienia VMSS, które to polecenie cmdlet jest uaktualniane.</span><span class="sxs-lookup"><span data-stu-id="3d722-121">Specifies the name of the VMSS instance that this cmdlet upgrades.</span></span>

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

### <span data-ttu-id="3d722-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3d722-122">-Confirm</span></span>
<span data-ttu-id="3d722-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d722-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d722-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d722-124">-WhatIf</span></span>
<span data-ttu-id="3d722-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d722-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d722-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3d722-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d722-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d722-127">CommonParameters</span></span>
<span data-ttu-id="3d722-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d722-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d722-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d722-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d722-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3d722-130">INPUTS</span></span>

### <span data-ttu-id="3d722-131">System. String</span><span class="sxs-lookup"><span data-stu-id="3d722-131">System.String</span></span>

### <span data-ttu-id="3d722-132">System. String []</span><span class="sxs-lookup"><span data-stu-id="3d722-132">System.String[]</span></span>

## <span data-ttu-id="3d722-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3d722-133">OUTPUTS</span></span>

### <span data-ttu-id="3d722-134">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="3d722-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="3d722-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3d722-135">NOTES</span></span>

## <span data-ttu-id="3d722-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3d722-136">RELATED LINKS</span></span>

[<span data-ttu-id="3d722-137">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="3d722-137">Update-AzVmss</span></span>](./Update-AzVmss.md)


