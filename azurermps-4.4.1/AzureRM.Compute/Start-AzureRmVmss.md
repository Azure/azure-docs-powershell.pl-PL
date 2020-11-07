---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Start-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Start-AzureRmVmss.md
ms.openlocfilehash: 6b3291a77f7c69372124b8c0de2ba78c8810f02b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717598"
---
# <span data-ttu-id="92a42-101">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="92a42-101">Start-AzureRmVmss</span></span>

## <span data-ttu-id="92a42-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="92a42-102">SYNOPSIS</span></span>
<span data-ttu-id="92a42-103">Uruchamia VMSS lub zestaw maszyn wirtualnych w VMSS.</span><span class="sxs-lookup"><span data-stu-id="92a42-103">Starts the VMSS or a set of virtual machines within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92a42-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="92a42-104">SYNTAX</span></span>

```
Start-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92a42-105">Opis</span><span class="sxs-lookup"><span data-stu-id="92a42-105">DESCRIPTION</span></span>
<span data-ttu-id="92a42-106">Polecenie cmdlet **Start-AzureRmVmss** uruchamia wszystkie maszyny wirtualne w zestawie skali maszyny wirtualnej (VMSS) lub zestaw maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="92a42-106">The **Start-AzureRmVmss** cmdlet starts all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="92a42-107">W celu wybrania zestawu maszyn wirtualnych można użyć parametru *InstanceId* .</span><span class="sxs-lookup"><span data-stu-id="92a42-107">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="92a42-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="92a42-108">EXAMPLES</span></span>

### <span data-ttu-id="92a42-109">Przykład 1. Uruchom określony zestaw maszyn wirtualnych w VMSS</span><span class="sxs-lookup"><span data-stu-id="92a42-109">Example 1: Start a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

<span data-ttu-id="92a42-110">To polecenie umożliwia uruchomienie określonego zestawu maszyn wirtualnych określonego przez tablicę ciągów identyfikatora wystąpienia, która należy do VMSS o nazwie ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="92a42-110">This command starts a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="92a42-111">Przykład 2: uruchamianie wszystkich maszyn wirtualnych w ramach VMSS</span><span class="sxs-lookup"><span data-stu-id="92a42-111">Example 2: Start all virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="92a42-112">To polecenie umożliwia uruchomienie wszystkich maszyn wirtualnych należących do VMSS o nazwie ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="92a42-112">This command starts all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="92a42-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="92a42-113">PARAMETERS</span></span>

### <span data-ttu-id="92a42-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92a42-114">-DefaultProfile</span></span>
<span data-ttu-id="92a42-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="92a42-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92a42-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="92a42-116">-InstanceId</span></span>
<span data-ttu-id="92a42-117">Określa, jako tablicę ciągów, identyfikator lub identyfikatory wystąpień, które uruchamia polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92a42-117">Specifies, as a string array, the ID or IDs of the instances that cmdlet starts.</span></span>
<span data-ttu-id="92a42-118">Na przykład: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="92a42-118">For instance: `-InstanceId "0", "3"`</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92a42-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92a42-119">-ResourceGroupName</span></span>
<span data-ttu-id="92a42-120">Określa nazwę grupy zasobów VMSS.</span><span class="sxs-lookup"><span data-stu-id="92a42-120">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="92a42-121">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="92a42-121">-VMScaleSetName</span></span>
<span data-ttu-id="92a42-122">Określa nazwę VMSS, którą to polecenie cmdlet uruchamia maszyny wirtualne.</span><span class="sxs-lookup"><span data-stu-id="92a42-122">Specifies the name of the VMSS that this cmdlet starts the virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92a42-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="92a42-123">-Confirm</span></span>
<span data-ttu-id="92a42-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92a42-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92a42-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92a42-125">-WhatIf</span></span>
<span data-ttu-id="92a42-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92a42-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="92a42-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="92a42-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92a42-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92a42-128">CommonParameters</span></span>
<span data-ttu-id="92a42-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92a42-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92a42-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92a42-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92a42-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="92a42-131">INPUTS</span></span>

## <span data-ttu-id="92a42-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="92a42-132">OUTPUTS</span></span>

###  
<span data-ttu-id="92a42-133">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="92a42-133">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="92a42-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="92a42-134">NOTES</span></span>

## <span data-ttu-id="92a42-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="92a42-135">RELATED LINKS</span></span>

[<span data-ttu-id="92a42-136">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="92a42-136">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="92a42-137">Nowe — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="92a42-137">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="92a42-138">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="92a42-138">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="92a42-139">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="92a42-139">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="92a42-140">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="92a42-140">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="92a42-141">Zatrzymaj — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="92a42-141">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="92a42-142">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="92a42-142">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


