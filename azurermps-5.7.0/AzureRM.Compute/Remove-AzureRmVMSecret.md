---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMSecret.md
ms.openlocfilehash: 84f8abc6c298d7c82bef2494086deef3e4130842
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717221"
---
# <span data-ttu-id="2dd81-101">Remove-AzureRmVMSecret</span><span class="sxs-lookup"><span data-stu-id="2dd81-101">Remove-AzureRmVMSecret</span></span>

## <span data-ttu-id="2dd81-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2dd81-102">SYNOPSIS</span></span>
<span data-ttu-id="2dd81-103">Usuwa elementy tajne (a) z obiektu maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="2dd81-103">Removes (a) secret(s) from a virtual machine object</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2dd81-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2dd81-104">SYNTAX</span></span>

```
Remove-AzureRmVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String[]>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2dd81-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2dd81-105">DESCRIPTION</span></span>
<span data-ttu-id="2dd81-106">Polecenie cmdlet Remove-AzureRmVMSecret usuwa niejawne (a) elementy z obiektu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2dd81-106">The Remove-AzureRmVMSecret cmdlet removes (a) secret(s) from a virtual machine object.</span></span>

## <span data-ttu-id="2dd81-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2dd81-107">EXAMPLES</span></span>

### <span data-ttu-id="2dd81-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2dd81-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "rg1" -Name "vm1" | Remove-AzureRmVMSecret | Update-AzureRmVM
```

<span data-ttu-id="2dd81-109">Usuwa wszystkie klucze tajne maszyny wirtualnej "VM1" w grupie zasobów "RG1" i zaktualizowanie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="2dd81-109">Removes all secrets from a virtual machine "vm1" in resource group "rg1" and update the VM</span></span>

## <span data-ttu-id="2dd81-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2dd81-110">PARAMETERS</span></span>

### <span data-ttu-id="2dd81-111">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="2dd81-111">-SourceVaultId</span></span>
<span data-ttu-id="2dd81-112">Określa tablicę identyfikatorów magazynu źródłowego, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2dd81-112">Specifies an array of source vault IDs that this cmdlet removes.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dd81-113">-VM</span><span class="sxs-lookup"><span data-stu-id="2dd81-113">-VM</span></span>
<span data-ttu-id="2dd81-114">Umożliwia określenie maszyny wirtualnej, z której to polecenie cmdlet usunie (a) Secret (s).</span><span class="sxs-lookup"><span data-stu-id="2dd81-114">Specifies the virtual machine from which this cmdlet removes (a) secret(s).</span></span>
<span data-ttu-id="2dd81-115">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="2dd81-115">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2dd81-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2dd81-116">-Confirm</span></span>
<span data-ttu-id="2dd81-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2dd81-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dd81-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dd81-118">-WhatIf</span></span>
<span data-ttu-id="2dd81-119">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2dd81-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2dd81-120">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2dd81-120">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dd81-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dd81-121">CommonParameters</span></span>
<span data-ttu-id="2dd81-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dd81-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dd81-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2dd81-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dd81-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2dd81-124">INPUTS</span></span>

### <span data-ttu-id="2dd81-125">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="2dd81-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="2dd81-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2dd81-126">OUTPUTS</span></span>

### <span data-ttu-id="2dd81-127">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="2dd81-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="2dd81-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2dd81-128">NOTES</span></span>

## <span data-ttu-id="2dd81-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2dd81-129">RELATED LINKS</span></span>

