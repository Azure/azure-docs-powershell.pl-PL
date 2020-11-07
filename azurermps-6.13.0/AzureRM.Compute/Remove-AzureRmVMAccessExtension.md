---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 22C490C2-0135-4375-897E-7224DBBE13A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMAccessExtension.md
ms.openlocfilehash: 0360bcdb766de681ab6f54682007076e18266051
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716589"
---
# <span data-ttu-id="89744-101">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="89744-101">Remove-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="89744-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="89744-102">SYNOPSIS</span></span>
<span data-ttu-id="89744-103">Usuwa rozszerzenie VMAccess z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="89744-103">Removes the VMAccess extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89744-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="89744-104">SYNTAX</span></span>

```
Remove-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89744-105">Opis</span><span class="sxs-lookup"><span data-stu-id="89744-105">DESCRIPTION</span></span>
<span data-ttu-id="89744-106">Polecenie cmdlet **Remove-AzureRmVMAccessExtension** usuwa rozszerzenie maszyny wirtualnej dostępu do maszyny wirtualnej (VMAccess) z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="89744-106">The **Remove-AzureRmVMAccessExtension** cmdlet removes the Virtual Machine Access (VMAccess) Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="89744-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="89744-107">EXAMPLES</span></span>

## <span data-ttu-id="89744-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="89744-108">PARAMETERS</span></span>

### <span data-ttu-id="89744-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89744-109">-DefaultProfile</span></span>
<span data-ttu-id="89744-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="89744-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89744-111">-Force</span><span class="sxs-lookup"><span data-stu-id="89744-111">-Force</span></span>
<span data-ttu-id="89744-112">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="89744-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="89744-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="89744-113">-Name</span></span>
<span data-ttu-id="89744-114">Określa nazwę rozszerzenia, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89744-114">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="89744-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89744-115">-ResourceGroupName</span></span>
<span data-ttu-id="89744-116">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="89744-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="89744-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="89744-117">-VMName</span></span>
<span data-ttu-id="89744-118">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="89744-118">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="89744-119">To polecenie cmdlet usuwa VMAccess dla maszyny wirtualnej, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="89744-119">This cmdlet removes VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="89744-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="89744-120">-Confirm</span></span>
<span data-ttu-id="89744-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89744-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89744-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89744-122">-WhatIf</span></span>
<span data-ttu-id="89744-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89744-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89744-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="89744-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89744-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89744-125">CommonParameters</span></span>
<span data-ttu-id="89744-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89744-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89744-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89744-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89744-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="89744-128">INPUTS</span></span>

### <span data-ttu-id="89744-129">System. String</span><span class="sxs-lookup"><span data-stu-id="89744-129">System.String</span></span>

## <span data-ttu-id="89744-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="89744-130">OUTPUTS</span></span>

### <span data-ttu-id="89744-131">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="89744-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="89744-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="89744-132">NOTES</span></span>

## <span data-ttu-id="89744-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="89744-133">RELATED LINKS</span></span>

[<span data-ttu-id="89744-134">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="89744-134">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="89744-135">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="89744-135">Set-AzureRmVMAccessExtension</span></span>](./Set-AzureRmVMAccessExtension.md)

[<span data-ttu-id="89744-136">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="89744-136">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)
