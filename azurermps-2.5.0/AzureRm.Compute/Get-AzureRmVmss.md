---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmss
schema: 2.0.0
ms.openlocfilehash: ec66d20e0d9a63b8101b1a9a46410c9e64ac2079
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898805"
---
# <span data-ttu-id="c2aa0-101">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c2aa0-101">Get-AzureRmVmss</span></span>

## <span data-ttu-id="c2aa0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c2aa0-102">SYNOPSIS</span></span>
<span data-ttu-id="c2aa0-103">Pobiera właściwości VMSS.</span><span class="sxs-lookup"><span data-stu-id="c2aa0-103">Gets the properties of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2aa0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c2aa0-104">SYNTAX</span></span>

### <span data-ttu-id="c2aa0-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c2aa0-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2aa0-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="c2aa0-106">FriendMethod</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2aa0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c2aa0-107">DESCRIPTION</span></span>
<span data-ttu-id="c2aa0-108">Polecenie cmdlet **Get-AzureRmVmss** umożliwia wyświetlenie modelu i widoku wystąpienia zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="c2aa0-108">The **Get-AzureRmVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="c2aa0-109">Widok modelu to określone przez użytkownika właściwości maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c2aa0-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="c2aa0-110">Widok wystąpienia jest stanem poziomu wystąpienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c2aa0-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="c2aa0-111">Określ parametr *status* , aby uzyskać dostęp tylko do widoku wystąpienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c2aa0-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="c2aa0-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c2aa0-112">EXAMPLES</span></span>

### <span data-ttu-id="c2aa0-113">Przykład 1: uzyskiwanie właściwości VMSS</span><span class="sxs-lookup"><span data-stu-id="c2aa0-113">Example 1: Get the properties of a VMSS</span></span>
```
PS C:\> Get-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="c2aa0-114">To polecenie pobiera właściwości VMSS o nazwie VMSS001 należące do grupy zasobów o nazwie Group001.</span><span class="sxs-lookup"><span data-stu-id="c2aa0-114">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="c2aa0-115">Ponieważ polecenie nie określa parametru przełącznika *InstanceView* , funkcja cmdlet pobiera widok modelu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c2aa0-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

## <span data-ttu-id="c2aa0-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c2aa0-116">PARAMETERS</span></span>

### <span data-ttu-id="c2aa0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2aa0-117">-DefaultProfile</span></span>
<span data-ttu-id="c2aa0-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c2aa0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2aa0-119">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="c2aa0-119">-InstanceView</span></span>
<span data-ttu-id="c2aa0-120">Wskazuje, że ten aplet polecenia pobiera tylko widok wystąpienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c2aa0-120">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

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

### <span data-ttu-id="c2aa0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2aa0-121">-ResourceGroupName</span></span>
<span data-ttu-id="c2aa0-122">Określa nazwę grupy zasobów VMSS.</span><span class="sxs-lookup"><span data-stu-id="c2aa0-122">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="c2aa0-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="c2aa0-123">-VMScaleSetName</span></span>
<span data-ttu-id="c2aa0-124">Gatunek nazwy VMSS.</span><span class="sxs-lookup"><span data-stu-id="c2aa0-124">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="c2aa0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2aa0-125">CommonParameters</span></span>
<span data-ttu-id="c2aa0-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2aa0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2aa0-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2aa0-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2aa0-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2aa0-128">INPUTS</span></span>

### <span data-ttu-id="c2aa0-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c2aa0-129">None</span></span>
<span data-ttu-id="c2aa0-130">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="c2aa0-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c2aa0-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c2aa0-131">OUTPUTS</span></span>

### <span data-ttu-id="c2aa0-132">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="c2aa0-132">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="c2aa0-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c2aa0-133">NOTES</span></span>

## <span data-ttu-id="c2aa0-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c2aa0-134">RELATED LINKS</span></span>

[<span data-ttu-id="c2aa0-135">Nowe — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c2aa0-135">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="c2aa0-136">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c2aa0-136">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="c2aa0-137">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c2aa0-137">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="c2aa0-138">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c2aa0-138">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="c2aa0-139">Start — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c2aa0-139">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="c2aa0-140">Zatrzymaj — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c2aa0-140">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="c2aa0-141">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c2aa0-141">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


