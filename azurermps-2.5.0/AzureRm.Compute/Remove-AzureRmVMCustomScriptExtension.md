---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A65E82D5-706B-4470-A51E-936E381DA78F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmcustomscriptextension
schema: 2.0.0
ms.openlocfilehash: 70715c4bb4c3e5f805f297c8b68def0f5b3a0d6f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898942"
---
# <span data-ttu-id="6e616-101">Remove-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="6e616-101">Remove-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="6e616-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6e616-102">SYNOPSIS</span></span>
<span data-ttu-id="6e616-103">Usuwa niestandardowe rozszerzenie skryptu z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6e616-103">Removes a custom script extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e616-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6e616-104">SYNTAX</span></span>

```
Remove-AzureRmVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e616-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6e616-105">DESCRIPTION</span></span>
<span data-ttu-id="6e616-106">Polecenie cmdlet **Remove-AzureRmVMCustomScriptExtension** usuwa rozszerzenie maszyny wirtualnej skryptu niestandardowego z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6e616-106">The **Remove-AzureRmVMCustomScriptExtension** cmdlet removes a custom script Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="6e616-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6e616-107">EXAMPLES</span></span>

## <span data-ttu-id="6e616-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6e616-108">PARAMETERS</span></span>

### <span data-ttu-id="6e616-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e616-109">-DefaultProfile</span></span>
<span data-ttu-id="6e616-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6e616-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e616-111">-Force</span><span class="sxs-lookup"><span data-stu-id="6e616-111">-Force</span></span>
<span data-ttu-id="6e616-112">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="6e616-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e616-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6e616-113">-Name</span></span>
<span data-ttu-id="6e616-114">Określa nazwę niestandardowego rozszerzenia skryptu, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e616-114">Specifies the name of the custom script extension that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e616-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e616-115">-ResourceGroupName</span></span>
<span data-ttu-id="6e616-116">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6e616-116">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e616-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="6e616-117">-VMName</span></span>
<span data-ttu-id="6e616-118">Określa nazwę maszyny wirtualnej, z poziomu której to polecenie cmdlet usuwa niestandardowe rozszerzenie skryptu.</span><span class="sxs-lookup"><span data-stu-id="6e616-118">Specifies the name of a virtual machine from which this cmdlet removes the custom script extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e616-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6e616-119">-Confirm</span></span>
<span data-ttu-id="6e616-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e616-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e616-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e616-121">-WhatIf</span></span>
<span data-ttu-id="6e616-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e616-122">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="6e616-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6e616-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e616-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e616-124">CommonParameters</span></span>
<span data-ttu-id="6e616-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e616-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e616-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e616-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e616-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6e616-127">INPUTS</span></span>

### <span data-ttu-id="6e616-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="6e616-128">None</span></span>
<span data-ttu-id="6e616-129">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="6e616-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6e616-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6e616-130">OUTPUTS</span></span>

### <span data-ttu-id="6e616-131">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="6e616-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="6e616-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6e616-132">NOTES</span></span>

## <span data-ttu-id="6e616-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6e616-133">RELATED LINKS</span></span>

[<span data-ttu-id="6e616-134">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="6e616-134">Get-AzureRmVMCustomScriptExtension</span></span>](./Get-AzureRmVMCustomScriptExtension.md)

[<span data-ttu-id="6e616-135">Set-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="6e616-135">Set-AzureRmVMCustomScriptExtension</span></span>](./Set-AzureRmVMCustomScriptExtension.md)
