---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSecret.md
ms.openlocfilehash: df6103cbd3ca58b5e324618c9ad2d8be5820fc96
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504007"
---
# <span data-ttu-id="6d268-101">Remove-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="6d268-101">Remove-AzVMSecret</span></span>

## <span data-ttu-id="6d268-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6d268-102">SYNOPSIS</span></span>
<span data-ttu-id="6d268-103">Usuwa elementy tajne (a) z obiektu maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="6d268-103">Removes (a) secret(s) from a virtual machine object</span></span>

## <span data-ttu-id="6d268-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6d268-104">SYNTAX</span></span>

```
Remove-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d268-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6d268-105">DESCRIPTION</span></span>
<span data-ttu-id="6d268-106">Polecenie cmdlet Remove-AzVMSecret usuwa niejawne (a) elementy z obiektu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6d268-106">The Remove-AzVMSecret cmdlet removes (a) secret(s) from a virtual machine object.</span></span>

## <span data-ttu-id="6d268-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6d268-107">EXAMPLES</span></span>

### <span data-ttu-id="6d268-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6d268-108">Example 1</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "rg1" -Name "vm1" | Remove-AzVMSecret | Update-AzVM
```

<span data-ttu-id="6d268-109">Usuwa wszystkie klucze tajne maszyny wirtualnej "VM1" w grupie zasobów "RG1" i zaktualizowanie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="6d268-109">Removes all secrets from a virtual machine "vm1" in resource group "rg1" and update the VM</span></span>

## <span data-ttu-id="6d268-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6d268-110">PARAMETERS</span></span>

### <span data-ttu-id="6d268-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d268-111">-DefaultProfile</span></span>
<span data-ttu-id="6d268-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6d268-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d268-113">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="6d268-113">-SourceVaultId</span></span>
<span data-ttu-id="6d268-114">Określa tablicę identyfikatorów magazynu źródłowego, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d268-114">Specifies an array of source vault IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6d268-115">-VM</span><span class="sxs-lookup"><span data-stu-id="6d268-115">-VM</span></span>
<span data-ttu-id="6d268-116">Umożliwia określenie maszyny wirtualnej, z której to polecenie cmdlet usunie (a) Secret (s).</span><span class="sxs-lookup"><span data-stu-id="6d268-116">Specifies the virtual machine from which this cmdlet removes (a) secret(s).</span></span>
<span data-ttu-id="6d268-117">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="6d268-117">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="6d268-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6d268-118">-Confirm</span></span>
<span data-ttu-id="6d268-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d268-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d268-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d268-120">-WhatIf</span></span>
<span data-ttu-id="6d268-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d268-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d268-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6d268-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d268-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d268-123">CommonParameters</span></span>
<span data-ttu-id="6d268-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d268-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d268-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d268-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d268-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6d268-126">INPUTS</span></span>

### <span data-ttu-id="6d268-127">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6d268-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="6d268-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6d268-128">OUTPUTS</span></span>

### <span data-ttu-id="6d268-129">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6d268-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="6d268-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6d268-130">NOTES</span></span>

## <span data-ttu-id="6d268-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6d268-131">RELATED LINKS</span></span>
