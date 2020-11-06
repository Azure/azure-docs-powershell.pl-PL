---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D5943E9F-E4E6-4A1F-A144-44691CF32FC8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDataDisk.md
ms.openlocfilehash: 774166f88e4ca94e5e21c2b96817596c082a429c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525662"
---
# <span data-ttu-id="7c565-101">Remove-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="7c565-101">Remove-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="7c565-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7c565-102">SYNOPSIS</span></span>
<span data-ttu-id="7c565-103">Usuwa dysk danych z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7c565-103">Removes a data disk from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c565-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7c565-104">SYNTAX</span></span>

```
Remove-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-DataDiskNames] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c565-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7c565-105">DESCRIPTION</span></span>
<span data-ttu-id="7c565-106">Polecenie cmdlet **Remove-AzureRmVMDataDisk** usuwa dysk danych z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7c565-106">The **Remove-AzureRmVMDataDisk** cmdlet removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="7c565-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7c565-107">EXAMPLES</span></span>

### <span data-ttu-id="7c565-108">Przykład 1: usuwanie dysku danych z maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="7c565-108">Example 1: Remove a data disk from a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" 
PS C:\> Remove-AzureRmVMDataDisk -VM $VirtualMachine -Name "Disk3"
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="7c565-109">Pierwsze polecenie uzyskuje maszynę wirtualną o nazwie VirtualMachine07 przy użyciu polecenia cmdlet **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="7c565-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="7c565-110">Polecenie zapisuje maszynę wirtualną w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="7c565-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="7c565-111">Drugie polecenie usuwa dysk danych o nazwie disk3 z maszyny wirtualnej przechowywanej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="7c565-111">The second command removes the data disk named Disk3 from the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="7c565-112">Polecenie ostatnie umożliwia zaktualizowanie stanu maszyny wirtualnej przechowywanej w $VirtualMachine w programie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="7c565-112">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="7c565-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7c565-113">PARAMETERS</span></span>

### <span data-ttu-id="7c565-114">-DataDiskNames</span><span class="sxs-lookup"><span data-stu-id="7c565-114">-DataDiskNames</span></span>
<span data-ttu-id="7c565-115">Określa nazwy jednego lub kilku dysków danych, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c565-115">Specifies the names of one or more data disks that this cmdlet removes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c565-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c565-116">-DefaultProfile</span></span>
<span data-ttu-id="7c565-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7c565-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c565-118">-VM</span><span class="sxs-lookup"><span data-stu-id="7c565-118">-VM</span></span>
<span data-ttu-id="7c565-119">Określa lokalny obiekt maszyny wirtualnej, z którego ma zostać usunięty dysk danych.</span><span class="sxs-lookup"><span data-stu-id="7c565-119">Specifies the local virtual machine object from which to remove a data disk.</span></span>
<span data-ttu-id="7c565-120">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="7c565-120">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c565-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7c565-121">-Confirm</span></span>
<span data-ttu-id="7c565-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c565-122">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="7c565-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c565-123">-WhatIf</span></span>
<span data-ttu-id="7c565-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c565-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7c565-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7c565-125">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="7c565-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c565-126">CommonParameters</span></span>
<span data-ttu-id="7c565-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c565-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c565-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c565-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c565-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7c565-129">INPUTS</span></span>

## <span data-ttu-id="7c565-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7c565-130">OUTPUTS</span></span>

## <span data-ttu-id="7c565-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7c565-131">NOTES</span></span>

## <span data-ttu-id="7c565-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7c565-132">RELATED LINKS</span></span>

[<span data-ttu-id="7c565-133">Dodaj-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="7c565-133">Add-AzureRmVMDataDisk</span></span>](./Add-AzureRmVMDataDisk.md)

[<span data-ttu-id="7c565-134">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7c565-134">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


