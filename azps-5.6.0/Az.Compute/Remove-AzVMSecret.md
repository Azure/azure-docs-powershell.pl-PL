---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSecret.md
ms.openlocfilehash: 794447801789bd8923012c19914ee41e736fb945
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985244"
---
# <span data-ttu-id="fd00c-101">Remove-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="fd00c-101">Remove-AzVMSecret</span></span>

## <span data-ttu-id="fd00c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd00c-102">SYNOPSIS</span></span>
<span data-ttu-id="fd00c-103">Usuwa (a) tajemnice z obiektu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="fd00c-103">Removes (a) secret(s) from a virtual machine object</span></span>

## <span data-ttu-id="fd00c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fd00c-104">SYNTAX</span></span>

```
Remove-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd00c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="fd00c-105">DESCRIPTION</span></span>
<span data-ttu-id="fd00c-106">Polecenie Remove-AzVMSecret usuwa (a) sekrety z obiektu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="fd00c-106">The Remove-AzVMSecret cmdlet removes (a) secret(s) from a virtual machine object.</span></span>

## <span data-ttu-id="fd00c-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fd00c-107">EXAMPLES</span></span>

### <span data-ttu-id="fd00c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fd00c-108">Example 1</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "rg1" -Name "vm1" | Remove-AzVMSecret | Update-AzVM
```

<span data-ttu-id="fd00c-109">Usuwa wszystkie tajemnice z maszyny wirtualnej "maszyny wirtualnej "maszyny wirtualnej 1" w grupie zasobów "rg1" i aktualizuje maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="fd00c-109">Removes all secrets from a virtual machine "vm1" in resource group "rg1" and update the VM</span></span>

## <span data-ttu-id="fd00c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd00c-110">PARAMETERS</span></span>

### <span data-ttu-id="fd00c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd00c-111">-DefaultProfile</span></span>
<span data-ttu-id="fd00c-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fd00c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd00c-113">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="fd00c-113">-SourceVaultId</span></span>
<span data-ttu-id="fd00c-114">Określa tablicę identyfikatorów magazynu źródłowego usuwanych przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd00c-114">Specifies an array of source vault IDs that this cmdlet removes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd00c-115">— MASZYNY WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="fd00c-115">-VM</span></span>
<span data-ttu-id="fd00c-116">Określa maszynę wirtualną, z której to polecenie cmdlet usuwa (a) tajnych.</span><span class="sxs-lookup"><span data-stu-id="fd00c-116">Specifies the virtual machine from which this cmdlet removes (a) secret(s).</span></span>
<span data-ttu-id="fd00c-117">Aby uzyskać obiekt maszyny wirtualnej, użyj Get-AzVM cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd00c-117">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="fd00c-118">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fd00c-118">-Confirm</span></span>
<span data-ttu-id="fd00c-119">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fd00c-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd00c-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd00c-120">-WhatIf</span></span>
<span data-ttu-id="fd00c-121">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd00c-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd00c-122">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="fd00c-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd00c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd00c-123">CommonParameters</span></span>
<span data-ttu-id="fd00c-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd00c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd00c-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd00c-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd00c-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fd00c-126">INPUTS</span></span>

### <span data-ttu-id="fd00c-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="fd00c-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="fd00c-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fd00c-128">OUTPUTS</span></span>

### <span data-ttu-id="fd00c-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="fd00c-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="fd00c-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fd00c-130">NOTES</span></span>

## <span data-ttu-id="fd00c-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fd00c-131">RELATED LINKS</span></span>
