---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVmss.md
ms.openlocfilehash: 22e281d7aa6e2d71506ddb616f96a149dcff6068
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893706"
---
# <span data-ttu-id="8dd93-101">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8dd93-101">Get-AzVmss</span></span>

## <span data-ttu-id="8dd93-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8dd93-102">SYNOPSIS</span></span>
<span data-ttu-id="8dd93-103">Pobiera właściwości VMSS.</span><span class="sxs-lookup"><span data-stu-id="8dd93-103">Gets the properties of a VMSS.</span></span>

## <span data-ttu-id="8dd93-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8dd93-104">SYNTAX</span></span>

### <span data-ttu-id="8dd93-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8dd93-105">DefaultParameter (Default)</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8dd93-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="8dd93-106">FriendMethod</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8dd93-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8dd93-107">DESCRIPTION</span></span>
<span data-ttu-id="8dd93-108">Polecenie cmdlet **Get-AzVmss** umożliwia wyświetlenie modelu i widoku wystąpienia zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="8dd93-108">The **Get-AzVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="8dd93-109">Widok modelu to określone przez użytkownika właściwości maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8dd93-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="8dd93-110">Widok wystąpienia jest stanem poziomu wystąpienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8dd93-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="8dd93-111">Określ parametr *status* , aby uzyskać dostęp tylko do widoku wystąpienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8dd93-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="8dd93-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8dd93-112">EXAMPLES</span></span>

### <span data-ttu-id="8dd93-113">Przykład 1: uzyskiwanie właściwości VMSS</span><span class="sxs-lookup"><span data-stu-id="8dd93-113">Example 1: Get the properties of a VMSS</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="8dd93-114">To polecenie pobiera właściwości VMSS o nazwie VMSS001 należące do grupy zasobów o nazwie Group001.</span><span class="sxs-lookup"><span data-stu-id="8dd93-114">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="8dd93-115">Ponieważ polecenie nie określa parametru przełącznika *InstanceView* , funkcja cmdlet pobiera widok modelu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8dd93-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

## <span data-ttu-id="8dd93-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8dd93-116">PARAMETERS</span></span>

### <span data-ttu-id="8dd93-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dd93-117">-DefaultProfile</span></span>
<span data-ttu-id="8dd93-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8dd93-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8dd93-119">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="8dd93-119">-InstanceView</span></span>
<span data-ttu-id="8dd93-120">Wskazuje, że ten aplet polecenia pobiera tylko widok wystąpienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8dd93-120">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dd93-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dd93-121">-ResourceGroupName</span></span>
<span data-ttu-id="8dd93-122">Określa nazwę grupy zasobów VMSS.</span><span class="sxs-lookup"><span data-stu-id="8dd93-122">Specifies the name of the Resource Group of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dd93-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="8dd93-123">-VMScaleSetName</span></span>
<span data-ttu-id="8dd93-124">Gatunek nazwy VMSS.</span><span class="sxs-lookup"><span data-stu-id="8dd93-124">Species the name of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dd93-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dd93-125">CommonParameters</span></span>
<span data-ttu-id="8dd93-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8dd93-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dd93-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8dd93-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dd93-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8dd93-128">INPUTS</span></span>

### <span data-ttu-id="8dd93-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="8dd93-129">None</span></span>
<span data-ttu-id="8dd93-130">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="8dd93-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8dd93-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8dd93-131">OUTPUTS</span></span>

### <span data-ttu-id="8dd93-132">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="8dd93-132">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="8dd93-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8dd93-133">NOTES</span></span>

## <span data-ttu-id="8dd93-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8dd93-134">RELATED LINKS</span></span>

[<span data-ttu-id="8dd93-135">Nowe — AzVmss</span><span class="sxs-lookup"><span data-stu-id="8dd93-135">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="8dd93-136">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8dd93-136">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="8dd93-137">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8dd93-137">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="8dd93-138">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8dd93-138">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="8dd93-139">Start — AzVmss</span><span class="sxs-lookup"><span data-stu-id="8dd93-139">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="8dd93-140">Zatrzymaj — AzVmss</span><span class="sxs-lookup"><span data-stu-id="8dd93-140">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="8dd93-141">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8dd93-141">Update-AzVmss</span></span>](./Update-AzVmss.md)


