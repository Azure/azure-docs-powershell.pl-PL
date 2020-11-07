---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A65E82D5-706B-4470-A51E-936E381DA78F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMCustomScriptExtension.md
ms.openlocfilehash: ee0762dfa78a5bd863ede7b56cb746c2c8cab3be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719151"
---
# <span data-ttu-id="d59b0-101">Remove-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="d59b0-101">Remove-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="d59b0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d59b0-102">SYNOPSIS</span></span>
<span data-ttu-id="d59b0-103">Usuwa niestandardowe rozszerzenie skryptu z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d59b0-103">Removes a custom script extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d59b0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d59b0-104">SYNTAX</span></span>

```
Remove-AzureRmVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d59b0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d59b0-105">DESCRIPTION</span></span>
<span data-ttu-id="d59b0-106">Polecenie cmdlet **Remove-AzureRmVMCustomScriptExtension** usuwa rozszerzenie maszyny wirtualnej skryptu niestandardowego z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d59b0-106">The **Remove-AzureRmVMCustomScriptExtension** cmdlet removes a custom script Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="d59b0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d59b0-107">EXAMPLES</span></span>

## <span data-ttu-id="d59b0-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d59b0-108">PARAMETERS</span></span>

### <span data-ttu-id="d59b0-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d59b0-109">-DefaultProfile</span></span>
<span data-ttu-id="d59b0-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d59b0-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d59b0-111">-Force</span><span class="sxs-lookup"><span data-stu-id="d59b0-111">-Force</span></span>
<span data-ttu-id="d59b0-112">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="d59b0-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d59b0-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d59b0-113">-Name</span></span>
<span data-ttu-id="d59b0-114">Określa nazwę niestandardowego rozszerzenia skryptu, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d59b0-114">Specifies the name of the custom script extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d59b0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d59b0-115">-ResourceGroupName</span></span>
<span data-ttu-id="d59b0-116">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d59b0-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="d59b0-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="d59b0-117">-VMName</span></span>
<span data-ttu-id="d59b0-118">Określa nazwę maszyny wirtualnej, z poziomu której to polecenie cmdlet usuwa niestandardowe rozszerzenie skryptu.</span><span class="sxs-lookup"><span data-stu-id="d59b0-118">Specifies the name of a virtual machine from which this cmdlet removes the custom script extension.</span></span>

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

### <span data-ttu-id="d59b0-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d59b0-119">-Confirm</span></span>
<span data-ttu-id="d59b0-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d59b0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d59b0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d59b0-121">-WhatIf</span></span>
<span data-ttu-id="d59b0-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d59b0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d59b0-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d59b0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d59b0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d59b0-124">CommonParameters</span></span>
<span data-ttu-id="d59b0-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d59b0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d59b0-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d59b0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d59b0-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d59b0-127">INPUTS</span></span>

### <span data-ttu-id="d59b0-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d59b0-128">System.String</span></span>

## <span data-ttu-id="d59b0-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d59b0-129">OUTPUTS</span></span>

### <span data-ttu-id="d59b0-130">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d59b0-130">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="d59b0-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d59b0-131">NOTES</span></span>

## <span data-ttu-id="d59b0-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d59b0-132">RELATED LINKS</span></span>

[<span data-ttu-id="d59b0-133">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="d59b0-133">Get-AzureRmVMCustomScriptExtension</span></span>](./Get-AzureRmVMCustomScriptExtension.md)

[<span data-ttu-id="d59b0-134">Set-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="d59b0-134">Set-AzureRmVMCustomScriptExtension</span></span>](./Set-AzureRmVMCustomScriptExtension.md)
