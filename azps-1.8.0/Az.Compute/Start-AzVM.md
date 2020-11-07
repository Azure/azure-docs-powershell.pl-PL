---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
ms.openlocfilehash: 84e24bdcd69a3100e3030e6d1947240494aea8e3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710181"
---
# <span data-ttu-id="47b9a-101">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="47b9a-101">Start-AzVM</span></span>

## <span data-ttu-id="47b9a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="47b9a-102">SYNOPSIS</span></span>
<span data-ttu-id="47b9a-103">Rozpoczynanie maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="47b9a-103">Starts an Azure virtual machine.</span></span>

## <span data-ttu-id="47b9a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="47b9a-104">SYNTAX</span></span>

### <span data-ttu-id="47b9a-105">ResourceGroupNameParameterSetName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="47b9a-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzVM [-Name] <String> [-ResourceGroupName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47b9a-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="47b9a-106">IdParameterSetName</span></span>
```
Start-AzVM [[-Name] <String>] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47b9a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="47b9a-107">DESCRIPTION</span></span>
<span data-ttu-id="47b9a-108">Polecenie cmdlet **Start-AzVM** rozpoczyna działanie maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="47b9a-108">The **Start-AzVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="47b9a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="47b9a-109">EXAMPLES</span></span>

### <span data-ttu-id="47b9a-110">Przykład 1. uruchomienie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="47b9a-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="47b9a-111">To polecenie umożliwia uruchomienie maszyny wirtualnej o nazwie VirtualMachine07 w ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="47b9a-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="47b9a-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="47b9a-112">PARAMETERS</span></span>

### <span data-ttu-id="47b9a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47b9a-113">-AsJob</span></span>
<span data-ttu-id="47b9a-114">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="47b9a-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="47b9a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47b9a-115">-DefaultProfile</span></span>
<span data-ttu-id="47b9a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="47b9a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47b9a-117">-ID</span><span class="sxs-lookup"><span data-stu-id="47b9a-117">-Id</span></span>
<span data-ttu-id="47b9a-118">Identyfikator maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="47b9a-118">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="47b9a-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="47b9a-119">-Name</span></span>
<span data-ttu-id="47b9a-120">Nazwa maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="47b9a-120">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47b9a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47b9a-121">-ResourceGroupName</span></span>
<span data-ttu-id="47b9a-122">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="47b9a-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="47b9a-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="47b9a-123">-Confirm</span></span>
<span data-ttu-id="47b9a-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47b9a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47b9a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47b9a-125">-WhatIf</span></span>
<span data-ttu-id="47b9a-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47b9a-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="47b9a-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="47b9a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47b9a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47b9a-128">CommonParameters</span></span>
<span data-ttu-id="47b9a-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47b9a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47b9a-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47b9a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47b9a-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="47b9a-131">INPUTS</span></span>

### <span data-ttu-id="47b9a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="47b9a-132">System.String</span></span>

## <span data-ttu-id="47b9a-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="47b9a-133">OUTPUTS</span></span>

### <span data-ttu-id="47b9a-134">Microsoft. Azure. Commands. COMPUTE. models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="47b9a-134">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="47b9a-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="47b9a-135">NOTES</span></span>

## <span data-ttu-id="47b9a-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="47b9a-136">RELATED LINKS</span></span>

[<span data-ttu-id="47b9a-137">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="47b9a-137">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="47b9a-138">Nowe — AzVM</span><span class="sxs-lookup"><span data-stu-id="47b9a-138">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="47b9a-139">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="47b9a-139">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="47b9a-140">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="47b9a-140">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="47b9a-141">Zatrzymaj — AzVM</span><span class="sxs-lookup"><span data-stu-id="47b9a-141">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="47b9a-142">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="47b9a-142">Update-AzVM</span></span>](./Update-AzVM.md)


