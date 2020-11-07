---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/start-azurermvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Start-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Start-AzureRmVM.md
ms.openlocfilehash: 121d9353baaa10058e101d3f8a7d398f345052ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718354"
---
# <span data-ttu-id="3cf81-101">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3cf81-101">Start-AzureRmVM</span></span>

## <span data-ttu-id="3cf81-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3cf81-102">SYNOPSIS</span></span>
<span data-ttu-id="3cf81-103">Rozpoczynanie maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3cf81-103">Starts an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3cf81-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3cf81-104">SYNTAX</span></span>

### <span data-ttu-id="3cf81-105">ResourceGroupNameParameterSetName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3cf81-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzureRmVM [-Name] <String> [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cf81-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="3cf81-106">IdParameterSetName</span></span>
```
Start-AzureRmVM [-Name] <String> [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cf81-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3cf81-107">DESCRIPTION</span></span>
<span data-ttu-id="3cf81-108">Polecenie cmdlet **Start-AzureRmVM** rozpoczyna działanie maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3cf81-108">The **Start-AzureRmVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="3cf81-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3cf81-109">EXAMPLES</span></span>

### <span data-ttu-id="3cf81-110">Przykład 1. uruchomienie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="3cf81-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="3cf81-111">To polecenie umożliwia uruchomienie maszyny wirtualnej o nazwie VirtualMachine07 w ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="3cf81-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="3cf81-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3cf81-112">PARAMETERS</span></span>

### <span data-ttu-id="3cf81-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3cf81-113">-AsJob</span></span>
<span data-ttu-id="3cf81-114">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="3cf81-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="3cf81-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cf81-115">-DefaultProfile</span></span>
<span data-ttu-id="3cf81-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3cf81-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3cf81-117">-ID</span><span class="sxs-lookup"><span data-stu-id="3cf81-117">-Id</span></span>
<span data-ttu-id="3cf81-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3cf81-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cf81-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3cf81-119">-Name</span></span>
<span data-ttu-id="3cf81-120">Nazwa maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3cf81-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="3cf81-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cf81-121">-ResourceGroupName</span></span>
<span data-ttu-id="3cf81-122">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3cf81-122">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cf81-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3cf81-123">-Confirm</span></span>
<span data-ttu-id="3cf81-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cf81-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cf81-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cf81-125">-WhatIf</span></span>
<span data-ttu-id="3cf81-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cf81-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3cf81-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3cf81-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cf81-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cf81-128">CommonParameters</span></span>
<span data-ttu-id="3cf81-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cf81-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cf81-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cf81-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cf81-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3cf81-131">INPUTS</span></span>

### <span data-ttu-id="3cf81-132">System. String</span><span class="sxs-lookup"><span data-stu-id="3cf81-132">System.String</span></span>

## <span data-ttu-id="3cf81-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3cf81-133">OUTPUTS</span></span>

### <span data-ttu-id="3cf81-134">Microsoft. Azure. Commands. COMPUTE. models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="3cf81-134">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="3cf81-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3cf81-135">NOTES</span></span>

## <span data-ttu-id="3cf81-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3cf81-136">RELATED LINKS</span></span>

[<span data-ttu-id="3cf81-137">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3cf81-137">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="3cf81-138">Nowe — AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3cf81-138">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="3cf81-139">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3cf81-139">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="3cf81-140">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3cf81-140">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="3cf81-141">Zatrzymaj — AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3cf81-141">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="3cf81-142">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3cf81-142">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


