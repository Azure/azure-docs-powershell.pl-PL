---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A65E82D5-706B-4470-A51E-936E381DA78F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMCustomScriptExtension.md
ms.openlocfilehash: 2d1edd8e511042f677928f171d7e31859cc5390f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525669"
---
# <span data-ttu-id="daa8b-101">Remove-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="daa8b-101">Remove-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="daa8b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="daa8b-102">SYNOPSIS</span></span>
<span data-ttu-id="daa8b-103">Usuwa niestandardowe rozszerzenie skryptu z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="daa8b-103">Removes a custom script extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="daa8b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="daa8b-104">SYNTAX</span></span>

```
Remove-AzureRmVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="daa8b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="daa8b-105">DESCRIPTION</span></span>
<span data-ttu-id="daa8b-106">Polecenie cmdlet **Remove-AzureRmVMCustomScriptExtension** usuwa rozszerzenie maszyny wirtualnej skryptu niestandardowego z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="daa8b-106">The **Remove-AzureRmVMCustomScriptExtension** cmdlet removes a custom script Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="daa8b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="daa8b-107">EXAMPLES</span></span>

## <span data-ttu-id="daa8b-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="daa8b-108">PARAMETERS</span></span>

### <span data-ttu-id="daa8b-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daa8b-109">-DefaultProfile</span></span>
<span data-ttu-id="daa8b-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="daa8b-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="daa8b-111">-Force</span><span class="sxs-lookup"><span data-stu-id="daa8b-111">-Force</span></span>
<span data-ttu-id="daa8b-112">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="daa8b-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="daa8b-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="daa8b-113">-Name</span></span>
<span data-ttu-id="daa8b-114">Określa nazwę niestandardowego rozszerzenia skryptu, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="daa8b-114">Specifies the name of the custom script extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="daa8b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="daa8b-115">-ResourceGroupName</span></span>
<span data-ttu-id="daa8b-116">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="daa8b-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="daa8b-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="daa8b-117">-VMName</span></span>
<span data-ttu-id="daa8b-118">Określa nazwę maszyny wirtualnej, z poziomu której to polecenie cmdlet usuwa niestandardowe rozszerzenie skryptu.</span><span class="sxs-lookup"><span data-stu-id="daa8b-118">Specifies the name of a virtual machine from which this cmdlet removes the custom script extension.</span></span>

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

### <span data-ttu-id="daa8b-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="daa8b-119">-Confirm</span></span>
<span data-ttu-id="daa8b-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="daa8b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="daa8b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="daa8b-121">-WhatIf</span></span>
<span data-ttu-id="daa8b-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="daa8b-122">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="daa8b-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="daa8b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="daa8b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daa8b-124">CommonParameters</span></span>
<span data-ttu-id="daa8b-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="daa8b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daa8b-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="daa8b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daa8b-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="daa8b-127">INPUTS</span></span>

## <span data-ttu-id="daa8b-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="daa8b-128">OUTPUTS</span></span>

## <span data-ttu-id="daa8b-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="daa8b-129">NOTES</span></span>

## <span data-ttu-id="daa8b-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="daa8b-130">RELATED LINKS</span></span>

[<span data-ttu-id="daa8b-131">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="daa8b-131">Get-AzureRmVMCustomScriptExtension</span></span>](./Get-AzureRmVMCustomScriptExtension.md)

[<span data-ttu-id="daa8b-132">Set-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="daa8b-132">Set-AzureRmVMCustomScriptExtension</span></span>](./Set-AzureRmVMCustomScriptExtension.md)
