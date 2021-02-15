---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9C216103-EB77-468E-8684-F5E5400B73A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsssshpublickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSshPublicKey.md
ms.openlocfilehash: 0ba5f9cd618c86eec15eb8b0a02956e5997fc627
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238939"
---
# <span data-ttu-id="14f87-101">Add-AzVmssSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="14f87-101">Add-AzVmssSshPublicKey</span></span>

## <span data-ttu-id="14f87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14f87-102">SYNOPSIS</span></span>
<span data-ttu-id="14f87-103">Dodaje klucze publiczne SSH do usługi maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="14f87-103">Adds SSH public keys to the VMSS.</span></span>

## <span data-ttu-id="14f87-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="14f87-104">SYNTAX</span></span>

```
Add-AzVmssSshPublicKey [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Path] <String>]
 [[-KeyData] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14f87-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="14f87-105">DESCRIPTION</span></span>
<span data-ttu-id="14f87-106">Polecenie cmdlet **Add-AzVmssSshPublicKey** dodaje klucze publiczne, których można używać do łączenia się z maszynami wirtualnymi zestawu skal za pośrednictwem bezpiecznego powłoki (SSH, Secure Shell).</span><span class="sxs-lookup"><span data-stu-id="14f87-106">The **Add-AzVmssSshPublicKey** cmdlet adds the public keys that you can use to connect to the Virtual Machine Scale Set (VMSS) virtual machines over Secure Shell (SSH).</span></span>

## <span data-ttu-id="14f87-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="14f87-107">EXAMPLES</span></span>

### <span data-ttu-id="14f87-108">Przykład 1. Dodawanie klucza publicznego SSH do usługi maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="14f87-108">Example 1: Add an SSH public key to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssSshPublicKey -VirtualMachineScaleSet $VMSS -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="14f87-109">W tym przykładzie dodano klucz publiczny SSH do usług maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="14f87-109">This example adds an SSH public key to the VMSS.</span></span>
<span data-ttu-id="14f87-110">Pierwsze polecenie tworzy obiekt konfiguracji maszyny WIRTUALNEJ za pomocą polecenia cmdlet **New-AzVmssConfig** i zapisuje wynik w zmiennej o nazwie $VMSS.</span><span class="sxs-lookup"><span data-stu-id="14f87-110">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="14f87-111">Drugie polecenie dodaje klawisz SSH z określonymi danymi klucza i przechowuje klucz w określonej ścieżce na komputerze wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="14f87-111">The second command adds an SSH key with the specified key data and stores the key at the specified path on the virtual machine.</span></span>

## <span data-ttu-id="14f87-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14f87-112">PARAMETERS</span></span>

### <span data-ttu-id="14f87-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14f87-113">-DefaultProfile</span></span>
<span data-ttu-id="14f87-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="14f87-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14f87-115">-KeyData</span><span class="sxs-lookup"><span data-stu-id="14f87-115">-KeyData</span></span>
<span data-ttu-id="14f87-116">Określa dane klucza publicznego SSH RSA.</span><span class="sxs-lookup"><span data-stu-id="14f87-116">Specifies a SSH RSA public key data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14f87-117">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="14f87-117">-Path</span></span>
<span data-ttu-id="14f87-118">Określa pełną ścieżkę pliku na komputerze wirtualnym, na którym to polecenie cmdlet przechowuje klucz publiczny SSH.</span><span class="sxs-lookup"><span data-stu-id="14f87-118">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="14f87-119">Jeśli plik już istnieje, to polecenie cmdlet dołączy klucz do pliku.</span><span class="sxs-lookup"><span data-stu-id="14f87-119">If the file already exists, this cmdlet appends the key to the file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14f87-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="14f87-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="14f87-121">Określa obiekt MASZYNY.MASZYNY.WIRTUALNE.</span><span class="sxs-lookup"><span data-stu-id="14f87-121">Specifies the VMSS object.</span></span>
<span data-ttu-id="14f87-122">Aby utworzyć obiekt, możesz użyć polecenia cmdlet [New-AzVmssConfig.](./New-AzVmssConfig.md)</span><span class="sxs-lookup"><span data-stu-id="14f87-122">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14f87-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="14f87-123">-Confirm</span></span>
<span data-ttu-id="14f87-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="14f87-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14f87-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14f87-125">-WhatIf</span></span>
<span data-ttu-id="14f87-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14f87-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="14f87-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="14f87-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14f87-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14f87-128">CommonParameters</span></span>
<span data-ttu-id="14f87-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14f87-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14f87-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="14f87-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14f87-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="14f87-131">INPUTS</span></span>

### <span data-ttu-id="14f87-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="14f87-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="14f87-133">System.String</span><span class="sxs-lookup"><span data-stu-id="14f87-133">System.String</span></span>

## <span data-ttu-id="14f87-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="14f87-134">OUTPUTS</span></span>

### <span data-ttu-id="14f87-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="14f87-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="14f87-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="14f87-136">NOTES</span></span>

## <span data-ttu-id="14f87-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="14f87-137">RELATED LINKS</span></span>

[<span data-ttu-id="14f87-138">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="14f87-138">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
