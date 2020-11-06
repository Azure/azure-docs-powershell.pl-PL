---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMSecret.md
ms.openlocfilehash: 171d6c9b5b7e23f8e90e146a8ff4a03c514c66a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525641"
---
# <span data-ttu-id="b1163-101">Remove-AzureRmVMSecret</span><span class="sxs-lookup"><span data-stu-id="b1163-101">Remove-AzureRmVMSecret</span></span>

## <span data-ttu-id="b1163-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b1163-102">SYNOPSIS</span></span>
<span data-ttu-id="b1163-103">Usuwa elementy tajne (a) z obiektu maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="b1163-103">Removes (a) secret(s) from a virtual machine object</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1163-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b1163-104">SYNTAX</span></span>

```
Remove-AzureRmVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1163-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b1163-105">DESCRIPTION</span></span>
<span data-ttu-id="b1163-106">Polecenie cmdlet Remove-AzureRmVMSecret usuwa niejawne (a) elementy z obiektu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b1163-106">The Remove-AzureRmVMSecret cmdlet removes (a) secret(s) from a virtual machine object.</span></span>

## <span data-ttu-id="b1163-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b1163-107">EXAMPLES</span></span>

### <span data-ttu-id="b1163-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b1163-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "rg1" -Name "vm1" | Remove-AzureRmVM | Update-AzureRmVM
```

<span data-ttu-id="b1163-109">Usuwa wszystkie klucze tajne maszyny wirtualnej "VM1" w grupie zasobów "RG1" i zaktualizowanie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="b1163-109">Removes all secrets from a virtual machine "vm1" in resource group "rg1" and update the VM</span></span>

## <span data-ttu-id="b1163-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b1163-110">PARAMETERS</span></span>

### <span data-ttu-id="b1163-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1163-111">-DefaultProfile</span></span>
<span data-ttu-id="b1163-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b1163-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1163-113">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="b1163-113">-SourceVaultId</span></span>
<span data-ttu-id="b1163-114">Określa tablicę identyfikatorów magazynu źródłowego, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1163-114">Specifies an array of source vault IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b1163-115">-VM</span><span class="sxs-lookup"><span data-stu-id="b1163-115">-VM</span></span>
<span data-ttu-id="b1163-116">Umożliwia określenie maszyny wirtualnej, z której to polecenie cmdlet usunie (a) Secret (s).</span><span class="sxs-lookup"><span data-stu-id="b1163-116">Specifies the virtual machine from which this cmdlet removes (a) secret(s).</span></span>
<span data-ttu-id="b1163-117">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="b1163-117">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="b1163-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b1163-118">-Confirm</span></span>
<span data-ttu-id="b1163-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1163-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1163-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1163-120">-WhatIf</span></span>
<span data-ttu-id="b1163-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1163-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1163-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b1163-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1163-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1163-123">CommonParameters</span></span>
<span data-ttu-id="b1163-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1163-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1163-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1163-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1163-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b1163-126">INPUTS</span></span>

### <span data-ttu-id="b1163-127">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b1163-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="b1163-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b1163-128">OUTPUTS</span></span>

### <span data-ttu-id="b1163-129">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b1163-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="b1163-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b1163-130">NOTES</span></span>

## <span data-ttu-id="b1163-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b1163-131">RELATED LINKS</span></span>

