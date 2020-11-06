---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Restart-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Restart-AzureRmVM.md
ms.openlocfilehash: 5a848c2e4a13df6a38c67e067531ff8581bd595e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525621"
---
# <span data-ttu-id="b9a0d-101">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b9a0d-101">Restart-AzureRmVM</span></span>

## <span data-ttu-id="b9a0d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b9a0d-102">SYNOPSIS</span></span>
<span data-ttu-id="b9a0d-103">Ponowne uruchamianie maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b9a0d-103">Restarts an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9a0d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b9a0d-104">SYNTAX</span></span>

### <span data-ttu-id="b9a0d-105">RestartResourceGroupNameParameterSetName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b9a0d-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9a0d-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="b9a0d-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9a0d-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="b9a0d-107">RestartIdParameterSetName</span></span>
```
Restart-AzureRmVM [-Id] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9a0d-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="b9a0d-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzureRmVM [-Id] <String> [-Name] <String> [-PerformMaintenance]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9a0d-109">Opis</span><span class="sxs-lookup"><span data-stu-id="b9a0d-109">DESCRIPTION</span></span>
<span data-ttu-id="b9a0d-110">Polecenie cmdlet **restart-AzureRmVM** powoduje ponowne uruchomienie maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b9a0d-110">The **Restart-AzureRmVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="b9a0d-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b9a0d-111">EXAMPLES</span></span>

### <span data-ttu-id="b9a0d-112">Przykład 1: ponowne uruchomienie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="b9a0d-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="b9a0d-113">To polecenie powoduje ponowne uruchomienie maszyny wirtualnej o nazwie VirtualMachine07 w ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="b9a0d-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="b9a0d-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b9a0d-114">PARAMETERS</span></span>

### <span data-ttu-id="b9a0d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9a0d-115">-DefaultProfile</span></span>
<span data-ttu-id="b9a0d-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b9a0d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9a0d-117">-ID</span><span class="sxs-lookup"><span data-stu-id="b9a0d-117">-Id</span></span>
<span data-ttu-id="b9a0d-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b9a0d-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartIdParameterSetName, PerformMaintenanceIdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9a0d-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b9a0d-119">-Name</span></span>
<span data-ttu-id="b9a0d-120">Nazwa maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b9a0d-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="b9a0d-121">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="b9a0d-121">-PerformMaintenance</span></span>
<span data-ttu-id="b9a0d-122">Aby przeprowadzić konserwację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b9a0d-122">To perform the maintenance of virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PerformMaintenanceResourceGroupNameParameterSetName, PerformMaintenanceIdParameterSetName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9a0d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9a0d-123">-ResourceGroupName</span></span>
<span data-ttu-id="b9a0d-124">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b9a0d-124">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartResourceGroupNameParameterSetName, PerformMaintenanceResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9a0d-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b9a0d-125">-Confirm</span></span>
<span data-ttu-id="b9a0d-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9a0d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9a0d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9a0d-127">-WhatIf</span></span>
<span data-ttu-id="b9a0d-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9a0d-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b9a0d-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b9a0d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9a0d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9a0d-130">CommonParameters</span></span>
<span data-ttu-id="b9a0d-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9a0d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9a0d-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9a0d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9a0d-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b9a0d-133">INPUTS</span></span>

## <span data-ttu-id="b9a0d-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b9a0d-134">OUTPUTS</span></span>

## <span data-ttu-id="b9a0d-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b9a0d-135">NOTES</span></span>

## <span data-ttu-id="b9a0d-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b9a0d-136">RELATED LINKS</span></span>

[<span data-ttu-id="b9a0d-137">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b9a0d-137">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="b9a0d-138">Nowe — AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b9a0d-138">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="b9a0d-139">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b9a0d-139">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="b9a0d-140">Start — AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b9a0d-140">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="b9a0d-141">Zatrzymaj — AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b9a0d-141">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="b9a0d-142">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b9a0d-142">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


