---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmss.md
ms.openlocfilehash: b3e9f2608703eebd5ad24846aad7b5a1ad11e8ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553007"
---
# <span data-ttu-id="951df-101">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="951df-101">Get-AzureRmVmss</span></span>

## <span data-ttu-id="951df-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="951df-102">SYNOPSIS</span></span>
<span data-ttu-id="951df-103">Pobiera właściwości VMSS.</span><span class="sxs-lookup"><span data-stu-id="951df-103">Gets the properties of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="951df-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="951df-104">SYNTAX</span></span>

### <span data-ttu-id="951df-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="951df-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [<CommonParameters>]
```

### <span data-ttu-id="951df-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="951df-106">FriendMethod</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [<CommonParameters>]
```

## <span data-ttu-id="951df-107">Opis</span><span class="sxs-lookup"><span data-stu-id="951df-107">DESCRIPTION</span></span>
<span data-ttu-id="951df-108">Polecenie cmdlet **Get-AzureRmVmss** umożliwia wyświetlenie modelu i widoku wystąpienia zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="951df-108">The **Get-AzureRmVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="951df-109">Widok modelu to określone przez użytkownika właściwości maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="951df-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="951df-110">Widok wystąpienia jest stanem poziomu wystąpienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="951df-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="951df-111">Określ parametr *status* , aby uzyskać dostęp tylko do widoku wystąpienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="951df-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="951df-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="951df-112">EXAMPLES</span></span>

### <span data-ttu-id="951df-113">Przykład 1: uzyskiwanie właściwości VMSS</span><span class="sxs-lookup"><span data-stu-id="951df-113">Example 1: Get the properties of a VMSS</span></span>
```
PS C:\> Get-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="951df-114">To polecenie pobiera właściwości VMSS o nazwie VMSS001 należące do grupy zasobów o nazwie Group001.</span><span class="sxs-lookup"><span data-stu-id="951df-114">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="951df-115">Ponieważ polecenie nie określa parametru przełącznika *InstanceView* , funkcja cmdlet pobiera widok modelu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="951df-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

## <span data-ttu-id="951df-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="951df-116">PARAMETERS</span></span>

### <span data-ttu-id="951df-117">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="951df-117">-InstanceView</span></span>
<span data-ttu-id="951df-118">Wskazuje, że ten aplet polecenia pobiera tylko widok wystąpienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="951df-118">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="951df-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="951df-119">-ResourceGroupName</span></span>
<span data-ttu-id="951df-120">Określa nazwę grupy zasobów VMSS.</span><span class="sxs-lookup"><span data-stu-id="951df-120">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="951df-121">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="951df-121">-VMScaleSetName</span></span>
<span data-ttu-id="951df-122">Gatunek nazwy VMSS.</span><span class="sxs-lookup"><span data-stu-id="951df-122">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="951df-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="951df-123">CommonParameters</span></span>
<span data-ttu-id="951df-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="951df-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="951df-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="951df-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="951df-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="951df-126">INPUTS</span></span>

### <span data-ttu-id="951df-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="951df-127">None</span></span>
<span data-ttu-id="951df-128">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="951df-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="951df-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="951df-129">OUTPUTS</span></span>

### <span data-ttu-id="951df-130">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="951df-130">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="951df-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="951df-131">NOTES</span></span>

## <span data-ttu-id="951df-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="951df-132">RELATED LINKS</span></span>

[<span data-ttu-id="951df-133">Nowe — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="951df-133">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="951df-134">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="951df-134">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="951df-135">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="951df-135">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="951df-136">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="951df-136">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="951df-137">Start — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="951df-137">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="951df-138">Zatrzymaj — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="951df-138">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="951df-139">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="951df-139">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


