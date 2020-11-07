---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A65E82D5-706B-4470-A51E-936E381DA78F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMCustomScriptExtension.md
ms.openlocfilehash: 83041e17a930ee63c17f68d6ce8ce2797a25318c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710248"
---
# <span data-ttu-id="b1468-101">Remove-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="b1468-101">Remove-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="b1468-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b1468-102">SYNOPSIS</span></span>
<span data-ttu-id="b1468-103">Usuwa niestandardowe rozszerzenie skryptu z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b1468-103">Removes a custom script extension from a virtual machine.</span></span>

## <span data-ttu-id="b1468-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b1468-104">SYNTAX</span></span>

```
Remove-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1468-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b1468-105">DESCRIPTION</span></span>
<span data-ttu-id="b1468-106">Polecenie cmdlet **Remove-AzVMCustomScriptExtension** usuwa rozszerzenie maszyny wirtualnej skryptu niestandardowego z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b1468-106">The **Remove-AzVMCustomScriptExtension** cmdlet removes a custom script Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="b1468-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b1468-107">EXAMPLES</span></span>

## <span data-ttu-id="b1468-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b1468-108">PARAMETERS</span></span>

### <span data-ttu-id="b1468-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1468-109">-DefaultProfile</span></span>
<span data-ttu-id="b1468-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b1468-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1468-111">-Force</span><span class="sxs-lookup"><span data-stu-id="b1468-111">-Force</span></span>
<span data-ttu-id="b1468-112">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b1468-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b1468-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b1468-113">-Name</span></span>
<span data-ttu-id="b1468-114">Określa nazwę niestandardowego rozszerzenia skryptu, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1468-114">Specifies the name of the custom script extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b1468-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1468-115">-ResourceGroupName</span></span>
<span data-ttu-id="b1468-116">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b1468-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="b1468-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="b1468-117">-VMName</span></span>
<span data-ttu-id="b1468-118">Określa nazwę maszyny wirtualnej, z poziomu której to polecenie cmdlet usuwa niestandardowe rozszerzenie skryptu.</span><span class="sxs-lookup"><span data-stu-id="b1468-118">Specifies the name of a virtual machine from which this cmdlet removes the custom script extension.</span></span>

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

### <span data-ttu-id="b1468-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b1468-119">-Confirm</span></span>
<span data-ttu-id="b1468-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1468-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1468-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1468-121">-WhatIf</span></span>
<span data-ttu-id="b1468-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1468-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1468-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b1468-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1468-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1468-124">CommonParameters</span></span>
<span data-ttu-id="b1468-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1468-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1468-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1468-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1468-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b1468-127">INPUTS</span></span>

### <span data-ttu-id="b1468-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b1468-128">System.String</span></span>

## <span data-ttu-id="b1468-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b1468-129">OUTPUTS</span></span>

### <span data-ttu-id="b1468-130">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="b1468-130">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="b1468-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b1468-131">NOTES</span></span>

## <span data-ttu-id="b1468-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b1468-132">RELATED LINKS</span></span>

[<span data-ttu-id="b1468-133">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="b1468-133">Get-AzVMCustomScriptExtension</span></span>](./Get-AzVMCustomScriptExtension.md)

[<span data-ttu-id="b1468-134">Set-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="b1468-134">Set-AzVMCustomScriptExtension</span></span>](./Set-AzVMCustomScriptExtension.md)
