---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 47F0EE55-78C0-4C71-BD32-C7CB7B200DC3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Restart-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Restart-AzureRmVmss.md
ms.openlocfilehash: 479aaf61169cb09d8561e9f09b05a5852c93b58d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525617"
---
# <span data-ttu-id="2093e-101">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2093e-101">Restart-AzureRmVmss</span></span>

## <span data-ttu-id="2093e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2093e-102">SYNOPSIS</span></span>
<span data-ttu-id="2093e-103">Ponowne uruchomienie VMSS lub maszyny wirtualnej w VMSS.</span><span class="sxs-lookup"><span data-stu-id="2093e-103">Restarts the VMSS or a virtual machine within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2093e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2093e-104">SYNTAX</span></span>

```
Restart-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2093e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2093e-105">DESCRIPTION</span></span>
<span data-ttu-id="2093e-106">Polecenie cmdlet **restart-AzureRmVmss** powoduje ponowne uruchomienie zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="2093e-106">The **Restart-AzureRmVmss** cmdlet restarts the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="2093e-107">Tego polecenia cmdlet można również użyć w celu ponownego uruchomienia określonej maszyny wirtualnej w VMSS przy użyciu parametru *InstanceId* .</span><span class="sxs-lookup"><span data-stu-id="2093e-107">This cmdlet can also be used to restart a specific virtual machine inside the VMSS by using the *InstanceId* parameter.</span></span>

## <span data-ttu-id="2093e-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2093e-108">EXAMPLES</span></span>

### <span data-ttu-id="2093e-109">Przykład 1. Uruchom ponownie VMSS</span><span class="sxs-lookup"><span data-stu-id="2093e-109">Example 1: Restart the VMSS</span></span>
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001";
```

<span data-ttu-id="2093e-110">To polecenie uruchamia ponownie VMSS o nazwie VMSS001 należącej do grupy zasobów o nazwie Group001.</span><span class="sxs-lookup"><span data-stu-id="2093e-110">This command restarts the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="2093e-111">Przykład 2: ponowne uruchomienie określonej maszyny wirtualnej w obrębie VMSS</span><span class="sxs-lookup"><span data-stu-id="2093e-111">Example 2: Restart a specific virtual machine within the VMSS</span></span>
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group004" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="2093e-112">To polecenie powoduje ponowne uruchomienie maszyny wirtualnej o IDENTYFIKATORze wystąpienia 1 w VMSS o nazwie VMSS001 należącej do grupy zasobów o nazwie Group001.</span><span class="sxs-lookup"><span data-stu-id="2093e-112">This command restarts a virtual machine that has the instance ID of 1 in the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="2093e-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2093e-113">PARAMETERS</span></span>

### <span data-ttu-id="2093e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2093e-114">-DefaultProfile</span></span>
<span data-ttu-id="2093e-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2093e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2093e-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="2093e-116">-InstanceId</span></span>
<span data-ttu-id="2093e-117">Określa jako tablicę ciągów identyfikator wystąpień, które muszą być ponownie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2093e-117">Specifies, as a string array, the ID of the instances that need restarted.</span></span>

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

### <span data-ttu-id="2093e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2093e-118">-ResourceGroupName</span></span>
<span data-ttu-id="2093e-119">Określa nazwę grupy zasobów VMSS.</span><span class="sxs-lookup"><span data-stu-id="2093e-119">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="2093e-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="2093e-120">-VMScaleSetName</span></span>
<span data-ttu-id="2093e-121">Gatunek nazwa VMSS, które zostanie ponownie rozuruchamiane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2093e-121">Species the name of the VMSS that this cmdlet restarts.</span></span>

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

### <span data-ttu-id="2093e-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2093e-122">-Confirm</span></span>
<span data-ttu-id="2093e-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2093e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2093e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2093e-124">-WhatIf</span></span>
<span data-ttu-id="2093e-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2093e-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2093e-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2093e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2093e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2093e-127">CommonParameters</span></span>
<span data-ttu-id="2093e-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2093e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2093e-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2093e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2093e-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2093e-130">INPUTS</span></span>

## <span data-ttu-id="2093e-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2093e-131">OUTPUTS</span></span>

###  
<span data-ttu-id="2093e-132">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="2093e-132">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="2093e-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2093e-133">NOTES</span></span>

## <span data-ttu-id="2093e-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2093e-134">RELATED LINKS</span></span>

[<span data-ttu-id="2093e-135">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2093e-135">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="2093e-136">Nowe — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2093e-136">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="2093e-137">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2093e-137">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="2093e-138">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2093e-138">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="2093e-139">Start — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2093e-139">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="2093e-140">Zatrzymaj — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2093e-140">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="2093e-141">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2093e-141">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


