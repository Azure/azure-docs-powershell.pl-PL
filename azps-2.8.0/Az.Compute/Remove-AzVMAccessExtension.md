---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 22C490C2-0135-4375-897E-7224DBBE13A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAccessExtension.md
ms.openlocfilehash: 1fececa1c7d40e8ea2667ecd6461740a6714d744
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706271"
---
# <span data-ttu-id="72e5a-101">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="72e5a-101">Remove-AzVMAccessExtension</span></span>

## <span data-ttu-id="72e5a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="72e5a-102">SYNOPSIS</span></span>
<span data-ttu-id="72e5a-103">Usuwa rozszerzenie VMAccess z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="72e5a-103">Removes the VMAccess extension from a virtual machine.</span></span>

## <span data-ttu-id="72e5a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="72e5a-104">SYNTAX</span></span>

```
Remove-AzVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72e5a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="72e5a-105">DESCRIPTION</span></span>
<span data-ttu-id="72e5a-106">Polecenie cmdlet **Remove-AzVMAccessExtension** usuwa rozszerzenie maszyny wirtualnej dostępu do maszyny wirtualnej (VMAccess) z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="72e5a-106">The **Remove-AzVMAccessExtension** cmdlet removes the Virtual Machine Access (VMAccess) Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="72e5a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="72e5a-107">EXAMPLES</span></span>

## <span data-ttu-id="72e5a-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="72e5a-108">PARAMETERS</span></span>

### <span data-ttu-id="72e5a-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72e5a-109">-DefaultProfile</span></span>
<span data-ttu-id="72e5a-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="72e5a-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72e5a-111">-Force</span><span class="sxs-lookup"><span data-stu-id="72e5a-111">-Force</span></span>
<span data-ttu-id="72e5a-112">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="72e5a-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="72e5a-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="72e5a-113">-Name</span></span>
<span data-ttu-id="72e5a-114">Określa nazwę rozszerzenia, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72e5a-114">Specifies the name of the extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72e5a-115">-Nowait</span><span class="sxs-lookup"><span data-stu-id="72e5a-115">-NoWait</span></span>
<span data-ttu-id="72e5a-116">Rozpoczyna operację i wraca natychmiast, zanim operacja zostanie ukończona.</span><span class="sxs-lookup"><span data-stu-id="72e5a-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="72e5a-117">W celu ustalenia, czy operacja została wykonana pomyślnie, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="72e5a-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="72e5a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72e5a-118">-ResourceGroupName</span></span>
<span data-ttu-id="72e5a-119">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="72e5a-119">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72e5a-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="72e5a-120">-VMName</span></span>
<span data-ttu-id="72e5a-121">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="72e5a-121">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="72e5a-122">To polecenie cmdlet usuwa VMAccess dla maszyny wirtualnej, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="72e5a-122">This cmdlet removes VMAccess for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72e5a-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="72e5a-123">-Confirm</span></span>
<span data-ttu-id="72e5a-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72e5a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72e5a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72e5a-125">-WhatIf</span></span>
<span data-ttu-id="72e5a-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72e5a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72e5a-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="72e5a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72e5a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72e5a-128">CommonParameters</span></span>
<span data-ttu-id="72e5a-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72e5a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72e5a-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="72e5a-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72e5a-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="72e5a-131">INPUTS</span></span>

### <span data-ttu-id="72e5a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="72e5a-132">System.String</span></span>

## <span data-ttu-id="72e5a-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="72e5a-133">OUTPUTS</span></span>

### <span data-ttu-id="72e5a-134">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="72e5a-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="72e5a-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="72e5a-135">NOTES</span></span>

## <span data-ttu-id="72e5a-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="72e5a-136">RELATED LINKS</span></span>

[<span data-ttu-id="72e5a-137">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="72e5a-137">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="72e5a-138">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="72e5a-138">Set-AzVMAccessExtension</span></span>](./Set-AzVMAccessExtension.md)

[<span data-ttu-id="72e5a-139">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="72e5a-139">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)
